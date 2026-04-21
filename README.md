# ClinVar Pathogenic Variant Analysis & Rare Neurodevelopmental Gene Prioritization (Chromosome 1)

## Overview
This project identifies rare disease-associated genes by integrating ClinVar pathogenic variants with functional enrichment, network analysis, and population-aware prioritization.
The pipeline highlights genes with both known pathogenic impact and high diagnostic uncertainty — ideal candidates for functional validation in model organisms.
---

## Objectives
- Extract pathogenic variants from ClinVar
- Map variants to genes
- Identify biologically relevant pathways
- Prioritize rare neuro-associated candidate genes
- Infer gene–disease associations
- Incorporate VUS burden to highlight clinically relevant but under-characterized genes
---

## Workflow

### 1. Variant Extraction
- Source: ClinVar VCF (GRCh38)
- Filter: Pathogenic variants
- Chromosome: 1

### 2. Variant–Gene Mapping
- Extracted gene annotations
- Cleaned multi-gene entries
- Generated gene frequency table

### 3. Functional Enrichment
- Tool: Enrichr
- Databases:
  - GO Biological Process
  - KEGG Pathways

### 4. Neuro-Specific Filtering
- Selected pathways related to:
  - Neurodevelopment
  - Neurodegeneration
  - Brain function

### 5. Network Analysis
- Constructed gene–pathway network
- Identified hub genes

### 6. Rarity-Based Prioritization
Used gene frequency as a proxy for rarity
Prioritized genes with lower background frequency

### 7. VUS Integration and final Gene Ranking
Computed gene-level VUS counts
Normalized VUS burden
Integrated into scoring model
Combined Functional enrichment Rarity score and VUS support
Generated final prioritized gene list
---

## 🔬 Version 2 Update (Key Contribution)

### Population-Aware Prioritization
- Gene frequency used as a proxy for rarity
- Low-frequency genes prioritized as rare disease candidates

### Automated Gene–Disease Mapping
- Derived from KEGG pathway associations
- Generated gene–disease relationships programmatically

### Final Candidate Selection
- Integrated:
  - Neuro enrichment
  - Variant frequency
  - Pathway mapping

---

## Key Results

### Top Candidate Genes
- APP
- NRXN1
- SHANK3
- CDK5
- MEF2C
- WNT5A


## Main Results (v3)

### Top 10 Prioritized Genes (Integrated Score)

| Rank | Gene     | Pathogenic Score | VUS_Norm   | Integrated_Score | Key Association                  |
|------|----------|------------------|------------|------------------|----------------------------------|
| 1    | NRXN1    | 26               | 0.209      | 31.43            | Synaptic function, ASD           |
| 2    | RELN     | 20               | 0.309      | 26.17            | Neurodevelopment                 |
| 3    | CDK5     | 26               | 0.002      | 26.05            | Neurodegeneration                |
| 4    | **SHANK3** | 24             | 0.081      | 25.96            | Synaptic scaffolding, Phelan-McDermid syndrome |
| 5    | APP      | 24               | 0.042      | 25.02            | Neurodegeneration                |
| 6    | WNT5A    | 24               | 0.024      | 24.57            | Neurodevelopment                 |
| 7    | NTRK2    | 22               | 0.065      | 23.42            | Neurotrophic signaling           |
| 8    | OPHN1    | 22               | 0.038      | 22.83            | Intellectual disability          |
| 9    | MEF2C    | 22               | 0.032      | 22.70            | Neurodevelopment                 |
| 10   | DMD      | 14               | 0.535      | 21.49            | Muscular / neurological overlap  |


### Biological Insights
- Neurodegeneration: APP, CDK5
- Synaptic/Psychiatric: NRXN1, SHANK3
- Neurodevelopment: MEF2C, WNT5A

### VUS Interpretation
High VUS burden observed in synaptic genes (NRXN1, SHANK3)
Extremely high VUS counts in large genes (DMD, RELN) suggest gene-size bias
Moderate VUS enrichment indicates unresolved pathogenic variants
---

## Outputs

### Data
- `results/v2_population/final_rare_neuro_genes.csv`
- `results/v2_population/final_gene_disease_table.csv`
- `results/v2_population/auto_gene_disease_from_kegg.csv`
- `results/v2_population/final_gene_disease_collapsed.csv`

## Key Outputs

- results/v2_population/final_master_with_VUS.csv → Final ranked gene list
- data/clinvar/vus_variants.txt → Extracted VUS dataset

### Figures
- Neuro gene network
- Hub gene network

---

## Conclusion

This study demonstrates that pathogenic variants converge on key neurological pathways. A population-aware filtering strategy enables prioritization of rare, disease-relevant genes.

---

## Limitations
- Population frequency inferred indirectly
- No direct integration of large-scale datasets (e.g., gnomAD)

---

## Future Directions
- Integrate population allele frequencies from large datasets
- Extend to genome-wide analysis
- Incorporate transcriptomic validation

---

## Repository Structure
data/ # Raw data (ClinVar, population)
scripts/ # Analysis scripts
results/ # Output files
figures/ # Visualizations
docs/ # Documentation
