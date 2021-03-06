# Differential gene expression workshop

| Audience | Computational Skills | Prerequisites | Duration |
:----------|:----------|:----------|:----------|
| Biologists | Intermediate R | Introduction to R | 1.5-day workshop (~10 hours of trainer-led time)|

This repository has teaching materials for a **1.5-day**, hands-on **Introduction to differential gene expression (DGE) analysis** workshop. The workshop will lead participants through performing a differential gene expression analysis workflow on RNA-seq count data using R/RStudio. Working knowledge of R is required or completion of the [Introduction to R workshop](https://github.com/hbctraining/Intro-to-R).

### Learning Objectives

- QC on count data using Principal Component Analysis (PCA) and heirarchical clustering
- Using DESeq2 to obtain a list of significantly different genes
- Visualizing expression patterns of differentially expressed genes
- Performing functional analysis on gene lists with R-based tools

> These materials are developed for a trainer-led workshop, but also amenable to self-guided learning.

### Contents

#### Differential Gene Expression (DGE) using RNA-seq raw counts data

| Lessons            | Duration |
|:------------------------|:----------|
|[Setting up and DGE overview](lessons/01_DGE_setup_and_overview.md) | 70 min |
|[Introduction to count normalization](lessons/02_DGE_count_normalization.md) | 60 min |
|[QC using principal component analysis (PCA) and heirarchical clustering](lessons/03_DGE_QC_analysis.md) | 90 min |
|[Getting started with DESeq2](lessons/04_DGE_DESeq2_analysis.md) | 70 min |
|[Pairwise comparisons with DEseq2](lessons/05_DGE_DESeq2_analysis2.md) | 45 min |
|[Visualization of DGE analysis results](lessons/06_DGE_visualizing_results.md) | 45 min |
|[Summary of DGE workflow](lessons/07_DGE_summarizing_workflow.md) | 15 min |
|[Complex designs with DESeq2 (LRT)](lessons/08_DGE_LRT.md) | 60 min |
|[Functional Analysis](lessons/10_functional_analysis.md) | 85 min |

***

### Installation Requirements

Download the most recent versions of R and RStudio for your laptop:

 - [R](http://lib.stat.cmu.edu/R/CRAN/) 
 - [RStudio](https://www.rstudio.com/products/rstudio/download/#download)
 
Install the required R packages by running the following code in RStudio:

```r
source("http://bioconductor.org/biocLite.R") 
biocLite(c("RColorBrewer", "pheatmap", "DESeq2", "clusterProfiler", 
           "DOSE", "org.Hs.eg.db", "pathview", "purrr", "DEGreport", "stephenturner/annotables"))
```

Load the libraries to make sure the packages installed properly:

```r
library(DESeq2)
library(ggplot2)
library(RColorBrewer)
library(pheatmap)
library(clusterProfiler)
library(DEGreport)
library(org.Hs.eg.db)
library(DOSE)
library(pathview)
library(purrr)
library(annotables)
```

### Practical exercises
After completion of the workshop, practice of concepts can be explored with [these exercises](https://hbctraining.github.io/DGE_workshop/exercises/DGE_analysis_exercises.html). An answer key is [available](https://hbctraining.github.io/DGE_workshop/exercises/DGE_analysis_exercises%20answer_key.html) to check answers.

****

*These materials have been developed by members of the teaching team at the [Harvard Chan Bioinformatics Core (HBC)](http://bioinformatics.sph.harvard.edu/). These are open access materials distributed under the terms of the [Creative Commons Attribution license](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0), which permits unrestricted use, distribution, and reproduction in any medium, provided the original author and source are credited.*
