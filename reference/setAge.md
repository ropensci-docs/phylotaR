# Set the age of a tree

Return a tree with the age altered.

## Usage

``` r
setAge(tree, val)
```

## Arguments

- tree:

  `TreeMan` object

- val:

  new age

## Details

Use this function to change the age of a tree. For example, you might
want to convert the tree so that its age equals 1. This function will
achieve that by modiyfing every branch, while maintaining their relative
lengths.

## See also

[`setPD`](https://docs.ropensci.org/phylotaR/reference/setPD.md)
<https://github.com/DomBennett/treeman/wiki/set-methods>

## Examples

``` r

tree <- randTree(10)
tree <- setAge(tree, val = 1)
summary(tree)
#> Tree (TreeMan Object):
#>   + 10 tips
#>   + 9 internal nodes
#>   + Binary
#>   + PD 2.56
#>   + Root node is "n1"
```
