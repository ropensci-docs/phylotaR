# Get pre-nodes for multiple nodes

Return node ids for connecting `id` to root.

## Usage

``` r
getNdsPrids(tree, ids, ordrd = FALSE, parallel = FALSE, progress = "none")
```

## Arguments

- tree:

  `TreeMan` object

- ids:

  vector of node ids

- ordrd:

  logical, ensure returned prids are ordered ID to root

- parallel:

  logical, make parallel?

- progress:

  name of the progress bar to use, see
  [`create_progress_bar`](https://rdrr.io/pkg/plyr/man/create_progress_bar.html)

## Details

Returns a list, parallizable. The function will work faster if `ordrd`
is FALSE.

## See also

[`getNdPrids`](https://docs.ropensci.org/phylotaR/reference/getNdPrids.md),
[`getNdPtids`](https://docs.ropensci.org/phylotaR/reference/getNdPtids.md),
[`getNdsPtids`](https://docs.ropensci.org/phylotaR/reference/getNdsPtids.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

tree <- randTree(10)
getNdsPrids(tree, ids = tree["tips"])
#> $t1
#> [1] "n8" "n2" "n1"
#> 
#> $t10
#> [1] "n4" "n3" "n2" "n1"
#> 
#> $t2
#> [1] "n7" "n3" "n2" "n1"
#> 
#> $t3
#> [1] "n9" "n7" "n3" "n2" "n1"
#> 
#> $t4
#> [1] "n9" "n7" "n3" "n2" "n1"
#> 
#> $t5
#> [1] "n6" "n5" "n1"
#> 
#> $t6
#> [1] "n6" "n5" "n1"
#> 
#> $t7
#> [1] "n8" "n2" "n1"
#> 
#> $t8
#> [1] "n4" "n3" "n2" "n1"
#> 
#> $t9
#> [1] "n5" "n1"
#> 
```
