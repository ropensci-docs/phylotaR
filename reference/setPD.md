# Set the phylogenetic diversity

Return a tree with the phylogenetic diversity altered.

## Usage

``` r
setPD(tree, val)
```

## Arguments

- tree:

  `TreeMan` object

- val:

  new phylogenetic diversity

## Details

Use this function to convert the phylogenetic diversity of a tree. For
example, you might want to convert the tree so the sum of all branches
is 1. This function will achieve that by modiyfing every branch, while
maintaining their relative lengths.

## See also

[`setAge`](https://docs.ropensci.org/phylotaR/reference/setAge.md)
<https://github.com/DomBennett/treeman/wiki/set-methods>

## Examples

``` r

tree <- randTree(10)
tree <- setPD(tree, val = 1)
summary(tree)
#> Tree (TreeMan Object):
#>   + 10 tips
#>   + 9 internal nodes
#>   + Binary
#>   + PD 1
#>   + Root node is "n1"
```
