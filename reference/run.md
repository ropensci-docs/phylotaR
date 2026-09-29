# Run phylotaR pipeline

Run the entire phylotaR pipeline. All generated files will be stored in
the wd. The process can be stopped at anytime and restarted with
`restart`. `nstages` must be a numeric value representing the number of
stages that will be run. Stages are run in the following order: 1 -
taxise, 2 - download, 3 - cluster and 4 - cluster2.

For example, specifying `nstages` = 3, will run taxise, download and
cluster. Stages can also be run individually, see linked functions
below.

## Usage

``` r
run(wd, nstages = 4)
```

## Arguments

- wd:

  Working directory

- nstages:

  Number of total stages to run, max 4.

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
[`reset()`](https://docs.ropensci.org/phylotaR/reference/reset.md),
[`restart()`](https://docs.ropensci.org/phylotaR/reference/restart.md),
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
  # e.g. "/usr/local/ncbi/blast/bin/"
  setup(wd = wd, txid = 9504, ncbi_dr = ncbi_dr)  # txid for Aotus primate genus
  run(wd = wd)
} # }
```
