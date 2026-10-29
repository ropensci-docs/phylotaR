# Get pre-distance

Return root to tip distance (prdst) for `id`

## Usage

``` r
getNdPrdst(tree, id)
```

## Arguments

- tree:

  `TreeMan` object

- id:

  node id

## Details

Sums the lengths of all branches from `id` to root.

## See also

[`getNdsPrdst`](https://docs.ropensci.org/phylotaR/reference/getNdsPrdst.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

tree <- randTree(10)
getNdPrdst(tree, id = "t1") # return the distance to root from t1
#> [1] 3.752139
```
