# Calculate the balances of all nodes

Returns the absolute differences in number of descendants for
bifurcating branches of every node

## Usage

``` r
calcNdsBlnc(tree, ids, parallel = FALSE, progress = "none")
```

## Arguments

- tree:

  `TreeMan` object

- ids:

  node ids

- parallel:

  logical, make parallel?

- progress:

  name of the progress bar to use, see
  [`create_progress_bar`](https://rdrr.io/pkg/plyr/man/create_progress_bar.html)

## Details

Runs
[`calcNdBlnc()`](https://docs.ropensci.org/phylotaR/reference/calcNdBlnc.md)
across all node IDs. `NA` is returned if the node is polytomous.
Parallelizable.

## See also

[`calcNdBlnc`](https://docs.ropensci.org/phylotaR/reference/calcNdBlnc.md),
<https://github.com/DomBennett/treeman/wiki/calc-methods>

## Examples

``` r

tree <- randTree(10)
calcNdsBlnc(tree, ids = tree["nds"])
#> [1] 1.0 2.0 0.5 1.0 0.0 0.5 0.5 0.0 0.0
```
