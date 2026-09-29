# Get lineage

Return unique taxonomic names for connecting `id` to root.

## Usage

``` r
getNdLng(tree, id)
```

## Arguments

- tree:

  `TreeMan` object

- id:

  node id

## Details

Returns a vector.

## See also

[`getNdsLng`](https://docs.ropensci.org/phylotaR/reference/getNdsLng.md),
[`getNdsFrmTxnyms`](https://docs.ropensci.org/phylotaR/reference/getNdsFrmTxnyms.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

data(mammals)
# return human lineage
getNdLng(mammals, id = "Homo_sapiens")
#>  [1] "Mammalia"         "Theria"           "Eutheria"         "Boreoeutheria"   
#>  [5] "Euarchontoglires" "Primates"         "Haplorrhini"      "Simiiformes"     
#>  [9] "Catarrhini"       "Hominoidea"       "Hominidae"        "Homininae"       
```
