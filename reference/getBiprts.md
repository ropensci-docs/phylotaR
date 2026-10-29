# Get the sets of labels for each bipartition in tree

Returns a list of tip IDs for each branch in the tree. Options allow the
user to act as if the root is not present and to use a universal code
for comparing between trees.

## Usage

``` r
getBiprts(tree, tips = tree@tips, root = TRUE, universal = FALSE)
```

## Arguments

- tree:

  `TreeMan` object

- tips:

  vector of tips IDs to use for bipartitions

- root:

  Include the root for the bipartitions? Default TRUE.

- universal:

  Create a code for comparing between trees

## Details

Setting `root` to FALSE will ignore the bipartitions created by the
root. Setting `universal` to TRUE will return a vector of 0s and 1s, not
a list of tips. These codes will always begin with 1, and will allow for
the comparison of splits between trees as they do not have "chiralty",
so to speak.

## See also

[`calcDstRF`](https://docs.ropensci.org/phylotaR/reference/calcDstRF.md)

## Examples

``` r

tree <- randTree(10)
# get all of the tip IDs for each branch in the rooted tree
(getBiprts(tree))
#> $n1
#> $n1[[1]]
#>  [1] "t1"  "t10" "t2"  "t3"  "t4"  "t5"  "t6"  "t7"  "t8"  "t9" 
#> 
#> $n1[[2]]
#> character(0)
#> 
#> 
#> $n2
#> $n2[[1]]
#> [1] "t10" "t2"  "t4"  "t5"  "t7"  "t8" 
#> 
#> $n2[[2]]
#> [1] "t1" "t3" "t6" "t9"
#> 
#> 
#> $n3
#> $n3[[1]]
#> [1] "t1" "t3" "t6" "t9"
#> 
#> $n3[[2]]
#> [1] "t10" "t2"  "t4"  "t5"  "t7"  "t8" 
#> 
#> 
#> $n4
#> $n4[[1]]
#> [1] "t3" "t6"
#> 
#> $n4[[2]]
#> [1] "t1"  "t10" "t2"  "t4"  "t5"  "t7"  "t8"  "t9" 
#> 
#> 
#> $n5
#> $n5[[1]]
#> [1] "t1" "t9"
#> 
#> $n5[[2]]
#> [1] "t10" "t2"  "t3"  "t4"  "t5"  "t6"  "t7"  "t8" 
#> 
#> 
#> $n6
#> $n6[[1]]
#> [1] "t2" "t4" "t7" "t8"
#> 
#> $n6[[2]]
#> [1] "t1"  "t10" "t3"  "t5"  "t6"  "t9" 
#> 
#> 
#> $n7
#> $n7[[1]]
#> [1] "t2" "t4" "t8"
#> 
#> $n7[[2]]
#> [1] "t1"  "t10" "t3"  "t5"  "t6"  "t7"  "t9" 
#> 
#> 
#> $n8
#> $n8[[1]]
#> [1] "t2" "t4"
#> 
#> $n8[[2]]
#> [1] "t1"  "t10" "t3"  "t5"  "t6"  "t7"  "t8"  "t9" 
#> 
#> 
#> $n9
#> $n9[[1]]
#> [1] "t10" "t5" 
#> 
#> $n9[[2]]
#> [1] "t1" "t2" "t3" "t4" "t6" "t7" "t8" "t9"
#> 
#> 
# ignore the root and get bipartitions for unrooted tree
(getBiprts(tree, root = FALSE))
#> $n2
#> $n2[[1]]
#> [1] "t10" "t2"  "t4"  "t5"  "t7"  "t8" 
#> 
#> $n2[[2]]
#> [1] "t1" "t3" "t6" "t9"
#> 
#> 
#> $n3
#> $n3[[1]]
#> [1] "t1" "t3" "t6" "t9"
#> 
#> $n3[[2]]
#> [1] "t10" "t2"  "t4"  "t5"  "t7"  "t8" 
#> 
#> 
#> $n4
#> $n4[[1]]
#> [1] "t3" "t6"
#> 
#> $n4[[2]]
#> [1] "t1"  "t10" "t2"  "t4"  "t5"  "t7"  "t8"  "t9" 
#> 
#> 
#> $n5
#> $n5[[1]]
#> [1] "t1" "t9"
#> 
#> $n5[[2]]
#> [1] "t10" "t2"  "t3"  "t4"  "t5"  "t6"  "t7"  "t8" 
#> 
#> 
#> $n6
#> $n6[[1]]
#> [1] "t2" "t4" "t7" "t8"
#> 
#> $n6[[2]]
#> [1] "t1"  "t10" "t3"  "t5"  "t6"  "t9" 
#> 
#> 
#> $n7
#> $n7[[1]]
#> [1] "t2" "t4" "t8"
#> 
#> $n7[[2]]
#> [1] "t1"  "t10" "t3"  "t5"  "t6"  "t7"  "t9" 
#> 
#> 
#> $n8
#> $n8[[1]]
#> [1] "t2" "t4"
#> 
#> $n8[[2]]
#> [1] "t1"  "t10" "t3"  "t5"  "t6"  "t7"  "t8"  "t9" 
#> 
#> 
#> $n9
#> $n9[[1]]
#> [1] "t10" "t5" 
#> 
#> $n9[[2]]
#> [1] "t1" "t2" "t3" "t4" "t6" "t7" "t8" "t9"
#> 
#> 
# use the universal code for comparing splits between trees
(getBiprts(tree, root = FALSE, universal = TRUE))
#> [1] "1001001001" "1110110111" "1000000001" "1101011001" "1101011101"
#> [6] "1101011111" "1011101111"
```
