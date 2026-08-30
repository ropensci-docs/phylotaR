# Add clade to tree

Returns a tree with added clade

## Usage

``` r
addClade(tree, id, clade)
```

## Arguments

- tree:

  `TreeMan` object

- id:

  tip/node ID in tree to which the clade will be added

- clade:

  `TreeMan` object

## Details

Add a `TreeMan` object to an existing `TreeMan` object by specifying an
ID at which to attach. If the id specified is an internal node, then the
original clade descending from that node will be replaced. Before
running, ensure no IDs are shared between the `tree` and the `clade`,
except for the IDs in the clade of that tree that will be replaced.
Note, returned tree will not have a node matrix.

## See also

[`rmClade`](https://docs.ropensci.org/phylotaR/reference/rmClade.md),
[`getSubtree`](https://docs.ropensci.org/phylotaR/reference/getSubtree.md),
<https://github.com/DomBennett/treeman/wiki/manip-methods>

## Examples

``` r

t1 <- randTree(100)
# extract a clade
cld <- getSubtree(t1, "n2")
# remove the same clade
t2 <- rmClade(t1, "n2")
# add the clade again
t3 <- addClade(t2, "n2", cld)
# t1 and t3 should be the same
# note there is no need to remove a clade before adding
t3 <- addClade(t1, "n2", cld) # same tree
```
