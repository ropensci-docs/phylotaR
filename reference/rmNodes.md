# Remove nodes from a tree

Returns a tree with a node ID(s) removed

## Usage

``` r
rmNodes(tree, nids, progress = "none")
```

## Arguments

- tree:

  `TreeMan` object

- nids:

  internal node IDs

- progress:

  name of the progress bar to use, see
  [`create_progress_bar`](https://rdrr.io/pkg/plyr/man/create_progress_bar.html)

## Details

Removes nodes in a tree. Joins the nodes following to the nodes
preceding the node to be removed. Creates polytomies. Warning: do not
use this function to remove tip nodes, this create a corrupted tree.

## See also

[`addTip`](https://docs.ropensci.org/phylotaR/reference/addTip.md),
[`rmTips`](https://docs.ropensci.org/phylotaR/reference/rmTips.md),
<https://github.com/DomBennett/treeman/wiki/manip-methods>

## Examples

``` r

tree <- randTree(10)
tree <- rmNodes(tree, "n3")
summary(tree) # tree is now polytmous
#> Tree (TreeMan Object):
#>   + 10 tips
#>   + 8 internal nodes
#>   + Polytomous
#>   + PD 10.2
#>   + Root node is "n1"
```
