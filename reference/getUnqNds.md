# Get unique nodes represented by tips

Return a list of IDs for any node that are represented by tip IDs given.

## Usage

``` r
getUnqNds(tree, tids)
```

## Arguments

- tree:

  `TreeMan` object

- tids:

  vector of tip IDs

## Details

Returns a vector.

## See also

[`getCnnctdNds`](https://docs.ropensci.org/phylotaR/reference/getCnnctdNds.md),
[`calcFrPrp`](https://docs.ropensci.org/phylotaR/reference/calcFrPrp.md),
[`calcPhyDv`](https://docs.ropensci.org/phylotaR/reference/calcPhyDv.md)

## Examples

``` r

tree <- randTree(10)
unqnds <- getUnqNds(tree, c("t1", "t2"))
```
