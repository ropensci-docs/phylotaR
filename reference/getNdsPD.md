# Get phylogenetic diversities of nodes

Return summed value of all descending spns

## Usage

``` r
getNdsPD(tree, ids, parallel = FALSE, progress = "none")
```

## Arguments

- tree:

  `TreeMan` object

- ids:

  vector of node ids

- parallel:

  logical, make parallel?

- progress:

  name of the progress bar to use, see
  [`create_progress_bar`](https://rdrr.io/pkg/plyr/man/create_progress_bar.html)

## Details

Sums the lengths of all descending branches from a node.

## See also

[`getNdPD`](https://docs.ropensci.org/phylotaR/reference/getNdPD.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

tree <- randTree(10)
getNdsPD(tree, ids = tree["all"]) # return PD of all ids
#>        n1        n2        n3        n4        n5        n6        n7        n8 
#> 11.107549 10.043449  8.850029  7.977889  6.953430  2.301880  2.916683  1.121731 
#>        n9        t1        t2        t3        t4        t5        t6        t7 
#>  1.525615  0.000000  0.000000  0.000000  0.000000  0.000000  0.000000  0.000000 
#>        t8        t9       t10 
#>  0.000000  0.000000  0.000000 
```
