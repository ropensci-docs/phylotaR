# Make tree ultrametric

Returns a tree with all tips ending at time 0

## Usage

``` r
ultrTree(tree)
```

## Arguments

- tree:

  `TreeMan` object

## Details

Re-calculates the branch lengths in the tree so that all tips are
brought to the same time point: all species are extant.

## See also

<https://github.com/DomBennett/treeman/wiki/manip-methods>

## Examples

``` r

tree <- randTree(10)
(getDcsd(tree)) # list all extinct tips
#> [1] "t1"  "t10" "t2"  "t3"  "t4"  "t5"  "t6"  "t7"  "t9" 
tree <- ultrTree(tree)
(getDcsd(tree)) # list all extinct tips
#> character(0)
```
