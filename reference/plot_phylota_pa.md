# Plot presence/absence matrix

Plot presence/absence of taxa by each cluster in phylota object.

## Usage

``` r
plot_phylota_pa(phylota, cids, txids, cnms = cids, txnms = txids)
```

## Arguments

- phylota:

  Phylota object

- cids:

  Vector of cluster IDs

- txids:

  Vector of taxonomic IDs

- cnms:

  Cluster names

- txnms:

  Taxonomic names

## Value

geom_object

## Details

Cluster names and taxonomic names can be given to the function, by
default IDs are used.

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
[`plot_phylota_treemap()`](https://docs.ropensci.org/phylotaR/reference/plot_phylota_treemap.md),
[`read_phylota()`](https://docs.ropensci.org/phylotaR/reference/read_phylota.md),
[`write_sqs()`](https://docs.ropensci.org/phylotaR/reference/write_sqs.md)

## Examples

``` r
library(phylotaR)
data(cycads)
# drop all but first ten
cycads <- drop_clstrs(cycads, cycads@cids[1:10])
# plot all
p <- plot_phylota_pa(phylota = cycads, cids = cycads@cids, txids = cycads@txids)
print(p)  # lots of information, difficult to interpret

# get genus-level taxonomic names
genus_txids <- get_txids(cycads, txids = cycads@txids, rnk = 'genus')
genus_txids <- unique(genus_txids)
# dropping missing
genus_txids <- genus_txids[genus_txids !=  '']
genus_nms <- get_tx_slot(cycads, genus_txids, slt_nm = 'scnm')
# make alphabetical for plotting
genus_nms <- sort(genus_nms, decreasing = TRUE)
# generate geom_object
p <- plot_phylota_pa(phylota = cycads, cids = cycads@cids, txids = genus_txids,
                     txnms = genus_nms)
# plot
print(p)  # easier to interpret
```
