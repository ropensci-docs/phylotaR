# Get lineage for multiple nodes

Return unique taxonyms for connecting `ids` to root.

## Usage

``` r
getNdsLng(tree, ids, parallel = FALSE, progress = "none")
```

## Arguments

- tree:

  `TreeMan` object

- ids:

  vector of node ids

- parallel:

  logical, make parallel?

- progress:

  name of the progress bar to use, see
  [`create_progress_bar`](https://rdrr.io/pkg/plyr/man/create_progress_bar.html)

## Details

Returns a list, parallelizable.

## See also

[`getNdLng`](https://docs.ropensci.org/phylotaR/reference/getNdLng.md),
[`getNdsFrmTxnyms`](https://docs.ropensci.org/phylotaR/reference/getNdsFrmTxnyms.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

data(mammals)
# return human and gorilla lineages
getNdsLng(mammals, id = c("Homo_sapiens", "Gorilla_gorilla"))
#> $Homo_sapiens
#>  [1] "Mammalia"         "Theria"           "Eutheria"         "Boreoeutheria"   
#>  [5] "Euarchontoglires" "Primates"         "Haplorrhini"      "Simiiformes"     
#>  [9] "Catarrhini"       "Hominoidea"       "Hominidae"        "Homininae"       
#> 
#> $Gorilla_gorilla
#>  [1] "Mammalia"         "Theria"           "Eutheria"         "Boreoeutheria"   
#>  [5] "Euarchontoglires" "Primates"         "Haplorrhini"      "Simiiformes"     
#>  [9] "Catarrhini"       "Hominoidea"       "Hominidae"        "Homininae"       
#> 
```
