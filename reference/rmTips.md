# Remove tips from a tree

Returns a tree with a tip ID(s) removed

## Usage

``` r
rmTips(tree, tids, drp_intrnl = TRUE, progress = "none")
```

## Arguments

- tree:

  `TreeMan` object

- tids:

  tip IDs

- drp_intrnl:

  Boolean, drop internal branches, default FALSE

- progress:

  name of the progress bar to use, see
  [`create_progress_bar`](https://rdrr.io/pkg/plyr/man/create_progress_bar.html)

## Details

Removes tips in a tree. Set drp_intrnl to FALSE to convert internal
nodes into new tips. Warning: do not use this function to remove
internal nodes, this create a corrupted tree.

## See also

[`addTip`](https://docs.ropensci.org/phylotaR/reference/addTip.md),
[`rmNodes`](https://docs.ropensci.org/phylotaR/reference/rmNodes.md),
<https://github.com/DomBennett/treeman/wiki/manip-methods>

## Examples

``` r

tree <- randTree(10)
tree <- rmTips(tree, "t1")
summary(tree)
#> Tree (TreeMan Object):
#>   + 9 tips
#>   + 8 internal nodes
#>   + Binary
#>   + PD 8.39
#>   + Root node is "n1"
# running the function using an internal
# node will create a corrupted tree
tree <- rmTips(tree, "n3")
# run summary() to make sure a change has
# not created a corruption
# summary(tree)
```
