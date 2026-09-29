# Get outgroup

Return the outgroup based on a tree and a vector of IDs.

## Usage

``` r
getOtgrp(tree, ids)
```

## Arguments

- tree:

  `TreeMan` object

- ids:

  vector of node ids

## Details

Returns a id, character. If there are multiple possible outgroups,
returns NULL.

## See also

<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

data(mammals)
# orangutan is an outgroup wrt humans and chimps
getOtgrp(mammals, ids = c("Homo_sapiens", "Pan_troglodytes", "Pongo_pygmaeus"))
#> [1] "Pongo_pygmaeus"
```
