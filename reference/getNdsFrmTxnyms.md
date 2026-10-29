# Get IDs for nodes represented txnyms

Return a list of IDs for any node that contains the given txnyms.

## Usage

``` r
getNdsFrmTxnyms(tree, txnyms)
```

## Arguments

- tree:

  `TreeMan` object

- txnyms:

  vector of taxonomic group names

## Details

Returns a list. Txnyms must be spelt correctly.

## See also

[`taxaResolve`](https://docs.ropensci.org/phylotaR/reference/taxaResolve.md),
[`setTxnyms`](https://docs.ropensci.org/phylotaR/reference/setTxnyms.md),
[`searchTxnyms`](https://docs.ropensci.org/phylotaR/reference/searchTxnyms.md),
[`getNdsLng`](https://docs.ropensci.org/phylotaR/reference/getNdsLng.md),
[`getNdLng`](https://docs.ropensci.org/phylotaR/reference/getNdLng.md)

## Examples

``` r

data(mammals)
# what ID represents the apes?
getNdsFrmTxnyms(mammals, "Hominoidea")
#> $Hominoidea
#> [1] "n2960"
#> 
```
