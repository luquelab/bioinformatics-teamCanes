---
layout: default
title: Tutorial
nav_order: 3
---
## Tutorial

This tutorial provides an overview of running project's bioinformatics pipeline on a [sample data](https://github.com/luquelab/bioinformatics-teamCanes/tree/main/examples/sequences.fasta) obtained from [NCBI](https://www.ncbi.nlm.nih.gov/). The expected output is provided in [examples/output](https://github.com/luquelab/bioinformatics-teamCanes/tree/main/examples/output) folder. 

## Running the Bioinformatics Pipeline via Google Colab

1. Open the [Colab notebook](https://colab.research.google.com/github/luquelab/bioinformatics-teamCanes/blob/main/notebooks/main_pipeline.ipynb) containing the Bioinformatics Pipeline. The pipeline is composed of multiple well documented steps explaining performed analyses and resulting output files.  
2. In the top menu, select `Runtime` > `Run all` to run the whole pipeline. Alternatively, run code blocks one by one starting with the top block that installs packages required for proper functioning of the pipeline.  
3. Navigate to **Part 1. Step 1: Upload and Store Sequences File** and upload the fasta file with sample DNA sequences when prompted.  
4. Access and analyze generated output files as pipeline runs or wait until the whole pipeline finishes. It may take up to 15-30 minutes due to BLAST and HHMER searches that predict the function of your sequences and their organismal origin.   
5. The **results** folder (located in your specified root directory or default **project_x_analysis** directory, if not modified) contains sub-folders with outputs for analyses performed on different steps of the pipeline.   
6. Download individual output files from their corresponding directories or download the whole generated output directory (**project_x_analysis** or **project_x_analysis/results**).  
7. Compare your results to the output provided in [examples/output](https://github.com/luquelab/bioinformatics-teamCanes/tree/main/examples/output) folder.   
