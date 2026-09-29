# Remove a user-defined slot

Returns a tree with a user-defined tree slot removed.

## Usage

``` r
rmOtherSlt(tree, slt_nm)
```

## Arguments

- tree:

  `TreeMan` object

- slt_nm:

  name of slot to be removed

## Details

A user can specify a new slot using the `setNdSlt()` function or upon
reading a tree. This can be removed using this function by specifying
the name of the slot to be removed.

## See also

[`setNdOther`](https://docs.ropensci.org/phylotaR/reference/setNdOther.md),
[`setNdsOther`](https://docs.ropensci.org/phylotaR/reference/setNdsOther.md),
<https://github.com/DomBennett/treeman/wiki/set-methods>

## Examples

``` r

tree <- randTree(10)
vals <- runif(min = 0, max = 1, n = tree["nall"])
tree <- setNdsOther(tree, tree["all"], vals, "confidence")
tree <- updateSlts(tree)
summary(tree)
#> Tree (TreeMan Object):
#>   + 10 tips
#>   + 9 internal nodes
#>   + Binary
#>   + PD 9.01
#>   + Root node is "n1"
#>   + With additional node slots:
#>     [confidence]
tree <- rmOtherSlt(tree, "confidence")
tree <- updateSlts(tree)
summary(tree)
#> Tree (TreeMan Object):
#>   + 10 tips
#>   + 9 internal nodes
#>   + Binary
#>   + PD 9.01
#>   + Root node is "n1"
```
