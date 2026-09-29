# Reduce clusters to specific rank

Identifies higher level taxa for each sequence in clusters for given
rank. Selects representative sequences for each unique taxon using the
choose_by functions. By default, the function will choose the top ten
sequences by first sorting by those with fewest number of ambiguous
sequences, then by youngest, then by sequence length.

## Usage

``` r
drop_by_rank(
  phylota,
  rnk = "species",
  keep_higher = FALSE,
  n = 10,
  choose_by = c("pambgs", "age", "nncltds"),
  greatest = c(FALSE, FALSE, TRUE)
)
```

## Arguments

- phylota:

  Phylota object

- rnk:

  Taxonomic rank

- keep_higher:

  Keep higher taxonomic ranks?

- n:

  Number of sequences per taxon

- choose_by:

  Vector of selection functions

- greatest:

  Greatest of lowest for each choose_by function

## Value

phylota

## See also

Other tools-public:
[`calc_mad()`](https://docs.ropensci.org/phylotaR/reference/calc_mad.md),
[`calc_wrdfrq()`](https://docs.ropensci.org/phylotaR/reference/calc_wrdfrq.md),
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
data("dragonflies")
# For faster computations, let's only work with the 5 clusters.
dragonflies <- drop_clstrs(phylota = dragonflies, cid = dragonflies@cids[10:15])


# We can use drop_by_rank() to reduce to 10 sequences per genus for each cluster
(reduced_1 <- drop_by_rank(phylota = dragonflies, rnk = 'genus', n = 10,
                           choose_by = c('pambgs', 'age', 'nncltds'),
                           greatest = c(FALSE, FALSE, TRUE)))
#> Phylota Table (Anisoptera)
#> - [6] clusters
#> - [411] sequences
#> - [162] source taxa

# We can specify what aspects of the sequences we would like to select per genus
# By default we select the sequences with fewest ambiguous nucleotides (e.g.
# we avoid Ns), the youngest age and then longest sequence.
# We can reverse the 'greatest' to get the opposite.
(reduced_2 <- drop_by_rank(phylota = dragonflies, rnk = 'genus', n = 10,
                           choose_by = c('pambgs', 'age', 'nncltds'),
                           greatest = c(TRUE, TRUE, FALSE)))
#> Phylota Table (Anisoptera)
#> - [6] clusters
#> - [411] sequences
#> - [174] source taxa


# Leading to smaller sequnces ...
r1_sqlngth <- mean(get_sq_slot(phylota = reduced_1,
                                sid = reduced_1@sids, slt_nm = 'nncltds'))
r2_sqlngth <- mean(get_sq_slot(phylota = reduced_2,
                                sid = reduced_2@sids, slt_nm = 'nncltds'))
(r1_sqlngth > r2_sqlngth)
#> [1] FALSE
# ... with more ambigous characters ....
r1_pambgs <- mean(get_sq_slot(phylota = reduced_1, sid = reduced_1@sids,
                              slt_nm = 'pambgs'))
r2_pambgs <- mean(get_sq_slot(phylota = reduced_2, sid = reduced_2@sids,
                              slt_nm = 'pambgs'))
(r1_pambgs < r2_pambgs)
#> [1] TRUE
# .... and older ages (measured in days since being added to GenBank).
r1_age <- mean(get_sq_slot(phylota = reduced_1, sid = reduced_1@sids,
                           slt_nm = 'age'))
r2_age <- mean(get_sq_slot(phylota = reduced_2, sid = reduced_2@sids,
                           slt_nm = 'age'))
(r1_age < r2_age)
#> [1] FALSE


# Or... we can simply reduce the clusters to just one sequence per genus
(dragonflies <- drop_by_rank(phylota = dragonflies, rnk = 'genus', n = 1))
#> Phylota Table (Anisoptera)
#> - [6] clusters
#> - [73] sequences
#> - [72] source taxa
```
