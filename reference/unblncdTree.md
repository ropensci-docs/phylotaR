# Generate an unbalanced tree

Returns an unbalanced `TreeMan` tree with `n` tips.

## Usage

``` r
unblncdTree(n, wndmtrx = FALSE, parallel = FALSE)
```

## Arguments

- n:

  number of tips, integer, must be 3 or greater

- wndmtrx:

  T/F add node matrix? Default FALSE.

- parallel:

  T/F run in parallel? Default FALSE.

## Details

Equivalent to `ape`'s `stree(type='left')` but returns a `TreeMan` tree.
Tree is always rooted and bifurcating.

## See also

[`TreeMan-class`](https://docs.ropensci.org/phylotaR/reference/TreeMan-class.md),
[`randTree`](https://docs.ropensci.org/phylotaR/reference/randTree.md),
[`blncdTree`](https://docs.ropensci.org/phylotaR/reference/blncdTree.md)

## Examples

``` r

tree <- unblncdTree(5)
```
