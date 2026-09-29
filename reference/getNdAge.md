# Get age

Return the age for `id`. Requires the known age of the tree to be
provided.

## Usage

``` r
getNdAge(tree, id, tree_age)
```

## Arguments

- tree:

  `TreeMan` object

- id:

  node id

- tree_age:

  numeric value of known age of tree

## Details

Returns a numeric.

## See also

[`getNdsAge`](https://docs.ropensci.org/phylotaR/reference/getNdsAge.md),
[`getSpnAge`](https://docs.ropensci.org/phylotaR/reference/getSpnAge.md),
[`getSpnsAge`](https://docs.ropensci.org/phylotaR/reference/getSpnsAge.md),
[`getPrnt`](https://docs.ropensci.org/phylotaR/reference/getPrnt.md),
[`getAge`](https://docs.ropensci.org/phylotaR/reference/getAge.md)
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

data(mammals)
# when did apes emerge?
# get parent id for all apes
prnt_id <- getPrnt(mammals, ids = c("Homo_sapiens", "Hylobates_concolor"))
# mammal_age <- getAge(mammals)  # ~166.2, needs to be performed when tree is not up-to-date
getNdAge(mammals, id = prnt_id, tree_age = 166.2)
#> [1] 23.5
```
