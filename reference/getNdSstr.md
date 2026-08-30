# Get sister id

Returns the id of the sister(s) of node id given.

## Usage

``` r
getNdSstr(tree, id)
```

## Arguments

- tree:

  `TreeMan` object

- id:

  node id

## Details

An error is raised if there is no sister (e.g. for the root). There can
be more than one sister if tree is polytomous.

## See also

[`getNdsSstr`](https://docs.ropensci.org/phylotaR/reference/getNdsSstr.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

tree <- randTree(10)
getNdSstr(tree, id = "t1")
#> [1] "n4"
```
