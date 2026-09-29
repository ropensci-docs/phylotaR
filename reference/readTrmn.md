# Read a .trmn tree

Return a `TreeMan` or `TreeMen` object from a .trmn treefile

## Usage

``` r
readTrmn(file, wndmtrx = FALSE, parallel = FALSE, progress = "none")
```

## Arguments

- file:

  file path

- wndmtrx:

  T/F add node matrix? Default FALSE.

- parallel:

  logical, make parallel?

- progress:

  name of the progress bar to use, see
  [`create_progress_bar`](https://rdrr.io/pkg/plyr/man/create_progress_bar.html)

## Details

Read a tree(s) from a file using the .trmn format. It is faster to read
and write tree files using treeman with the .trmn file format. In
addition it is possible to encode more information than possible with
the Newick, e.g. any taxonomic information and additional slot names
added to the tree are recorded in the file.

## See also

[`writeTrmn`](https://docs.ropensci.org/phylotaR/reference/writeTrmn.md),
[`readTree`](https://docs.ropensci.org/phylotaR/reference/readTree.md),[`writeTree`](https://docs.ropensci.org/phylotaR/reference/writeTree.md),
[`randTree`](https://docs.ropensci.org/phylotaR/reference/randTree.md),
[`saveTreeMan`](https://docs.ropensci.org/phylotaR/reference/saveTreeMan.md),
[`loadTreeMan`](https://docs.ropensci.org/phylotaR/reference/loadTreeMan.md)

## Examples

``` r

tree <- randTree(10)
writeTrmn(tree, file = "test.trmn")
tree <- readTrmn("test.trmn")
file.remove("test.trmn")
#> [1] TRUE
```
