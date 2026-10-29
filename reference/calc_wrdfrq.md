# Calculate word frequencies

For all sequences in a cluster(s) calculate the frequency of separate
words in either the sequence definitions or the reported feature name.

## Usage

``` r
calc_wrdfrq(
  phylota,
  cid,
  min_frq = 0.1,
  min_nchar = 1,
  type = c("dfln", "nm"),
  ignr_pttrn = "[^a-z0-9]"
)
```

## Arguments

- phylota:

  Phylota object

- cid:

  Cluster ID(s)

- min_frq:

  Minimum frequency

- min_nchar:

  Minimum number of characters for a word

- type:

  Definitions (dfln) or features (nm)

- ignr_pttrn:

  Ignore pattern, REGEX for text to ignore.

## Value

list

## Details

By default, anything that is not alphanumeric is ignored. 'dfln' and
'nm' match the slot names in a SeqRec, see list_seqrec_slots().

## See also

Other tools-public:
[`calc_mad()`](https://docs.ropensci.org/phylotaR/reference/calc_mad.md),
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
[`plot_phylota_treemap()`](https://docs.ropensci.org/phylotaR/reference/plot_phylota_treemap.md),
[`read_phylota()`](https://docs.ropensci.org/phylotaR/reference/read_phylota.md),
[`write_sqs()`](https://docs.ropensci.org/phylotaR/reference/write_sqs.md)

## Examples

``` r
data('dragonflies')
# work out what gene region the cluster is likely representing with word freqs.
random_cids <- sample(dragonflies@cids, 10)
# most frequent words in definition line
(calc_wrdfrq(phylota = dragonflies, cid = random_cids, type = 'dfln'))
#> $`430`
#> named numeric(0)
#> 
#> $`653`
#> named numeric(0)
#> 
#> $`15`
#> named numeric(0)
#> 
#> $`478`
#> wrds
#>      rrna       and 
#> 0.1525424 0.1016949 
#> 
#> $`548`
#> wrds
#>      gene  sequence 
#> 0.1411765 0.1294118 
#> 
#> $`161`
#> named numeric(0)
#> 
#> $`498`
#> wrds
#>     gene sequence 
#>     0.15     0.15 
#> 
#> $`413`
#> named numeric(0)
#> 
#> $`222`
#> wrds
#>        h3       cds      gene   histone   partial 
#> 0.1528384 0.1135371 0.1135371 0.1135371 0.1135371 
#> 
#> $`29`
#> named numeric(0)
#> 
# most frequent words in feature name
(calc_wrdfrq(phylota = dragonflies, cid = random_cids, type = 'nm'))
#> $`430`
#> numeric(0)
#> 
#> $`653`
#> numeric(0)
#> 
#> $`15`
#> barcode 
#>       1 
#> 
#> $`478`
#> numeric(0)
#> 
#> $`548`
#> numeric(0)
#> 
#> $`161`
#> numeric(0)
#> 
#> $`498`
#> numeric(0)
#> 
#> $`413`
#> barcode 
#>       1 
#> 
#> $`222`
#> numeric(0)
#> 
#> $`29`
#> numeric(0)
#> 
```
