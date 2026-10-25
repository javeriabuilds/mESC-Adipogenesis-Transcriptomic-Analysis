# Exploratory Transcriptome Reanalysis of mESC Adipogenesis

**Focus:** Extracellular matrix (ECM) remodelling and lipid metabolism  
**Research context:** Mouse embryonic stem-cell differentiation into adipocytes

## Overview

Adipocyte differentiation involves coordinated changes in gene expression as cells acquire a specialized identity. This project presents an exploratory reanalysis of an existing, repository-provided processed gene-expression matrix associated with research on mouse embryonic stem-cell adipogenesis.

The analysis examines sample-level expression patterns and selected genes associated with extracellular matrix (ECM) remodelling and lipid metabolism. The workflow combines data quality checks, principal component analysis (PCA), candidate-gene summaries, and focused descriptive gene panels.

The objective is to investigate patterns in the available data while making the analytical scope and limitations explicit.

## Research Question

What expression patterns are observed in selected genes associated with ECM remodelling and lipid metabolism across the available mouse embryonic stem-cell adipogenesis samples?

## Analytical Workflow

1. **Data inspection and quality control:** Examined the expression matrix structure, sample labels, gene identifiers, and duplicate gene-symbol rows.
2. **Sample-level exploration:** Applied PCA to explore variation among the six samples.
3. **Candidate-gene analysis:** Summarized expression values for selected genes discussed in the associated research, including *Lpl*, *Acer3*, *Plg*, *Itga5*, *Igfbp6*, and *Pik3cg*.
4. **Focused gene panels:** Compared descriptive expression summaries for selected ECM-remodelling and lipid-metabolism genes.
5. **Technical validation:** Ran notebook checks and exported analysis summaries, validation results, and a run manifest.

## Selected Results

- **Expression matrix:** The imported matrix contained 46,603 rows and seven columns, including six samples and one gene-identifier column. The matrix contained 46,475 unique gene symbols before the notebook's gene-symbol handling steps.
- **Sample-level variation:** The first two principal components explained approximately 43.7% and 20.8% of the variance, respectively, or 64.4% combined.
- **Candidate and gene-panel summaries:** Descriptive comparisons were generated for selected candidate genes and ECM/lipid-metabolism panels to support further investigation of expression patterns.
- **Technical checks:** All six notebook technical validation checks passed during the recorded Google Colab run.

These results describe the available processed matrix. They do not establish statistically significant differential expression, causality, or experimental validation.

## Data and Reproducibility

The analysis uses a repository-provided variance-stabilizing transformation (VST) gene-expression matrix.

**Associated research**

Al-Sayegh and colleagues (2026), *Multi-omics integration reveals convergent extracellular matrix remodelling and lipid metabolic reprogramming as central axes of adipocyte differentiation from mouse embryonic stem cells.*

- DOI: [10.1080/21623945.2026.2680625](https://doi.org/10.1080/21623945.2026.2680625)
- Associated research repository: [msc-bioinformatics-mohamed-alsayegh](https://github.com/mxa1429/msc-bioinformatics-mohamed-alsayegh)
- BioProject: PRJNA1126392
- Proteomics dataset: PXD078584

### Running the notebook

1. Open `NYUAD_Exploratory_Transcriptome_Reanalysis_of_mESC_Adipogenesis.ipynb` from this repository.
2. Open the notebook in [Google Colab](https://colab.research.google.com/) or a compatible Jupyter environment.
3. Run the notebook cells in order.
4. Allow the notebook to install or import its required dependencies and retrieve the expression matrix from the configured source.
5. Review the PCA visualization, descriptive gene summaries, technical checks, and exported results.

**Scope:** This is an exploratory transcriptome reanalysis. The gene-level comparisons are descriptive and should not be interpreted as formal differential-expression results or as a complete reproduction of the paper's multi-omics analysis.

## Limitations and Interpretation

- The analysis uses a repository-provided processed expression matrix; its exact correspondence to the complete input data used in the final paper's analyses has not been independently confirmed.
- VST values are not raw counts. This notebook does not reproduce the paper's DESeq2 differential-expression analysis.
- Candidate-gene and gene-panel comparisons are descriptive, not formal differential-expression tests or pathway-enrichment tests.
- The candidate list is used exploratorily and should not be interpreted as independent validation of the paper's findings.
- Proteomics comparisons were withheld because the reporter-channel-to-condition mapping could not be verified. Complete cross-omics integration was therefore not performed.

Accordingly, this project should be interpreted as an **exploratory transcriptome reanalysis**, rather than a reproduction of the published study's complete computational analysis.

## Author

**Javeria Shakir**  
B.Tech Biotechnology | Interests: bioinformatics, computational biology, and molecular mechanisms of cellular differentiation
