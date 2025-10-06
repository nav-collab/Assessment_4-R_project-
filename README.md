# Comparative Analysis of Gene Expression and Protein k-mer Usage in *E. coli* and *Staphylococcus aureus*

This repository contains an RMarkdown workflow for the analysis of gene expression and coding sequence (CDS) data in *Escherichia coli* and *Staphylococcus aureus*. The workflow covers RNA-seq data analysis, coding sequence statistics, codon usage bias, amino acid composition, and protein k-mer frequency analysis.

## Features

**Gene Expression Analysis:**
- Processing gene expression data from RNA-seq experiments.
- Calculating mean expression per gene and identifying highly and weakly expressed genes.
- Visualizing gene expression distributions using histograms.
- Comparative statistical analysis of tree growth data (circumference) over a 10–15 year period, including t-tests and boxplots.

**Coding DNA Sequence (CDS) Analysis:**
- Downloading CDS data from Ensembl for *E. coli* K-12 MG1655 and *S. aureus*.
- Computing CDS statistics: total base pairs, mean and median CDS lengths.
- Visualizing CDS length distributions via boxplots.

**Nucleotide and Amino Acid Analysis:**
- Counting nucleotide frequencies (A, T, G, C) in CDS.
- Translating CDS into amino acid sequences.
- Counting amino acid frequencies and visualizing them with barplots.

**Codon Usage and k-mer Analysis:**
- Calculating codon usage bias using RSCU (Relative Synonymous Codon Usage).
- Visualizing codon usage differences between *E. coli* and *S. aureus*.
- Analyzing protein k-mers (3–5 amino acids) to identify over- and under-represented motifs.
- Comparative k-mer frequency plots for both organisms.

## Repository Contents

- `assessment.Rmd` – Main RMarkdown file containing all code, analysis, and plots for tasks 1–6.
- `gene_expression.tsv` – Gene expression dataset used for mean expression and histogram analyses.
- `growth_data.csv` – Tree circumference data for statistical analysis.
- `staphylococcus_aureus_cds.fa` – Coding DNA sequences for *S. aureus*.
- `ecoli_cds.fa` – Coding DNA sequences for *E. coli*.
- `README.md` – This file describing the repository and its contents.

## Prerequisites

This project requires **R (>= 4.0)** and the following R packages:

**Core Packages:**
- `seqinr`  
- `R.utils`  
- `tidyverse` (including `dplyr`, `ggplot2`)  
- `knitr`  

**Optional Visualization Packages:**
- `ggpubr`  
- `viridis`  

## Usage

1. Open `assessment.Rmd` in RStudio.  
2. Ensure all datasets (`gene_expression.tsv`, `growth_data.csv`, `staphylococcus_aureus_cds.fa`, `ecoli_cds.fa`) are in the working directory.  
3. Knit the RMarkdown document to HTML or PDF to view all results, tables, and plots.  

## Outputs

- Tables of gene expression mean, CDS length statistics, and codon usage (RSCU).  
- Boxplots and histograms for CDS length and gene expression.  
- Barplots showing nucleotide and amino acid frequencies.  
- Over- and under-represented protein k-mer plots (3-, 4-, and 5-mers) for both *E. coli* and *S. aureus*.  
- Comparative analysis showing differences in amino acid usage, codon preferences, and k-mer motifs across the two bacterial species.

## Observations

- *E. coli* has a larger genome and more coding sequences than *S. aureus*.  
- Nucleotide composition differs: *E. coli* is GC-rich, whereas *S. aureus* is AT-rich.  
- Codon usage bias reflects genomic
