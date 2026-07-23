# Host MHC Haplotypes Dictate Susceptibility to Bacterial Superantigen-Induced Acute Respiratory Distress Syndrome

Analysis code associated with a study investigating how murine MHC haplotype influences susceptibility to staphylococcal enterotoxin B (SEB)-induced acute respiratory distress syndrome (ARDS).

## Overview

This repository contains code used for:

- Single-cell RNA sequencing analysis
- TCR V(D)J repertoire analysis
- Differential expression analysis
- Figure generation for manuscript preparation

The study compares resistant and susceptible mouse strains following SEB exposure to identify immunologic and transcriptomic mechanisms associated with ARDS susceptibility.

## Experimental Design

Mouse strains included:

- C57BL/6J, H2<sup>b</sup>
- C3H/HeJ,H2<sup>k</sup>

SEB exposure protocol:

- 5 µg intranasal SEB at 0 h
- 2 µg intraperitoneal SEB at +2 h
- 72 h endpoint collection

## Repository Structure

```text
SEB_ARDS_H2_ManuscriptFiguresCode.Rmd
SEB_ARDS_H2_DataAnalysisCode.Rmd
```
`SEB_ARDS_H2_DataAnalysisCode.Rmd` documents the primary analysis workflow, including data preprocessing, Seurat object creation, quality control, DoubletFinder analysis, integration, TCR V(D)J metadata processing, CD3<sup>+</sup> T cell subsetting, and differential expression analysis.

`SEB_ARDS_H2_ManuscriptFiguresCode.Rmd` contains code used for manuscript figure generation, including UMAP visualization, cell type annotation plots, cell proportion analyses, TCR Vβ analyses, heatmaps, and selected statistical visualizations.

## Data Availability

Raw sequencing data and processed analysis objects are available through the Gene Expression Omnibus under accession number **GSE331494**.

Processed analysis objects available through GEO include:

- `integrated.RDS`  
  Integrated Seurat object containing all events from all experimental conditions.

- `cd3_pos.RDS`  
  Subsetted Seurat object containing CD3e<sup>+</sup> events derived from the integrated object.

- `vdj_all.RDS`  
  Table containing TCR V(D)J sequencing information and clonotype metadata.

Large sequencing files and processed RDS objects are intentionally excluded from this GitHub repository and should be downloaded directly from GEO.

## Software Requirements

Analysis was performed in R-4.5.2.

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

Manuscript under review with Advanced Science as of 2026/07/22.

## Author

Chloe Weyer-Nichols 
University of South Carolina School of Medicine
Department of Pathology, Microbiology, and Immunology
Nagarkatti Laboratory
```
