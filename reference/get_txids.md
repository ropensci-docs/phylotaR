# Get taxonomic IDs by rank

Return taxonomic IDs for a vector of sequence IDs or all sequences in a
cluster. User can specify what rank the IDs should be returned. If NULL,
the lowest level is returned.

## Usage

``` r
get_txids(
  phylota,
  cid = NULL,
  sid = NULL,
  txids = NULL,
  rnk = NULL,
  keep_higher = FALSE
)
```

## Arguments

- phylota:

  Phylota object

- cid:

  Cluster ID

- sid:

  Sequence ID(s)

- txids:

  Vector of txids

- rnk:

  Taxonomic rank

- keep_higher:

  Keep higher taxonomic IDs?

## Value

vector

## Details

txids can either be provided by user or they can be determined for a
vector of sids or for a cid. If keep_higher is TRUE, any sequence that
has a identity that is higher than the given rank will be returned. If
FALSE, these sequences will return ”.

## See also

Other tools-public:
[`calc_mad()`](https://docs.ropensci.org/phylotaR/reference/calc_mad.md),
[`calc_wrdfrq()`](https://docs.ropensci.org/phylotaR/reference/calc_wrdfrq.md),
[`drop_by_rank()`](https://docs.ropensci.org/phylotaR/reference/drop_by_rank.md),
[`drop_clstrs()`](https://docs.ropensci.org/phylotaR/reference/drop_clstrs.md),
[`drop_sqs()`](https://docs.ropensci.org/phylotaR/reference/drop_sqs.md),
[`get_clstr_slot()`](https://docs.ropensci.org/phylotaR/reference/get_clstr_slot.md),
[`get_nsqs()`](https://docs.ropensci.org/phylotaR/reference/get_nsqs.md),
[`get_ntaxa()`](https://docs.ropensci.org/phylotaR/reference/get_ntaxa.md),
[`get_sq_slot()`](https://docs.ropensci.org/phylotaR/reference/get_sq_slot.md),
[`get_stage_times()`](https://docs.ropensci.org/phylotaR/reference/get_stage_times.md),
[`get_tx_slot()`](https://docs.ropensci.org/phylotaR/reference/get_tx_slot.md),
[`is_txid_in_clstr()`](https://docs.ropensci.org/phylotaR/reference/is_txid_in_clstr.md),
[`is_txid_in_sq()`](https://docs.ropensci.org/phylotaR/reference/is_txid_in_sq.md),
[`list_clstrrec_slots()`](https://docs.ropensci.org/phylotaR/reference/list_clstrrec_slots.md),
[`list_ncbi_ranks()`](https://docs.ropensci.org/phylotaR/reference/list_ncbi_ranks.md),
[`list_seqrec_slots()`](https://docs.ropensci.org/phylotaR/reference/list_seqrec_slots.md),
[`list_taxrec_slots()`](https://docs.ropensci.org/phylotaR/reference/list_taxrec_slots.md),
[`plot_phylota_pa()`](https://docs.ropensci.org/phylotaR/reference/plot_phylota_pa.md),
[`plot_phylota_treemap()`](https://docs.ropensci.org/phylotaR/reference/plot_phylota_treemap.md),
[`read_phylota()`](https://docs.ropensci.org/phylotaR/reference/read_phylota.md),
[`write_sqs()`](https://docs.ropensci.org/phylotaR/reference/write_sqs.md)

## Examples

``` r
data('bromeliads')
# get all the genus IDs and names
genus_ids <- get_txids(phylota = bromeliads, txids = bromeliads@txids,
                       rnk = 'genus')
genus_ids <- unique(genus_ids)
# drop empty IDs -- this happens if a given lineage has no ID for specified rank
genus_ids <- genus_ids[genus_ids != '']
# get names
(get_tx_slot(phylota = bromeliads, txid = genus_ids, slt_nm = 'scnm'))
#>              100680             2815862             2815856             2707094 
#>      "Cottendorfia"          "Karawata"  "Pseudaraeococcus"        "Wittmackia" 
#>             2184980             2184933             2184932             2184931 
#>          "Forzzaea"         "Sincoraea"       "Rokautskyia"  "Hoplocryptanthus" 
#>             1387303             1349361              796805              713961 
#>         "Lapanthus"      "Canistropsis"      "Disteganthus"         "Eduandrea" 
#>              326799              326795              326788              213064 
#>            "Portea"   "Hohenbergiopsis"          "Fernseea"          "Edmundoa" 
#>              106462              106458              106452              106447 
#>         "Ochagavia"      "Neoglaziovia"           "Greigia"      "Fascicularia" 
#>              106440              106438              106430              106424 
#>      "Deinacanthon"        "Chevaliera"        "Androlepis"    "Acanthostachys" 
#>               49536               49531               49529               49522 
#>        "Wittrockia"        "Ronnbergia"         "Quesnelia"       "Orthophytum" 
#>               49520               49512               49496               49493 
#>        "Nidularium"           "Lymania"       "Cryptanthus"         "Canistrum" 
#>               49491               49476               15119               15114 
#>       "Hohenbergia"       "Araeococcus"        "Billbergia"           "Aechmea" 
#>                4616                4614               15164              100682 
#>          "Bromelia"            "Ananas"              "Puya"     "Deuterocohnia" 
#>               49487               49526               49483               49485 
#>        "Fosterella"        "Pitcairnia"            "Dyckia"       "Encholirium" 
#>               49516              222987               15141             2821261 
#>             "Navia"         "Brewcaria"           "Hechtia"        "Bakerantha" 
#>             2821262              261216               49479              106432 
#>     "Mesoamerantha"         "Lindmania"        "Brocchinia"           "Ayensua" 
#>               49534               49518              213045             1908703 
#>           "Vriesea"        "Neoregelia"          "Werauhia"          "Lutheria" 
#>               49514              106428             1908700             1908698 
#>      "Mezobromelia"        "Alcantarea"         "Jagrantia"           "Goudaea" 
#>             1908705             2969759             1908706             1908701 
#>       "Stigmatodon"        "Hylaeaicum"           "Zizkaea"         "Josemania" 
#>             2002971               15170              294096               49489 
#>         "Waltillia"        "Tillandsia"        "Viridantha"          "Guzmania" 
#>              106471             1908553             1908702             1908697 
#>          "Racinaea"          "Wallisia"        "Lemeltonia"         "Barfussia" 
#>             1908704             1908699               15123               15137 
#>   "Pseudalcantarea"       "Gregbrownia"          "Catopsis" "Glomeropitcairnia" 
```
