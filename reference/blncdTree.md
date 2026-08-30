# Generate a balanced tree

Returns a balanced `TreeMan` tree with `n` tips.

## Usage

``` r
blncdTree(n, wndmtrx = FALSE, parallel = FALSE)
```

## Arguments

- n:

  number of tips, integer, must be 3 or greater

- wndmtrx:

  T/F add node matrix? Default FALSE.

- parallel:

  T/F run in parallel? Default FALSE.

## Details

Equivalent to `ape`'s `stree(type='balanced')` but returns a `TreeMan`
tree. Tree is always rooted and bifurcating.

## See also

[`TreeMan-class`](https://docs.ropensci.org/phylotaR/reference/TreeMan-class.md),
[`randTree`](https://docs.ropensci.org/phylotaR/reference/randTree.md),
[`unblncdTree`](https://docs.ropensci.org/phylotaR/reference/unblncdTree.md)

## Examples

``` r

tree <- blncdTree(5)
```
