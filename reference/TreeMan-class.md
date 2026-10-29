# TreeMan-class

S4 class for representing phylogenetic trees as a list of nodes.

## Usage

``` r
# S4 method for class 'TreeMan,character'
x[[i]]

# S4 method for class 'TreeMan,character,missing,missing'
x[i, j, ..., drop = TRUE]

# S4 method for class 'TreeMan'
as.character(x)

# S4 method for class 'TreeMan'
show(object)

# S4 method for class 'TreeMan'
print(x)

# S4 method for class 'TreeMan'
str(object, max.level = 2L, ...)

# S4 method for class 'TreeMan'
summary(object)

# S4 method for class 'TreeMan'
cTrees(x, ...)
```

## Arguments

- x:

  `TreeMan` object

- i:

  node ID or slot name

- j:

  missing

- ...:

  additional tree objects

- drop:

  missing

- object:

  `TreeMan` object

- max.level:

  [`str()`](https://rdrr.io/r/utils/str.html) maximum number of levels
  to show

## Details

A `TreeMan` object holds a list of nodes. The idea of the `TreeMan`
class is to make adding and removing nodes as similar as possible to
adding and removing elements in a list. Note that internal nodes and
tips are both considered nodes. Trees can be polytomous but not
unrooted.

Each node within the `TreeMan` `ndlst` contains the following data
slots:

- `id`: character string for the node ID

- `txnym`: name of taxonomic clade (optional)

- `spn`: length of the preceding branch

- `prid`: ID of the immediately preceding node, NULL if root

- `ptid`: IDs of the immediately connecting nodes

See below in 'Examples' for these methods in use.

## Slots

- `ndlst`:

  list of nodes

- `nds`:

  vector of node ids that are internal nodes

- `nnds`:

  numeric of number of internal nodes in tree

- `tips`:

  vector of node ids that are tips

- `ntips`:

  numeric of number of internal nodes in tree

- `all`:

  vector of all node ids

- `nall`:

  numeric of number of all nodes in tree

- `pd`:

  numeric of total branch length of tree

- `tinds`:

  indexes of all tip nodes in tree

- `prinds`:

  indexes of all pre-nodes in tree

- `wspn`:

  logical, do nodes have spans

- `wtxnyms`:

  logical, do nodes have txnyms

- `ply`:

  logical, is tree bifurcating

- `root`:

  character of node id of root, if no root then empty character

- `updtd`:

  logical, if tree slots have been updated since initiation or change

- `othr_slt_nms`:

  vector, character list of additional data slots added to nodes

- `ndmtrx`:

  matrix, T/Fs representing tree structure

## See also

[`randTree`](https://docs.ropensci.org/phylotaR/reference/randTree.md),
[`Node-class`](https://docs.ropensci.org/phylotaR/reference/Node-class.md),
[`phylo-to-TreeMan`](https://docs.ropensci.org/phylotaR/reference/phylo-to-TreeMan.md),
[`TreeMan-to-phylo`](https://docs.ropensci.org/phylotaR/reference/TreeMan-to-phylo.md)

## Examples

``` r

# Generate random tree
tree <- randTree(10)
# Print to get basic stats
summary(tree)
#> Tree (TreeMan Object):
#>   + 10 tips
#>   + 9 internal nodes
#>   + Binary
#>   + PD 8.78
#>   + Root node is "n1"
# Slots....
tree["tips"] # return all tips IDs
#>  [1] "t1"  "t10" "t2"  "t3"  "t4"  "t5"  "t6"  "t7"  "t8"  "t9" 
tree["nds"] # return all internal node IDs
#> [1] "n1" "n2" "n3" "n4" "n5" "n6" "n7" "n8" "n9"
tree["ntips"] # count all tips
#> [1] 10
tree["nnds"] # count all internal nodes
#> [1] 9
tree["root"] # identify root node
#> [1] "n1"
tree[["t1"]] # return t1 node object
#> Node (tip node):
#>   + ID: "t1"
#>   + prid: "n7"
#>   + spn: 0.031
#>   + predist: 3.3
#>   + pd: 0
tree["pd"] # return phylogenetic diversity
#> [1] 8.77691
tree["ply"] # is polytomous?
#> [1] FALSE
# Additional special slots (calculated upon call)
tree["age"] # get tree's age
#> [1] 4.567286
tree["ultr"] # determine if tree is ultrametric
#> [1] FALSE
tree["spns"] # get all the spans of the tree IDs
#>         n1         n2         n3         n4         n5         n6         n7 
#> 0.00000000 0.73531960 0.19595673 0.98053967 0.74152153 0.05144628 0.53021246 
#>         n8         n9         t1         t2         t3         t4         t5 
#> 0.69582388 0.68855600 0.03123033 0.22556253 0.30083081 0.63646561 0.47902455 
#>         t6         t7         t8         t9        t10 
#> 0.43217126 0.70643384 0.94857658 0.18033877 0.21689988 
tree["prids"] # get all the IDs of preceding nodes
#>   n1   n2   n3   n4   n5   n6   n7   n8   n9   t1   t2   t3   t4   t5   t6   t7 
#> "n1" "n1" "n2" "n3" "n4" "n5" "n6" "n7" "n4" "n7" "n9" "n6" "n8" "n8" "n2" "n3" 
#>   t8   t9  t10 
#> "n9" "n1" "n5" 
tree["ptids"] # get all the IDs of following nodes
#> $n1
#> [1] "n2" "t9"
#> 
#> $n2
#> [1] "n3" "t6"
#> 
#> $n3
#> [1] "n4" "t7"
#> 
#> $n4
#> [1] "n5" "n9"
#> 
#> $n5
#> [1] "n6"  "t10"
#> 
#> $n6
#> [1] "n7" "t3"
#> 
#> $n7
#> [1] "n8" "t1"
#> 
#> $n8
#> [1] "t4" "t5"
#> 
#> $n9
#> [1] "t2" "t8"
#> 
#> $t1
#> character(0)
#> 
#> $t2
#> character(0)
#> 
#> $t3
#> character(0)
#> 
#> $t4
#> character(0)
#> 
#> $t5
#> character(0)
#> 
#> $t6
#> character(0)
#> 
#> $t7
#> character(0)
#> 
#> $t8
#> character(0)
#> 
#> $t9
#> character(0)
#> 
#> $t10
#> character(0)
#> 
tree["txnyms"] # get all the taxonyms of all nodes
#>  n1  n2  n3  n4  n5  n6  n7  n8  n9  t1  t2  t3  t4  t5  t6  t7  t8  t9 t10 
#>  NA  NA  NA  NA  NA  NA  NA  NA  NA  NA  NA  NA  NA  NA  NA  NA  NA  NA  NA 
# In addition [] can be used for any user-defined slot
# Because all nodes are lists with metadata we can readily
#  get specific information on nodes of interest
nd <- tree[["n2"]]
summary(nd)
#> Node (internal node):
#>   + ID: "n2"
#>   + prid: "n1"
#>   + ptid: "n3", "t6"
#>   + nkids: 9
#>   + spn: 0.74
#>   + predist: 0.74
#>   + pd: 7.9
# And then use the same syntax for the tree
nd["nkids"] # .... nkids, pd, etc.
#> [1] 9

# Convert to phylo and plot
library(ape)
tree <- as(tree, "phylo")
plot(tree)
```
