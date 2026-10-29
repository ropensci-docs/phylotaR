# Get age range

Return start and end ages for `id` from when it first appears to when it
splits

## Usage

``` r
getSpnAge(tree, id, tree_age)
```

## Arguments

- tree:

  `TreeMan` object

- id:

  node id

- tree_age:

  numeric value of known age of tree

## Details

Returns a dataframe.

## See also

[`getNdAge`](https://docs.ropensci.org/phylotaR/reference/getNdAge.md),
[`getNdsAge`](https://docs.ropensci.org/phylotaR/reference/getNdsAge.md),
[`getSpnsAge`](https://docs.ropensci.org/phylotaR/reference/getSpnsAge.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

data(mammals)
# mammal_age <- getAge(mammals)  # ~166.2, needs to be performed when tree is not up-to-date
getSpnAge(mammals, id = "Homo_sapiens", tree_age = 166.2)
#>            spn start end
#> 1 Homo_sapiens   9.7   0
```
