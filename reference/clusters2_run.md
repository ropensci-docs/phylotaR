# Run the cluster2 stage

Run the fourth stage of the phylotaR pipeline, cluster2. Identify
clusters at higher taxonomic levels by merging sister clusters.

## Usage

``` r
clusters2_run(wd)
```

## Arguments

- wd:

  Working directory

## See also

Other run-public:
[`ClstrArc-class`](https://docs.ropensci.org/phylotaR/reference/ClstrArc-class.md),
[`ClstrRec-class`](https://docs.ropensci.org/phylotaR/reference/ClstrRec-class.md),
[`Phylota-class`](https://docs.ropensci.org/phylotaR/reference/Phylota-class.md),
[`SeqArc-class`](https://docs.ropensci.org/phylotaR/reference/SeqArc-class.md),
[`SeqRec-class`](https://docs.ropensci.org/phylotaR/reference/SeqRec-class.md),
[`TaxDict-class`](https://docs.ropensci.org/phylotaR/reference/TaxDict-class.md),
[`TaxRec-class`](https://docs.ropensci.org/phylotaR/reference/TaxRec-class.md),
[`clusters_run()`](https://docs.ropensci.org/phylotaR/reference/clusters_run.md),
[`parameters_reset()`](https://docs.ropensci.org/phylotaR/reference/parameters_reset.md),
[`reset()`](https://docs.ropensci.org/phylotaR/reference/reset.md),
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
  # individually run stages
  taxise_run(wd = wd)
  download_run(wd = wd)
  clusters_run(wd = wd)
  clusters2_run(wd = wd)
} # }
```
