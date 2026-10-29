# Write a .trmn tree

Write to disk a `TreeMan` or `TreeMan` object using the .trmn treefile

## Usage

``` r
writeTrmn(tree, file)
```

## Arguments

- tree:

  TreeMan object or TreeMen object

- file:

  file path

## Details

Write a tree(s) to file using the .trmn format. It is faster to read and
write tree files using treeman with the .trmn file format. In addition
it is possible to encode more information than possible with the Newick,
e.g. any taxonomic information and additional slot names added to the
tree are recorded in the file.

## See also

[`readTrmn`](https://docs.ropensci.org/phylotaR/reference/readTrmn.md),
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
