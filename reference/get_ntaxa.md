# Count number of unique taxa

Count the number of unique taxa represented by cluster(s) or sequences
in phylota table Use rnk to specify a taxonomic level to count. If NULL
counts will be made to the lowest level reported on NCBI.

## Usage

``` r
get_ntaxa(phylota, cid = NULL, sid = NULL, rnk = NULL, keep_higher = FALSE)
```

## Arguments

- phylota:

  Phylota object

- cid:

  Cluster ID(s)

- sid:

  Sequence ID(s)

- rnk:

  Taxonomic rank

- keep_higher:

  Keep higher taxonomic ranks?

## Value

vector

## See also

Other tools-public:
[`calc_mad()`](https://docs.ropensci.org/phylotaR/reference/calc_mad.md),
[`calc_wrdfrq()`](https://docs.ropensci.org/phylotaR/reference/calc_wrdfrq.md),
[`drop_by_rank()`](https://docs.ropensci.org/phylotaR/reference/drop_by_rank.md),
[`drop_clstrs()`](https://docs.ropensci.org/phylotaR/reference/drop_clstrs.md),
[`drop_sqs()`](https://docs.ropensci.org/phylotaR/reference/drop_sqs.md),
[`get_clstr_slot()`](https://docs.ropensci.org/phylotaR/reference/get_clstr_slot.md),
[`get_nsqs()`](https://docs.ropensci.org/phylotaR/reference/get_nsqs.md),
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
data('bromeliads')
# how many species are there?
(get_ntaxa(phylota = bromeliads, cid = '0', rnk = 'species'))
#>    0 
#> 1050 
# how many genera are there?
(get_ntaxa(phylota = bromeliads, cid = '0', rnk = 'genus'))
#>  0 
#> 76 
# how many families are there?
(get_ntaxa(phylota = bromeliads, cid = '0', rnk = 'family'))
#> 0 
#> 1 
# use list_ncbi_ranks() to see available rank names
(list_ncbi_ranks())
#>  [1] "superkingdom" "kingdom"      "phylum"       "subphylum"    "class"       
#>  [6] "superorder"   "order"        "suborder"     "infraorder"   "parvorder"   
#> [11] "family"       "genus"        "species"      "subspecies"  
```
