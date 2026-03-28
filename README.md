# CCR9 Expression Profiling in Melanoma CD8+ T Cells
**Analysis for the publication: "Secretory IgA amplification during immune checkpoint blockade enhances the control of tumor growth by enterotropic T cells"**

This repository contains the scRNA-seq processing pipeline used to validate the expression of the chemokine receptor **CCR9** in cytotoxic T cells within the tumor microenvironment.

### Project Overview
The analysis focuses on CD8+ T cells isolated from melanoma patients to investigate how enterotropic T cells expressing CCR9 contribute to tumor growth control during immune checkpoint blockade (ICB).

### Data Source
*   **Dataset:** Processed scRNA-seq data from NCBI Gene Expression Omnibus (GEO).
*   **Accession:** [GSE123139](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE123139).
*   **Sample Size:** 18 patients with metadata including tissue origin, disease stage, and treatment.

### Computational Workflow
1.  **Data Integration:** Importing preprocessed matrices into `Scanpy (v1.9.6)` as AnnData objects and concatenating via `pandas`.
2.  **Cell Selection:** Filtering for **CD8+ T cells** based on the expression of canonical markers: *CD3D, CD3E, CD3G, CD8A,* and *CD8B*.
3.  **Visualization:** Targeted analysis of **CCR9** expression across patient groups using advanced dot plot parameters to ensure statistical clarity.

### Key Tools
*   **Scanpy:** For single-cell analysis and visualization.
*   **Pandas:** For metadata management and object concatenation.
