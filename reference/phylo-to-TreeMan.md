# Convert phylo to TreeMan

Return a `TreeMan` from ape's `phylo`. This will preserve node labels,
if they are a alphanumeric.

## See also

[`TreeMan-to-phylo`](https://docs.ropensci.org/phylotaR/reference/TreeMan-to-phylo.md),
[`TreeMen-to-multiPhylo`](https://docs.ropensci.org/phylotaR/reference/TreeMen-to-multiPhylo.md)
[`multiPhylo-to-TreeMen`](https://docs.ropensci.org/phylotaR/reference/multiPhylo-to-TreeMen.md)
[`TreeMan-class`](https://docs.ropensci.org/phylotaR/reference/TreeMan-class.md)

## Examples

``` r

library(ape)
tree <- compute.brlen(rtree(10))
tree <- as(tree, "TreeMan")
```
