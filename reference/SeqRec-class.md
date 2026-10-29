# Sequence record

Sequence record contains sequence data.

## Usage

``` r
# S4 method for class 'SeqRec'
as.character(x)

# S4 method for class 'SeqRec'
show(object)

# S4 method for class 'SeqRec'
print(x)

# S4 method for class 'SeqRec'
str(object, max.level = 2L, ...)

# S4 method for class 'SeqRec'
summary(object)
```

## Arguments

- x:

  `SeqRec` object

- object:

  `SeqRec` object

- max.level:

  Maximum level of nesting for str()

- ...:

  Further arguments for str()

## Details

Sequence is stored as raw. Use rawToChar().

## Slots

- `id`:

  Unique ID

- `nm`:

  Best-guess sequence name

- `accssn`:

  Accession

- `vrsn`:

  Accession version

- `url`:

  URL

- `txid`:

  Taxonomic ID of source taxon

- `orgnsm`:

  Scientific name of source taxon

- `sq`:

  Sequence

- `dfln`:

  Definition line

- `ml_typ`:

  Molecule type, e.g. DNA

- `rec_typ`:

  Record type: Whole or feature

- `nncltds`:

  Number of nucleotides

- `nambgs`:

  Number of ambiguous nucleotides

- `pambgs`:

  Proportion of ambiguous nucleotides

- `gcr`:

  GC ratio

- `age`:

  Number of days between sequence upload and running pipeline

## See also

