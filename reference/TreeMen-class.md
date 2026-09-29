# TreeMen-class

S4 class for multiple phylogenetic trees

## Usage

``` r
# S4 method for class 'TreeMen'
cTrees(x, ...)

# S4 method for class 'TreeMen,ANY'
x[[i]]

# S4 method for class 'TreeMen,character,missing,missing'
x[i, j, ..., drop = TRUE]

# S4 method for class 'TreeMen'
as.character(x)

# S4 method for class 'TreeMen'
show(object)

# S4 method for class 'TreeMen'
str(object, max.level = 2L, ...)

# S4 method for class 'TreeMen'
print(x)

# S4 method for class 'TreeMen'
summary(object)
```

## Arguments

- x:

  `TreeMen` object

- ...:

  additional tree objects

- i:

  tree index (integer or character)

- j:

  missing

- drop:

  missing

- object:

  `TreeMen` object

- max.level:

  [`str()`](https://rdrr.io/r/utils/str.html) maximum level

## Slots

- `treelst`:

  list of `TreeMan` objects

- `ntips`:

  sum of tips per tree

- `ntrees`:

  total number of trees

## See also

[`cTrees`](https://docs.ropensci.org/phylotaR/reference/cTrees.md)
