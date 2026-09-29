# Convert multiPhylo to TreeMen

Return a `TreeMen` from ape's `mutlPhylo`

## See also

[`TreeMan-to-phylo`](https://docs.ropensci.org/phylotaR/reference/TreeMan-to-phylo.md),
[`phylo-to-TreeMan`](https://docs.ropensci.org/phylotaR/reference/phylo-to-TreeMan.md),
[`TreeMen-to-multiPhylo`](https://docs.ropensci.org/phylotaR/reference/TreeMen-to-multiPhylo.md)
[`TreeMan-class`](https://docs.ropensci.org/phylotaR/reference/TreeMan-class.md)

## Examples

``` r

library(ape)
trees <- c(rtree(10), rtree(10), rtree(10))
trees <- as(trees, "TreeMen")
```
