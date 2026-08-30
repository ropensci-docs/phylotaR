# Calculate the Robinson-Foulds distance between two trees

Returns the Robinson-Foulds distance between two trees.

## Usage

``` r
calcDstRF(tree_1, tree_2, nrmlsd = FALSE)
```

## Arguments

- tree_1:

  `TreeMan` object

- tree_2:

  `TreeMan` object

- nrmlsd:

  Boolean, should returned value be between 0 and 1? Default, FALSE.

## Details

RF distance is calculated as the sum of partitions in one tree that are
not shared by the other. The maximum number of split differences is the
total number of nodes in both trees (excluding the roots). Trees are
assumed to be bifurcating, this is not tested. The metric is calculated
as if trees are unrooted. Parallelizable.

## References

Robinson, D. R.; Foulds, L. R. (1981). "Comparison of phylogenetic
trees". Mathematical Biosciences 53: 131-147.

## See also

[`calcDstBLD`](https://docs.ropensci.org/phylotaR/reference/calcDstBLD.md),
[`calcDstTrp`](https://docs.ropensci.org/phylotaR/reference/calcDstTrp.md)
<https://github.com/DomBennett/treeman/wiki/calc-methods>

## Examples

``` r

tree_1 <- randTree(10)
tree_2 <- randTree(10)
calcDstRF(tree_1, tree_2)
#> [1] 14
```
