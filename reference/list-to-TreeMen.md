# Convert list to a TreeMen

Return a `TreeMen` object from a list of `TreeMans`

## See also

[`TreeMen-class`](https://docs.ropensci.org/phylotaR/reference/TreeMen-class.md)

## Examples

``` r

trees <- list("tree_1" = randTree(10), "tree_2" = randTree(10))
trees <- as(trees, "TreeMen")
```
