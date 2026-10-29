# Get node labels based on online taxonomic database

Return names of each node in tree based on searching tip labels through
Global Names Resolver <http://resolver.globalnames.org/> in NCBI.

## Usage

``` r
searchTxnyms(tree, cache = FALSE, parent = NULL, clean = TRUE, infer = TRUE)
```

## Arguments

- tree:

  TreeMan object

- cache:

  T/F, create a local cache of downloaded names?

- parent:

  specify parent of all names to prevent false names

- clean:

  T/F, ensure returned names contain no special characters?

- infer:

  T/F, infer taxonyms for unfound nodes?

## Details

For each node, all the descendants are searched, the taxonomic lineages
returned and then searched to find the lowest shared name. All the tip
labels are searched against a specified taxonomic database through the
GNR and NCBI. (So far only tested with NCBI database.) Use the infer
argument to ensure a taxonym is returned for all nodes. If infer is
true, all nodes without an identifed taxonym adopt the taxonym of their
parent. Will raise a warning if connection fails and will return NULL.

## See also

[`taxaResolve`](https://docs.ropensci.org/phylotaR/reference/taxaResolve.md),
[`setTxnyms`](https://docs.ropensci.org/phylotaR/reference/setTxnyms.md),
[`getNdsFrmTxnyms`](https://docs.ropensci.org/phylotaR/reference/getNdsFrmTxnyms.md)

## Examples

``` r
# \donttest{
tree <- randTree(8)
new_tids <- c(
  "Gallus_gallus", "Aileuropoda_melanoleucha", "Ailurus_fulgens",
  "Rattus_rattus", "Mus_musculus", "Gorilla_gorilla", "Pan_trogoldytes", "Homo_sapiens"
)
tree <- setNdsID(tree, tree["tips"], new_tids)
nd_labels <- searchTxnyms(tree)
#> ---- Connection failed: trying again in [2s]----
#> ---- Connection failed: trying again in [4s]----
#> ---- Connection failed: trying again in [8s]----
#> ---- Connection failed: trying again in [16s]----
#> ---- Connection failed: trying again in [32s]----
#> Warning: Failed to connect, server may be down.
if (!is.null(nd_labels)) {
  print(nd_labels)
}
# }
```
