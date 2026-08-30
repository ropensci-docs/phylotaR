# Get post-nodes to tips

Return node ids for connecting `id` to kids.

## Usage

``` r
getNdPtids(tree, id)
```

## Arguments

- tree:

  `TreeMan` object

- id:

  node id

## Details

Returns a vector.

## See also

[`getNdsPtids`](https://docs.ropensci.org/phylotaR/reference/getNdsPtids.md),
[`getNdPrids`](https://docs.ropensci.org/phylotaR/reference/getNdPrids.md),
[`getNdsPrids`](https://docs.ropensci.org/phylotaR/reference/getNdsPrids.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

tree <- randTree(10)
# get all nodes from root to tip
getNdPtids(tree, id = "n1")
#>  [1] "n2"  "n3"  "n4"  "n5"  "n6"  "n7"  "n8"  "n9"  "t1"  "t2"  "t3"  "t4" 
#> [13] "t5"  "t6"  "t7"  "t8"  "t9"  "t10"
```
