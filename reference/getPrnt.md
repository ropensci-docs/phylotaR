# Get parent

Return parental (most recent common ancestor) node id for `ids`.

## Usage

``` r
getPrnt(tree, ids)
```

## Arguments

- tree:

  `TreeMan` object

- ids:

  vector of node ids

## Details

Returns a character.

## See also

[`getSubtree`](https://docs.ropensci.org/phylotaR/reference/getSubtree.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

data(mammals)
# choosing ids from the two main branches of apes allows to find the parent for all apes
ape_id <- getPrnt(mammals, ids = c("Homo_sapiens", "Hylobates_concolor"))
```
