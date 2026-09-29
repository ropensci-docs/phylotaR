# Get pre-distances

Return root to tip distances (prdst) for `ids`

## Usage

``` r
getNdsPrdst(tree, ids, parallel = FALSE, progress = "none")
```

## Arguments

- tree:

  `TreeMan` object

- ids:

  vector of node ids

- parallel:

  logical, make parallel?

- progress:

  name of the progress bar to use, see
  [`create_progress_bar`](https://rdrr.io/pkg/plyr/man/create_progress_bar.html)

## Details

Sums the lengths of all branches from `ids` to root.

## See also

[`getNdPrdst`](https://docs.ropensci.org/phylotaR/reference/getNdPrdst.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

tree <- randTree(10)
getNdsPrdst(tree, ids = tree["tips"]) # return prdsts for all tips
#>       t1      t10       t2       t3       t4       t5       t6       t7 
#> 1.014101 1.906025 1.569293 2.024987 2.872199 2.330097 2.032350 1.027848 
#>       t8       t9 
#> 2.152831 2.508484 
```
