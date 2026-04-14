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

---

---

## Functional Enrichment Analysis

To further understand the biological significance of the identified genes, functional enrichment analysis was performed.

### Gene Ontology (GO)

Enriched biological processes include:

- Regulation of immune effector process
- Humoral immune response
- Complement activation
- Heart contraction and cardiac conduction

---

### KEGG Pathways

Top enriched pathways:

- Complement and coagulation cascades
- Pathways in cancer
- Thyroid hormone signaling
- Peroxisome

---

## Gene–Pathway Relationships

Gene-level mapping revealed that multiple genes contribute to key biological pathways:

- Immune-related pathways (complement system)
- Cardiovascular pathways (heart contraction)
- Disease pathways (cancer and metabolism)

Some genes participate in multiple pathways, indicating their central role in disease mechanisms.

---

## Results (Extended Analysis)

### Enrichment Files
- results/go_enrichment.csv
- results/kegg_enrichment.csv

### Gene–Pathway Mapping
- results/gene_pathway_mapping.csv

### Figures
- figures/go_enrichment_plot.png
- figures/kegg_enrichment_plot.png
- figures/gene_pathway_network.png

---

## Biological Interpretation

Functional enrichment analysis revealed that ClinVar pathogenic variants are strongly associated with immune system regulation, cardiovascular function, and disease-related pathways. The enrichment of complement and coagulation cascades highlights the importance of immune and inflammatory mechanisms. Cardiac-related pathways indicate variants affecting heart function, while cancer-related pathways suggest roles in genomic instability and DNA repair.

---

## Summary

This integrative analysis highlights the functional landscape of pathogenic variants and provides insight into the molecular mechanisms underlying human diseases.
Neuro Gene Prioritization and Network Analysis

To investigate the neurological relevance of pathogenic variants, neuro-related Gene Ontology (GO) terms were extracted and associated genes were analyzed.

Top Neuro Genes
NGF
PARK7
PINK1
NTRK1
DOCK7
DISC1

These genes showed high frequency across neuro-related pathways, indicating their central role in neuronal processes.

Gene–Disease Associations

Key genes were mapped to known rare neurological disorders:

PINK1, PARK7 → Parkinson’s disease
NTRK1 → Congenital insensitivity to pain
DOCK7 → Epileptic encephalopathy
MFSD2A → Microcephaly syndrome
Network Analysis

A gene–pathway network was constructed to identify hub genes.

Hub genes identified:

NGF
PINK1
PARK7
NTRK1

These genes showed high connectivity, suggesting their importance in neurodegeneration and neuronal signaling.
