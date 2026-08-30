# Get extinct tips from a tree

Return all extinct tip `ID`s.

## Usage

``` r
getDcsd(tree, tol = 1e-08)
```

## Arguments

- tree:

  `TreeMan` object

- tol:

  zero tolerance

## Details

Returns a vector.

## See also

[`getLvng`](https://docs.ropensci.org/phylotaR/reference/getLvng.md),
[`isUltrmtrc`](https://docs.ropensci.org/phylotaR/reference/isUltrmtrc.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

tree <- randTree(10)
(getDcsd(tree))
#> [1] "t1"  "t10" "t2"  "t4"  "t5"  "t6"  "t7"  "t8"  "t9" 
```
