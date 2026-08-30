# Calculate the distance matrix

Returns a distance matrix for specified ids of a tree.

## Usage

``` r
calcDstMtrx(tree, ids, parallel = FALSE, progress = "none")
```

## Arguments

- tree:

  `TreeMan` object

- ids:

  IDs of nodes/tips

- parallel:

  logical, make parallel?

- progress:

  name of the progress bar to use, see
  [`create_progress_bar`](https://rdrr.io/pkg/plyr/man/create_progress_bar.html)

## Details

The distance between every id in the tree is calculated by summing the
lengths of the branches that connect them. This can be useful for
testing the distances between trees, checking for evoltuionary isolated
tips etc. Parallelizable.

## See also

[`calcDstBLD`](https://docs.ropensci.org/phylotaR/reference/calcDstBLD.md),
[`calcDstRF`](https://docs.ropensci.org/phylotaR/reference/calcDstRF.md),
[`calcDstTrp`](https://docs.ropensci.org/phylotaR/reference/calcDstTrp.md)
<https://github.com/DomBennett/treeman/wiki/calc-methods>

## Examples

``` r
# checking the distance between two trees

tree_1 <- randTree(10)
tree_2 <- randTree(10)
dmat1 <- calcDstMtrx(tree_1, tree_1["tips"])
dmat2 <- calcDstMtrx(tree_2, tree_2["tips"])
mdl <- cor.test(x = dmat1, y = dmat2)
as.numeric(1 - mdl$estimate) # 1 - Pearson's r
#> [1] 0.5503735
```
