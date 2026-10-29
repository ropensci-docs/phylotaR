# Set-up parameters

Set up working directory with parameters.

## Usage

``` r
setup(
  wd,
  txid,
  ncbi_dr = ".",
  v = FALSE,
  overwrite = FALSE,
  outsider = FALSE,
  ...
)
```

## Arguments

- wd:

  Working directory

- txid:

  Root taxonomic ID(s), vector or numeric

- ncbi_dr:

  Directory to NCBI BLAST tools, default '.'

- v:

  Verbose, T/F

- overwrite:

  Overwrite existing cache?

- outsider:

  Run through `outsider`? T/F

- ...:

  Additional parameters

## Details

See
[`parameters`](https://docs.ropensci.org/phylotaR/reference/parameters.md)()
for a description of all parameters and their defaults. You can change
parameters after a folder has been set up with
[`parameters_reset`](https://docs.ropensci.org/phylotaR/reference/parameters_reset.md)().

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
[`run()`](https://docs.ropensci.org/phylotaR/reference/run.md),
[`taxise_run()`](https://docs.ropensci.org/phylotaR/reference/taxise_run.md)

## Examples

``` r
if (FALSE) { # \dontrun{
  
  # Note: this example requires BLAST to run.
  
  # example with temp folder
  wd <- file.path(tempdir(), 'aotus')
  # setup for aotus, make sure aotus/ folder already exists
  if (!dir.exists(wd)) {
    dir.create(wd)
  }
  ncbi_dr <- '[SET BLAST+ BIN PATH HERE]'
  # e.g. "/usr/local/ncbi/blast/bin/"
  setup(wd = wd, txid = 9504, ncbi_dr = ncbi_dr)  # txid for Aotus primate genus
  # see ?parameters for all available parameter options
} # }
```
