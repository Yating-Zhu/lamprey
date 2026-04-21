# lamprey

This repository contains custom downstream analysis notebooks used for visualization and interpretation of publicly available lamprey single-cell RNA-seq data.

No novel software package or algorithm is introduced in this repository. The code provided here is used for downstream analysis, figure generation, and interpretation based on processed single-cell datasets from the original study.

## Data and Code Availability

### Data Availability

This repository utilizes data from the following article:
[**"Single-cell transcriptome atlas of lamprey exploring Natterin-induced white adipose tissue browning "**](https://doi.org/10.1038/s41467-025-56153-w)

The data used for this analysis is freely available under the following resources:

- **CNGB Nucleotide Sequence Archive**: All data generated in this study are freely accessible under accession code **CNP0005120**. 
- **NCBI BioProject Database**: All raw sequencing data generated during this study are available under accession number **PRJNA1194219**.
- **Zenodo**: The processed scRNA-seq data and associated annotation metadata are available under DOI [10.5281/zenodo.14338297](https://doi.org/10.5281/zenodo.14338297).

Processed data can be interactively explored and downloaded from [CNGB Project page](https://db.cngb.org/search/project/CNP0005120/).

### Code Availability

The custom analysis code used in this study has been deposited in the following repositories:
- **GitHub Repository**: [https://github.com/lskfs/lamprey-single-cell-atlas](https://github.com/lskfs/lamprey-single-cell-atlas)
- **Zenodo Repository**: [https://doi.org/10.5281/zenodo.14338297](https://doi.org/10.5281/zenodo.14338297)

### Methodology

The quality control and cell clustering steps for this analysis were performed based on the code provided in the GitHub repository referenced in the paper [**"Single-cell transcriptome atlas of lamprey exploring Natterin-induced white adipose tissue browning "**](https://doi.org/10.1038/s41467-025-56153-w). Please refer to the repository for further details on the methodologies used in those processes.

## Overview

This repository contains analysis notebooks used for:

- UMAP visualization
- marker gene feature plotting
- marker heatmap generation
- tissue-specific marker comparison
- co-expression analysis

The main notebook currently used for this analysis is:

- `lamprey_VLR-like_20260403update.ipynb`

## System Requirements

The analysis was performed using:

- **R version 4.4.1**
- **Seurat version 5.2.1**
- **ggplot2 version 4.0.0**
- **harmony version 1.2.3**

Additional R packages used in the notebook include:

- Matrix
- future
- dplyr
- data.table
- pheatmap
- reshape2
- patchwork

The code was tested on:

- **Ubuntu 22.04 LTS** in an HPC cluster environment

Required non-standard hardware:

- **None**

## Installation Guide

1. Clone this repository:

```bash
git clone https://github.com/Yating-Zhu/lamprey.git
cd lamprey
```

2. Install the required R packages:

```r
install.packages(c(
  "Seurat",
  "ggplot2",
  "harmony",
  "Matrix",
  "future",
  "dplyr",
  "data.table",
  "pheatmap",
  "reshape2",
  "patchwork"
))
```

3. Open the notebook in **Jupyter Notebook / JupyterLab with an R kernel**, or another environment that supports `.ipynb` notebooks using R.

Typical installation time on a normal desktop computer:

- Approximately **5–15 minutes**, depending on whether the required R packages are already installed.


### To reproduce the full analysis

1. Download the relevant processed single-cell RNA-seq data from the public resources listed in the Data Availability section.
2. Prepare the corresponding local Seurat `.rds` objects for blood, gill, and intestine samples.
3. Replace the local file paths in the first data-loading cell of the notebook.
4. Run the notebook sequentially.

The demo dataset is intended to demonstrate code execution and expected output formats. Full reproduction of the manuscript figures requires the complete processed datasets.

## Reproducibility

The demo dataset can be used to reproduce representative output formats, including:

- UMAP plots
- selected marker gene feature plots
- marker heatmaps
- representative co-expression plots

Full reproduction of **Figure 1**, **Figure S1**, and **Figure S2** requires the complete processed datasets and the corresponding local Seurat `.rds` objects for blood, gill, and intestine samples.

## License

This repository is released under the **MIT License**.
