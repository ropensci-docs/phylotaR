# Set the branch lengths of specific nodes

Return a tree with the spans of nodes altered.

## Usage

``` r
setNdsSpn(tree, ids, vals, parallel = FALSE, progress = "none")
```

## Arguments

- tree:

  `TreeMan` object

- ids:

  ids of nodes whose preceding edges are to be changed

- vals:

  new spans

- parallel:

  logical, make parallel?

- progress:

  name of the progress bar to use, see
  [`create_progress_bar`](https://rdrr.io/pkg/plyr/man/create_progress_bar.html)

## Details

Runs `setNdSpn` over multiple nodes. Parallelizable.

## See also

[`setNdSpn`](https://docs.ropensci.org/phylotaR/reference/setNdSpn.md)
<https://github.com/DomBennett/treeman/wiki/set-methods>

## Examples

``` r

tree <- randTree(10)
# make tree taxonomic
tree <- setNdsSpn(tree, ids = tree["all"], vals = 1)
summary(tree)
#> Tree (TreeMan Object):
#>   + 10 tips
#>   + 9 internal nodes
#>   + Binary
#>   + PD 19
#>   + Root node is "n1"
# remove spns by setting all to 0
tree <- setNdsSpn(tree, ids = tree["all"], vals = 0)
summary(tree)
#> Tree (TreeMan Object):
#>   + 10 tips
#>   + 9 internal nodes
#>   + Binary
#>   + Without node spans
#>   + Root node is "n1"
```
