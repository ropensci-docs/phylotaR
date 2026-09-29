# Plot treemap of Phylota object

Treemaps show relative size with boxes. The user can explore which taxa
or clusters are most represented either by sequence or cluster number.
If cluster IDs are provided, the plot is made for clusters. If taxonomic
IDs are provided, the plot is made for taxa.

## Usage

``` r
plot_phylota_treemap(
  phylota,
  cids = NULL,
  txids = NULL,
  cnms = cids,
  txnms = txids,
  with_labels = TRUE,
  area = c("ntx", "nsq", "ncl"),
  fill = c("NULL", "typ", "ntx", "nsq", "ncl")
)
```

## Arguments

- phylota:

  Phylota object

- cids:

  Cluster IDs

- txids:

  Taxonomic IDs

- cnms:

  Cluster names

- txnms:

  Taxonomic names

- with_labels:

  Show names per box?

- area:

  What determines the size per box?

- fill:

  What determines the coloured fill per box?

## Value

geom_object

## Details

The function can take a long time to run for large Phylota objects over
many taxonomic IDs because searches are made across lineages. The idea
of the function is to assess the data dominance of specific clusters and
taxa.

## See also

Other tools-public:
[`calc_mad()`](https://docs.ropensci.org/phylotaR/reference/calc_mad.md),
[`calc_wrdfrq()`](https://docs.ropensci.org/phylotaR/reference/calc_wrdfrq.md),
[`drop_by_rank()`](https://docs.ropensci.org/phylotaR/reference/drop_by_rank.md),
[`drop_clstrs()`](https://docs.ropensci.org/phylotaR/reference/drop_clstrs.md),
[`drop_sqs()`](https://docs.ropensci.org/phylotaR/reference/drop_sqs.md),
[`get_clstr_slot()`](https://docs.ropensci.org/phylotaR/reference/get_clstr_slot.md),
[`get_nsqs()`](https://docs.ropensci.org/phylotaR/reference/get_nsqs.md),
[`get_ntaxa()`](https://docs.ropensci.org/phylotaR/reference/get_ntaxa.md),
[`get_sq_slot()`](https://docs.ropensci.org/phylotaR/reference/get_sq_slot.md),
[`get_stage_times()`](https://docs.ropensci.org/phylotaR/reference/get_stage_times.md),
[`get_tx_slot()`](https://docs.ropensci.org/phylotaR/reference/get_tx_slot.md),
[`get_txids()`](https://docs.ropensci.org/phylotaR/reference/get_txids.md),
[`is_txid_in_clstr()`](https://docs.ropensci.org/phylotaR/reference/is_txid_in_clstr.md),
[`is_txid_in_sq()`](https://docs.ropensci.org/phylotaR/reference/is_txid_in_sq.md),
[`list_clstrrec_slots()`](https://docs.ropensci.org/phylotaR/reference/list_clstrrec_slots.md),
[`list_ncbi_ranks()`](https://docs.ropensci.org/phylotaR/reference/list_ncbi_ranks.md),
[`list_seqrec_slots()`](https://docs.ropensci.org/phylotaR/reference/list_seqrec_slots.md),
[`list_taxrec_slots()`](https://docs.ropensci.org/phylotaR/reference/list_taxrec_slots.md),
[`plot_phylota_pa()`](https://docs.ropensci.org/phylotaR/reference/plot_phylota_pa.md),
[`read_phylota()`](https://docs.ropensci.org/phylotaR/reference/read_phylota.md),
[`write_sqs()`](https://docs.ropensci.org/phylotaR/reference/write_sqs.md)

## Examples

``` r
data("tinamous")
# Plot clusters, size by n. sq, fill by n. tx
p <- plot_phylota_treemap(phylota = tinamous, cids = tinamous@cids,
                          area = 'nsq', fill = 'ntx')
#> Warning: `aes_string()` was deprecated in ggplot2 3.0.0.
#> ℹ Please use tidy evaluation idioms with `aes()`.
#> ℹ See also `vignette("ggplot2-in-packages")` for more information.
#> ℹ The deprecated feature was likely used in the phylotaR package.
#>   Please report the issue at <https://github.com/ropensci/phylotaR/issues>.
print(p)

# Plot taxa, size by n. sq, fill by ncl
txids <- get_txids(tinamous, txids = tinamous@txids, rnk = 'genus')
txids <- txids[txids !=  '']
txids <- unique(txids)
txnms <- get_tx_slot(tinamous, txids, slt_nm = 'scnm')
p <- plot_phylota_treemap(phylota = tinamous, txids = txids, txnms = txnms,
                          area = 'nsq', fill = 'ncl')
print(p)
```
