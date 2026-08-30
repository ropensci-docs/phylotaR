# Taxonomic record

Taxonomic dictionary contains a taxonomic tree and NCBI taxonomy data
for all taxonomic IDs.

## Usage

``` r
# S4 method for class 'TaxRec'
as.character(x)

# S4 method for class 'TaxRec'
show(object)

# S4 method for class 'TaxRec'
print(x)

# S4 method for class 'TaxRec'
str(object, max.level = 2L, ...)

# S4 method for class 'TaxRec'
summary(object)
```

## Arguments

- x:

  `TaxRec` object

- object:

  `TaxRec` object

- max.level:

  Maximum level of nesting for str()

- ...:

  Further arguments for str()

## Slots

- `id`:

  Taxonomic ID

- `scnm`:

  Scientific name

- `cmnm`:

  Common name

- `rnk`:

  Rank

- `lng`:

  Lineage

- `prnt`:

  Parent

## See also

Other run-public:
[`ClstrArc-class`](https://docs.ropensci.org/phylotaR/reference/ClstrArc-class.md),
[`ClstrRec-class`](https://docs.ropensci.org/phylotaR/reference/ClstrRec-class.md),
[`Phylota-class`](https://docs.ropensci.org/phylotaR/reference/Phylota-class.md),
[`SeqArc-class`](https://docs.ropensci.org/phylotaR/reference/SeqArc-class.md),
[`SeqRec-class`](https://docs.ropensci.org/phylotaR/reference/SeqRec-class.md),
[`TaxDict-class`](https://docs.ropensci.org/phylotaR/reference/TaxDict-class.md),
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
taxrec <- aotus@txdct@recs[[aotus@txdct@txids[[1]]]]
# this is a TaxRec object
# it contains NCBI's taxonomic information for a single node
show(taxrec)
#> TaxRec [id 2688256 (unclassified Aotus (in: primates))]
# you can access its different data slots with @
taxrec@id    # taxonomic ID
#> [1] "2688256"
taxrec@scnm  # scientific name
#> [1] "unclassified Aotus (in: primates)"
taxrec@cmnm  # common name, '' if none
#> [1] ""
taxrec@rnk   # rank
#> [1] "no rank"
taxrec@lng   # lineage information: list of IDs and ranks
#> $ids
#>  [1] "131567"  "2759"    "33154"   "33208"   "6072"    "33213"   "33511"  
#>  [8] "7711"    "89593"   "7742"    "7776"    "117570"  "117571"  "8287"   
#> [15] "1338369" "32523"   "32524"   "40674"   "32525"   "9347"    "1437010"
#> [22] "314146"  "9443"    "376913"  "314293"  "9479"    "376918"  "9504"   
#> [29] "2688256"
#> 
#> $rnks
#>  [1] "no rank"      "superkingdom" "clade"        "kingdom"      "clade"       
#>  [6] "clade"        "clade"        "phylum"       "subphylum"    "clade"       
#> [11] "clade"        "clade"        "clade"        "superclass"   "clade"       
#> [16] "clade"        "clade"        "class"        "clade"        "clade"       
#> [21] "clade"        "superorder"   "order"        "suborder"     "infraorder"  
#> [26] "parvorder"    "family"       "genus"        "no rank"     
#> 
taxrec@prnt  # parent ID
#> [1] "9504"
```
