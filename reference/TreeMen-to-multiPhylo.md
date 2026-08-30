# Convert TreeMen to multiPhylo

Return ape's `multiPhylo` from a `TreeMen`

## See also

[`TreeMan-to-phylo`](https://docs.ropensci.org/phylotaR/reference/TreeMan-to-phylo.md),
[`phylo-to-TreeMan`](https://docs.ropensci.org/phylotaR/reference/phylo-to-TreeMan.md),
[`multiPhylo-to-TreeMen`](https://docs.ropensci.org/phylotaR/reference/multiPhylo-to-TreeMen.md)
[`TreeMan-class`](https://docs.ropensci.org/phylotaR/reference/TreeMan-class.md)

## Examples

``` r

library(ape)
trees <- cTrees(randTree(10), randTree(10), randTree(10))
trees <- as(trees, "multiPhylo")
```
