# Get a node slot for multiple nodes

Returns the values of named slot as a vector for atomic values, else
list.

## Usage

``` r
getNdsSlt(tree, slt_nm, ids, parallel = FALSE, progress = "none")
```

## Arguments

- tree:

  `TreeMan` object

- slt_nm:

  slot name

- ids:

  vector of node ids

- parallel:

  logical, make parallel?

- progress:

  name of the progress bar to use, see
  [`create_progress_bar`](https://rdrr.io/pkg/plyr/man/create_progress_bar.html)

## Details

Returned object depends on name, either character, vector or numeric.
Parallelizable. Default node slots are: id, spn, prid, ptid and txnym.

## See also

[`getNdSlt`](https://docs.ropensci.org/phylotaR/reference/getNdSlt.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

tree <- randTree(10)
getNdsSlt(tree, slt_nm = "spn", ids = tree["tips"]) # return spans of all tips
#>           t1          t10           t2           t3           t4           t5 
#> 0.5081212099 0.6583406578 0.0002173744 0.4607886851 0.4825757614 0.7221059527 
#>           t6           t7           t8           t9 
#> 0.6016585629 0.3351444209 0.4105077630 0.7371745745 
```
