# Get age of tree

Returns age, numeric, of tree

## Usage

``` r
getAge(tree, parallel = FALSE)
```

## Arguments

- tree:

  `TreeMan` object

- parallel:

  logical, make parallel?

## Details

Calculates the age of a tree, determined as the maximum tip to root
distance.

## See also

[`updateSlts`](https://docs.ropensci.org/phylotaR/reference/updateSlts.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

tree <- randTree(10)
(getAge(tree))
#> [1] 3.207328
```
