# ClinVar Pathogenic Variant Analysis (Chromosome 1)

## Objective
To analyze pathogenic variants from ClinVar and identify key disease-associated genes.

## Workflow
1. Download ClinVar VCF
2. Extract chromosome 1 variants
3. Filter pathogenic variants
4. Extract gene names
5. Identify top genes

## Key Findings
Top genes:
- USH2A
- ABCA4
- MUTYH
- RYR2

These genes are associated with retinal diseases, cancer, and cardiac disorders.

## Tools Used
- bcftools
- R (vcfR package)

## Output
- gene_counts.csv
- top_genes.png

