# Get children IDs

Return the node ids of all tips that descend from node.

## Usage

``` r
getNdKids(tree, id)
```

## Arguments

- tree:

  `TreeMan` object

- id:

  node id

## Details

Returns a vector

## See also

[`getNdsKids`](https://docs.ropensci.org/phylotaR/reference/getNdsKids.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

tree <- randTree(10)
# everyone descends from root
getNdKids(tree, id = tree["root"])
#>  [1] "t1"  "t2"  "t3"  "t4"  "t5"  "t6"  "t7"  "t8"  "t9"  "t10"
```
