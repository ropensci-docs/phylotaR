# Node-class

The `Node` is an S4 class used for displaying node information. It is
only generated when a user implements the `[[]]` on a tree. Information
is only accurate if tree has been updated with `updateTree()`.

## Usage

``` r
# S4 method for class 'Node'
as.character(x)

# S4 method for class 'Node'
show(object)

# S4 method for class 'Node'
print(x)

# S4 method for class 'Node'
summary(object)

# S4 method for class 'Node,character,missing,missing'
x[i, j, ..., drop = TRUE]
```

## Arguments

- x:

  `Node` object

- object:

  `Node` object

- i:

  slot name

- j:

  missing

- ...:

  missing

- drop:

  missing

## Slots

- `id`:

  unique ID for node in tree\['ndlst'\]

- `spn`:

  length of preceding branch

- `prid`:

  parent node ID

- `ptid`:

  child node ID

- `kids`:

  descending tip IDs

- `nkids`:

  number of descending tip IDs

- `txnym`:

  list of associated taxonyms

- `pd`:

  total branch length represented by node

- `prdst`:

  total branch length of connected prids

- `root`:

  T/F root node?

- `tip`:

  T/F tip node?

## See also

[`TreeMan-class`](https://docs.ropensci.org/phylotaR/reference/TreeMan-class.md),
[`TreeMen-class`](https://docs.ropensci.org/phylotaR/reference/TreeMen-class.md)
