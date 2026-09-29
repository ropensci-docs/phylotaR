# Calculate the balance of a node

Returns the balance of a node.

## Usage

``` r
calcNdBlnc(tree, id)
```

## Arguments

- tree:

  `TreeMan` object

- id:

  node id

## Details

Balance is calculated as the absolute difference between the number of
descendents of the two bifurcating edges of a node and the expected
value for a balanced tree. `NA` is returned if the node is polytomous or
a tip.

## See also

[`calcNdsBlnc`](https://docs.ropensci.org/phylotaR/reference/calcNdsBlnc.md),
<https://github.com/DomBennett/treeman/wiki/calc-methods>

## Examples

``` r

tree <- randTree(10)
calcNdBlnc(tree, id = tree["root"]) # root balance
#> [1] 2
```
