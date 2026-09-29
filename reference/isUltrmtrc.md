# Is tree ultrametric?

Return TRUE if all tips end at 0, else FALSE.

## Usage

``` r
isUltrmtrc(tree, tol = 1e-08)
```

## Arguments

- tree:

  `TreeMan` object

- tol:

  zero tolerance

## Details

Returns a boolean. This function works in the background for the
`['ultr']` slot in a `TreeMan` object.

## See also

[`getLvng`](https://docs.ropensci.org/phylotaR/reference/getLvng.md),
[`getDcsd`](https://docs.ropensci.org/phylotaR/reference/getDcsd.md)

## Examples

``` r

tree <- randTree(10)
(isUltrmtrc(tree))
#> [1] FALSE
```
