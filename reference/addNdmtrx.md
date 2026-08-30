# Add node matrix to a tree

Return tree with node matrix added.

## Usage

``` r
addNdmtrx(tree, shared = FALSE, ...)
```

## Arguments

- tree:

  `TreeMan` object

- shared:

  T/F, should the bigmatrix be shared? See bigmemory documentation.

- ...:

  `as.big.matrix()` additional arguments

## Details

The node matrix makes 'enquiry'-type computations faster: determining
node ages, number of descendants etc. But it takes up large amounts of
memory and has no impact on adding or removing tips. Note, trees with
the node matrix can not be written to disk using the 'serialization
format' i.e. with `save` or `saveRDS`. The matrix is generated with
bigmemory's \`as.big.matrix()\`.

## See also

[`updateSlts`](https://docs.ropensci.org/phylotaR/reference/updateSlts.md),
[`rmNdmtrx`](https://docs.ropensci.org/phylotaR/reference/rmNdmtrx.md),
<https://cran.r-project.org/package=bigmemory>

## Examples

``` r
#
tree <- randTree(10, wndmtrx = FALSE)
summary(tree)
#> Tree (TreeMan Object):
#>   + 10 tips
#>   + 9 internal nodes
#>   + Binary
#>   + PD 10.2
#>   + Root node is "n1"
tree <- addNdmtrx(tree)
#> Note, trees with `ndmtrx` cannot be saved and loaded using `save()` or `savehistory()`. Loading from these files may cause unusual behaviour.
summary(tree)
#> Tree (TreeMan Object):
#>   + 10 tips
#>   + 9 internal nodes
#>   + With node matrix
#>   + Binary
#>   + PD 10.2
#>   + Root node is "n1"
```
