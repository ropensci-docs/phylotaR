# Update tree slots after manipulation

Return tree with updated slots.

## Usage

``` r
updateSlts(tree)
```

## Arguments

- tree:

  `TreeMan` object

## Details

Tree slots in the `TreeMan` object are usually automatically updated.
For certain single node manipulations they are not. Run this function to
update the slots.

## See also

[`addNdmtrx`](https://docs.ropensci.org/phylotaR/reference/addNdmtrx.md),
[`getAge`](https://docs.ropensci.org/phylotaR/reference/getAge.md)
