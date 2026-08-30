# Remove node matrix

Return tree with memory heavy node matrix removed.

## Usage

``` r
rmNdmtrx(tree)
```

## Arguments

- tree:

  `TreeMan` object

## Details

Potential uses: reduce memory load of a tree, save tree using
serialization methods.

## See also

[`addNdmtrx`](https://docs.ropensci.org/phylotaR/reference/addNdmtrx.md)

## Examples

``` r
#
tree <- randTree(10)
summary(tree)
#> Tree (TreeMan Object):
#>   + 10 tips
#>   + 9 internal nodes
#>   + Binary
#>   + PD 9.44
#>   + Root node is "n1"
tree <- rmNdmtrx(tree)
summary(tree)
#> Tree (TreeMan Object):
#>   + 10 tips
#>   + 9 internal nodes
#>   + Binary
#>   + PD 9.44
#>   + Root node is "n1"
```
