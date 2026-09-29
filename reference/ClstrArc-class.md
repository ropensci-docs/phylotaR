# Cluster record archive

Multiple cluster records.

## Usage

``` r
# S4 method for class 'ClstrArc'
as.character(x)

# S4 method for class 'ClstrArc'
show(object)

# S4 method for class 'ClstrArc'
print(x)

# S4 method for class 'ClstrArc'
str(object, max.level = 2L, ...)

# S4 method for class 'ClstrArc'
summary(object)

# S4 method for class 'ClstrArc,character'
x[[i]]

# S4 method for class 'ClstrArc,character,missing,missing'
x[i, j, ..., drop = TRUE]
```

## Arguments

- x:

  `ClstrArc` object

- object:

  `ClstrArc` object

- max.level:

  Maximum level of nesting for str()

- ...:

  Further arguments for str()

- i:

  cid(s)

- j:

  Unused

- drop:

  Unused

## Slots

- `ids`:

  Vector of cluster record IDs

- `clstrs`:

  List of ClstrArc named by ID

## See also

Other run-public:
[`ClstrRec-class`](https://docs.ropensci.org/phylotaR/reference/ClstrRec-class.md),
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
clstrarc <- aotus@clstrs
# this is a ClstrArc object
# it contains cluster records
show(clstrarc)
#> Archive of cluster record(s)
#>  - [184] clusters
# you can access its different data slots with @
clstrarc@ids     # unique cluster ID
#>   [1] "0"   "1"   "2"   "3"   "4"   "5"   "6"   "7"   "8"   "9"   "10"  "11" 
#>  [13] "12"  "13"  "14"  "15"  "16"  "17"  "18"  "19"  "20"  "21"  "22"  "23" 
#>  [25] "24"  "25"  "26"  "27"  "28"  "29"  "30"  "31"  "32"  "33"  "34"  "35" 
#>  [37] "36"  "37"  "38"  "39"  "40"  "41"  "42"  "43"  "44"  "45"  "46"  "47" 
#>  [49] "48"  "49"  "50"  "51"  "52"  "53"  "54"  "55"  "56"  "57"  "58"  "59" 
#>  [61] "60"  "61"  "62"  "63"  "64"  "65"  "66"  "67"  "68"  "69"  "70"  "71" 
#>  [73] "72"  "73"  "74"  "75"  "76"  "77"  "78"  "79"  "80"  "81"  "82"  "83" 
#>  [85] "84"  "85"  "86"  "87"  "88"  "89"  "90"  "91"  "92"  "93"  "94"  "95" 
#>  [97] "96"  "97"  "98"  "99"  "100" "101" "102" "103" "104" "105" "106" "107"
#> [109] "108" "109" "110" "111" "112" "113" "114" "115" "116" "117" "118" "119"
#> [121] "120" "121" "122" "123" "124" "125" "126" "127" "128" "129" "130" "131"
#> [133] "132" "133" "134" "135" "136" "137" "138" "139" "140" "141" "142" "143"
#> [145] "144" "145" "146" "147" "148" "149" "150" "151" "152" "153" "154" "155"
#> [157] "156" "157" "158" "159" "160" "161" "162" "163" "164" "165" "166" "167"
#> [169] "168" "169" "170" "171" "172" "173" "174" "175" "176" "177" "178" "179"
#> [181] "180" "181" "182" "183"
clstrarc@clstrs  # list of cluster records
#> $`0`
#> Cluster Record [id 0]
#>  - [subtree] type
#>  - [AF129795.1] seed sequence
#>  - [173] sequences
#>  - [5] taxa
#> 
#> $`1`
#> Cluster Record [id 1]
#>  - [subtree] type
#>  - [DQ098863.1] seed sequence
#>  - [66] sequences
#>  - [10] taxa
#> 
#> $`2`
#> Cluster Record [id 2]
#>  - [subtree] type
#>  - [AY659849.1] seed sequence
#>  - [55] sequences
#>  - [5] taxa
#> 
#> $`3`
#> Cluster Record [id 3]
#>  - [subtree] type
#>  - [DI178118.1] seed sequence
#>  - [52] sequences
#>  - [2] taxa
#> 
#> $`4`
#> Cluster Record [id 4]
#>  - [subtree] type
#>  - [LC075891.1] seed sequence
#>  - [50] sequences
#>  - [2] taxa
#> 
#> $`5`
#> Cluster Record [id 5]
#>  - [subtree] type
#>  - [HM761925.1] seed sequence
#>  - [49] sequences
#>  - [9] taxa
#> 
#> $`6`
#> Cluster Record [id 6]
#>  - [subtree] type
#>  - [HM763429.1] seed sequence
#>  - [49] sequences
#>  - [9] taxa
#> 
#> $`7`
#> Cluster Record [id 7]
#>  - [subtree] type
#>  - [JQ933053.1] seed sequence
#>  - [48] sequences
#>  - [9] taxa
#> 
#> $`8`
#> Cluster Record [id 8]
#>  - [subtree] type
#>  - [HM759641.1] seed sequence
#>  - [48] sequences
#>  - [9] taxa
#> 
#> $`9`
#> Cluster Record [id 9]
#>  - [subtree] type
#>  - [KC761951.1] seed sequence
#>  - [47] sequences
#>  - [9] taxa
#> 
#> $`10`
#> Cluster Record [id 10]
#>  - [subtree] type
#>  - [MT489103.1] seed sequence
#>  - [45] sequences
#>  - [8] taxa
#> 
#> $`11`
#> Cluster Record [id 11]
#>  - [subtree] type
#>  - [KC762127.1] seed sequence
#>  - [45] sequences
#>  - [9] taxa
#> 
#> $`12`
#> Cluster Record [id 12]
#>  - [subtree] type
#>  - [KC761371.1] seed sequence
#>  - [45] sequences
#>  - [9] taxa
#> 
#> $`13`
#> Cluster Record [id 13]
#>  - [subtree] type
#>  - [KC760228.1] seed sequence
#>  - [43] sequences
#>  - [9] taxa
#> 
#> $`14`
#> Cluster Record [id 14]
#>  - [subtree] type
#>  - [JQ932794.1] seed sequence
#>  - [43] sequences
#>  - [4] taxa
#> 
#> $`15`
#> Cluster Record [id 15]
#>  - [direct] type
#>  - [LC075891.1] seed sequence
#>  - [43] sequences
#>  - [1] taxa
#> 
#> $`16`
#> Cluster Record [id 16]
#>  - [subtree] type
#>  - [EF658652.1] seed sequence
#>  - [41] sequences
#>  - [9] taxa
#> 
#> $`17`
#> Cluster Record [id 17]
#>  - [subtree] type
#>  - [HM760775.1] seed sequence
#>  - [41] sequences
#>  - [8] taxa
#> 
#> $`18`
#> Cluster Record [id 18]
#>  - [subtree] type
#>  - [MT488555.1] seed sequence
#>  - [41] sequences
#>  - [8] taxa
#> 
#> $`19`
#> Cluster Record [id 19]
#>  - [subtree] type
#>  - [U38998.1] seed sequence
#>  - [40] sequences
#>  - [8] taxa
#> 
#> $`20`
#> Cluster Record [id 20]
#>  - [subtree] type
#>  - [DQ321662.1] seed sequence
#>  - [35] sequences
#>  - [8] taxa
#> 
#> $`21`
#> Cluster Record [id 21]
#>  - [subtree] type
#>  - [JQ932751.1] seed sequence
#>  - [35] sequences
#>  - [2] taxa
#> 
#> $`22`
#> Cluster Record [id 22]
#>  - [subtree] type
#>  - [JN161069.1] seed sequence
#>  - [30] sequences
#>  - [1] taxa
#> 
#> $`23`
#> Cluster Record [id 23]
#>  - [direct] type
#>  - [LC456000.1] seed sequence
#>  - [30] sequences
#>  - [1] taxa
#> 
#> $`24`
#> Cluster Record [id 24]
#>  - [subtree] type
#>  - [JN161069.1] seed sequence
#>  - [30] sequences
#>  - [1] taxa
#> 
#> $`25`
#> Cluster Record [id 25]
#>  - [subtree] type
#>  - [AF333711.1] seed sequence
#>  - [28] sequences
#>  - [1] taxa
#> 
#> $`26`
#> Cluster Record [id 26]
#>  - [subtree] type
#>  - [JQ932884.1] seed sequence
#>  - [24] sequences
#>  - [4] taxa
#> 
#> $`27`
#> Cluster Record [id 27]
#>  - [subtree] type
#>  - [LC075890.1] seed sequence
#>  - [24] sequences
#>  - [2] taxa
#> 
#> $`28`
#> Cluster Record [id 28]
#>  - [subtree] type
#>  - [DQ098867.1] seed sequence
#>  - [24] sequences
#>  - [2] taxa
#> 
#> $`29`
#> Cluster Record [id 29]
#>  - [subtree] type
#>  - [AY900534.1] seed sequence
#>  - [21] sequences
#>  - [1] taxa
#> 
#> $`30`
#> Cluster Record [id 30]
#>  - [subtree] type
#>  - [AF378747.1] seed sequence
#>  - [20] sequences
#>  - [1] taxa
#> 
#> $`31`
#> Cluster Record [id 31]
#>  - [subtree] type
#>  - [AY227055.1] seed sequence
#>  - [20] sequences
#>  - [1] taxa
#> 
#> $`32`
#> Cluster Record [id 32]
#>  - [subtree] type
#>  - [HM763430.1] seed sequence
#>  - [20] sequences
#>  - [2] taxa
#> 
#> $`33`
#> Cluster Record [id 33]
#>  - [subtree] type
#>  - [HM759643.1] seed sequence
#>  - [20] sequences
#>  - [2] taxa
#> 
#> $`34`
#> Cluster Record [id 34]
#>  - [subtree] type
#>  - [HM761926.1] seed sequence
#>  - [20] sequences
#>  - [2] taxa
#> 
#> $`35`
#> Cluster Record [id 35]
#>  - [subtree] type
#>  - [JQ932877.1] seed sequence
#>  - [19] sequences
#>  - [4] taxa
#> 
#> $`36`
#> Cluster Record [id 36]
#>  - [subtree] type
#>  - [JQ933028.1] seed sequence
#>  - [19] sequences
#>  - [2] taxa
#> 
#> $`37`
#> Cluster Record [id 37]
#>  - [subtree] type
#>  - [JQ932999.1] seed sequence
#>  - [18] sequences
#>  - [1] taxa
#> 
#> $`38`
#> Cluster Record [id 38]
#>  - [subtree] type
#>  - [AF027542.1] seed sequence
#>  - [18] sequences
#>  - [1] taxa
#> 
#> $`39`
#> Cluster Record [id 39]
#>  - [subtree] type
#>  - [AF333712.1] seed sequence
#>  - [18] sequences
#>  - [1] taxa
#> 
#> $`40`
#> Cluster Record [id 40]
#>  - [direct] type
#>  - [LC075890.1] seed sequence
#>  - [18] sequences
#>  - [1] taxa
#> 
#> $`41`
#> Cluster Record [id 41]
#>  - [subtree] type
#>  - [MT483703.1] seed sequence
#>  - [18] sequences
#>  - [2] taxa
#> 
#> $`42`
#> Cluster Record [id 42]
#>  - [subtree] type
#>  - [MT488555.1] seed sequence
#>  - [18] sequences
#>  - [2] taxa
#> 
#> $`43`
#> Cluster Record [id 43]
#>  - [subtree] type
#>  - [MT492158.1] seed sequence
#>  - [18] sequences
#>  - [2] taxa
#> 
#> $`44`
#> Cluster Record [id 44]
#>  - [subtree] type
#>  - [MT483753.1] seed sequence
#>  - [18] sequences
#>  - [2] taxa
#> 
#> $`45`
#> Cluster Record [id 45]
#>  - [subtree] type
#>  - [MT488933.1] seed sequence
#>  - [18] sequences
#>  - [2] taxa
#> 
#> $`46`
#> Cluster Record [id 46]
#>  - [subtree] type
#>  - [MT488817.1] seed sequence
#>  - [18] sequences
#>  - [2] taxa
#> 
#> $`47`
#> Cluster Record [id 47]
#>  - [subtree] type
#>  - [MT489103.1] seed sequence
#>  - [18] sequences
#>  - [2] taxa
#> 
#> $`48`
#> Cluster Record [id 48]
#>  - [subtree] type
#>  - [MT489061.1] seed sequence
#>  - [18] sequences
#>  - [2] taxa
#> 
#> $`49`
#> Cluster Record [id 49]
#>  - [subtree] type
#>  - [MT489018.1] seed sequence
#>  - [18] sequences
#>  - [2] taxa
#> 
#> $`50`
#> Cluster Record [id 50]
#>  - [subtree] type
#>  - [MT488976.1] seed sequence
#>  - [18] sequences
#>  - [2] taxa
#> 
#> $`51`
#> Cluster Record [id 51]
#>  - [subtree] type
#>  - [JQ932845.1] seed sequence
#>  - [16] sequences
#>  - [3] taxa
#> 
#> $`52`
#> Cluster Record [id 52]
#>  - [subtree] type
#>  - [MT488890.1] seed sequence
#>  - [16] sequences
#>  - [2] taxa
#> 
#> $`53`
#> Cluster Record [id 53]
#>  - [subtree] type
#>  - [MF615377.1] seed sequence
#>  - [14] sequences
#>  - [3] taxa
#> 
#> $`54`
#> Cluster Record [id 54]
#>  - [direct] type
#>  - [LC456005.1] seed sequence
#>  - [14] sequences
#>  - [1] taxa
#> 
#> $`55`
#> Cluster Record [id 55]
#>  - [subtree] type
#>  - [DQ321662.1] seed sequence
#>  - [13] sequences
#>  - [2] taxa
#> 
#> $`56`
#> Cluster Record [id 56]
#>  - [subtree] type
#>  - [AF161946.1] seed sequence
#>  - [12] sequences
#>  - [4] taxa
#> 
#> $`57`
#> Cluster Record [id 57]
#>  - [subtree] type
#>  - [JQ932800.1] seed sequence
#>  - [12] sequences
#>  - [3] taxa
#> 
#> $`58`
#> Cluster Record [id 58]
#>  - [subtree] type
#>  - [JQ932874.1] seed sequence
#>  - [12] sequences
#>  - [1] taxa
#> 
#> $`59`
#> Cluster Record [id 59]
#>  - [subtree] type
#>  - [KY508404.1] seed sequence
#>  - [12] sequences
#>  - [1] taxa
#> 
#> $`60`
#> Cluster Record [id 60]
#>  - [subtree] type
#>  - [JQ932840.1] seed sequence
#>  - [11] sequences
#>  - [1] taxa
#> 
#> $`61`
#> Cluster Record [id 61]
#>  - [subtree] type
#>  - [AF107750.1] seed sequence
#>  - [11] sequences
#>  - [1] taxa
#> 
#> $`62`
#> Cluster Record [id 62]
#>  - [subtree] type
#>  - [AY900546.1] seed sequence
#>  - [11] sequences
#>  - [1] taxa
#> 
#> $`63`
#> Cluster Record [id 63]
#>  - [subtree] type
#>  - [AY646200.1] seed sequence
#>  - [10] sequences
#>  - [4] taxa
#> 
#> $`64`
#> Cluster Record [id 64]
#>  - [subtree] type
#>  - [JQ932868.1] seed sequence
#>  - [10] sequences
#>  - [2] taxa
#> 
#> $`65`
#> Cluster Record [id 65]
#>  - [subtree] type
#>  - [AY894647.1] seed sequence
#>  - [10] sequences
#>  - [1] taxa
#> 
#> $`66`
#> Cluster Record [id 66]
#>  - [subtree] type
#>  - [JQ932807.1] seed sequence
#>  - [9] sequences
#>  - [1] taxa
#> 
#> $`67`
#> Cluster Record [id 67]
#>  - [subtree] type
#>  - [AF338375.1] seed sequence
#>  - [8] sequences
#>  - [6] taxa
#> 
#> $`68`
#> Cluster Record [id 68]
#>  - [subtree] type
#>  - [JQ932913.1] seed sequence
#>  - [7] sequences
#>  - [2] taxa
#> 
#> $`69`
#> Cluster Record [id 69]
#>  - [subtree] type
#>  - [HM758650.1] seed sequence
#>  - [7] sequences
#>  - [5] taxa
#> 
#> $`70`
#> Cluster Record [id 70]
#>  - [subtree] type
#>  - [AY900559.1] seed sequence
#>  - [7] sequences
#>  - [1] taxa
#> 
#> $`71`
#> Cluster Record [id 71]
#>  - [direct] type
#>  - [EF658652.1] seed sequence
#>  - [7] sequences
#>  - [1] taxa
#> 
#> $`72`
#> Cluster Record [id 72]
#>  - [subtree] type
#>  - [JQ933020.1] seed sequence
#>  - [6] sequences
#>  - [4] taxa
#> 
#> $`73`
#> Cluster Record [id 73]
#>  - [subtree] type
#>  - [KC761051.1] seed sequence
#>  - [6] sequences
#>  - [4] taxa
#> 
#> $`74`
#> Cluster Record [id 74]
#>  - [subtree] type
#>  - [HM759273.1] seed sequence
#>  - [6] sequences
#>  - [5] taxa
#> 
#> $`75`
#> Cluster Record [id 75]
#>  - [subtree] type
#>  - [AY449069.1] seed sequence
#>  - [6] sequences
#>  - [1] taxa
#> 
#> $`76`
#> Cluster Record [id 76]
#>  - [subtree] type
#>  - [AY684991.1] seed sequence
#>  - [6] sequences
#>  - [1] taxa
#> 
#> $`77`
#> Cluster Record [id 77]
#>  - [direct] type
#>  - [AY449069.1] seed sequence
#>  - [6] sequences
#>  - [1] taxa
#> 
#> $`78`
#> Cluster Record [id 78]
#>  - [subtree] type
#>  - [DQ989366.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`79`
#> Cluster Record [id 79]
#>  - [subtree] type
#>  - [JQ933005.1] seed sequence
#>  - [5] sequences
#>  - [1] taxa
#> 
#> $`80`
#> Cluster Record [id 80]
#>  - [subtree] type
#>  - [JQ932259.1] seed sequence
#>  - [5] sequences
#>  - [1] taxa
#> 
#> $`81`
#> Cluster Record [id 81]
#>  - [subtree] type
#>  - [JQ932880.1] seed sequence
#>  - [5] sequences
#>  - [1] taxa
#> 
#> $`82`
#> Cluster Record [id 82]
#>  - [subtree] type
#>  - [JQ932869.1] seed sequence
#>  - [5] sequences
#>  - [3] taxa
#> 
#> $`83`
#> Cluster Record [id 83]
#>  - [subtree] type
#>  - [HM756838.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`84`
#> Cluster Record [id 84]
#>  - [subtree] type
#>  - [HM757379.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`85`
#> Cluster Record [id 85]
#>  - [subtree] type
#>  - [HM757554.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`86`
#> Cluster Record [id 86]
#>  - [subtree] type
#>  - [HM757720.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`87`
#> Cluster Record [id 87]
#>  - [subtree] type
#>  - [HM758212.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`88`
#> Cluster Record [id 88]
#>  - [subtree] type
#>  - [HM758297.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`89`
#> Cluster Record [id 89]
#>  - [subtree] type
#>  - [HM758463.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`90`
#> Cluster Record [id 90]
#>  - [subtree] type
#>  - [HM758930.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`91`
#> Cluster Record [id 91]
#>  - [subtree] type
#>  - [HM759101.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`92`
#> Cluster Record [id 92]
#>  - [subtree] type
#>  - [HM759372.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`93`
#> Cluster Record [id 93]
#>  - [subtree] type
#>  - [HM759729.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`94`
#> Cluster Record [id 94]
#>  - [subtree] type
#>  - [HM759896.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`95`
#> Cluster Record [id 95]
#>  - [subtree] type
#>  - [HM760080.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`96`
#> Cluster Record [id 96]
#>  - [subtree] type
#>  - [HM760256.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`97`
#> Cluster Record [id 97]
#>  - [subtree] type
#>  - [HM760525.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`98`
#> Cluster Record [id 98]
#>  - [subtree] type
#>  - [HM760608.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`99`
#> Cluster Record [id 99]
#>  - [subtree] type
#>  - [HM761193.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`100`
#> Cluster Record [id 100]
#>  - [subtree] type
#>  - [HM761507.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`101`
#> Cluster Record [id 101]
#>  - [subtree] type
#>  - [HM761768.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`102`
#> Cluster Record [id 102]
#>  - [subtree] type
#>  - [HM762092.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`103`
#> Cluster Record [id 103]
#>  - [subtree] type
#>  - [HM762180.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`104`
#> Cluster Record [id 104]
#>  - [subtree] type
#>  - [HM762427.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`105`
#> Cluster Record [id 105]
#>  - [subtree] type
#>  - [HM762765.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`106`
#> Cluster Record [id 106]
#>  - [subtree] type
#>  - [HM763261.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`107`
#> Cluster Record [id 107]
#>  - [subtree] type
#>  - [HM763727.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`108`
#> Cluster Record [id 108]
#>  - [subtree] type
#>  - [HM764102.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`109`
#> Cluster Record [id 109]
#>  - [subtree] type
#>  - [HM764317.1] seed sequence
#>  - [5] sequences
#>  - [5] taxa
#> 
#> $`110`
#> Cluster Record [id 110]
#>  - [subtree] type
#>  - [KR902342.1] seed sequence
#>  - [4] sequences
#>  - [3] taxa
#> 
#> $`111`
#> Cluster Record [id 111]
#>  - [subtree] type
#>  - [AF014508.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`112`
#> Cluster Record [id 112]
#>  - [subtree] type
#>  - [AF014506.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`113`
#> Cluster Record [id 113]
#>  - [subtree] type
#>  - [KC762160.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`114`
#> Cluster Record [id 114]
#>  - [subtree] type
#>  - [KC762072.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`115`
#> Cluster Record [id 115]
#>  - [subtree] type
#>  - [KC762014.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`116`
#> Cluster Record [id 116]
#>  - [subtree] type
#>  - [KC761980.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`117`
#> Cluster Record [id 117]
#>  - [subtree] type
#>  - [KC761918.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`118`
#> Cluster Record [id 118]
#>  - [subtree] type
#>  - [KC761889.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`119`
#> Cluster Record [id 119]
#>  - [subtree] type
#>  - [KC761833.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`120`
#> Cluster Record [id 120]
#>  - [subtree] type
#>  - [KC761782.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`121`
#> Cluster Record [id 121]
#>  - [subtree] type
#>  - [KC761695.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`122`
#> Cluster Record [id 122]
#>  - [subtree] type
#>  - [KC761632.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`123`
#> Cluster Record [id 123]
#>  - [subtree] type
#>  - [KC761601.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`124`
#> Cluster Record [id 124]
#>  - [subtree] type
#>  - [KC761569.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`125`
#> Cluster Record [id 125]
#>  - [subtree] type
#>  - [KC761504.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`126`
#> Cluster Record [id 126]
#>  - [subtree] type
#>  - [KC761470.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`127`
#> Cluster Record [id 127]
#>  - [subtree] type
#>  - [KC761405.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`128`
#> Cluster Record [id 128]
#>  - [subtree] type
#>  - [KC761242.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`129`
#> Cluster Record [id 129]
#>  - [subtree] type
#>  - [KC761177.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`130`
#> Cluster Record [id 130]
#>  - [subtree] type
#>  - [KC761016.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`131`
#> Cluster Record [id 131]
#>  - [subtree] type
#>  - [KC760988.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`132`
#> Cluster Record [id 132]
#>  - [subtree] type
#>  - [JQ932280.1] seed sequence
#>  - [4] sequences
#>  - [3] taxa
#> 
#> $`133`
#> Cluster Record [id 133]
#>  - [subtree] type
#>  - [JQ932662.1] seed sequence
#>  - [4] sequences
#>  - [3] taxa
#> 
#> $`134`
#> Cluster Record [id 134]
#>  - [subtree] type
#>  - [HM762511.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`135`
#> Cluster Record [id 135]
#>  - [subtree] type
#>  - [HM764645.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`136`
#> Cluster Record [id 136]
#>  - [subtree] type
#>  - [AF027546.1] seed sequence
#>  - [4] sequences
#>  - [1] taxa
#> 
#> $`137`
#> Cluster Record [id 137]
#>  - [subtree] type
#>  - [HM764908.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`138`
#> Cluster Record [id 138]
#>  - [subtree] type
#>  - [HM765175.1] seed sequence
#>  - [4] sequences
#>  - [4] taxa
#> 
#> $`139`
#> Cluster Record [id 139]
#>  - [subtree] type
#>  - [AB239200.1] seed sequence
#>  - [4] sequences
#>  - [1] taxa
#> 
#> $`140`
#> Cluster Record [id 140]
#>  - [direct] type
#>  - [DQ098863.1] seed sequence
#>  - [4] sequences
#>  - [1] taxa
#> 
#> $`141`
#> Cluster Record [id 141]
#>  - [direct] type
#>  - [DQ098851.1] seed sequence
#>  - [4] sequences
#>  - [1] taxa
#> 
#> $`142`
#> Cluster Record [id 142]
#>  - [subtree] type
#>  - [HM758657.1] seed sequence
#>  - [4] sequences
#>  - [2] taxa
#> 
#> $`143`
#> Cluster Record [id 143]
#>  - [subtree] type
#>  - [MW321653.1] seed sequence
#>  - [3] sequences
#>  - [2] taxa
#> 
#> $`144`
#> Cluster Record [id 144]
#>  - [subtree] type
#>  - [AF014509.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`145`
#> Cluster Record [id 145]
#>  - [subtree] type
#>  - [KC762104.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`146`
#> Cluster Record [id 146]
#>  - [subtree] type
#>  - [KC761277.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`147`
#> Cluster Record [id 147]
#>  - [subtree] type
#>  - [KC761210.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`148`
#> Cluster Record [id 148]
#>  - [subtree] type
#>  - [KC761755.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`149`
#> Cluster Record [id 149]
#>  - [subtree] type
#>  - [KC761438.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`150`
#> Cluster Record [id 150]
#>  - [subtree] type
#>  - [KC761338.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`151`
#> Cluster Record [id 151]
#>  - [subtree] type
#>  - [KC760954.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`152`
#> Cluster Record [id 152]
#>  - [subtree] type
#>  - [KC760866.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`153`
#> Cluster Record [id 153]
#>  - [subtree] type
#>  - [KC760833.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`154`
#> Cluster Record [id 154]
#>  - [subtree] type
#>  - [KC760802.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`155`
#> Cluster Record [id 155]
#>  - [subtree] type
#>  - [KC760770.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`156`
#> Cluster Record [id 156]
#>  - [subtree] type
#>  - [KC760738.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`157`
#> Cluster Record [id 157]
#>  - [subtree] type
#>  - [KC760712.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`158`
#> Cluster Record [id 158]
#>  - [subtree] type
#>  - [KC760681.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`159`
#> Cluster Record [id 159]
#>  - [subtree] type
#>  - [KC760611.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`160`
#> Cluster Record [id 160]
#>  - [subtree] type
#>  - [KC760514.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`161`
#> Cluster Record [id 161]
#>  - [subtree] type
#>  - [KC760417.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`162`
#> Cluster Record [id 162]
#>  - [subtree] type
#>  - [KC760385.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`163`
#> Cluster Record [id 163]
#>  - [subtree] type
#>  - [KC760326.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`164`
#> Cluster Record [id 164]
#>  - [subtree] type
#>  - [KC760263.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`165`
#> Cluster Record [id 165]
#>  - [subtree] type
#>  - [HM761011.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`166`
#> Cluster Record [id 166]
#>  - [subtree] type
#>  - [HM761143.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`167`
#> Cluster Record [id 167]
#>  - [subtree] type
#>  - [HM762858.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`168`
#> Cluster Record [id 168]
#>  - [subtree] type
#>  - [HM763019.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`169`
#> Cluster Record [id 169]
#>  - [subtree] type
#>  - [HM763994.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`170`
#> Cluster Record [id 170]
#>  - [subtree] type
#>  - [HM764396.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`171`
#> Cluster Record [id 171]
#>  - [subtree] type
#>  - [AY900524.1] seed sequence
#>  - [3] sequences
#>  - [1] taxa
#> 
#> $`172`
#> Cluster Record [id 172]
#>  - [subtree] type
#>  - [HM764813.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`173`
#> Cluster Record [id 173]
#>  - [subtree] type
#>  - [AY449065.1] seed sequence
#>  - [3] sequences
#>  - [1] taxa
#> 
#> $`174`
#> Cluster Record [id 174]
#>  - [subtree] type
#>  - [AY449057.1] seed sequence
#>  - [3] sequences
#>  - [1] taxa
#> 
#> $`175`
#> Cluster Record [id 175]
#>  - [subtree] type
#>  - [HM756999.1] seed sequence
#>  - [3] sequences
#>  - [3] taxa
#> 
#> $`176`
#> Cluster Record [id 176]
#>  - [subtree] type
#>  - [AB239246.1] seed sequence
#>  - [3] sequences
#>  - [1] taxa
#> 
#> $`177`
#> Cluster Record [id 177]
#>  - [subtree] type
#>  - [AB239226.1] seed sequence
#>  - [3] sequences
#>  - [1] taxa
#> 
#> $`178`
#> Cluster Record [id 178]
#>  - [subtree] type
#>  - [FJ154793.1] seed sequence
#>  - [3] sequences
#>  - [1] taxa
#> 
#> $`179`
#> Cluster Record [id 179]
#>  - [direct] type
#>  - [AY449065.1] seed sequence
#>  - [3] sequences
#>  - [1] taxa
#> 
#> $`180`
#> Cluster Record [id 180]
#>  - [direct] type
#>  - [AY449057.1] seed sequence
#>  - [3] sequences
#>  - [1] taxa
#> 
#> $`181`
#> Cluster Record [id 181]
#>  - [direct] type
#>  - [MF632276.1] seed sequence
#>  - [3] sequences
#>  - [1] taxa
#> 
#> $`182`
#> Cluster Record [id 182]
#>  - [subtree] type
#>  - [HM759274.1] seed sequence
#>  - [3] sequences
#>  - [2] taxa
#> 
#> $`183`
#> Cluster Record [id 183]
#>  - [subtree] type
#>  - [AF338376.1] seed sequence
#>  - [3] sequences
#>  - [2] taxa
#> 
# access cluster records [[
(clstrarc[[clstrarc@ids[[1]]]])  # first cluster record
#> Cluster Record [id 0]
#>  - [subtree] type
#>  - [AF129795.1] seed sequence
#>  - [173] sequences
#>  - [5] taxa
# generate new cluster archives with [
(clstrarc[clstrarc@ids[1:10]])  # first 10 clusters
#> Archive of cluster record(s)
#>  - [10] clusters
```
