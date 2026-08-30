# Calculate phylogenetic diversity

Returns the phylogenetic diversity of a tree for the tips specified.

## Usage

``` r
calcPhyDv(tree, tids, parallel = FALSE, progress = "none")
```

## Arguments

- tree:

  `TreeMan` object

- tids:

  tip ids

- parallel:

  logical, make parallel?

- progress:

  name of the progress bar to use, see
  [`create_progress_bar`](https://rdrr.io/pkg/plyr/man/create_progress_bar.html)

## Details

Faith's phylogenetic diversity is calculated as the sum of all connected
branches for specified tips in a tree. It can be used to investigate how
biodviersity as measured by the phylogeny changes. Parallelizable. The
function uses `getCnntdNds()`.

## References

Faith, D. (1992). Conservation evaluation and phylogenetic diversity.
Biological Conservation, 61, 1-10.

## See also

[`calcFrPrp`](https://docs.ropensci.org/phylotaR/reference/calcFrPrp.md),
[`calcOvrlp`](https://docs.ropensci.org/phylotaR/reference/calcOvrlp.md),
[`getCnnctdNds`](https://docs.ropensci.org/phylotaR/reference/getCnnctdNds.md),
<https://github.com/DomBennett/treeman/wiki/calc-methods>

## Examples

``` r

tree <- randTree(10)
calcPhyDv(tree, tree["tips"])
#> [1] 8.28878
```
