# Resolve taxonmic names online

Resolve taxonomic names via the Global Names Resolver.

## Usage

``` r
taxaResolve(
  nms,
  batch = 100,
  datasource = 4,
  genus = TRUE,
  cache = FALSE,
  parent = NULL
)
```

## Arguments

- nms:

  vector of names

- batch:

  size of the batches to be queried

- datasource:

  ID number of the datasource

- genus:

  boolean, if true will search against GNR with just the genus name for
  names that failed to resolve using the full species name

- cache:

  T/F, create a local cache of downloaded names?

- parent:

  specify parent of all names to prevent false names

## Details

Returns dataframe containing GNR metadata for each name wames that
cannot be resolved are returned as NA. Various datasources are
available, see <http://resolver.globalnames.org/data_sources> for a list
and IDs. Default is 4 for NCBI. Will raise a warning if connection fails
and will return NULL.

## See also

[`searchTxnyms`](https://docs.ropensci.org/phylotaR/reference/searchTxnyms.md),
[`setTxnyms`](https://docs.ropensci.org/phylotaR/reference/setTxnyms.md),
[`getNdsFrmTxnyms`](https://docs.ropensci.org/phylotaR/reference/getNdsFrmTxnyms.md)

## Examples

``` r
# \donttest{
my_lovely_names <- c(
  "Gallus gallus", "Pongo pingu", "Homo sapiens",
  "Arabidopsis thaliana", "Macaca thibetana", "Bacillus subtilis"
)
res <- taxaResolve(nms = my_lovely_names)
#> ---- Connection failed: trying again in [2s]----
#> ---- Connection failed: trying again in [4s]----
#> ---- Connection failed: trying again in [8s]----
#> ---- Connection failed: trying again in [16s]----
#> ---- Connection failed: trying again in [32s]----
#> Warning: Failed to connect, server may be down.
if (!is.null(res) && nrow(res) > 0) {
  length(colnames(res)) # 10 different metadata for returned names
  # let's look at the lineages
  lineages <- strsplit(as.vector(res$lineage), "\\|")
  print(lineages[[6]]) # the bacteria has far fewer taxonomic levels
}
# }
```
