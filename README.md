# Understanding Bivalve Gametogenesis

Comparative transcriptomics for bivalve gametogenesis

### Subdirectory Info

`code/` contains code

-   `01-retrievegenomes.Rmd` downloads refseq annotated *Bivalvia* genomes from NCBI

-   `02-blastoncds.Rmd` runs tblastn to find genes associated with gamete generation (uses gamete generation genes containing fasta as querey, and cds genome files for bivalve species as database)

-   `03-phyluce.Rmd` follows the [phyluce III tutorial](https://phyluce.readthedocs.io/en/latest/tutorials/tutorial-3.html) for harvesting UCE loci from genomes

`data/` contains data

-   `data/SwissProt-GO:0007276.fa` fasta files of all NCBI genes under gamete generation GO term

-   `data/genome_info-20250407.tsv` NCBI table with metainfo on the refseq annotated *Bivalvia* genomes

-   `data/genomes_refseq/` has the ncbi output sequences

-   `data/phyluce/` contains all the data related to phyluce including:

    -   .2bit genome files: `GCF_#########/GCF_#########.2bit`

    -   UCE baits used: `Baits_Bivalve_v1.fasta` and `Baits_Bivalve_v2.fasta`

    -   the lastz uce hit output files: `v1-genome-lastz` and `v2-genome-lastz`

    -   fasta uce hit output files: `v1-genome-fasta` and `v2-genome-fasta`

    -   uces from baits: `uce_frombaits_v1` and `uce_frombaits_v2`

    -   logs from running phyluce: `phyluce.log` (v1 error log) and `phyluce_v2.log` (v2 error log), `phyluce_probe_run_multiple_lastzs_sqlite.log` (lastz run log), and `phyluce_probe_slice_sequence_from_genomes` (lastz to fasta run log)

    -   comparison of lastz and fasta bait v1 and bait v2 UCE hits: `sequence_summary.csv`

`output/` stores outputs

-   `blastout/GCF_########.tab` : blast output

-   `blastout/GCF_########_with_headers.tab` : blast output with headers

-   `blastout/GCF_########_sep.tab` : blast output with seperated entry column (to obtain SPID)

-   `GCF_########_SPID.txt` : SwissProt ID / UniProt Accession numbers from Blast Output

-   `GCF_########_uniprotout` : UniProt Table for that species

-   `GCF_########_annotation.tab` : combination of BLAST table and UniProt Table for that species

-   `genelist_GCF_#########.csv` : BLAST table and UniProt table table, but only keeps relevant columns (for brevity)

`visuals/` stores visuals

`blastdb/` is the blast database created when running blast
