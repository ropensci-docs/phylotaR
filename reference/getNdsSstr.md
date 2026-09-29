# Get sister id

Returns the ids of the sister(s) of nd ids given.

## Usage

``` r
getNdsSstr(tree, ids, parallel = FALSE, progress = "none")
```

## Arguments

- tree:

  `TreeMan` object

- ids:

  nd ids

- parallel:

  logical, make parallel?

- progress:

  name of the progress bar to use, see
  [`create_progress_bar`](https://rdrr.io/pkg/plyr/man/create_progress_bar.html)

## Details

An error is raised if there is no sister (e.g. for the root). There can
be more than one sister if tree is polytomous. Parallelizable.

## See also

[`getNdSstr`](https://docs.ropensci.org/phylotaR/reference/getNdSstr.md),
<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

tree <- randTree(10)
getNdsSstr(tree, ids = tree["tips"])
#>  [1] "t9"  "t3"  "t8"  "t10" "t6"  "n8"  "t4"  "n7"  "t2"  "t1" 
```
