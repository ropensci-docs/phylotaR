# Cluster record

Cluster record contains all information on a cluster.

## Usage

``` r
# S4 method for class 'ClstrRec'
as.character(x)

# S4 method for class 'ClstrRec'
show(object)

# S4 method for class 'ClstrRec'
print(x)

# S4 method for class 'ClstrRec'
str(object, max.level = 2L, ...)

# S4 method for class 'ClstrRec'
summary(object)
```

## Arguments

- x:

  `ClstrRec` object

- object:

  `ClstrRec` object

- max.level:

  Maximum level of nesting for str()

- ...:

  Further arguments for str()

## Slots

- `id`:

  Cluster ID, integer

- `sids`:

  Sequence IDs

- `nsqs`:

  Number of sequences

- `txids`:

  Source txids for sequences

- `ntx`:

  Number of taxa

- `typ`:

  Cluster type: direct, subtree or merged

- `seed`:

  Seed sequence ID

- `prnt`:

  Parent taxonomic ID

## See also

Other run-public:
[`ClstrArc-class`](https://docs.ropensci.org/phylotaR/reference/ClstrArc-class.md),
[`Phylota-class`](https://docs.ropensci.org/phylotaR/reference/Phylota-class.md),
[`SeqArc-class`](https://docs.ropensci.org/phylotaR/reference/SeqArc-class.md),
[`SeqRec-class`](https://docs.ropensci.org/phylotaR/reference/SeqRec-class.md),
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
clstrrec <- aotus@clstrs@clstrs[[1]]
# this is a ClstrRec object
# it contains cluster information
show(clstrrec)
#> Cluster Record [id 0]
#>  - [subtree] type
#>  - [AF129795.1] seed sequence
#>  - [173] sequences
#>  - [5] taxa
# you can access its different data slots with @
clstrrec@id     # cluster id
#> [1] 0
clstrrec@sids   # sequence IDs
#>   [1] "AF129792.1" "AF129793.1" "AF129794.1" "AF129795.1" "AF129796.1"
#>   [6] "AF129797.1" "AF129798.1" "AF129799.1" "AF129800.1" "AF129801.1"
#>  [11] "AF129802.1" "AF129803.1" "AF129804.1" "AF129805.1" "AF129806.1"
#>  [16] "AF129807.1" "AF129808.1" "AF132755.1" "AF132756.1" "AF132757.1"
#>  [21] "AF132758.1" "AF132759.1" "AF132760.1" "AF132761.1" "AF132762.1"
#>  [26] "AF132763.1" "AF132764.1" "AF132765.1" "AF132766.1" "AF132767.1"
#>  [31] "AF132768.1" "AF132769.1" "AF132770.1" "AF169485.1" "AF169486.1"
#>  [36] "AF169487.1" "AY227055.1" "AY227056.1" "AY227057.1" "AY227058.1"
#>  [41] "AY227059.1" "AY227060.1" "AY227061.1" "AY227062.1" "AY227063.1"
#>  [46] "AY227064.1" "AY227065.1" "AY227066.1" "AY227067.1" "AY227068.1"
#>  [51] "AY227069.1" "AY227070.1" "AY227071.1" "AY227072.1" "AY227073.1"
#>  [56] "AY227074.1" "AY429142.1" "AY429143.1" "AY493661.1" "AY563180.2"
#>  [61] "AY563181.2" "AY563182.2" "AY563183.2" "AY563184.2" "AY563185.2"
#>  [66] "AY563186.2" "AY563188.2" "AY563189.2" "AY563190.2" "AY563191.2"
#>  [71] "AY563192.2" "AY563193.2" "AY563194.2" "AY563195.2" "AY563196.2"
#>  [76] "AY563197.2" "AY563198.2" "AY563199.2" "AY563200.2" "AY563201.2"
#>  [81] "AY563202.2" "AY563203.2" "AY563204.2" "AY563206.2" "AY563207.2"
#>  [86] "AY563208.2" "AY563209.2" "AY563210.2" "AY563211.2" "AY563212.2"
#>  [91] "AY563213.2" "AY563214.2" "AY563215.2" "AY563216.2" "AY563217.2"
#>  [96] "AY563218.2" "AY563219.2" "AY563220.2" "AY563221.2" "AY563222.2"
#> [101] "AY563223.2" "AY563224.2" "AY563225.2" "AY563226.2" "AY563227.2"
#> [106] "AY563228.2" "AY563229.2" "AY563230.2" "AY563231.2" "AY563232.2"
#> [111] "AY563233.2" "AY563234.2" "AY563236.2" "AY563237.2" "AY563239.2"
#> [116] "AY563241.2" "AY563242.2" "AY563243.2" "AY563244.2" "AY563245.2"
#> [121] "AY563246.2" "AY563247.2" "AY563248.2" "AY563249.2" "AY563250.2"
#> [126] "AY563251.2" "AY563252.2" "AY563253.2" "AY563254.2" "AY563255.2"
#> [131] "AY563256.2" "AY563257.2" "AY563258.2" "AY563259.2" "AY563260.2"
#> [136] "AY563261.2" "AY563262.2" "AY563263.2" "DQ162624.1" "DQ162626.1"
#> [141] "DQ162627.1" "DQ162628.1" "DQ162629.1" "DQ162630.1" "DQ162633.1"
#> [146] "DQ162634.1" "DQ162635.1" "DQ162645.1" "DQ162646.1" "DQ162647.1"
#> [151] "DQ162648.1" "DQ162660.1" "DQ162661.1" "DQ162668.1" "DQ162676.1"
#> [156] "DQ162679.1" "DQ162682.1" "DQ162683.1" "DQ162688.1" "DQ162699.1"
#> [161] "DQ162704.1" "DQ162705.1" "DQ162710.1" "DQ162711.1" "DQ162718.1"
#> [166] "DQ162719.1" "DQ162727.1" "DQ162729.1" "DQ162732.1" "DQ162736.1"
#> [171] "MF615382.1" "MF615383.1" "MF615384.1"
clstrrec@nsqs   # number of sequences
#> [1] 173
clstrrec@txids  # taxonomic IDs of sequences
#>   [1] "231953" "231953" "231953" "231953" "231953" "231953" "231953" "231953"
#>   [9] "231953" "231953" "231953" "231953" "231953" "231953" "231953" "231953"
#>  [17] "231953" "231953" "231953" "231953" "57176"  "57176"  "57176"  "57176" 
#>  [25] "57176"  "57176"  "57176"  "57176"  "57176"  "57176"  "57176"  "57176" 
#>  [33] "57176"  "57175"  "57175"  "57175"  "57175"  "57175"  "57175"  "57175" 
#>  [41] "57175"  "57175"  "57175"  "57175"  "57175"  "57175"  "57175"  "57175" 
#>  [49] "57175"  "57175"  "57175"  "57175"  "57175"  "57175"  "57175"  "57175" 
#>  [57] "57175"  "57175"  "57175"  "57175"  "57175"  "57175"  "57175"  "57175" 
#>  [65] "57175"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293" 
#>  [73] "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293" 
#>  [81] "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293" 
#>  [89] "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293" 
#>  [97] "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293" 
#> [105] "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293" 
#> [113] "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293" 
#> [121] "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293" 
#> [129] "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293" 
#> [137] "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293" 
#> [145] "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293" 
#> [153] "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293" 
#> [161] "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293"  "37293" 
#> [169] "37293"  "37293"  "37293"  "30591"  "30591" 
clstrrec@ntx    # number unique taxonomic IDs
#> [1] 5
clstrrec@typ    # cluster type: merged, subtree, direct or paraphyly
#> [1] "subtree"
clstrrec@prnt   # MRCA of all taxa
#> [1] "9504"
clstrrec@seed   # most inter-connected sequence
#> [1] "AF129795.1"
```
