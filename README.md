# Anopheles Genomic Data Exploration

## Overview
This repository contains the Jupyter notebook for exploring and processing genomic data from four Anopheles mosquito species: **gambiae**, **bissau**, **gcs3**, and **coluzzii**. The goal of this project is to explore SNP data from the Vector Observatory, clean and preprocess it, apply feature engineering techniques, and train machine learning models for taxonomic classification of Anopheles species.

## Files Explored
The exploration is based on four genomic data files in the **Zarr** format. These files are organized as follows:

1. **AB0142-C.gatk.zarr** - Species: **gambiae**
2. **AG0152-C.gatk.zarr** - Species: **bissau**
3. **AK0105-C.gatk.zarr** - Species: **gcs3**
4. **AR0047-C.gatk.zarr** - Species: **coluzzii**

Each file contains multiple chromosomes (e.g., `2L`, `2R`, `3L`, etc.) with associated **SNP data** that includes genotype information (GT), allele depth (AD), and genotype quality (GQ).

## Exploratory Data Analysis (EDA)

### Directory Structure Overview

## root-word
The main directory containing genomic data for multiple chromosomes and unplaced data.

### 2L
- **calldata**: Contains genotype data for the 2L chromosome.
  - `AD`: Allele Depth.
  - `GQ`: Genotype Quality.
  - `GT`: Genotype.
- **variants**: Contains information related to the variants on chromosome 2L.
  - `MQ`: Mapping Quality.

### 2R
- **calldata**: Contains genotype data for the 2R chromosome.
  - `AD`: Allele Depth.
  - `GQ`: Genotype Quality.
  - `GT`: Genotype.
- **variants**: Contains information related to the variants on chromosome 2R.
  - `MQ`: Mapping Quality.

### 3L
- **calldata**: Contains genotype data for the 3L chromosome.
  - `AD`: Allele Depth.
  - `GQ`: Genotype Quality.
  - `GT`: Genotype.
- **variants**: Contains information related to the variants on chromosome 3L.
  - `MQ`: Mapping Quality.

### 3R
- **calldata**: Contains genotype data for the 3R chromosome.
  - `AD`: Allele Depth.
  - `GQ`: Genotype Quality.
  - `GT`: Genotype.
- **variants**: Contains information related to the variants on chromosome 3R.
  - `MQ`: Mapping Quality.

### Mt
- **calldata**: Contains genotype data for the mitochondrial chromosome (Mt).
  - `AD`: Allele Depth.
  - `GQ`: Genotype Quality.
  - `GT`: Genotype.
- **variants**: Contains information related to the variants on the mitochondrial chromosome.
  - `MQ`: Mapping Quality.

### UNKN
- **calldata**: Contains genotype data for an unknown chromosome (UNKN).
  - `AD`: Allele Depth.
  - `GQ`: Genotype Quality.
  - `GT`: Genotype.
- **variants**: Contains information related to the variants on the unknown chromosome.
  - `MQ`: Mapping Quality.

### X
- **calldata**: Contains genotype data for the X chromosome.
  - `AD`: Allele Depth.
  - `GQ`: Genotype Quality.
  - `GT`: Genotype.
- **variants**: Contains information related to the variants on the X chromosome.
  - `MQ`: Mapping Quality.

### Y_unplaced
- **calldata**: Contains genotype data for the Y chromosome (unplaced).
  - `AD`: Allele Depth.
  - `GQ`: Genotype Quality.
  - `GT`: Genotype.
- **variants**: Contains information related to the variants on the unplaced Y chromosome.
  - `MQ`: Mapping Quality.




### Key Findings from the Data Exploration:
- **GT values**: Represent the genotype data for each sample. The unique values observed in the GT array are {-1, 0, 1, 2, 3}, with the -1 representing missing data.
- **Genotype Quality (GQ)**: Measures the confidence in the genotype call.
- **Allele Depth (AD)**: Represents the number of reads supporting each allele at a particular position.
- **Mapping Quality (MQ)**: Measures the confidence in the alignment of the sequencing reads.

We performed basic statistical analyses and visualizations for the SNP distributions and observed the following:
- **Missing Data**: Missing genotype information was handled using imputation techniques (e.g., KNN).
- **Class Imbalance**: Species such as **coluzzii** had significantly more samples than others like **gcs3**, leading to potential bias in training models.
  

