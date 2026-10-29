# Return matrix of txid in sequence

Searches through lineages of sequences' source organisms to determine
whether each txid is represented by the sequence.

## Usage

``` r
mk_txid_in_sq_mtrx(phylota, txids, sids = phylota@sids)
```

## Arguments

- phylota:

  Phylota

- txids:

  Taxonomic IDs

- sids:

  Sequence IDs

## Value

matrix

## See also

Other tools-private:
[`summary_phylota()`](https://docs.ropensci.org/phylotaR/reference/summary_phylota.md),
[`update_phylota()`](https://docs.ropensci.org/phylotaR/reference/update_phylota.md)
