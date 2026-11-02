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

### the latest iteration:
 https://ftp-trace.ncbi.nlm.nih.gov/ReferenceSamples/giab/release/references/GRCh38/GRCh38_GIABv3_no_alt_analysis_set_maskedGRC_decoys_MAP2K3_KMT2C_KCNJ18.fasta.gz

See readme for more info:  
https://ftp-trace.ncbi.nlm.nih.gov/ReferenceSamples/giab/release/references/README_GIAB_Mapping_References.md

 ```
In 2023, we further refined the GRCh38 reference:

Full name: `GRCh38_GIABv3_no_alt_analysis_set_maskedGRC_decoys_MAP2K3_KMT2C_KCNJ18.fasta.gz`  
Abbreviated name for inclusion in filenames: GRCh38-GIABv3

The refined GIABv3 GRCh38 corrects false duplication and false collapse errors 
in GRCh38 relative to T2T-CHM13 described in the [FixItFelix paper](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-023-02863-7). 
The false duplications are also described in this [GRC blog post](http://genomeref.blogspot.com/2021/07/one-of-these-things-doest-belong.html).  
We have masked the GRC-identified GRCh38 false duplications and added decoy sequences 
for collapsed genic regions identified in the FixItFelix paper.  The result is 
very similar to the FixItFelix modified reference with the reduced decoy set, 
but GIABv3 uses the final boundaries of false duplications recommended by GRC, 
as well as non-human contaminating sequence. Further, non-ACTGN contained in the 
reference are hard masked as Ns. Like the other GIAB GRCh38 references, we start 
with the `GCA_000001405.15_GRCh38_no_alt_analysis_set` reference that does not 
include ALT loci or the GRCh38d1 decoy.  Information on how this reference was
generated can be found here, https://ftp-trace.ncbi.nlm.nih.gov/ReferenceSamples/giab/release/references/GRCh38/GRCh38_reference_update_to_GIABv3.ipynb
```
