---
layout: default
title: Documentation
nav_order: 2
---

## Documentation

The bioinformatics pipeline available as [Colab notebook](https://colab.research.google.com/github/luquelab/bioinformatics-teamCanes/blob/main/notebooks/main_pipeline.ipynb) has an extensive documentation for each step. For convenience, the documentation is also included here.  

The pipeline integrates several stages of analysis — from calculating basic sequence properties such as length and GC content, to advanced tasks like pairwise alignments, phylogenetic tree construction, and functional and origin organismal prediction using online tools such as NCBI BLASTx and EMBL-EBI HMMER (using Pfam database). It also includes data visualization outputs like bar plots and heatmaps, helping users to intuitively interpret sequence similarities and evolutionary patterns.  

All outputs are organized into clearly defined folders, making it easier to track each stage of the analysis. Whether you're a student learning the basics of sequence analysis or a researcher conducting high-throughput comparisons, this pipeline offers a robust and modular foundation to support a wide range of genomic investigations.     

---

## Pipeline overview  

The first code block installs Biopython and imports necessary libraries and modules that are required for uninterrupted analysis of sequences, visualization of graphs and plots, recording of results, saving of output files in proper directories.  

### Directory Structure Setup  

This code block sets up the structure of the output directories each containing the results from a specific analysis/part of the pipeline. The default name of the root directory is **project_x_analysis** and can be modified by the user.  

---

## Part 1: Sequence Analysis Pipeline    
This portion of the pipeline performs analyses on sequences of interest provided by the user. The analyses include calculation and visualization of some of the sequence properties such as sequence length and GC content, sequence alignments and similarities, as well as construction of phylogenetic trees.  

### Step 1: Upload and Store Sequences File   

A user is directed to upload a fasta file with DNA sequences of interest. The uploaded file is also saved in /data folder of the root directory for user's convenience.   


### Step 2: Load Sequences and Compute Basic Properties    
The code block here:  
- Loads the sequences from the uploaded FASTA file.  
- Calculates the length (in bp and kb) and GC content for each sequence.   
- Translates each nucleotide sequence into a protein sequence (translation halts at the first stop codon).  
- Saves these computed properties into a CSV file.  
- Visualizes sequence properties by generating bar charts for sequence lengths and GC content. Each figure is saved as a high-resolution PNG in the **sequence_properties** folder.  


### Step 3: Pairwise Alignments & Similarity Calculations     
The code block here calculates the percent identity between pairs of sequences of interest by:  
- Performing pairwise alignments (global alignments for both nucleotide and protein sequences).  
- Calculating percent identity from the alignments.  
- Saving the results in a CSV file along with the formatted alignments.  


### Step 4: Full Similarity Matrices and Heatmaps    
The code here:  
- Generates full similarity matrices for nucleotide and protein sequences by computing pairwise percent identities.  
- Saves the matrices as CSV ciles and visualizes them as heatmaps.   

### Step 5: Build Phylogenetic Trees   
This code block uses computed similarity matrices to   
- Obtain distance matrices.  
- Construct phylogenetic trees (neighbor-joining trees) for both nucleotide and protein sequences.  
- Save the trees in Newick format and tree visualizations in PNG format.  


## Part 2: Functional & Organism Prediction Pipeline     
This portion of the pipeline leverages online tools to predict the function and organismal origin of the sequences of interest.     
The workflow includes:  
- BLAST Search: each sequence of interest is used to perform a BLASTx search against the NCBI database. The resulting XML files are parsed to extract hit definitions and predicted organism information.  
- HMMER Search: an online HMMER search (against the Pfam database) is conducted using the translated protein sequence to predict domain structures. The predictions are then aggregated and saved into CSV files.   
- Output file organization: functional prediction files are copied to organism-specific folders for further analysis.  
