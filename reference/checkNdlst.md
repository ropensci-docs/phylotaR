# Check if ndlst is correct

Return T/F fpr `ndlst` consistency

## Usage

``` r
checkNdlst(ndlst, root)
```

## Arguments

- ndlst:

  `ndlst`

- root:

  root ID

## Details

Tests whether each node in tree points to valid other node IDs. Also
ensures \`spn\` and \`root\` are correct. Reports nodes that have
errors.

## See also

[`fastCheckTreeMan`](https://docs.ropensci.org/phylotaR/reference/fastCheckTreeMan.md),
[`checkTreeMen`](https://docs.ropensci.org/phylotaR/reference/checkTreeMen.md)

## Examples

``` r

tree <- randTree(100)
(checkNdlst(tree@ndlst, tree@root))
#> [1] TRUE
```
