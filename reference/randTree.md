# Generate a random tree

Returns a random `TreeMan` tree with `n` tips.

## Usage

``` r
randTree(n, wndmtrx = FALSE, parallel = FALSE)
```

## Arguments

- n:

  number of tips, integer, must be 3 or greater

- wndmtrx:

  T/F add node matrix? Default FALSE.

- parallel:

  T/F run in parallel? Default FALSE.

## Details

Equivalent to `ape`'s
[`rtree()`](https://rdrr.io/pkg/ape/man/rtree.html) but returns a
`TreeMan` tree. Tree is always rooted and bifurcating.

## See also

[`TreeMan-class`](https://docs.ropensci.org/phylotaR/reference/TreeMan-class.md),
[`blncdTree`](https://docs.ropensci.org/phylotaR/reference/blncdTree.md),
[`unblncdTree`](https://docs.ropensci.org/phylotaR/reference/unblncdTree.md)

## Examples

``` r

tree <- randTree(5)
```
