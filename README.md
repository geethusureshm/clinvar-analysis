# ClinVar Pathogenic Variant Analysis (Chromosome 1)

## Overview
This project identifies rare disease-associated genes by integrating ClinVar pathogenic variants with functional enrichment, network analysis, and population-aware prioritization.

---

## Objectives
- Extract pathogenic variants from ClinVar
- Map variants to genes
- Identify biologically relevant pathways
- Prioritize rare neuro-associated candidate genes
- Infer gene–disease associations

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

### Biological Insights
- Neurodegeneration: APP, CDK5
- Synaptic/Psychiatric: NRXN1, SHANK3
- Neurodevelopment: MEF2C, WNT5A

---

## Outputs

### Data
- `results/v2_population/final_rare_neuro_genes.csv`
- `results/v2_population/final_gene_disease_table.csv`
- `results/v2_population/auto_gene_disease_from_kegg.csv`
- `results/v2_population/final_gene_disease_collapsed.csv`

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