Other run-public:
[`ClstrArc-class`](https://docs.ropensci.org/phylotaR/reference/ClstrArc-class.md),
[`ClstrRec-class`](https://docs.ropensci.org/phylotaR/reference/ClstrRec-class.md),
[`Phylota-class`](https://docs.ropensci.org/phylotaR/reference/Phylota-class.md),
[`SeqArc-class`](https://docs.ropensci.org/phylotaR/reference/SeqArc-class.md),
[`TaxDict-class`](https://docs.ropensci.org/phylotaR/reference/TaxDict-class.md),
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
seqrec <- aotus@sqs@sqs[[1]]
# this is a SeqRec object
# it contains sequence records
show(seqrec)
#> SeqRec [ID: KR528418.1]
# you can access its different data slots with @
seqrec@id       # sequence ID, accession + feature location
#> [1] "KR528418.1"
seqrec@nm       # feature name, '' if none
#> [1] ""
seqrec@accssn   # accession
#> [1] "KR528418"
seqrec@vrsn     # accession version
#> [1] "KR528418.1"
seqrec@url      # NCBI GenBank URL
#> [1] "https://www.ncbi.nlm.nih.gov/nuccore/KR528418.1"
seqrec@txid     # Taxonomic ID
#> [1] "231953"
seqrec@orgnsm   # free-text organism name
#> [1] "Aotus sp. (in: primates)"
seqrec@sq       # sequence, in raw format
#>    [1] 41 54 47 41 43 54 54 43 43 43 43 43 43 47 43 41 41 41 41 43 41 43 41 43
#>   [25] 43 43 41 43 54 41 47 43 41 41 41 41 41 54 43 41 54 54 41 41 54 47 41 47
#>   [49] 54 43 41 54 54 54 41 54 54 47 41 54 43 54 43 43 43 43 41 43 41 43 43 41
#>   [73] 54 43 43 41 41 43 41 54 54 54 43 43 54 43 54 54 47 41 54 47 41 41 41 54
#>   [97] 54 54 54 47 47 43 54 43 41 43 54 43 54 54 41 47 47 43 41 54 54 54 47 43
#>  [121] 43 54 41 41 54 43 41 54 54 43 41 41 41 54 54 41 43 43 41 43 43 47 47 43
#>  [145] 43 54 41 54 54 43 54 54 41 47 43 54 41 54 41 43 41 54 54 41 43 41 43 41
#>  [169] 43 43 41 47 41 54 41 43 43 54 43 41 41 43 54 47 43 43 54 54 43 54 43 43
#>  [193] 54 43 54 47 54 43 47 43 43 43 41 54 41 54 43 41 43 43 43 47 41 47 41 43
#>  [217] 47 54 54 41 41 43 54 41 54 47 47 43 54 47 41 47 54 41 41 54 54 43 47 43
#>  [241] 54 41 54 41 54 41 43 41 54 47 43 43 41 41 43 47 47 43 47 43 54 54 43 43
#>  [265] 41 54 41 54 54 43 54 54 43 47 54 41 54 47 54 43 54 54 54 54 54 43 54 43
#>  [289] 43 41 54 41 54 54 47 47 54 43 47 47 47 47 41 43 54 54 54 41 43 54 41 43
#>  [313] 47 47 41 54 43 54 54 54 43 43 54 54 54 54 54 43 54 47 41 41 47 41 43 54
#>  [337] 54 47 41 41 41 54 41 54 43 47 47 54 41 54 54 41 54 43 43 54 41 43 54 41
#>  [361] 54 54 54 41 43 41 41 43 43 41 54 41 47 43 43 41 43 41 47 43 41 54 54 54
#>  [385] 41 54 41 47 47 43 54 41 54 47 54 54 43 54 54 43 43 41 54 47 41 47 47 43
#>  [409] 43 41 41 41 54 41 54 43 41 54 54 43 54 47 41 47 47 41 47 43 43 41 43 41
#>  [433] 47 54 41 41 54 54 41 43 41 41 41 43 43 54 54 43 54 41 54 43 41 47 43 54
#>  [457] 41 54 43 43 43 43 54 41 54 41 54 43 47 47 41 54 43 54 47 41 43 43 54 54
#>  [481] 47 54 41 43 41 41 54 47 41 41 54 54 54 47 41 47 47 54 47 47 43 54 54 43
#>  [505] 54 43 41 47 54 41 47 41 54 41 41 41 47 43 43 41 43 54 43 54 43 41 43 41
#>  [529] 43 47 41 54 54 43 54 54 54 41 43 54 54 54 54 43 41 43 54 54 54 41 54 43
#>  [553] 54 54 41 43 43 43 54 54 54 41 54 54 41 54 43 47 43 41 47 43 43 43 54 41
#>  [577] 47 43 41 47 43 43 41 54 54 43 41 43 43 54 43 54 54 41 54 54 54 54 54 41
#>  [601] 43 41 54 47 41 41 41 43 41 47 47 41 54 43 41 41 41 43 41 41 54 43 43 41
#>  [625] 54 43 41 47 47 41 41 54 41 47 54 41 54 43 54 47 41 43 43 43 43 47 41 43
#>  [649] 41 41 41 41 54 43 41 43 47 54 54 43 43 41 43 43 43 43 54 41 54 54 41 43
#>  [673] 41 43 41 47 43 54 41 41 41 47 41 54 41 54 54 43 54 41 47 47 41 54 54 47
#>  [697] 41 54 43 54 54 54 43 54 54 43 54 43 54 54 41 54 43 43 43 54 41 41 54 41
#>  [721] 41 47 43 43 54 41 41 43 43 43 54 41 54 54 54 41 54 41 43 43 43 47 41 43
#>  [745] 43 54 54 43 54 41 41 43 47 47 41 43 43 43 41 47 41 54 41 41 54 54 41 54
#>  [769] 41 43 41 43 54 41 47 43 43 41 41 43 43 43 54 43 54 43 41 41 43 41 43 43
#>  [793] 43 43 41 43 43 43 43 41 43 41 54 54 41 41 47 43 43 41 47 41 41 54 47 41
#>  [817] 54 41 54 54 54 54 43 54 41 54 54 54 47 43 41 54 41 54 47 43 41 41 54 54
#>  [841] 43 54 41 43 47 47 54 43 54 41 54 54 43 43 54 41 41 54 41 41 41 43 54 54
#>  [865] 47 47 41 47 47 47 47 54 41 43 54 41 47 43 54 43 54 41 47 54 41 43 54 54
#>  [889] 54 43 54 41 54 43 43 54 41 41 54 54 54 54 41 41 54 47 47 54 54 41 54 43
#>  [913] 43 43 43 41 54 41 43 54 41 43 41 54 54 54 43 54 43 43 41 41 41 43 41 47
#>  [937] 43 41 41 41 47 43 41 54 41 41 54 41 54 54 54 43 47 41 43 43 43 41 54 54
#>  [961] 41 43 54 43 41 41 41 54 54 43 54 41 54 54 43 54 47 41 41 43 54 43 54 41
#>  [985] 47 54 41 47 43 54 47 41 43 43 54 41 43 54 41 41 43 54 43 54 54 41 43 41
#> [1009] 54 47 41 41 54 54 47 47 41 47 47 54 43 41 41 43 43 41 47 54 54 47 41 47
#> [1033] 54 41 43 43 43 43 54 54 43 47 54 41 41 43 43 41 54 54 47 47 43 43 41 41
#> [1057] 41 43 43 47 43 41 54 43 43 41 54 54 41 54 41 54 41 43 54 54 43 54 54 43
#> [1081] 41 54 54 41 54 54 47 54 54 41 43 43 43 54 41 41 54 41 43 43 43 43 54 54
#> [1105] 54 54 43 47 43 43 54 54 41 41 54 54 47 41 41 41 41 54 41 41 41 54 54 41
#> [1129] 43 54 54 41 41 41 54 47 41 54 41 41 47 54 43 43 54 54 47 54 41 47 54 41
#> [1153] 54 41 41 43 54 54 41 41 54 41 43 43 43 54 47 47 54 43 54 54 47 54 41 41
#> [1177] 41 43 43 41 47 41 41 41 54 47 47 41 41 47 54 41 54 54 54 41 43 54 43 43
#> [1201] 43 54 41 47 47 41 43 41 43 54 43 41 47 47 47 41 41 41 47 41 41 54 54 43
#> [1225] 43 54 41 54 54 43 54 41 43
seqrec@dfln     # sequence definition
#> [1] "Aotus sp. (in: primates) isolate Z25 cytochrome b (cytb) gene, complete cds; mitochondrial"
seqrec@ml_typ   # molecule type
#> [1] "DNA-linear"
seqrec@rec_typ  # whole record or feature
#> [1] "whole"
seqrec@nncltds  # sequence length
#> [1] 1233
seqrec@nambgs   # number of non-ATCGs
#> [1] 0
seqrec@pambgs   # proportion of non-ATCGs
#> [1] 0
seqrec@gcr      # GC-ratio
#> [1] 0.6066504
seqrec@age      # days since being added to GenBank
#> [1] 2749
# get the sequence like so....
(rawToChar(seqrec@sq))
#> [1] "ATGACTTCCCCCCGCAAAACACACCCACTAGCAAAAATCATTAATGAGTCATTTATTGATCTCCCCACACCATCCAACATTTCCTCTTGATGAAATTTTGGCTCACTCTTAGGCATTTGCCTAATCATTCAAATTACCACCGGCCTATTCTTAGCTATACATTACACACCAGATACCTCAACTGCCTTCTCCTCTGTCGCCCATATCACCCGAGACGTTAACTATGGCTGAGTAATTCGCTATATACATGCCAACGGCGCTTCCATATTCTTCGTATGTCTTTTTCTCCATATTGGTCGGGGACTTTACTACGGATCTTTCCTTTTTCTGAAGACTTGAAATATCGGTATTATCCTACTATTTACAACCATAGCCACAGCATTTATAGGCTATGTTCTTCCATGAGGCCAAATATCATTCTGAGGAGCCACAGTAATTACAAACCTTCTATCAGCTATCCCCTATATCGGATCTGACCTTGTACAATGAATTTGAGGTGGCTTCTCAGTAGATAAAGCCACTCTCACACGATTCTTTACTTTTCACTTTATCTTACCCTTTATTATCGCAGCCCTAGCAGCCATTCACCTCTTATTTTTACATGAAACAGGATCAAACAATCCATCAGGAATAGTATCTGACCCCGACAAAATCACGTTCCACCCCTATTACACAGCTAAAGATATTCTAGGATTGATCTTTCTTCTCTTATCCCTAATAAGCCTAACCCTATTTATACCCGACCTTCTAACGGACCCAGATAATTATACACTAGCCAACCCTCTCAACACCCCACCCCACATTAAGCCAGAATGATATTTTCTATTTGCATATGCAATTCTACGGTCTATTCCTAATAAACTTGGAGGGGTACTAGCTCTAGTACTTTCTATCCTAATTTTAATGGTTATCCCCATACTACATTTCTCCAAACAGCAAAGCATAATATTTCGACCCATTACTCAAATTCTATTCTGAACTCTAGTAGCTGACCTACTAACTCTTACATGAATTGGAGGTCAACCAGTTGAGTACCCCTTCGTAACCATTGGCCAAACCGCATCCATTATATACTTCTTCATTATTGTTACCCTAATACCCCTTTTCGCCTTAATTGAAAATAAATTACTTAAATGATAAGTCCTTGTAGTATAACTTAATACCCTGGTCTTGTAAACCAGAAATGGAAGTATTTACTCCCTAGGACACTCAGGGAAAGAATTCCTATTCTAC"
```
