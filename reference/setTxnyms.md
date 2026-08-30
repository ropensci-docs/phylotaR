# Set the txnym slots in a tree

Return a tree with txnyms added to specified nodes

## Usage

``` r
setTxnyms(tree, txnyms)
```

## Arguments

- tree:

  `TreeMan` object

- txnyms:

  named vector or list

## Details

Returns a tree. Specify the taxonomic groups for nodes in a tree by
providing a vector or list named by node IDs. Takes output from
`searchTxnyms`. Only letters, numbers and underscores allowed. To remove
special characters use regular expressions, e.g.
`gsub(['a-zA-Z0-9_'], '', txnym)`

## See also

[`taxaResolve`](https://docs.ropensci.org/phylotaR/reference/taxaResolve.md),
[`searchTxnyms`](https://docs.ropensci.org/phylotaR/reference/searchTxnyms.md),
[`getNdsLng`](https://docs.ropensci.org/phylotaR/reference/getNdsLng.md),
[`getNdLng`](https://docs.ropensci.org/phylotaR/reference/getNdLng.md),
<https://github.com/DomBennett/treeman/wiki/set-methods>

## Examples

``` r

data(mammals)
# let's change the txnym for humans
# what's its summary before we change anything?
summary(mammals[["Homo_sapiens"]])
#> Node (tip node):
#>   + ID: "Homo_sapiens"
#>   + txnym: "Homo"
#>   + prid: "n2938"
#>   + spn: 9.7
#>   + predist: 170
#>   + pd: 0
# now let's add Hominini
new_txnym <- list("Homo_sapiens" = c("Hominini", "Homo"))
mammals <- setTxnyms(mammals, new_txnym)
summary(mammals[["Homo_sapiens"]])
#> Node (tip node):
#>   + ID: "Homo_sapiens"
#>   + txnym: "Hominini", "Homo"
#>   + prid: "n2938"
#>   + spn: 9.7
#>   + predist: 170
#>   + pd: 0
```
