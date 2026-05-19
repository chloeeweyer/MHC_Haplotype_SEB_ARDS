# Host MHC Haplotypes Dictate Susceptibility to Bacterial Superantigen-Induced Acute Respiratory Distress Syndrome

Analysis code associated with a study investigating how murine MHC haplotype influences susceptibility to staphylococcal enterotoxin B (SEB)-induced acute respiratory distress syndrome (ARDS).

## Overview

This repository contains code used for:

- Single-cell RNA sequencing analysis
- TCR V(D)J repertoire analysis
- Differential expression
- Figure generation for manuscript preparation

The study compares resistant and susceptible mouse strains following SEB exposure to identify immunologic and transcriptomic mechanisms associated with ARDS susceptibility.

## Experimental Design

Mouse strains included:

- C57BL/6J (H2b)
- C3H/HeJ (H2k)

SEB exposure protocol:

- 5 µg intranasal SEB at 0 h
- 2 µg intraperitoneal SEB at +2 h
- 72 h endpoint collection

## Repository Structure

```text
SEB_ARDS_H2_ManuscriptFiguresCode.Rmd
SEB_ARDS_H2_DataAnalysisCode.Rmd
```

Contains code used for:

- Seurat processing and visualization
- UMAP generation
- Cell type annotation
- Differential expression analysis
- TCR Vβ analysis
- Figure generation
- Statistical analyses
- Data preprocessing and quality control

## Data Availability

Raw sequencing data are available through GEO: [ACCESSION_PENDING]

Processed analysis objects available through GEO include:

- `integrated.RDS`  
  Integrated Seurat object containing all events from all experimental conditions.

- `cd3_pos.RDS`  
  Subsetted Seurat object containing CD3e+ immune populations derived from the integrated object.

- `vdj_all.RDS`  
  Table containing TCR V(D)J sequencing information and clonotype metadata.

Large intermediate files are intentionally excluded from this GitHub repository and should be downloaded directly from GEO.

## Software Requirements

Analysis was performed in R.

Primary packages used include:

```r
library(Seurat)
library(dplyr)
library(patchwork)
library(readr)
library(data.table)
library(knitr)
library(ggplot2)
library(DoubletFinder)
library(ggrepel)
library(tidyr)
library(gt)
library(glue)
library(glmGamPoi)
```

Additional package dependencies may be required for specific downstream analyses or visualization steps.

## Manuscript Status

Manuscript in preparation.

## Author

Chloe Weyer-Nichols 
University of South Carolina School of Medicine
```