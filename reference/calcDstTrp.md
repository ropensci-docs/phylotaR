# Calculate the triplet distance between two trees

Returns the triplet distance between two trees.

## Usage

``` r
calcDstTrp(tree_1, tree_2, nrmlsd = FALSE, parallel = FALSE, progress = "none")
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

The triplet distance is calculated as the sum of different outgroups
among every triplet of tips between the two trees. Normalisation is
performed by dividing the resulting number by the total number of
triplets shared between the two trees. The triplet distance is
calculated only for shared tips between the two trees. Parallelizable.

## References

Critchlow DE, Pearl DK, Qian C. (1996) The Triples Distance for rooted
bifurcating phylogenetic trees. Systematic Biology, 45, 323-34.

## See also

[`calcDstBLD`](https://docs.ropensci.org/phylotaR/reference/calcDstBLD.md),
[`calcDstRF`](https://docs.ropensci.org/phylotaR/reference/calcDstRF.md)
<https://github.com/DomBennett/treeman/wiki/calc-methods>

## Examples

``` r

tree_1 <- randTree(10)
tree_2 <- randTree(10)
calcDstTrp(tree_1, tree_2)
#> [1] 80
```
