# Get ages for multiple nodes

Return the age for `ids`.

## Usage

``` r
getNdsAge(tree, ids, tree_age, parallel = FALSE, progress = "none")
```

## Arguments

- tree:

  `TreeMan` object

- ids:

  vector of node ids

- tree_age:

  numeric value of known age of tree

- parallel:

  logical, make parallel?

- progress:

  name of the progress bar to use, see
  [`create_progress_bar`](https://rdrr.io/pkg/plyr/man/create_progress_bar.html)

## Details

Returns a vector, parallelizable.

## See also

[`getNdAge`](https://docs.ropensci.org/phylotaR/reference/getNdAge.md),
[`getSpnAge`](https://docs.ropensci.org/phylotaR/reference/getSpnAge.md),
[`getSpnsAge`](https://docs.ropensci.org/phylotaR/reference/getSpnsAge.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

tree <- randTree(10)
getNdsAge(tree, ids = tree["nds"], tree_age = getAge(tree))
#>        n1        n2        n3        n4        n5        n6        n7        n8 
#> 2.4037820 2.0855576 2.2690312 1.1422668 1.6715032 0.9465052 0.8283989 1.5896087 
#>        n9 
#> 0.5606578 
```
