# Get slot data for each sequence

Get slot data for either or sequences in a cluster of a vector of
sequence IDs. Use list_seqrec_slots() for a list of available slots.

## Usage

``` r
get_sq_slot(phylota, cid = NULL, sid = NULL, slt_nm = list_seqrec_slots())
```

## Arguments

- phylota:

  Phylota object

- cid:

  Cluster ID

- sid:

  Sequence ID(s)

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
[`get_clstr_slot()`](https://docs.ropensci.org/phylotaR/reference/get_clstr_slot.md),
[`get_nsqs()`](https://docs.ropensci.org/phylotaR/reference/get_nsqs.md),
[`get_ntaxa()`](https://docs.ropensci.org/phylotaR/reference/get_ntaxa.md),
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
random_sid <- sample(aotus@sids, 1)
(get_sq_slot(phylota = aotus, sid = random_sid, slt_nm = 'dfln'))
#>                                                                                AF333723.1 
#> "Aotus nancymaae clone 11192.15 T-cell receptor gamma chain V-J region mRNA, partial cds" 
# see list_seqrec_slots() for available slots
(list_seqrec_slots())
#>  [1] "id"      "nm"      "accssn"  "vrsn"    "url"     "txid"    "orgnsm" 
#>  [8] "dfln"    "ml_typ"  "rec_typ" "nncltds" "nambgs"  "pambgs"  "gcr"    
#> [15] "age"    
```
