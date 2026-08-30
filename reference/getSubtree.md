# Get subtree

Return tree descending from `id`.

## Usage

``` r
getSubtree(tree, id)
```

## Arguments

- tree:

  `TreeMan` object

- id:

  node id

## Details

Returns a `TreeMan`, parallelizable. `id` must be an internal node.

## See also

[`getPrnt`](https://docs.ropensci.org/phylotaR/reference/getPrnt.md),
[`addClade`](https://docs.ropensci.org/phylotaR/reference/addClade.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

data(mammals)
# get tree of apes
ape_id <- getPrnt(mammals, ids = c("Homo_sapiens", "Hylobates_concolor"))
apes <- getSubtree(mammals, id = ape_id)
summary(apes)
#> Tree (TreeMan Object):
#>   + 16 tips
#>   + 12 internal nodes
#>   + With taxonomic names
#>   + Polytomous
#>   + PD 153
#>   + Root node is "n2960"
```
