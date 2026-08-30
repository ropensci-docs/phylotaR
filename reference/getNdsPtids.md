# Get post-nodes to tips for multiple nodes

Return node ids for connecting `ids` to kids.

## Usage

``` r
getNdsPtids(tree, ids, parallel = FALSE, progress = "none")
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

Returns a list, parallizable.

## See also

[`getNdPtids`](https://docs.ropensci.org/phylotaR/reference/getNdPtids.md),
[`getNdPrids`](https://docs.ropensci.org/phylotaR/reference/getNdPrids.md),
[`getNdsPrids`](https://docs.ropensci.org/phylotaR/reference/getNdsPrids.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

tree <- randTree(10)
# get all nodes to tip for all nodes
getNdsPtids(tree, ids = tree["nds"])
#> $n1
#>  [1] "n2"  "n3"  "n4"  "n5"  "n6"  "n7"  "n8"  "n9"  "t1"  "t2"  "t3"  "t4" 
#> [13] "t5"  "t6"  "t7"  "t8"  "t9"  "t10"
#> 
#> $n2
#>  [1] "n3"  "n4"  "n6"  "n7"  "n9"  "t1"  "t4"  "t5"  "t7"  "t8"  "t9"  "t10"
#> 
#> $n3
#> [1] "n4" "t5" "t8" "t9"
#> 
#> $n4
#> [1] "t5" "t9"
#> 
#> $n5
#> [1] "n8" "t2" "t3" "t6"
#> 
#> $n6
#> [1] "n7"  "n9"  "t1"  "t4"  "t7"  "t10"
#> 
#> $n7
#> [1] "t1" "t4"
#> 
#> $n8
#> [1] "t2" "t3"
#> 
#> $n9
#> [1] "t7"  "t10"
#> 
```
