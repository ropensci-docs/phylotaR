# Set a user defined slot

Return a tree with a user defined slot for node ID.

## Usage

``` r
setNdOther(tree, id, val, slt_nm)
```

## Arguments

- tree:

  `TreeMan` object

- id:

  id of the node

- val:

  data for slot

- slt_nm:

  slot name

## Details

A user can specify new slots in a tree. Add a new slot with this
function by providing a node ID, a value for the new slot and a unique
new slot name. Slot names must not be default `TreeMan` names. The new
value can be any data type.

## See also

[`setNdsOther`](https://docs.ropensci.org/phylotaR/reference/setNdsOther.md)
<https://github.com/DomBennett/treeman/wiki/set-methods>

## Examples

``` r

tree <- randTree(10)
tree <- setNdOther(tree, "t1", 1, "binary_val")
tree <- updateSlts(tree)
(getNdSlt(tree, id = "t1", slt_nm = "binary_val"))
#> [1] 1
```
