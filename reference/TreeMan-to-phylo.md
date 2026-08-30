# Convert TreeMan to phylo

Return ape's `phylo` from a `TreeMan`. This will preserve node labels if
they are different from the default labels (n#).

## See also

[`phylo-to-TreeMan`](https://docs.ropensci.org/phylotaR/reference/phylo-to-TreeMan.md),
[`TreeMen-to-multiPhylo`](https://docs.ropensci.org/phylotaR/reference/TreeMen-to-multiPhylo.md)
[`multiPhylo-to-TreeMen`](https://docs.ropensci.org/phylotaR/reference/multiPhylo-to-TreeMen.md)
[`TreeMan-class`](https://docs.ropensci.org/phylotaR/reference/TreeMan-class.md)

## Examples

``` r

library(ape)
tree <- randTree(10)
tree <- as(tree, "phylo")
```
