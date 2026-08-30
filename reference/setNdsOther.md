# Set a user defined slot for multiple nodes

Return a tree with a user defined slot for node IDs.

## Usage

``` r
setNdsOther(tree, ids, vals, slt_nm, parallel = FALSE, progress = "none")
```

## Arguments

- tree:

  `TreeMan` object

- ids:

  id sof the nodes

- vals:

  data for slot

- slt_nm:

  slot name

- parallel:

  logical, make parallel?

- progress:

  name of the progress bar to use, see
  [`create_progress_bar`](https://rdrr.io/pkg/plyr/man/create_progress_bar.html)

## Details

Runs
[`setNdOther()`](https://docs.ropensci.org/phylotaR/reference/setNdOther.md)
over multiple nodes. Parellizable.

## See also

[`setNdOther`](https://docs.ropensci.org/phylotaR/reference/setNdOther.md)
<https://github.com/DomBennett/treeman/wiki/set-methods>

## Examples

``` r

tree <- randTree(10)
# e.g. confidences for nodes
vals <- runif(min = 0, max = 1, n = tree["nall"])
tree <- setNdsOther(tree, tree["all"], vals, "confidence")
tree <- updateSlts(tree)
summary(tree)
#> Tree (TreeMan Object):
#>   + 10 tips
#>   + 9 internal nodes
#>   + Binary
#>   + PD 10.2
#>   + Root node is "n1"
#>   + With additional node slots:
#>     [confidence]
(getNdsSlt(tree, ids = tree["all"], slt_nm = "confidence"))
#>        n1        n2        n3        n4        n5        n6        n7        n8 
#> 0.4809234 0.8587359 0.9239257 0.7437844 0.7743736 0.4510006 0.8044644 0.1762576 
#>        n9        t1        t2        t3        t4        t5        t6        t7 
#> 0.7152410 0.9353107 0.2404478 0.4693941 0.1605854 0.3557688 0.9645920 0.7278199 
#>        t8        t9       t10 
#> 0.1427215 0.9365869 0.4791499 
```
