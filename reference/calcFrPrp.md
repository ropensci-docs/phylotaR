# Calculate evolutionary distinctness

Returns the evolutationary distinctness of ids using the fair proportion
metric.

## Usage

``` r
calcFrPrp(tree, tids, progress = "none")
```

## Arguments

- tree:

  `TreeMan` object

- tids:

  tip IDs

- progress:

  name of the progress bar to use, see
  [`create_progress_bar`](https://rdrr.io/pkg/plyr/man/create_progress_bar.html)

## Details

The fair proportion metric calculates the evolutionary distinctness of
tips in a tree through summing the total amount of branch length each
tip represents, where each branch in the tree is evenly divided between
all descendants. Parallelizable.

## References

Isaac, N.J.B., Turvey, S.T., Collen, B., Waterman, C. and Baillie,
J.E.M. (2007). Mammals on the EDGE: conservation priorities based on
threat and phylogeny. PLoS ONE, 2, e296.

## See also

[`calcPhyDv`](https://docs.ropensci.org/phylotaR/reference/calcPhyDv.md),
[`calcPrtFrPrp`](https://docs.ropensci.org/phylotaR/reference/calcPrtFrPrp.md),
<https://github.com/DomBennett/treeman/wiki/calc-methods>

## Examples

``` r

tree <- randTree(10)
calcFrPrp(tree, tree["tips"])
#>         t1        t10         t2         t3         t4         t5         t6 
#> 1.29316066 0.65100499 0.46602716 1.10509473 0.77772731 0.07540477 0.94844240 
#>         t7         t8         t9 
#> 0.68677047 1.27463660 1.32327011 
```
