# Calculate evolutionary distinctness for part of tree

Returns the evolutationary distinctness of ids using the fair proportion
metric.

## Usage

``` r
calcPrtFrPrp(tree, tids, ignr = NULL, progress = "none")
```

## Arguments

- tree:

  `TreeMan` object

- tids:

  tip IDs

- ignr:

  tips to ignore in calculation

- progress:

  name of the progress bar to use, see
  [`create_progress_bar`](https://rdrr.io/pkg/plyr/man/create_progress_bar.html)

## Details

Extension of
[`calcFrPrp()`](https://docs.ropensci.org/phylotaR/reference/calcFrPrp.md)
but with ignore argument. Use `ignr` to ignore certain tips from
calculation. For example, if any of tips are extinct you may wish to
ignore these.

## References

Isaac, N.J.B., Turvey, S.T., Collen, B., Waterman, C. and Baillie,
J.E.M. (2007). Mammals on the EDGE: conservation priorities based on
threat and phylogeny. PLoS ONE, 2, e296.

## See also

[`calcFrPrp`](https://docs.ropensci.org/phylotaR/reference/calcFrPrp.md)
<https://github.com/DomBennett/treeman/wiki/calc-methods>

## Examples

``` r

tree <- randTree(10)
calcPrtFrPrp(tree, c("t1", "t3"), ignr = "t2")
#>        t1        t3 
#> 1.2664055 0.7229127 
```
