# Run download stage

Run the second stage of phylotaR, download. This stage downloads
sequences for all nodes with sequence numbers less than mxsqs. It
hierarchically traverses the taxonomy for each node and downloads direct
and subtree sequences for all descendants.

## Usage

``` r
download_run(wd)
```

## Arguments

- wd:

  Working directory

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
} # }
```
