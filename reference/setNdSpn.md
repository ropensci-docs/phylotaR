# Set the branch length of a specific node

Return a tree with the span of a node altered.

## Usage

``` r
setNdSpn(tree, id, val)
```

## Arguments

- tree:

  `TreeMan` object

- id:

  id of node whose preceding edge is to be changed

- val:

  new span

## Details

Takes a tree, a node ID and a new value for the node's preceding branch
length (span).

## See also

[`setNdsSpn`](https://docs.ropensci.org/phylotaR/reference/setNdsSpn.md)
<https://github.com/DomBennett/treeman/wiki/set-methods>

## Examples

``` r

tree <- randTree(10)
tree <- setNdSpn(tree, id = "t1", val = 100)
tree <- updateSlts(tree)
summary(tree)
#> Tree (TreeMan Object):
#>   + 10 tips
#>   + 9 internal nodes
#>   + Binary
#>   + PD 107
#>   + Root node is "n1"
```
