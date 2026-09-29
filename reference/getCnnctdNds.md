# Get all nodes connected by given tips

Return a vector of IDs of all nodes that are connected to tip IDs given.

## Usage

``` r
getCnnctdNds(tree, tids)
```

## Arguments

- tree:

  `TreeMan` object

- tids:

  vector of tip IDs

## Details

Returns a vector. This function is the basis for
[`calcPhyDv()`](https://docs.ropensci.org/phylotaR/reference/calcPhyDv.md),
it determines the unique set of nodes connected for a set of tips.

## See also

[`getUnqNds`](https://docs.ropensci.org/phylotaR/reference/getUnqNds.md),
[`calcFrPrp`](https://docs.ropensci.org/phylotaR/reference/calcFrPrp.md),
[`calcPhyDv`](https://docs.ropensci.org/phylotaR/reference/calcPhyDv.md)

## Examples

``` r

tree <- randTree(10)
cnntdnds <- getCnnctdNds(tree, c("t1", "t2"))
```
