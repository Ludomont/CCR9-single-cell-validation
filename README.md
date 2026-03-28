# CCR9 Expression Analysis in Melanoma CD8+ T Cells
**Analytical pipeline for the publication in *Science Advances***

[![DOI:10.1126/sciadv.adk0617](https://img.shields.io/badge/DOI-10.1126%2Fsciadv.adk0617-blue.svg)](https://doi.org/10.1126/sciadv.adk0617)

### Project Overview
This repository contains the scRNA-seq processing and quality control pipeline used to investigate the role of enterotropic T cells in tumor growth control. The analysis specifically focuses on the expression of the chemokine receptor **CCR9** in cytotoxic T cells during immune checkpoint blockade (ICB).

**Publication:** [Secretory IgA amplification during immune checkpoint blockade enhances the control of tumor growth by enterotropic T cells](https://www.science.org/doi/10.1126/sciadv.adk0617)


**Data Source:** [NCBI GEO GSE123139](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE123139)
---

### Data & Methodology
The analysis was performed on single-cell transcriptomic data from **CD8+ T cells** isolated from melanoma patients.

*   **Data Source:** NCBI GEO accession [GSE123139](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE123139).
*   **Preprocessing:** Expression matrices were imported into `Scanpy (v1.9.6)` as AnnData objects and concatenated using `pandas` for a unified analysis.
*   **Metadata Integration:** Each sample was annotated with patient ID, tissue origin, disease stage, and treatment status.
*   **Cell Selection:** CD8+ T cells were identified and subsetted based on the expression of canonical markers: *CD3D, CD3E, CD3G, CD8A,* and *CD8B*.

### Key Visualization
The final analysis visualizes **CCR9 expression** across different patient groups using a customized dot plot to highlight phenotypic differences:
*   **Tool:** `sc.pl.dotplot`
*   **Parameters:** `dot_max=0.01`, `dot_min=0`, `log=True`, `standard_scale='var'`.

### Requirements
*   Python >= 3.8
*   Scanpy == 1.9.6
*   Pandas
*   Matplotlib / Seaborn
