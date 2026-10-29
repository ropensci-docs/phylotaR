# Write a Newick tree

Creates a Newick tree from a `TreeMan` object.

## Usage

``` r
writeTree(
  tree,
  file,
  append = FALSE,
  ndLabels = function(nd) {
     return(NULL)
 },
  parallel = FALSE,
  progress = "none"
)
```

## Arguments

- tree:

  `TreeMan` object

- file:

  file path

- append:

  T/F append tree to already existing file

- ndLabels:

  node label function

- parallel:

  logical, make parallel?

- progress:

  name of the progress bar to use, see
  [`create_progress_bar`](https://rdrr.io/pkg/plyr/man/create_progress_bar.html)

## Details

The `ndLabels` argument can be used to add a user defined node label in
the Newick tree. It should take only 1 argument, `nd`, the node
represented as a list. It should only return a single character value
that can be added to a newick string.

## See also

<https://en.wikipedia.org/wiki/Newick_format>,
[`readTree`](https://docs.ropensci.org/phylotaR/reference/readTree.md),
[`randTree`](https://docs.ropensci.org/phylotaR/reference/randTree.md),
[`readTrmn`](https://docs.ropensci.org/phylotaR/reference/readTrmn.md),
[`writeTrmn`](https://docs.ropensci.org/phylotaR/reference/writeTrmn.md),
[`saveTreeMan`](https://docs.ropensci.org/phylotaR/reference/saveTreeMan.md),
[`loadTreeMan`](https://docs.ropensci.org/phylotaR/reference/loadTreeMan.md)

## Examples

``` r

tree <- randTree(10)
# write out the tree with node labels as IDs
ndLabels <- function(n) {
  n[["id"]]
}
writeTree(tree, file = "example.tre", ndLabels = ndLabels)
#> NULL
file.remove("example.tre")
#> [1] TRUE
```
