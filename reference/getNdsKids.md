# Get children IDs for multiple nodes

Return the node ids of all tips that descend from each node in `ids`.

## Usage

``` r
getNdsKids(tree, ids, parallel = FALSE, progress = "none")
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

Returns a list, parallelizable.

## See also

[`getNdKids`](https://docs.ropensci.org/phylotaR/reference/getNdKids.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

tree <- randTree(10)
getNdsKids(tree, id = tree["nds"])
#> $n1
#>  [1] "t1"  "t2"  "t3"  "t4"  "t5"  "t6"  "t7"  "t8"  "t9"  "t10"
#> 
#> $n2
#> [1] "t1" "t2" "t3" "t4" "t5" "t6" "t7" "t8" "t9"
#> 
#> $n3
#> [1] "t1" "t2" "t3" "t4" "t5" "t7" "t8" "t9"
#> 
#> $n4
#> [1] "t2" "t3" "t5" "t7" "t8" "t9"
#> 
#> $n5
#> [1] "t2" "t5" "t8" "t9"
#> 
#> $n6
#> [1] "t3" "t7"
#> 
#> $n7
#> [1] "t2" "t5" "t9"
#> 
#> $n8
#> [1] "t2" "t5"
#> 
#> $n9
#> [1] "t1" "t4"
#> 
```
