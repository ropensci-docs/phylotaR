# Set the IDs of multiple nodes

Return a tree with the IDs of nodes altered.

## Usage

``` r
setNdsID(tree, ids, vals, parallel = FALSE, progress = "none")
```

## Arguments

- tree:

  `TreeMan` object

- ids:

  ids to be changed

- vals:

  new ids

- parallel:

  logical, make parallel?

- progress:

  name of the progress bar to use, see
  [`create_progress_bar`](https://rdrr.io/pkg/plyr/man/create_progress_bar.html)

## Details

Runs
[`setNdID()`](https://docs.ropensci.org/phylotaR/reference/setNdID.md)
over multiple nodes. Warning: all IDs must be unique, avoid spaces in
IDs, only use numbers, letters and underscores. Parellizable.

## See also

[`setNdID`](https://docs.ropensci.org/phylotaR/reference/setNdID.md)
<https://github.com/DomBennett/treeman/wiki/set-methods>

## Examples

``` r

tree <- randTree(10)
new_ids <- paste0("heffalump_", 1:tree["ntips"])
tree <- setNdsID(tree, tree["tips"], new_ids)
summary(tree)
#> Tree (TreeMan Object):
#>   + 10 tips
#>   + 9 internal nodes
#>   + Binary
#>   + PD 9.79
#>   + Root node is "n1"
```
