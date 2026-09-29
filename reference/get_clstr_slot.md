# Get slot data for each cluster record

Get slot data for cluster(s)

## Usage

``` r
get_clstr_slot(phylota, cid, slt_nm = list_clstrrec_slots())
```

## Arguments

- phylota:

  Phylota object

- cid:

  Cluster ID

- slt_nm:

  Slot name

## Value

vector

## See also

Other tools-public:
[`calc_mad()`](https://docs.ropensci.org/phylotaR/reference/calc_mad.md),
[`calc_wrdfrq()`](https://docs.ropensci.org/phylotaR/reference/calc_wrdfrq.md),
[`drop_by_rank()`](https://docs.ropensci.org/phylotaR/reference/drop_by_rank.md),
[`drop_clstrs()`](https://docs.ropensci.org/phylotaR/reference/drop_clstrs.md),
[`drop_sqs()`](https://docs.ropensci.org/phylotaR/reference/drop_sqs.md),
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
data('aotus')
random_cid <- sample(aotus@cids, 1)
(get_clstr_slot(phylota = aotus, cid = random_cid, slt_nm = 'seed'))
#>           14 
#> "JQ932794.1" 
# see list_clstrrec_slots() for available slots
(list_clstrrec_slots())
#> [1] "id"   "nsqs" "ntx"  "typ"  "prnt" "seed"
```
