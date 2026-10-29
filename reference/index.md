# Package index

## Running

Functions for starting/stopping the phylotaR pipeline.

- [`setup()`](https://docs.ropensci.org/phylotaR/reference/setup.md) :
  Set-up parameters
- [`run()`](https://docs.ropensci.org/phylotaR/reference/run.md) : Run
  phylotaR pipeline
- [`restart()`](https://docs.ropensci.org/phylotaR/reference/restart.md)
  : Restart a phylotaR pipeline run
- [`reset()`](https://docs.ropensci.org/phylotaR/reference/reset.md) :
  Reset a phylotaR pipeline run
- [`parameters()`](https://docs.ropensci.org/phylotaR/reference/parameters.md)
  : Default parameters
- [`parameters_reset()`](https://docs.ropensci.org/phylotaR/reference/parameters_reset.md)
  : Change parameters in a working directory
- [`taxise_run()`](https://docs.ropensci.org/phylotaR/reference/taxise_run.md)
  : Run taxise stage
- [`download_run()`](https://docs.ropensci.org/phylotaR/reference/download_run.md)
  : Run download stage
- [`clusters_run()`](https://docs.ropensci.org/phylotaR/reference/clusters_run.md)
  : Run the cluster stage
- [`clusters2_run()`](https://docs.ropensci.org/phylotaR/reference/clusters2_run.md)
  : Run the cluster2 stage

## Tools

Tools for interacting with the Phylota object

- [`read_phylota()`](https://docs.ropensci.org/phylotaR/reference/read_phylota.md)
  : Generate a Phylota object in R
- [`drop_by_rank()`](https://docs.ropensci.org/phylotaR/reference/drop_by_rank.md)
  : Reduce clusters to specific rank
- [`drop_clstrs()`](https://docs.ropensci.org/phylotaR/reference/drop_clstrs.md)
  : Drop cluster records from phylota object
- [`drop_sqs()`](https://docs.ropensci.org/phylotaR/reference/drop_sqs.md)
  : Drop sequences in a cluster
- [`get_clstr_slot()`](https://docs.ropensci.org/phylotaR/reference/get_clstr_slot.md)
  : Get slot data for each cluster record
- [`get_sq_slot()`](https://docs.ropensci.org/phylotaR/reference/get_sq_slot.md)
  : Get slot data for each sequence
- [`get_tx_slot()`](https://docs.ropensci.org/phylotaR/reference/get_tx_slot.md)
  : Get slot data for each taxon record
- [`get_nsqs()`](https://docs.ropensci.org/phylotaR/reference/get_nsqs.md)
  : Count number of sequences
- [`get_ntaxa()`](https://docs.ropensci.org/phylotaR/reference/get_ntaxa.md)
  : Count number of unique taxa
- [`get_txids()`](https://docs.ropensci.org/phylotaR/reference/get_txids.md)
  : Get taxonomic IDs by rank
- [`is_txid_in_clstr()`](https://docs.ropensci.org/phylotaR/reference/is_txid_in_clstr.md)
  : Is txid in cluster?
- [`is_txid_in_sq()`](https://docs.ropensci.org/phylotaR/reference/is_txid_in_sq.md)
  : Is txid in sequence?
- [`list_clstrrec_slots()`](https://docs.ropensci.org/phylotaR/reference/list_clstrrec_slots.md)
  : List all ClstrRec slots
- [`list_ncbi_ranks()`](https://docs.ropensci.org/phylotaR/reference/list_ncbi_ranks.md)
  : List all NCBI Ranks
- [`list_seqrec_slots()`](https://docs.ropensci.org/phylotaR/reference/list_seqrec_slots.md)
  : List all SeqRec slots
- [`list_taxrec_slots()`](https://docs.ropensci.org/phylotaR/reference/list_taxrec_slots.md)
  : List all TaxRec slots
- [`calc_wrdfrq()`](https://docs.ropensci.org/phylotaR/reference/calc_wrdfrq.md)
  : Calculate word frequencies
- [`calc_mad()`](https://docs.ropensci.org/phylotaR/reference/calc_mad.md)
  : Calculate MAD score
- [`write_sqs()`](https://docs.ropensci.org/phylotaR/reference/write_sqs.md)
  : Write out sequences
- [`plot_phylota_treemap()`](https://docs.ropensci.org/phylotaR/reference/plot_phylota_treemap.md)
  : Plot treemap of Phylota object
- [`plot_phylota_pa()`](https://docs.ropensci.org/phylotaR/reference/plot_phylota_pa.md)
  : Plot presence/absence matrix
- [`get_stage_times()`](https://docs.ropensci.org/phylotaR/reference/get_stage_times.md)
  : Get run times for different stages

## Data

Example Phylota objects

- [`aotus`](https://docs.ropensci.org/phylotaR/reference/aotus.md) :
  aotus
- [`bromeliads`](https://docs.ropensci.org/phylotaR/reference/bromeliads.md)
  : bromeliads
- [`cycads`](https://docs.ropensci.org/phylotaR/reference/cycads.md) :
  cycads
- [`dragonflies`](https://docs.ropensci.org/phylotaR/reference/dragonflies.md)
  : dragonflies
- [`sturgeons`](https://docs.ropensci.org/phylotaR/reference/sturgeons.md)
  : sturgeons
- [`tardigrades`](https://docs.ropensci.org/phylotaR/reference/tardigrades.md)
  : tardigrades
- [`tinamous`](https://docs.ropensci.org/phylotaR/reference/tinamous.md)
  : tinamous
- [`yeasts`](https://docs.ropensci.org/phylotaR/reference/yeasts.md) :
  yeasts

## Classes

S4 classes

- [`as.character(`*`<ClstrArc>`*`)`](https://docs.ropensci.org/phylotaR/reference/ClstrArc-class.md)
  [`show(`*`<ClstrArc>`*`)`](https://docs.ropensci.org/phylotaR/reference/ClstrArc-class.md)
  [`print(`*`<ClstrArc>`*`)`](https://docs.ropensci.org/phylotaR/reference/ClstrArc-class.md)
  [`str(`*`<ClstrArc>`*`)`](https://docs.ropensci.org/phylotaR/reference/ClstrArc-class.md)
  [`summary(`*`<ClstrArc>`*`)`](https://docs.ropensci.org/phylotaR/reference/ClstrArc-class.md)
  [`` `[[`( ``*`<ClstrArc>`*`,`*`<character>`*`)`](https://docs.ropensci.org/phylotaR/reference/ClstrArc-class.md)
  [`` `[`( ``*`<ClstrArc>`*`,`*`<character>`*`,`*`<missing>`*`,`*`<missing>`*`)`](https://docs.ropensci.org/phylotaR/reference/ClstrArc-class.md)
  : Cluster record archive
- [`as.character(`*`<ClstrRec>`*`)`](https://docs.ropensci.org/phylotaR/reference/ClstrRec-class.md)
  [`show(`*`<ClstrRec>`*`)`](https://docs.ropensci.org/phylotaR/reference/ClstrRec-class.md)
  [`print(`*`<ClstrRec>`*`)`](https://docs.ropensci.org/phylotaR/reference/ClstrRec-class.md)
  [`str(`*`<ClstrRec>`*`)`](https://docs.ropensci.org/phylotaR/reference/ClstrRec-class.md)
  [`summary(`*`<ClstrRec>`*`)`](https://docs.ropensci.org/phylotaR/reference/ClstrRec-class.md)
  : Cluster record
- [`as.character(`*`<Node>`*`)`](https://docs.ropensci.org/phylotaR/reference/Node-class.md)
  [`show(`*`<Node>`*`)`](https://docs.ropensci.org/phylotaR/reference/Node-class.md)
  [`print(`*`<Node>`*`)`](https://docs.ropensci.org/phylotaR/reference/Node-class.md)
  [`summary(`*`<Node>`*`)`](https://docs.ropensci.org/phylotaR/reference/Node-class.md)
  [`` `[`( ``*`<Node>`*`,`*`<character>`*`,`*`<missing>`*`,`*`<missing>`*`)`](https://docs.ropensci.org/phylotaR/reference/Node-class.md)
  : Node-class
- [`as.character(`*`<Phylota>`*`)`](https://docs.ropensci.org/phylotaR/reference/Phylota-class.md)
  [`show(`*`<Phylota>`*`)`](https://docs.ropensci.org/phylotaR/reference/Phylota-class.md)
  [`print(`*`<Phylota>`*`)`](https://docs.ropensci.org/phylotaR/reference/Phylota-class.md)
  [`str(`*`<Phylota>`*`)`](https://docs.ropensci.org/phylotaR/reference/Phylota-class.md)
  [`summary(`*`<Phylota>`*`)`](https://docs.ropensci.org/phylotaR/reference/Phylota-class.md)
  [`` `[[`( ``*`<Phylota>`*`,`*`<character>`*`)`](https://docs.ropensci.org/phylotaR/reference/Phylota-class.md)
  : Phylota object
- [`as.character(`*`<SeqArc>`*`)`](https://docs.ropensci.org/phylotaR/reference/SeqArc-class.md)
  [`show(`*`<SeqArc>`*`)`](https://docs.ropensci.org/phylotaR/reference/SeqArc-class.md)
  [`print(`*`<SeqArc>`*`)`](https://docs.ropensci.org/phylotaR/reference/SeqArc-class.md)
  [`str(`*`<SeqArc>`*`)`](https://docs.ropensci.org/phylotaR/reference/SeqArc-class.md)
  [`summary(`*`<SeqArc>`*`)`](https://docs.ropensci.org/phylotaR/reference/SeqArc-class.md)
  [`` `[[`( ``*`<SeqArc>`*`,`*`<character>`*`)`](https://docs.ropensci.org/phylotaR/reference/SeqArc-class.md)
  [`` `[`( ``*`<SeqArc>`*`,`*`<character>`*`,`*`<missing>`*`,`*`<missing>`*`)`](https://docs.ropensci.org/phylotaR/reference/SeqArc-class.md)
  : Sequence record archive
- [`as.character(`*`<SeqRec>`*`)`](https://docs.ropensci.org/phylotaR/reference/SeqRec-class.md)
  [`show(`*`<SeqRec>`*`)`](https://docs.ropensci.org/phylotaR/reference/SeqRec-class.md)
  [`print(`*`<SeqRec>`*`)`](https://docs.ropensci.org/phylotaR/reference/SeqRec-class.md)
  [`str(`*`<SeqRec>`*`)`](https://docs.ropensci.org/phylotaR/reference/SeqRec-class.md)
  [`summary(`*`<SeqRec>`*`)`](https://docs.ropensci.org/phylotaR/reference/SeqRec-class.md)
  : Sequence record
- [`as.character(`*`<TaxDict>`*`)`](https://docs.ropensci.org/phylotaR/reference/TaxDict-class.md)
  [`show(`*`<TaxDict>`*`)`](https://docs.ropensci.org/phylotaR/reference/TaxDict-class.md)
  [`print(`*`<TaxDict>`*`)`](https://docs.ropensci.org/phylotaR/reference/TaxDict-class.md)
  [`str(`*`<TaxDict>`*`)`](https://docs.ropensci.org/phylotaR/reference/TaxDict-class.md)
  [`summary(`*`<TaxDict>`*`)`](https://docs.ropensci.org/phylotaR/reference/TaxDict-class.md)
  : Taxonomic record dictionary
- [`as.character(`*`<TaxRec>`*`)`](https://docs.ropensci.org/phylotaR/reference/TaxRec-class.md)
  [`show(`*`<TaxRec>`*`)`](https://docs.ropensci.org/phylotaR/reference/TaxRec-class.md)
  [`print(`*`<TaxRec>`*`)`](https://docs.ropensci.org/phylotaR/reference/TaxRec-class.md)
  [`str(`*`<TaxRec>`*`)`](https://docs.ropensci.org/phylotaR/reference/TaxRec-class.md)
  [`summary(`*`<TaxRec>`*`)`](https://docs.ropensci.org/phylotaR/reference/TaxRec-class.md)
  : Taxonomic record
- [`` `[[`( ``*`<TreeMan>`*`,`*`<character>`*`)`](https://docs.ropensci.org/phylotaR/reference/TreeMan-class.md)
  [`` `[`( ``*`<TreeMan>`*`,`*`<character>`*`,`*`<missing>`*`,`*`<missing>`*`)`](https://docs.ropensci.org/phylotaR/reference/TreeMan-class.md)
  [`as.character(`*`<TreeMan>`*`)`](https://docs.ropensci.org/phylotaR/reference/TreeMan-class.md)
  [`show(`*`<TreeMan>`*`)`](https://docs.ropensci.org/phylotaR/reference/TreeMan-class.md)
  [`print(`*`<TreeMan>`*`)`](https://docs.ropensci.org/phylotaR/reference/TreeMan-class.md)
  [`str(`*`<TreeMan>`*`)`](https://docs.ropensci.org/phylotaR/reference/TreeMan-class.md)
  [`summary(`*`<TreeMan>`*`)`](https://docs.ropensci.org/phylotaR/reference/TreeMan-class.md)
  [`cTrees(`*`<TreeMan>`*`)`](https://docs.ropensci.org/phylotaR/reference/TreeMan-class.md)
  : TreeMan-class
- [`cTrees(`*`<TreeMen>`*`)`](https://docs.ropensci.org/phylotaR/reference/TreeMen-class.md)
  [`` `[[`( ``*`<TreeMen>`*`,`*`<ANY>`*`)`](https://docs.ropensci.org/phylotaR/reference/TreeMen-class.md)
  [`` `[`( ``*`<TreeMen>`*`,`*`<character>`*`,`*`<missing>`*`,`*`<missing>`*`)`](https://docs.ropensci.org/phylotaR/reference/TreeMen-class.md)
  [`as.character(`*`<TreeMen>`*`)`](https://docs.ropensci.org/phylotaR/reference/TreeMen-class.md)
  [`show(`*`<TreeMen>`*`)`](https://docs.ropensci.org/phylotaR/reference/TreeMen-class.md)
  [`str(`*`<TreeMen>`*`)`](https://docs.ropensci.org/phylotaR/reference/TreeMen-class.md)
  [`print(`*`<TreeMen>`*`)`](https://docs.ropensci.org/phylotaR/reference/TreeMen-class.md)
  [`summary(`*`<TreeMen>`*`)`](https://docs.ropensci.org/phylotaR/reference/TreeMen-class.md)
  : TreeMen-class
- [`multiPhylo-class`](https://docs.ropensci.org/phylotaR/reference/multiPhylo-class.md)
  [`multiPhylo`](https://docs.ropensci.org/phylotaR/reference/multiPhylo-class.md)
  : multiPhylo class
- [`phylo-class`](https://docs.ropensci.org/phylotaR/reference/phylo-class.md)
  [`phylo`](https://docs.ropensci.org/phylotaR/reference/phylo-class.md)
  : phylo class

## Taxise (private)

Internal functions for running the taxise stageuse `phylotaR:::` to
access.

- [`rank_get()`](https://docs.ropensci.org/phylotaR/reference/rank_get.md)
  : Get rank
- [`descendants_get()`](https://docs.ropensci.org/phylotaR/reference/descendants_get.md)
  : Get descendants
- [`sqs_count()`](https://docs.ropensci.org/phylotaR/reference/sqs_count.md)
  : Count number of sequences for txid
- [`clade_select()`](https://docs.ropensci.org/phylotaR/reference/clade_select.md)
  : Get all node IDs that will be processed
- [`txnds_count()`](https://docs.ropensci.org/phylotaR/reference/txnds_count.md)
  : Count number of descending taxonomic nodes
- [`txids_get()`](https://docs.ropensci.org/phylotaR/reference/txids_get.md)
  : Searches for descendant taxonomic IDs
- [`parent_get()`](https://docs.ropensci.org/phylotaR/reference/parent_get.md)
  : Get taxonomic parent
- [`tax_download()`](https://docs.ropensci.org/phylotaR/reference/tax_download.md)
  : Download taxonomic records
- [`taxdict_gen()`](https://docs.ropensci.org/phylotaR/reference/taxdict_gen.md)
  : Generate taxonomic dictionary
- [`taxtree_gen()`](https://docs.ropensci.org/phylotaR/reference/taxtree_gen.md)
  : Generate taxonomic tree

## Download (private)

Internal functions for running the download stageuse `phylotaR:::` to
access.

- [`searchterm_gen()`](https://docs.ropensci.org/phylotaR/reference/searchterm_gen.md)
  : Construct GenBank Search Term
- [`seq_download()`](https://docs.ropensci.org/phylotaR/reference/seq_download.md)
  : Download sequences for txids
- [`seqarc_gen()`](https://docs.ropensci.org/phylotaR/reference/seqarc_gen.md)
  : Generate sequence archive
- [`seqrec_augment()`](https://docs.ropensci.org/phylotaR/reference/seqrec_augment.md)
  : Augment sequence records list
- [`seqrec_convert()`](https://docs.ropensci.org/phylotaR/reference/seqrec_convert.md)
  : Convert raw Entrez gb text record to SeqRecs
- [`seqrec_gen()`](https://docs.ropensci.org/phylotaR/reference/seqrec_gen.md)
  : Generate sequence record
- [`seqrec_get()`](https://docs.ropensci.org/phylotaR/reference/seqrec_get.md)
  : seqrec_get
- [`hierarchic_download()`](https://docs.ropensci.org/phylotaR/reference/hierarchic_download.md)
  : Hierarchically get sequences for a txid
- [`sids_get()`](https://docs.ropensci.org/phylotaR/reference/sids_get.md)
  : Return random set of sequence IDs
- [`outfmt_get()`](https://docs.ropensci.org/phylotaR/reference/outfmt_get.md)
  : Determine 'outformat' format

## Cluster (private)

Internal functions for running the cluster stageuse `phylotaR:::` to
access.

- [`blast_clstr()`](https://docs.ropensci.org/phylotaR/reference/blast_clstr.md)
  : Cluster BLAST Results
- [`blast_filter()`](https://docs.ropensci.org/phylotaR/reference/blast_filter.md)
  : Filter BLAST results
- [`blast_sqs()`](https://docs.ropensci.org/phylotaR/reference/blast_sqs.md)
  : BLAST All vs All
- [`blastdb_gen()`](https://docs.ropensci.org/phylotaR/reference/blastdb_gen.md)
  : Generate a BLAST database
- [`blastn_run()`](https://docs.ropensci.org/phylotaR/reference/blastn_run.md)
  : Launch blastn
- [`clstr_all()`](https://docs.ropensci.org/phylotaR/reference/clstr_all.md)
  : Hierarchically cluster all sequences of a txid
- [`clstr_direct()`](https://docs.ropensci.org/phylotaR/reference/clstr_direct.md)
  : Cluster sequences directly associated with txid
- [`clstr_sqs()`](https://docs.ropensci.org/phylotaR/reference/clstr_sqs.md)
  : Identify clusters from sequences
- [`clstr_subtree()`](https://docs.ropensci.org/phylotaR/reference/clstr_subtree.md)
  : Cluster all sequences descending from a txid
- [`clstrarc_gen()`](https://docs.ropensci.org/phylotaR/reference/clstrarc_gen.md)
  : Generate cluster archive container class
- [`clstrarc_join()`](https://docs.ropensci.org/phylotaR/reference/clstrarc_join.md)
  : Join two cluster archive
- [`clstrrec_gen()`](https://docs.ropensci.org/phylotaR/reference/clstrrec_gen.md)
  : Generate list of clusters
- [`clstrs_calc()`](https://docs.ropensci.org/phylotaR/reference/clstrs_calc.md)
  : Calculate clusters for all sequences in wd

## Cluster2 (private)

Internal functions for running the cluster2 stageuse `phylotaR:::` to
access.

- [`seeds_blast()`](https://docs.ropensci.org/phylotaR/reference/seeds_blast.md)
  : BLAST seed sequences
- [`clstr2_calc()`](https://docs.ropensci.org/phylotaR/reference/clstr2_calc.md)
  : Cluster sets of clusters identified in cluster stage
- [`clstrs_join()`](https://docs.ropensci.org/phylotaR/reference/clstrs_join.md)
  : Join clusters for merging
- [`clstrs_merge()`](https://docs.ropensci.org/phylotaR/reference/clstrs_merge.md)
  : Merge joined clusters
- [`clstrs_renumber()`](https://docs.ropensci.org/phylotaR/reference/clstrs_renumber.md)
  : Renumber cluster IDs

## treeman orgin or example datasets

Docs from including treeman

- [`TreeMan-to-phylo`](https://docs.ropensci.org/phylotaR/reference/TreeMan-to-phylo.md)
  : Convert TreeMan to phylo
- [`TreeMen-to-multiPhylo`](https://docs.ropensci.org/phylotaR/reference/TreeMen-to-multiPhylo.md)
  : Convert TreeMen to multiPhylo
- [`addClade()`](https://docs.ropensci.org/phylotaR/reference/addClade.md)
  : Add clade to tree
- [`addNdmtrx()`](https://docs.ropensci.org/phylotaR/reference/addNdmtrx.md)
  : Add node matrix to a tree
- [`addTip()`](https://docs.ropensci.org/phylotaR/reference/addTip.md) :
  Add tip to a tree
- [`birds`](https://docs.ropensci.org/phylotaR/reference/birds.md) :
  birds
- [`blncdTree()`](https://docs.ropensci.org/phylotaR/reference/blncdTree.md)
  : Generate a balanced tree
- [`cTrees()`](https://docs.ropensci.org/phylotaR/reference/cTrees.md) :
  cTrees
- [`calcDstBLD()`](https://docs.ropensci.org/phylotaR/reference/calcDstBLD.md)
  : Calculate the BLD between two trees
- [`calcDstMtrx()`](https://docs.ropensci.org/phylotaR/reference/calcDstMtrx.md)
  : Calculate the distance matrix
- [`calcDstRF()`](https://docs.ropensci.org/phylotaR/reference/calcDstRF.md)
  : Calculate the Robinson-Foulds distance between two trees
- [`calcDstTrp()`](https://docs.ropensci.org/phylotaR/reference/calcDstTrp.md)
  : Calculate the triplet distance between two trees
- [`calcFrPrp()`](https://docs.ropensci.org/phylotaR/reference/calcFrPrp.md)
  : Calculate evolutionary distinctness
- [`calcNdBlnc()`](https://docs.ropensci.org/phylotaR/reference/calcNdBlnc.md)
  : Calculate the balance of a node
- [`calcNdsBlnc()`](https://docs.ropensci.org/phylotaR/reference/calcNdsBlnc.md)
  : Calculate the balances of all nodes
- [`calcOvrlp()`](https://docs.ropensci.org/phylotaR/reference/calcOvrlp.md)
  : Calculate phylogenetic overlap
- [`calcPhyDv()`](https://docs.ropensci.org/phylotaR/reference/calcPhyDv.md)
  : Calculate phylogenetic diversity
- [`calcPrtFrPrp()`](https://docs.ropensci.org/phylotaR/reference/calcPrtFrPrp.md)
  : Calculate evolutionary distinctness for part of tree
- [`checkNdlst()`](https://docs.ropensci.org/phylotaR/reference/checkNdlst.md)
  : Check if ndlst is correct
- [`checkTreeMen()`](https://docs.ropensci.org/phylotaR/reference/checkTreeMen.md)
  : Check if trees are correct
- [`fastCheckTreeMan()`](https://docs.ropensci.org/phylotaR/reference/fastCheckTreeMan.md)
  : Check if tree is correct, fast!
- [`getAge()`](https://docs.ropensci.org/phylotaR/reference/getAge.md) :
  Get age of tree
- [`getBiprts()`](https://docs.ropensci.org/phylotaR/reference/getBiprts.md)
  : Get the sets of labels for each bipartition in tree
- [`getCnnctdNds()`](https://docs.ropensci.org/phylotaR/reference/getCnnctdNds.md)
  : Get all nodes connected by given tips
- [`getDcsd()`](https://docs.ropensci.org/phylotaR/reference/getDcsd.md)
  : Get extinct tips from a tree
- [`getLvng()`](https://docs.ropensci.org/phylotaR/reference/getLvng.md)
  : Get extant tips from a tree
- [`getNdAge()`](https://docs.ropensci.org/phylotaR/reference/getNdAge.md)
  : Get age
- [`getNdKids()`](https://docs.ropensci.org/phylotaR/reference/getNdKids.md)
  : Get children IDs
- [`getNdLng()`](https://docs.ropensci.org/phylotaR/reference/getNdLng.md)
  : Get lineage
- [`getNdPD()`](https://docs.ropensci.org/phylotaR/reference/getNdPD.md)
  : Get phylogenetic diversity of node
- [`getNdPrdst()`](https://docs.ropensci.org/phylotaR/reference/getNdPrdst.md)
  : Get pre-distance
- [`getNdPrids()`](https://docs.ropensci.org/phylotaR/reference/getNdPrids.md)
  : Get pre-nodes to root
- [`getNdPtids()`](https://docs.ropensci.org/phylotaR/reference/getNdPtids.md)
  : Get post-nodes to tips
- [`getNdSlt()`](https://docs.ropensci.org/phylotaR/reference/getNdSlt.md)
  : Get a node slot
- [`getNdSstr()`](https://docs.ropensci.org/phylotaR/reference/getNdSstr.md)
  : Get sister id
- [`getNdsAge()`](https://docs.ropensci.org/phylotaR/reference/getNdsAge.md)
  : Get ages for multiple nodes
- [`getNdsFrmTxnyms()`](https://docs.ropensci.org/phylotaR/reference/getNdsFrmTxnyms.md)
  : Get IDs for nodes represented txnyms
- [`getNdsKids()`](https://docs.ropensci.org/phylotaR/reference/getNdsKids.md)
  : Get children IDs for multiple nodes
- [`getNdsLng()`](https://docs.ropensci.org/phylotaR/reference/getNdsLng.md)
  : Get lineage for multiple nodes
- [`getNdsPD()`](https://docs.ropensci.org/phylotaR/reference/getNdsPD.md)
  : Get phylogenetic diversities of nodes
- [`getNdsPrdst()`](https://docs.ropensci.org/phylotaR/reference/getNdsPrdst.md)
  : Get pre-distances
- [`getNdsPrids()`](https://docs.ropensci.org/phylotaR/reference/getNdsPrids.md)
  : Get pre-nodes for multiple nodes
- [`getNdsPtids()`](https://docs.ropensci.org/phylotaR/reference/getNdsPtids.md)
  : Get post-nodes to tips for multiple nodes
- [`getNdsSlt()`](https://docs.ropensci.org/phylotaR/reference/getNdsSlt.md)
  : Get a node slot for multiple nodes
- [`getNdsSstr()`](https://docs.ropensci.org/phylotaR/reference/getNdsSstr.md)
  : Get sister id
- [`getOtgrp()`](https://docs.ropensci.org/phylotaR/reference/getOtgrp.md)
  : Get outgroup
- [`getPath()`](https://docs.ropensci.org/phylotaR/reference/getPath.md)
  : Get path between nodes
- [`getPrnt()`](https://docs.ropensci.org/phylotaR/reference/getPrnt.md)
  : Get parent
- [`getSpnAge()`](https://docs.ropensci.org/phylotaR/reference/getSpnAge.md)
  : Get age range
- [`getSpnsAge()`](https://docs.ropensci.org/phylotaR/reference/getSpnsAge.md)
  : Get age ranges for multiple nodes
- [`getSubtree()`](https://docs.ropensci.org/phylotaR/reference/getSubtree.md)
  : Get subtree
- [`getUnqNds()`](https://docs.ropensci.org/phylotaR/reference/getUnqNds.md)
  : Get unique nodes represented by tips
- [`isUltrmtrc()`](https://docs.ropensci.org/phylotaR/reference/isUltrmtrc.md)
  : Is tree ultrametric?
- [`list-to-TreeMen`](https://docs.ropensci.org/phylotaR/reference/list-to-TreeMen.md)
  : Convert list to a TreeMen
- [`loadTreeMan()`](https://docs.ropensci.org/phylotaR/reference/loadTreeMan.md)
  : Load a TreeMan object in serialization format
- [`mammals`](https://docs.ropensci.org/phylotaR/reference/mammals.md) :
  mammals
- [`multiPhylo-to-TreeMen`](https://docs.ropensci.org/phylotaR/reference/multiPhylo-to-TreeMen.md)
  : Convert multiPhylo to TreeMen
- [`phylo-to-TreeMan`](https://docs.ropensci.org/phylotaR/reference/phylo-to-TreeMan.md)
  : Convert phylo to TreeMan
- [`pinTips()`](https://docs.ropensci.org/phylotaR/reference/pinTips.md)
  : Pin tips to a tree
- [`plants`](https://docs.ropensci.org/phylotaR/reference/plants.md) :
  plants
- [`pstMnp()`](https://docs.ropensci.org/phylotaR/reference/pstMnp.md) :
  Update prinds and tinds
- [`randTree()`](https://docs.ropensci.org/phylotaR/reference/randTree.md)
  : Generate a random tree
- [`readTree()`](https://docs.ropensci.org/phylotaR/reference/readTree.md)
  : Read a Newick tree
- [`readTrmn()`](https://docs.ropensci.org/phylotaR/reference/readTrmn.md)
  : Read a .trmn tree
- [`rmClade()`](https://docs.ropensci.org/phylotaR/reference/rmClade.md)
  : Remove a clade from a tree
- [`rmNdmtrx()`](https://docs.ropensci.org/phylotaR/reference/rmNdmtrx.md)
  : Remove node matrix
- [`rmNodes()`](https://docs.ropensci.org/phylotaR/reference/rmNodes.md)
  : Remove nodes from a tree
- [`rmOtherSlt()`](https://docs.ropensci.org/phylotaR/reference/rmOtherSlt.md)
  : Remove a user-defined slot
- [`rmTips()`](https://docs.ropensci.org/phylotaR/reference/rmTips.md) :
  Remove tips from a tree
- [`saveTreeMan()`](https://docs.ropensci.org/phylotaR/reference/saveTreeMan.md)
  : Save a TreeMan object in serialization format
- [`searchTxnyms()`](https://docs.ropensci.org/phylotaR/reference/searchTxnyms.md)
  : Get node labels based on online taxonomic database
- [`setAge()`](https://docs.ropensci.org/phylotaR/reference/setAge.md) :
  Set the age of a tree
- [`setNdID()`](https://docs.ropensci.org/phylotaR/reference/setNdID.md)
  : Set the ID of a node
- [`setNdOther()`](https://docs.ropensci.org/phylotaR/reference/setNdOther.md)
  : Set a user defined slot
- [`setNdSpn()`](https://docs.ropensci.org/phylotaR/reference/setNdSpn.md)
  : Set the branch length of a specific node
- [`setNdsID()`](https://docs.ropensci.org/phylotaR/reference/setNdsID.md)
  : Set the IDs of multiple nodes
- [`setNdsOther()`](https://docs.ropensci.org/phylotaR/reference/setNdsOther.md)
  : Set a user defined slot for multiple nodes
- [`setNdsSpn()`](https://docs.ropensci.org/phylotaR/reference/setNdsSpn.md)
  : Set the branch lengths of specific nodes
- [`setPD()`](https://docs.ropensci.org/phylotaR/reference/setPD.md) :
  Set the phylogenetic diversity
- [`setTxnyms()`](https://docs.ropensci.org/phylotaR/reference/setTxnyms.md)
  : Set the txnym slots in a tree
- [`taxaResolve()`](https://docs.ropensci.org/phylotaR/reference/taxaResolve.md)
  : Resolve taxonmic names online
- [`twoer()`](https://docs.ropensci.org/phylotaR/reference/twoer.md) :
  Generate a tree of two tips
- [`ultrTree()`](https://docs.ropensci.org/phylotaR/reference/ultrTree.md)
  : Make tree ultrametric
- [`unblncdTree()`](https://docs.ropensci.org/phylotaR/reference/unblncdTree.md)
  : Generate an unbalanced tree
- [`updateSlts()`](https://docs.ropensci.org/phylotaR/reference/updateSlts.md)
  : Update tree slots after manipulation
- [`writeTree()`](https://docs.ropensci.org/phylotaR/reference/writeTree.md)
  : Write a Newick tree
- [`writeTrmn()`](https://docs.ropensci.org/phylotaR/reference/writeTrmn.md)
  : Write a .trmn tree

## Misc (private)

Miscellaneous internal functionsuse `phylotaR:::` to access.

- [`blast_setup()`](https://docs.ropensci.org/phylotaR/reference/blast_setup.md)
  : Ensures NCBI BLAST tools are installed
- [`download_obj_check()`](https://docs.ropensci.org/phylotaR/reference/download_obj_check.md)
  : Check an object returned from rentrez function
- [`safely_connect()`](https://docs.ropensci.org/phylotaR/reference/safely_connect.md)
  : Safely run rentrez function
- [`search_and_cache()`](https://docs.ropensci.org/phylotaR/reference/search_and_cache.md)
  : Run rentrez function and cache results
- [`batcher()`](https://docs.ropensci.org/phylotaR/reference/batcher.md)
  : Download in batches
- [`info()`](https://docs.ropensci.org/phylotaR/reference/info.md) :
  Write info message to log
- [`error()`](https://docs.ropensci.org/phylotaR/reference/error.md) :
  Write error message to log
- [`warn()`](https://docs.ropensci.org/phylotaR/reference/warn.md) :
  Write warning message to log
- [`blastcache_load()`](https://docs.ropensci.org/phylotaR/reference/blastcache_load.md)
  : Load BLAST results from cache
- [`blastcache_save()`](https://docs.ropensci.org/phylotaR/reference/blastcache_save.md)
  : Save BLAST results to cache
- [`sids_check()`](https://docs.ropensci.org/phylotaR/reference/sids_check.md)
  : Check if sids exist
- [`sids_load()`](https://docs.ropensci.org/phylotaR/reference/sids_load.md)
  : Load sids from cache
- [`sids_save()`](https://docs.ropensci.org/phylotaR/reference/sids_save.md)
  : Save sids to cache
- [`cache_rm()`](https://docs.ropensci.org/phylotaR/reference/cache_rm.md)
  : Delete a cache
- [`cache_setup()`](https://docs.ropensci.org/phylotaR/reference/cache_setup.md)
  : Set-up a cache
- [`sqs_save()`](https://docs.ropensci.org/phylotaR/reference/sqs_save.md)
  : Save sequences to cache
- [`ncbicache_load()`](https://docs.ropensci.org/phylotaR/reference/ncbicache_load.md)
  : Retrieve cached NCBI query
- [`ncbicache_save()`](https://docs.ropensci.org/phylotaR/reference/ncbicache_save.md)
  : Save NCBI query result to cache
- [`stages_run()`](https://docs.ropensci.org/phylotaR/reference/stages_run.md)
  : Sequentially run each stage
- [`stage_args_check()`](https://docs.ropensci.org/phylotaR/reference/stage_args_check.md)
  : Check stage arguments
- [`mk_txid_in_sq_mtrx()`](https://docs.ropensci.org/phylotaR/reference/mk_txid_in_sq_mtrx.md)
  : Return matrix of txid in sequence
- [`obj_check()`](https://docs.ropensci.org/phylotaR/reference/obj_check.md)
  : Check if an object exists
- [`obj_load()`](https://docs.ropensci.org/phylotaR/reference/obj_load.md)
  : Load a named object from the cache
- [`obj_save()`](https://docs.ropensci.org/phylotaR/reference/obj_save.md)
  : Save a named object in the cache
- [`summary_phylota()`](https://docs.ropensci.org/phylotaR/reference/summary_phylota.md)
  : Summarise clusters in Phylota Table
- [`parameters_load()`](https://docs.ropensci.org/phylotaR/reference/parameters_load.md)
  : Load parameters from cache
- [`progress_init()`](https://docs.ropensci.org/phylotaR/reference/progress_init.md)
  : Initialise progress list in cache
- [`progress_read()`](https://docs.ropensci.org/phylotaR/reference/progress_read.md)
  : Read the progress from cache
- [`progress_reset()`](https://docs.ropensci.org/phylotaR/reference/progress_reset.md)
  : Reset progress
- [`progress_save()`](https://docs.ropensci.org/phylotaR/reference/progress_save.md)
  : Save current progress
- [`cmdln()`](https://docs.ropensci.org/phylotaR/reference/cmdln.md) :
  Run a command via terminal/command prompt
- [`update_phylota()`](https://docs.ropensci.org/phylotaR/reference/update_phylota.md)
  : Update slots
- [`parameters_setup()`](https://docs.ropensci.org/phylotaR/reference/parameters_setup.md)
  : Set Up Parameters
- [`clstrs_save()`](https://docs.ropensci.org/phylotaR/reference/clstrs_save.md)
  : Save clusters to cache
- [`gb_extract()`](https://docs.ropensci.org/phylotaR/reference/gb_extract.md)
  : Extract elements from a raw GenBank record
- [`rawseqrec_breakdown()`](https://docs.ropensci.org/phylotaR/reference/rawseqrec_breakdown.md)
  : Breakdown a sequence record into its features
