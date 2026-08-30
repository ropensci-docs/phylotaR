# Pin tips to a tree

Returns a tree with new tips added based on given lineages and time
points

## Usage

``` r
pinTips(tree, tids, lngs, end_ages, tree_age)
```

## Arguments

- tree:

  `TreeMan` object

- tids:

  new tip ids

- lngs:

  list of vectors of the lineages of each tid (ordered high to low rank)

- end_ages:

  end time points for each tid

- tree_age:

  age of tree

## Details

User must provide a vector of new tip IDs, a list of the ranked lineages
for these IDs (in ascending order) and a vector of end time points for
each new ID (0s for extant tips). The function expects the given tree to
be taxonomically informed; the `txnym` slot for every node should have a
taxonomic label. The function takes the lineage and tries to randomly
add the new tip at the lowest point in the taxonomic rank before the end
time point. Note, returned tree will not have a node matrix.

## See also

[`addTip`](https://docs.ropensci.org/phylotaR/reference/addTip.md),
[`rmTips`](https://docs.ropensci.org/phylotaR/reference/rmTips.md),
<https://github.com/DomBennett/treeman/wiki/manip-methods>

## Examples

``` r
# see https://github.com/DomBennett/treeman/wiki/Pinning-tips for a detailed example
```
