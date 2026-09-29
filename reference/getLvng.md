# Get extant tips from a tree

Return all extant tip `ID`s.

## Usage

``` r
getLvng(tree, tol = 1e-08)
```

## Arguments

- tree:

  `TreeMan` object

- tol:

  zero tolerance

## Details

Returns a vector.

## See also

[`getDcsd`](https://docs.ropensci.org/phylotaR/reference/getDcsd.md),
[`isUltrmtrc`](https://docs.ropensci.org/phylotaR/reference/isUltrmtrc.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

tree <- randTree(10)
(getLvng(tree))
#> [1] "t8"
```
