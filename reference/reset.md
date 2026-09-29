# Reset a phylotaR pipeline run

Resets the pipeline to a specified stage.

## Usage

``` r
reset(wd, stage, hard = FALSE)
```

## Arguments

- wd:

  Working directory

- stage:

  Name of stage to which the pipeline will be reset

- hard:

  T/F, delete all cached data?

## See also

Other run-public:
[`ClstrArc-class`](https://docs.ropensci.org/phylotaR/reference/ClstrArc-class.md),
[`ClstrRec-class`](https://docs.ropensci.org/phylotaR/reference/ClstrRec-class.md),
[`Phylota-class`](https://docs.ropensci.org/phylotaR/reference/Phylota-class.md),
[`SeqArc-class`](https://docs.ropensci.org/phylotaR/reference/SeqArc-class.md),
[`SeqRec-class`](https://docs.ropensci.org/phylotaR/reference/SeqRec-class.md),
[`TaxDict-class`](https://docs.ropensci.org/phylotaR/reference/TaxDict-class.md),
[`TaxRec-class`](https://docs.ropensci.org/phylotaR/reference/TaxRec-class.md),
[`clusters2_run()`](https://docs.ropensci.org/phylotaR/reference/clusters2_run.md),
[`clusters_run()`](https://docs.ropensci.org/phylotaR/reference/clusters_run.md),
[`parameters_reset()`](https://docs.ropensci.org/phylotaR/reference/parameters_reset.md),
[`restart()`](https://docs.ropensci.org/phylotaR/reference/restart.md),
[`run()`](https://docs.ropensci.org/phylotaR/reference/run.md),
[`setup()`](https://docs.ropensci.org/phylotaR/reference/setup.md),
[`taxise_run()`](https://docs.ropensci.org/phylotaR/reference/taxise_run.md)

## Examples

``` r
if (FALSE) { # \dontrun{
  
  # Note: this example requires BLAST and internet to run.
  
  # example with temp folder
  wd <- file.path(tempdir(), 'aotus')
  # setup for aotus, make sure aotus/ folder already exists
  if (!dir.exists(wd)) {
    dir.create(wd)
  }
  ncbi_dr <- '[SET BLAST+ BIN PATH HERE]'
  setup(wd = wd, txid = 9504, ncbi_dr = ncbi_dr)  # txid for Aotus primate genus
  # individually run taxise
  taxise_run(wd = wd)
  # reset back to taxise as if it has not been run
  reset(wd = 'aotus', stage = 'taxise')
  # run taxise again ....
  taxise_run(wd = wd)
} # }
```
