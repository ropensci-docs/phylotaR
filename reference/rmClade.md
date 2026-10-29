# Remove a clade from a tree

Returns a tree with a clade removed

## Usage

``` r
rmClade(tree, id)
```

## Arguments

- tree:

  `TreeMan` object

- id:

  node ID parent of clade to be removed

## Details

Inverse function of
[`getSubtree()`](https://docs.ropensci.org/phylotaR/reference/getSubtree.md).
Takes a tree and removes a clade based on an internal node specified.
Node is specified with `id`, all descending nodes and tips are removed.
The resulting tree will replace the missing clade with a tip of `id`.

## See also

[`addClade`](https://docs.ropensci.org/phylotaR/reference/addClade.md),
[`getSubtree`](https://docs.ropensci.org/phylotaR/reference/getSubtree.md),
[`rmTips`](https://docs.ropensci.org/phylotaR/reference/rmTips.md)
<https://github.com/DomBennett/treeman/wiki/manip-methods>

## Examples

``` r

t1 <- randTree(100)
# remove a clade
t2 <- rmClade(t1, "n2")
summary(t1)
#> Tree (TreeMan Object):
#>   + 100 tips
#>   + 99 internal nodes
#>   + Binary
#>   + PD 102
#>   + Root node is "n1"
summary(t2)
#> Tree (TreeMan Object):
#>   + 36 tips
#>   + 35 internal nodes
#>   + Binary
#>   + PD 35.3
#>   + Root node is "n1"
```
