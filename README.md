# Single-cell RNA-seq Analysis of Drosophila Projection Neurons

## Overview
This repository contains the computational pipeline and analysis scripts for the single-cell RNA-seq (Smart-seq2) data of *Drosophila* projection neurons (PNs). The analysis includes rigorous quality control (QC), filtering, normalization, and downstream clustering to match PN types across different developmental stages.

## Repository Structure

* **`Filtering_and_Normalization_Smart-seq2.ipynb`**
  Quality control, filtering, and normalization pipeline for Smart-seq2 data at the 12h APF developmental stage. It processes 384-well plates through multi-stage filtering: ERCC spike-in outliers → basic QC (counts & mitochondrial %) → neuronal marker expression.
  
* **`Matching_PN_Types.ipynb`**
  Downstream analysis for matching PN types. This notebook utilizes custom Iterative Clustering and Iterative Matching (`sct.ICIM`) and HDBSCAN to integrate and match cell types across different datasets and developmental stages (e.g., 0h, 12h, 24h).

## Data Availability
Due to file size limits, the large raw count matrices and `.h5ad` objects are not hosted in this repository. 
* The raw scRNAseq data and reference data can be downloaded from at GEO under accession number [GSE318611] and [GSE161228].
