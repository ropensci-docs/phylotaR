# Get phylogenetic diversity of node

Return summed value of all descending spns

## Usage

``` r
getNdPD(tree, id)
```

## Arguments

- tree:

  `TreeMan` object

- id:

  node id

## Details

Sums the lengths of all descending branches from a node.

## See also

[`getNdsPD`](https://docs.ropensci.org/phylotaR/reference/getNdsPD.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

tree <- randTree(10)
getNdPD(tree, id = "n1") # return PD of n1 which in this case is for the whole tree
#> [1] 5.626307
```
