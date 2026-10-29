# cTrees

Return `TreeMen` of concatenated trees.

## Usage

``` r
cTrees(x, ...)
```

## Arguments

- x:

  `TreeMan` or `TreeMen` objects

- ...:

  more `TreeMan` or `TreeMen` objects

## Details

Concatenate trees into single `TreeMen` object.

## See also

[`TreeMen-class`](https://docs.ropensci.org/phylotaR/reference/TreeMen-class.md),
[`TreeMan-class`](https://docs.ropensci.org/phylotaR/reference/TreeMan-class.md),
[`list-to-TreeMen`](https://docs.ropensci.org/phylotaR/reference/list-to-TreeMen.md)

## Examples

``` r

trees <- cTrees(randTree(10), randTree(10))
```
