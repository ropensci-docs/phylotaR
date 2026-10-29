# Set the ID of a node

Return a tree with the ID of a node altered.

## Usage

``` r
setNdID(tree, id, val)
```

## Arguments

- tree:

  `TreeMan` object

- id:

  id to be changed

- val:

  new id

## Details

IDs cannot be changed directly for the `TreeMan` class. To change an ID
use this function. Warning: all IDs must be unique, avoid spaces in IDs
and only use letters, numbers and underscores. Use
[`updateSlts`](https://docs.ropensci.org/phylotaR/reference/updateSlts.md)
after running.

## See also

[`setNdsID`](https://docs.ropensci.org/phylotaR/reference/setNdsID.md)
<https://github.com/DomBennett/treeman/wiki/set-methods>

## Examples

``` r

tree <- randTree(10)
tree <- setNdID(tree, "t1", "heffalump")
tree <- updateSlts(tree)
```
