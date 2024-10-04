# RNASeq Differential Expression Analysis using DESEQ2

This project provides a workflow for analyzing RNASeq data using the DESeq2 package in R. It includes steps for loading raw counts and metadata, running differential expression analysis, and creating visualizations such as PCA, heatmaps, and volcano plots.

## Installation
Install the required packages by running the following commands in R:

```r
# Install Bioconductor manager
install.packages("BiocManager")

# Install necessary packages
BiocManager::install(c("DESeq2", "SummarizedExperiment", "EnhancedVolcano", "apeglm"))
install.packages(c("gtable", "stringi", "tidyverse", "pheatmap", "PoiClaClu"))
```

## Usage
```r
Set working directory: Update the working directory path in the script.
setwd("C:/path/to/your/data")
Load data: Ensure Metadata.txt and Counts.txt files are present in your working directory.
metadata <- read.csv("Metadata.txt", sep="\t")
counts <- read.csv("Counts.txt", sep="\t")

```

Run analysis: Execute the provided R script to:

Create a DESeq2 dataset
Perform variance stabilizing transformation (VST)
Generate PCA, heatmaps, and volcano plots
Identify and filter significant differentially expressed genes
Export results: The results will be saved as finaltable.tsv.

## Visualization

The analysis includes:

PCA Plot: Visualizes sample clustering.
Heatmap: Shows sample-to-sample distance.
Volcano Plot: Highlights significant differentially expressed genes.

## Output

finaltable.tsv: Contains ordered differential expression results based on adjusted p-values and log2 fold changes.

## License

This project is licensed under the MIT License.
