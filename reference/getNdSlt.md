# Get a node slot

Returns the value of named slot.

## Usage

``` r
getNdSlt(tree, slt_nm, id)
```

## Arguments

- tree:

  `TreeMan` object

- slt_nm:

  slot name

- id:

  node id

## Details

Returned object depends on name, either character, vector or numeric.
Default node slots are: id, spn, prid, ptid and txnym. If slot is empty,
returns NA.

## See also

[`getNdsSlt`](https://docs.ropensci.org/phylotaR/reference/getNdsSlt.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

tree <- randTree(10)
getNdSlt(tree, slt_nm = "spn", id = "t1") # return span of t1
#> [1] 0.7973574
```
