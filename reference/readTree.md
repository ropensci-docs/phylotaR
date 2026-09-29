# Read a Newick tree

Return a `TreeMan` or `TreeMen` object from a Newick treefile

## Usage

``` r
readTree(
  file = NULL,
  text = NULL,
  spcl_slt_nm = "Unknown",
  wndmtrx = FALSE,
  parallel = FALSE,
  progress = "none"
)
```

## Arguments

- file:

  file path

- text:

  Newick character string

- spcl_slt_nm:

  name of special slot for internal node labels, default 'Unknown'.

- wndmtrx:

  T/F add node matrix? Default FALSE.

- parallel:

  logical, make parallel?

- progress:

  name of the progress bar to use, see
  [`create_progress_bar`](https://rdrr.io/pkg/plyr/man/create_progress_bar.html)

## Details

Read a single or multiple trees from a file, or a text string.
Parallelizable when reading multiple trees. The function will add any
internal node labels in the Newick tree as a user-defined data slots.
The name of this slot is defined with the `spcl_slt_nm`. These data can
be accessed/manipulated with the `` `getNdsSlt()` `` function. Trees are
always read as rooted. (Unrooted trees have polytomous root nodes.)

## See also

<https://en.wikipedia.org/wiki/Newick_format>,
[`addNdmtrx`](https://docs.ropensci.org/phylotaR/reference/addNdmtrx.md),
[`writeTree`](https://docs.ropensci.org/phylotaR/reference/writeTree.md),
[`randTree`](https://docs.ropensci.org/phylotaR/reference/randTree.md),
[`readTrmn`](https://docs.ropensci.org/phylotaR/reference/readTrmn.md),
[`writeTrmn`](https://docs.ropensci.org/phylotaR/reference/writeTrmn.md),
[`saveTreeMan`](https://docs.ropensci.org/phylotaR/reference/saveTreeMan.md),
[`loadTreeMan`](https://docs.ropensci.org/phylotaR/reference/loadTreeMan.md)

## Examples

``` r

# tree string with internal node labels as bootstrap results
tree <- readTree(
  text = "((A:1.0,B:1.0)0.9:1.0,(C:1.0,D:1.0)0.8:1.0)0.7:1.0;",
  spcl_slt_nm = "bootstrap"
)
# retrieve bootstrap values by node
tree["bootstrap"]
#>     A     B    n3     C     D    n6    n7 
#>    NA    NA "0.9"    NA    NA "0.8" "0.7" 
```
