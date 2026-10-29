# Calculate the BLD between two trees

Returns the branch length distance between two trees.

## Usage

``` r
calcDstBLD(tree_1, tree_2, nrmlsd = FALSE, parallel = FALSE, progress = "none")
```

## Arguments

- tree_1:

  `TreeMan` object

- tree_2:

  `TreeMan` object

- nrmlsd:

  Boolean, should returned value be between 0 and 1? Default, FALSE.

- parallel:

  logical, make parallel?

- progress:

  name of the progress bar to use, see
  [`create_progress_bar`](https://rdrr.io/pkg/plyr/man/create_progress_bar.html)

## Details

BLD is the Robinson-Foulds distance weighted by branch length. Instead
of summing the differences in partitions between the two trees, the
metric takes the square root of the squared difference in branch
lengths. Parallelizable.

## References

Kuhner, M. K. and Felsenstein, J. (1994) Simulation comparison of
phylogeny algorithms under equal and unequal evolutionary rates.
Molecular Biology and Evolution, 11, 459-468.

## See also

[`calcDstTrp`](https://docs.ropensci.org/phylotaR/reference/calcDstTrp.md),
[`calcDstRF`](https://docs.ropensci.org/phylotaR/reference/calcDstRF.md)
<https://github.com/DomBennett/treeman/wiki/calc-methods>

## Examples

``` r

tree_1 <- randTree(10)
tree_2 <- randTree(10)
calcDstBLD(tree_1, tree_2)
#> [1] 2.1869
```
