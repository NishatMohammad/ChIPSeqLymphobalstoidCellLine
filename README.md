# Understanding Interactions between Transcription Factors and Histone Modifications in Lymphoblastoid Cell Line through ChIP-Seq Analysis


## Project Overview
This project focuses on understanding the interactions between transcription factors (CTCF, SMC3, ZNF143, PolII) and histone modifications (H3K4me3, H3K36me3, H3k27ac, H3k27me3) in lymphoblastoid cell lines using ChIP-Seq data. By analyzing publicly available data from the ENCODE project, this analysis aims to provide insights into the regulation of genomic elements in immune cell differentiation.


## Table of Contents
- [Project Overview](#project-overview)
- [Introduction](#introduction)
- [Data Sources](#data-sources)
- [Installation](#installation)
- [Data Processing](#data-processing)
- [Peak Calling](#peak-calling)
- [Results and Visualization](#results-and-visualization)
- [References](#references)


## Introduction
ChIP-Seq (Chromatin Immunoprecipitation Sequencing) is a powerful technique used to study protein-DNA interactions. In this project, ChIP-Seq data was used to investigate how transcription factors and histone modifications regulate gene expression in lymphoblastoid cell lines (GM12878) mapped to the human reference genome GRCh38 (hg38).

The analysis involves the following steps:
1. **Data Retrieval**: Collecting ChIP-Seq data from ENCODE.
2. **Data Processing**: Quality control, filtering, and normalization of ChIP-Seq data.
3. **Data Analysis**: Clustering, correlation analysis, and identification of potential binding sites for transcription factors.
3. **Peak Calling**: Identifying and annotating genomic regions enriched for transcription factors and histone modifications.
4. **Data Analysis**: Clustering, correlation analysis, and identification of potential binding sites for transcription factors.
5. **Visualization**: Visualizing the data using heatmaps, genome browsers, and strand cross-correlation analysis.

## Data Sources
The ChIP-Seq data used in this project is publicly available from the [ENCODE project](https://www.encodeproject.org/). Specifically, data from the GM12878 lymphoblastoid cell line was mapped to the human genome GRCh38 (hg38). A subset of the entire data was used sourcing `compGenomRData` package in R


## Installation

To set up the project, clone the repository and install the necessary R packages:

```bash
git clone https://github.com/NishatMohammad/ChIPSeqLymphobalstoidCellLine.git
```


## Data Processing
The data processing workflow includes several key steps:

Data retrieval from `compGenomeData` package in R

Tile the genome into smaller windows (1000 base pairs) to analyze the coverage of transcription factors and histone modifications.

Normalize the data using Counts Per Million (CPM) to ensure comparability across samples.

Perform clustering to identify patterns of similarity between samples.

Generate Pearson correlation heatmaps to visualize the relationships between different samples.

Visualize data using genome browser tracks and strand cross-correlation to understand potential biases in the data.


## Peak Calling
Peak calling is a crucial step in identifying regions of the genome where transcription factors and histone modifications are enriched. This project involves the following steps:  

**1. Motif Analysis**: Identifying CTCF motif occurrences in ChIP-Seq data and correlating these with genomic peaks.  

**2. Peak Annotation**: Annotating peaks based on their genomic location (e.g., promoters, exons, introns, intergenic regions).  

**3. Peak Distribution**: Analyzing the distribution of peaks across various genomic features and visualizing the results in bar plots.  

Key findings from the peak calling process include identifying peaks that overlap with specific genomic features, such as promoters or exons, and quantifying the distribution of these peaks across different categories.


## Results and Visualization
The main results of the project include:

**Clustering**: The ChIP-Seq samples were clustered based on their similarity using Pearson correlation.

**Heatmaps**: Heatmaps to visualize the correlation between different transcription factors and histone modifications.

**Strand Cross-Correlation**: A plot was generated to assess the fragment size bias in the ChIP-Seq data.

**Peak Distribution**: The distribution of peaks across genomic regions was visualized, showing the frequency of peaks in promoters, exons, introns, and intergenic regions.

**Motif Hits**: A cumulative distribution of peaks containing the CTCF motif was plotted to assess motif enrichment around genomic regions.


## References
ENCODE Project Consortium. (2012). "An integrated encyclopedia of DNA elements in the human genome." Nature, 489(7414), 57-74. Retrieved January 02, 2025 from https://www.nature.com/articles/nature11247

Bioconductor. (2025). BSgenome.Hsapiens.UCSC.hg38: Full genomic sequences for Homo sapiens (UCSC genome hg38). Bioconductor. https://www.bioconductor.org/packages/release/data/annotation/html/BSgenome.Hsapiens.UCSC.hg38.html

Akalin, A., et al. (2020, November 26). ChIP quality control. In Computational Genomics with R. Retrieved January 02, 2025, from https://compgenomr.github.io/book/chip-quality-control.html
