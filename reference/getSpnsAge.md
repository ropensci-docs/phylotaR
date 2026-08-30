# Get age ranges for multiple nodes

Return start and end ages for `ids` from when they first appear to when
they split

## Usage

``` r
getSpnsAge(tree, ids, tree_age, parallel = FALSE, progress = "none")
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

Returns a dataframe, parallelizable.

## See also

[`getNdAge`](https://docs.ropensci.org/phylotaR/reference/getNdAge.md),
[`getNdsAge`](https://docs.ropensci.org/phylotaR/reference/getNdsAge.md),
[`getSpnAge`](https://docs.ropensci.org/phylotaR/reference/getSpnAge.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

tree <- randTree(10)
# all nodes but root
ids <- tree["nds"][tree["nds"] != tree["root"]]
getSpnsAge(tree, ids = ids, tree_age = getAge(tree))
#>   spn    start       end
#> 1  n2 3.171887 2.1793670
#> 2  n3 3.171887 2.4629002
#> 3  n4 2.179367 1.4259549
#> 4  n5 2.462900 1.9475839
#> 5  n6 2.462900 1.8489569
#> 6  n7 1.848957 1.7952116
#> 7  n8 1.425955 0.9799168
#> 8  n9 1.795212 1.6482859
```
