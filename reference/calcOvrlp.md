# Calculate phylogenetic overlap

Returns the sum of branch lengths represented by ids_1 and ids_2 for a
tree.

## Usage

``` r
calcOvrlp(
  tree,
  ids_1,
  ids_2,
  nrmlsd = FALSE,
  parallel = FALSE,
  progress = "none"
)
```

## Arguments

- tree:

  `TreeMan` object

- ids_1:

  tip ids of community 1

- ids_2:

  tip ids of community 2

- nrmlsd:

  Boolean, should returned value be between 0 and 1? Default, FALSE.

- parallel:

  logical, make parallel?

- progress:

  name of the progress bar to use, see
  [`create_progress_bar`](https://rdrr.io/pkg/plyr/man/create_progress_bar.html)

## Details

Use this to calculate the sum of branch lengths that are represented
between two communities. This measure is also known as the unique
fraction. It can be used to measure concepts of phylogenetic turnover.
Parallelizable.

## References

Lozupone, C., & Knight, R. (2005). UniFrac: a new phylogenetic method
for comparing microbial communities. Applied and Environmental
Microbiology, 71(12), 8228-35.

## See also

[`calcPhyDv`](https://docs.ropensci.org/phylotaR/reference/calcPhyDv.md)
<https://github.com/DomBennett/treeman/wiki/calc-methods>

## Examples

``` r

tree <- randTree(10)
ids_1 <- sample(tree["tips"], 5)
ids_2 <- sample(tree["tips"], 5)
calcOvrlp(tree, ids_1, ids_2)
#> [1] 4.155736
```
