# Spatial-RNA-Analysis

# Code Analysis and Visualization README

This README provides an overview of the Python code and its functionalities. The code performs various data analysis and visualization tasks using the Scanpy library. The purpose of this code is to analyze spatial transcriptomics data and generate visualizations to understand gene expression patterns. The data for the spatial analysis can be found [here](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE178361) with the paper that is available [here](https://doi.org/10.1038/s41586-022-04541-3)

## Table of Contents

1. [Introduction](#introduction)
2. [Dependencies](#dependencies)
3. [Code Explanation](#code-explanation)
4. [Usage](#usage)
5. [Results](#results)

## Introduction

This Python code is designed to analyze and visualize spatial transcriptomics data using the Scanpy library. The code reads the data, performs data preprocessing steps, calculates quality control metrics, identifies highly variable genes, performs dimensionality reduction, and clusters cells. It also identifies marker genes for each cluster and generates visualizations for exploration.

## Dependencies

To run this code, you'll need the following Python libraries:

- Scanpy
- Pandas
- Matplotlib
- Seaborn
- Numpy

Install these dependencies using the following command:

```bash
pip install scanpy pandas matplotlib seaborn numpy
```

## Code Explanation

The code can be divided into the following sections:

1. **Data Loading and Preprocessing**: The code starts by loading spatial transcriptomics data using `sc.read_visium`. It then performs data preprocessing steps like adding new columns to the data, filtering cells based on counts, and filtering genes.

2. **Quality Control and Visualization**: The code calculates quality control metrics using `sc.pp.calculate_qc_metrics` and generates histograms to visualize the distribution of certain metrics.

3. **Gene Filtering and Analysis**: The code further filters genes based on their expression levels and then performs principal component analysis (PCA), neighborhood graph construction, and UMAP embedding for dimensionality reduction and cell clustering. It also uses the Leiden algorithm for community detection.

4. **Marker Gene Identification**: The code identifies marker genes for each cluster using the Wilcoxon rank-sum test and selects significant markers based on adjusted p-values and fold changes.

5. **Visualization**: The code generates spatial and UMAP-based visualizations of clusters, gene expression, and other relevant information.

## Usage

1. Install the required dependencies.
2. Copy and paste the code into a Python script or Jupyter Notebook.
3. Modify file paths and parameters as needed.
4. Run the code step by step to observe the data analysis and visualization process.

## Results

The code provides insights into spatial transcriptomics data through various visualizations. It identifies clusters of cells, visualizes gene expression patterns, and highlights marker genes associated with each cluster. These results help in understanding the spatial distribution of gene expression in the tissue under study.

Please note that the provided code snippets might need adjustments according to your specific dataset and requirements. Make sure to customize file paths, parameters, and visualization options accordingly.

## Cited paper

Kadur Lakshminarasimha Murthy, P., Sontake, V., Tata, A. et al. Human distal lung maps and lineage hierarchies reveal a bipotent progenitor. Nature 604, 111–119 (2022). https://doi.org/10.1038/s41586-022-04541-3
