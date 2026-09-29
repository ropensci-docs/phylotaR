# Get path between nodes

Return node ids for connecting `from` to `to`.

## Usage

``` r
getPath(tree, from, to)
```

## Arguments

- tree:

  `TreeMan` object

- from:

  starting node id

- to:

  ending node id

## Details

Returns a vector, first id is `from` to `to`.

## See also

<https://github.com/DomBennett/treeman/wiki/get-methods>

## Examples

``` r

data(mammals)
# what's the phylogenetic distance from humans to gorillas?
ape_id <- getPrnt(mammals, ids = c("Homo_sapiens", "Hylobates_concolor"))
pth <- getPath(mammals, from = "Homo_sapiens", to = "Gorilla_gorilla")
sum(getNdsSlt(mammals, ids = pth, slt_nm = "spn"))
#> [1] 32.4
```
