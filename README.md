# Understanding Interactions between Transcription Factors and Histone Modifications in Lymphoblastoid Cell Line through ChIP-Seq Analysis

## Project Overview
This project focuses on understanding the interactions between transcription factors (e.g., CTCF, SMC3, ZNF143, PolII) and histone modifications (e.g., H3K4me3, H3K36me3, H3k27ac, H3k27me3) in lymphoblastoid cell lines using ChIP-Seq data. By analyzing publicly available data from the ENCODE project, this analysis aims to provide insights into the regulation of genomic elements in immune cell differentiation.

## Table of Contents
- [Project Overview](#project-overview)
- [Introduction](#introduction)
- [Data Sources](#data-sources)
- [Installation](#installation)
- [Data Processing](#data-processing)
- [Results and Visualization](#results-and-visualization)
- [References](#references)

## Introduction
ChIP-Seq (Chromatin Immunoprecipitation Sequencing) is a powerful technique used to study protein-DNA interactions. In this project, ChIP-Seq data was used to investigate how transcription factors and histone modifications regulate gene expression in lymphoblastoid cell lines (GM12878) mapped to the human reference genome GRCh38 (hg38).

The analysis involves the following steps:
1. **Data Retrieval**: Collecting ChIP-Seq data from ENCODE.
2. **Data Processing**: Quality control, filtering, and normalization of ChIP-Seq data.
3. **Data Analysis**: Clustering, correlation analysis, and identification of potential binding sites for transcription factors.
4. **Visualization**: Visualizing the data using heatmaps, genome browsers, and strand cross-correlation analysis.
5. **Interpretation**: Interpreting the interactions between transcription factors and histone modifications.

## Data Sources
The ChIP-Seq data used in this project is publicly available from the [ENCODE project](https://www.encodeproject.org/). Specifically, data from the GM12878 lymphoblastoid cell line was mapped to the human genome GRCh38 (hg38). A subset of the entire data was used sourcing <compGenomRData> package in R

## Installation

To set up the project, clone the repository and install the necessary R packages:

```bash
git clone https://github.com/NishatMohammad/ChIPSeqLymphobalstoidCellLine.git
```

## Data Processing
The data processing workflow includes several key steps:

Data retrieval from <compGenomeData> package in R

Tile the genome into smaller windows (1000 base pairs) to analyze the coverage of transcription factors and histone modifications.

Normalize the data using Counts Per Million (CPM) to ensure comparability across samples.

Perform clustering to identify patterns of similarity between samples.

Generate Pearson correlation heatmaps to visualize the relationships between different samples.

Visualize data using genome browser tracks and strand cross-correlation to understand potential biases in the data.

## Results and Visualization
The main results of the project include:

**Clustering**: The ChIP-Seq samples were clustered based on their similarity using Pearson correlation.

**Heatmaps**: Heatmaps to visualize the correlation between different transcription factors and histone modifications.

**Strand Cross-Correlation**: A plot was generated to assess the fragment size bias in the ChIP-Seq data.

## References
ENCODE Project Consortium. (2012). "An integrated encyclopedia of DNA elements in the human genome." Nature, 489(7414), 57-74. Retrieved January 02, 2025 from https://www.nature.com/articles/nature11247

Bioconductor. (2025). BSgenome.Hsapiens.UCSC.hg38: Full genomic sequences for Homo sapiens (UCSC genome hg38). Bioconductor. https://www.bioconductor.org/packages/release/data/annotation/html/BSgenome.Hsapiens.UCSC.hg38.html

Akalin, A., et al. (2020, November 26). ChIP quality control. In Computational Genomics with R. Retrieved January 02, 2025, from https://compgenomr.github.io/book/chip-quality-control.html
