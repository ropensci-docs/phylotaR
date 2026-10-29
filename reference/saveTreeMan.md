# Save a TreeMan object in serialization format

`TreeMan` equivalent to [`save()`](https://rdrr.io/r/base/save.html) but
able to handle node matrices.

## Usage

``` r
saveTreeMan(tree, file)
```

## Arguments

- tree:

  `TreeMan` object

- file:

  file path

## Details

It is not possible to use [`save()`](https://rdrr.io/r/base/save.html)
on `TreeMan` objects with node matrices. Node matrices are bigmemory
matrices and are therefore outside the R environment, see bigmemory
documentation for more information. Saving and loading a bigmemory
matrix may cause memory issues in R and cause R to crash.

This function can safely store a `TreeMan` object with and without a
node matrix. This function stores the tree using the serialization
format and the node matrix as a hidden .csv. Both parts of the tree can
be reloaded to an R environment with
[`loadTreeMan()`](https://docs.ropensci.org/phylotaR/reference/loadTreeMan.md).
The hidden node matrix filename is based on the file argument:
`file + _ndmtrx`

Reading and writing trees with `saveTreeMan()` and `loadTreeMan` is
faster than any of the other read and write functions.

## See also

[`loadTreeMan`](https://docs.ropensci.org/phylotaR/reference/loadTreeMan.md),
[`readTree`](https://docs.ropensci.org/phylotaR/reference/readTree.md),[`writeTree`](https://docs.ropensci.org/phylotaR/reference/writeTree.md),
[`readTrmn`](https://docs.ropensci.org/phylotaR/reference/readTrmn.md),
[`writeTrmn`](https://docs.ropensci.org/phylotaR/reference/writeTrmn.md)

## Examples

``` r

tree <- randTree(100, wndmtrx = TRUE)
#> Note, trees with `ndmtrx` cannot be saved and loaded using `save()` or `savehistory()`. Loading from these files may cause unusual behaviour.
saveTreeMan(tree, file = "test.RData")
rm(tree)
tree <- loadTreeMan(file = "test.RData")
file.remove("test.RData", "testRData_ndmtrx")
#> [1] TRUE TRUE
```
