# Taxonomic record dictionary

Taxonomic dictionary contains a taxonomic tree and NCBI taxonomy data
for all taxonomic IDs.

## Usage

``` r
# S4 method for class 'TaxDict'
as.character(x)

# S4 method for class 'TaxDict'
show(object)

# S4 method for class 'TaxDict'
print(x)

# S4 method for class 'TaxDict'
str(object, max.level = 2L, ...)

# S4 method for class 'TaxDict'
summary(object)
```

## Arguments

- x:

  `TaxDict` object

- object:

  `TaxDict` object

- max.level:

  Maximum level of nesting for str()

- ...:

  Further arguments for str()

## Slots

- `txids`:

  Taxonomic IDs of taxon records

- `recs`:

  Environment of records

- `prnt`:

  Parent taxonomic ID

- `txtr`:

  Taxonomic tree

## See also

Other run-public:
[`ClstrArc-class`](https://docs.ropensci.org/phylotaR/reference/ClstrArc-class.md),
[`ClstrRec-class`](https://docs.ropensci.org/phylotaR/reference/ClstrRec-class.md),
[`Phylota-class`](https://docs.ropensci.org/phylotaR/reference/Phylota-class.md),
[`SeqArc-class`](https://docs.ropensci.org/phylotaR/reference/SeqArc-class.md),
[`SeqRec-class`](https://docs.ropensci.org/phylotaR/reference/SeqRec-class.md),
[`TaxRec-class`](https://docs.ropensci.org/phylotaR/reference/TaxRec-class.md),
[`clusters2_run()`](https://docs.ropensci.org/phylotaR/reference/clusters2_run.md),
[`clusters_run()`](https://docs.ropensci.org/phylotaR/reference/clusters_run.md),
[`parameters_reset()`](https://docs.ropensci.org/phylotaR/reference/parameters_reset.md),
[`reset()`](https://docs.ropensci.org/phylotaR/reference/reset.md),
[`restart()`](https://docs.ropensci.org/phylotaR/reference/restart.md),
[`run()`](https://docs.ropensci.org/phylotaR/reference/run.md),
[`setup()`](https://docs.ropensci.org/phylotaR/reference/setup.md),
[`taxise_run()`](https://docs.ropensci.org/phylotaR/reference/taxise_run.md)

## Examples

``` r
data('aotus')
txdct <- aotus@txdct
# this is a TaxDict object
# it contains taxonomic information, including records and tree
show(txdct)
#> Taxonomic dictionary [22] recs, parent [id 9504]
# you can access its different data slots with @
txdct@txids  # taxonomic IDs
#>  [1] "2688256" "1263727" "1230482" "1090913" "1002694" "940829"  "867331" 
#>  [8] "413234"  "361674"  "292213"  "280755"  "261316"  "231953"  "222417" 
#> [15] "120088"  "57176"   "57175"   "43147"   "37293"   "30591"   "9505"   
#> [22] "9504"   
txdct@recs   # taxonomic records environment
#> <environment: 0x5641a40393d8>
txdct@txtr   # taxonomic tree
#> TreeMan Object of [19] tips
txdct@prnt   # MRCA
#> [1] "9504"
# access any record through the records environment
txdct@recs[[txdct@txids[[1]]]]
#> TaxRec [id 2688256 (unclassified Aotus (in: primates))]
# for interacting with the taxonomic tree, see the treeman package
summary(txdct@txtr)
#> Tree (TreeMan Object):
#>   + 19 tips
#>   + 3 internal nodes
#>   + Polytomous
#>   + PD 22
#>   + Root node is "9504"
```
