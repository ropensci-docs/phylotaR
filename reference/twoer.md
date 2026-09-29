# Generate a tree of two tips

Returns a `TreeMan` tree with two tips and a root.

## Usage

``` r
twoer(tids = c("t1", "t2"), spns = c(1, 1), rid = "root", root_spn = 0)
```

## Arguments

- tids:

  tip IDs

- spns:

  tip spans

- rid:

  root ID

- root_spn:

  root span

## Details

Useful for building larger trees with
[`addClade()`](https://docs.ropensci.org/phylotaR/reference/addClade.md).
Note, a node matrix cannot be added to a tree of two tips.

## See also

[`TreeMan-class`](https://docs.ropensci.org/phylotaR/reference/TreeMan-class.md),
[`randTree`](https://docs.ropensci.org/phylotaR/reference/randTree.md)

## Examples

``` r

tree <- twoer()
```
