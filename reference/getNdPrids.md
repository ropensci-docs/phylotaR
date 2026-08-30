# Get pre-nodes to root

Return node ids for connecting `id` to root.

## Usage

``` r
getNdPrids(tree, id)
```

## Arguments

- tree:

  `TreeMan` object

- id:

  node id

## Details

Returns a vector. IDs are returned order from node ID to root.

## See also

[`getNdsPrids`](https://docs.ropensci.org/phylotaR/reference/getNdsPrids.md),
[`getNdPtids`](https://docs.ropensci.org/phylotaR/reference/getNdPtids.md),
[`getNdsPtids`](https://docs.ropensci.org/phylotaR/reference/getNdsPtids.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

tree <- randTree(10)
# get all nodes to root
getNdPrids(tree, id = "t1")
#> [1] "n6" "n5" "n3" "n2" "n1"
```
