# Default parameters

Returns a parameter list with default parameter values.

## Usage

``` r
parameters(
  wd = ".",
  txid = character(),
  mkblstdb = "",
  blstn = "",
  v = FALSE,
  ncps = 1,
  mxnds = 1e+05,
  mdlthrs = 3000,
  mnsql = 250,
  mxsql = 2000,
  mxrtry = 100,
  mxsqs = 50000,
  mxevl = 1e-10,
  mncvrg = 51,
  btchsz = 100,
  db_only = FALSE,
  outsider = FALSE,
  srch_trm = paste0("NOT predicted[TI] ", "NOT \"whole genome shotgun\"[TI] ",
    "NOT unverified[TI] ", "NOT \"synthetic construct\"[Organism] ",
    "NOT refseq[filter] NOT TSA[Keyword]"),
  date = Sys.Date()
)
```

## Arguments

- wd:

  The working directory where all output files are saved.

- txid:

  Taxonomic group of interest, allows vectors.

- mkblstdb:

  File path to makeblastdb

- blstn:

  File path to blastn

- v:

  Print progress statements to console? Statements will always be
  printed to log.txt.

- ncps:

  The number of threads to use in the local-alignment search tool.

- mxnds:

  The maximum number of nodes descending from a taxonomic group. If
  there are more than this number, nodes at the lower taxonomic level
  are analysed.

- mdlthrs:

  'Model organism threshold'. Taxa with more sequences than this number
  will be considered model organisms and a random mdlthrs subset of
  their sequences will be downloaded.

- mnsql:

  The minimum length of sequence in nucleotide base pairs to download.

- mxsql:

  The maximum length of sequence in nucleotide base pairs to download.
  Any longer sequences will be ignored.

- mxrtry:

  The maximum number of attempts to make when downloading.

- mxsqs:

  The maximum number of sequences to BLAST in all-vs-all searches. If
  there are more sequences for a node, BLAST is performed at the lower
  taxonomic level.

- mxevl:

  The maximum E-value for a successful BLAST.

- mncvrg:

  The maximum percentile coverage defining an overlapping BLAST hit.
  Sequences with BLAST matches with lower values are not considered
  orthologous.

- btchsz:

  Batch size when querying NCBI

- db_only:

  Take sequences only from `restez` library? TRUE/FALSE. If TRUE,
  internet is still required (for taxonomic look-up) and a `restez` will
  need to be set up.

- outsider:

  Use `om..blast`? TRUE/FALSE. If TRUE, a module for running `blastn`
  will be installed and all BLAST commands will be run through it.
  `outsider` package is required.

- srch_trm:

  Sequence NCBI search term modifier. Use this parameter to change the
  default search term options. Default: avoid predicted, WGS,
  unverified, synthetic, RefSeq and Transcriptome Shotgun Assembly
  sequences.

- date:

  Date when pipeline was initiated

## Value

list

## Details

This function is NOT used to change the parameters in a folder. Use
parameters_reset() instead. The purpose of this function is to describe
the paramaters and present their default values.
