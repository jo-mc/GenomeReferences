# GenomeReferences

Best GRCh38 reference?

Reference genome(s) used for alignment:

[GRCh38-GIABv3,GRCh38_GIABv3_no_alt_analysis_set_maskedGRC_decoys_MAP2K3_KMT2C_KCNJ18.fasta.gz]

https://ftp-trace.ncbi.nlm.nih.gov/ReferenceSamples/giab/release/references/GRCh38/

## The GRCh38-GIABv3 reference:
- starts with the GRC reference for hg38 GCA_000001405.15_GRCh38_no_alt_analysis_set.fasta.gz,
standard GRCh38 primary assembly with the ALT contigs removed, so reads aren't split
across alternate haplotypes,
- hard masks false duplications and contaminating non-human sequence using GCA_000001405.15_GRCh38_GRC_exclusions.bed
- includes decoy sequence for three genes MAP2K3, KMT2C and KCNJ18 that have
known false duplication/assembly issues in GRCh38 are patched/corrected, which
improves variant calling specifically in those medically relevant genes.
- hard masks non-ACTGN bases

