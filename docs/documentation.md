---
layout: default
title: Documentation
nav_order: 2
---

## Documentation

The bioinformatics pipeline available as [Colab notebook](https://colab.research.google.com/github/luquelab/bioinformatics-teamCanes/blob/main/notebooks/main_pipeline.ipynb) has an extensive documentation for each step. For convenience, the documentation is also listed here.

The pipeline integrates several stages of analysis — from calculating basic sequence properties such as length and GC content, to advanced tasks like pairwise alignments, phylogenetic tree construction, and functional and origin organismal prediction using online tools such as NCBI BLASTx and EMBL-EBI HMMER (using Pfam database). It also includes data visualization outputs like bar plots and heatmaps, helping users to intuitively interpret sequence similarities and evolutionary patterns.

All outputs are organized into clearly defined folders, making it easier to track each stage of the analysis. Whether you're a student learning the basics of sequence analysis or a researcher conducting high-throughput comparisons, this pipeline offers a robust and modular foundation to support a wide range of genomic investigations.   

## Pipeline overview

**Directory Structure Setup**

---
This code block sets up the structure of the output directories each containing the results from a specific analysis/part of the pipeline. The default name of the root directory is **project_x_analysis** and can be modified by the user.
---
**Part 1**: Sequence Analysis Pipeline  
    **Step 1**: Upload and Store Sequences File  
    **Step 2**: Load Sequences and Compute Basic Properties  
        Visualizing Sequence Properties  
    **Step 3**: Pairwise Alignments & Similarity Calculations  
    **Step 4**: Full Similarity Matrices and Heatmaps  
    **Step 5**: Build Phylogenetic Trees  
**Part 2**: Functional & Organism Prediction Pipeline   
