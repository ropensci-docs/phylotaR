# Check stage arguments

Ensures stage arguments are valid, raises an error if not.

## Usage

``` r
stage_args_check(to, frm)
```

## Arguments

- to:

  ending stage

- frm:

  starting stage

## Value

character, stage message

## See also

Other run-private:
[`batcher()`](https://docs.ropensci.org/phylotaR/reference/batcher.md),
[`blast_clstr()`](https://docs.ropensci.org/phylotaR/reference/blast_clstr.md),
[`blast_filter()`](https://docs.ropensci.org/phylotaR/reference/blast_filter.md),
[`blast_setup()`](https://docs.ropensci.org/phylotaR/reference/blast_setup.md),
[`blast_sqs()`](https://docs.ropensci.org/phylotaR/reference/blast_sqs.md),
[`blastcache_load()`](https://docs.ropensci.org/phylotaR/reference/blastcache_load.md),
[`blastcache_save()`](https://docs.ropensci.org/phylotaR/reference/blastcache_save.md),
[`blastdb_gen()`](https://docs.ropensci.org/phylotaR/reference/blastdb_gen.md),
[`blastn_run()`](https://docs.ropensci.org/phylotaR/reference/blastn_run.md),
[`cache_rm()`](https://docs.ropensci.org/phylotaR/reference/cache_rm.md),
[`cache_setup()`](https://docs.ropensci.org/phylotaR/reference/cache_setup.md),
[`clade_select()`](https://docs.ropensci.org/phylotaR/reference/clade_select.md),
[`clstr2_calc()`](https://docs.ropensci.org/phylotaR/reference/clstr2_calc.md),
[`clstr_all()`](https://docs.ropensci.org/phylotaR/reference/clstr_all.md),
[`clstr_direct()`](https://docs.ropensci.org/phylotaR/reference/clstr_direct.md),
[`clstr_sqs()`](https://docs.ropensci.org/phylotaR/reference/clstr_sqs.md),
[`clstr_subtree()`](https://docs.ropensci.org/phylotaR/reference/clstr_subtree.md),
[`clstrarc_gen()`](https://docs.ropensci.org/phylotaR/reference/clstrarc_gen.md),
[`clstrarc_join()`](https://docs.ropensci.org/phylotaR/reference/clstrarc_join.md),
[`clstrrec_gen()`](https://docs.ropensci.org/phylotaR/reference/clstrrec_gen.md),
[`clstrs_calc()`](https://docs.ropensci.org/phylotaR/reference/clstrs_calc.md),
[`clstrs_join()`](https://docs.ropensci.org/phylotaR/reference/clstrs_join.md),
[`clstrs_merge()`](https://docs.ropensci.org/phylotaR/reference/clstrs_merge.md),
[`clstrs_renumber()`](https://docs.ropensci.org/phylotaR/reference/clstrs_renumber.md),
[`clstrs_save()`](https://docs.ropensci.org/phylotaR/reference/clstrs_save.md),
[`cmdln()`](https://docs.ropensci.org/phylotaR/reference/cmdln.md),
[`descendants_get()`](https://docs.ropensci.org/phylotaR/reference/descendants_get.md),
[`download_obj_check()`](https://docs.ropensci.org/phylotaR/reference/download_obj_check.md),
[`error()`](https://docs.ropensci.org/phylotaR/reference/error.md),
[`gb_extract()`](https://docs.ropensci.org/phylotaR/reference/gb_extract.md),
[`hierarchic_download()`](https://docs.ropensci.org/phylotaR/reference/hierarchic_download.md),
[`info()`](https://docs.ropensci.org/phylotaR/reference/info.md),
[`ncbicache_load()`](https://docs.ropensci.org/phylotaR/reference/ncbicache_load.md),
[`ncbicache_save()`](https://docs.ropensci.org/phylotaR/reference/ncbicache_save.md),
[`obj_check()`](https://docs.ropensci.org/phylotaR/reference/obj_check.md),
[`obj_load()`](https://docs.ropensci.org/phylotaR/reference/obj_load.md),
[`obj_save()`](https://docs.ropensci.org/phylotaR/reference/obj_save.md),
[`outfmt_get()`](https://docs.ropensci.org/phylotaR/reference/outfmt_get.md),
[`parameters_load()`](https://docs.ropensci.org/phylotaR/reference/parameters_load.md),
[`parameters_setup()`](https://docs.ropensci.org/phylotaR/reference/parameters_setup.md),
[`parent_get()`](https://docs.ropensci.org/phylotaR/reference/parent_get.md),
[`progress_init()`](https://docs.ropensci.org/phylotaR/reference/progress_init.md),
[`progress_read()`](https://docs.ropensci.org/phylotaR/reference/progress_read.md),
[`progress_reset()`](https://docs.ropensci.org/phylotaR/reference/progress_reset.md),
[`progress_save()`](https://docs.ropensci.org/phylotaR/reference/progress_save.md),
[`rank_get()`](https://docs.ropensci.org/phylotaR/reference/rank_get.md),
[`rawseqrec_breakdown()`](https://docs.ropensci.org/phylotaR/reference/rawseqrec_breakdown.md),
[`safely_connect()`](https://docs.ropensci.org/phylotaR/reference/safely_connect.md),
[`search_and_cache()`](https://docs.ropensci.org/phylotaR/reference/search_and_cache.md),
[`searchterm_gen()`](https://docs.ropensci.org/phylotaR/reference/searchterm_gen.md),
[`seeds_blast()`](https://docs.ropensci.org/phylotaR/reference/seeds_blast.md),
[`seq_download()`](https://docs.ropensci.org/phylotaR/reference/seq_download.md),
[`seqarc_gen()`](https://docs.ropensci.org/phylotaR/reference/seqarc_gen.md),
[`seqrec_augment()`](https://docs.ropensci.org/phylotaR/reference/seqrec_augment.md),
[`seqrec_convert()`](https://docs.ropensci.org/phylotaR/reference/seqrec_convert.md),
[`seqrec_gen()`](https://docs.ropensci.org/phylotaR/reference/seqrec_gen.md),
[`seqrec_get()`](https://docs.ropensci.org/phylotaR/reference/seqrec_get.md),
[`sids_check()`](https://docs.ropensci.org/phylotaR/reference/sids_check.md),
[`sids_get()`](https://docs.ropensci.org/phylotaR/reference/sids_get.md),
[`sids_load()`](https://docs.ropensci.org/phylotaR/reference/sids_load.md),
[`sids_save()`](https://docs.ropensci.org/phylotaR/reference/sids_save.md),
[`sqs_count()`](https://docs.ropensci.org/phylotaR/reference/sqs_count.md),
[`sqs_save()`](https://docs.ropensci.org/phylotaR/reference/sqs_save.md),
[`stages_run()`](https://docs.ropensci.org/phylotaR/reference/stages_run.md),
[`tax_download()`](https://docs.ropensci.org/phylotaR/reference/tax_download.md),
[`taxdict_gen()`](https://docs.ropensci.org/phylotaR/reference/taxdict_gen.md),
[`taxtree_gen()`](https://docs.ropensci.org/phylotaR/reference/taxtree_gen.md),
[`txids_get()`](https://docs.ropensci.org/phylotaR/reference/txids_get.md),
[`txnds_count()`](https://docs.ropensci.org/phylotaR/reference/txnds_count.md),
[`warn()`](https://docs.ropensci.org/phylotaR/reference/warn.md)
