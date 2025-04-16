---
layout: default
title: Sequence Analysis & Functional Prediction
---

# Bioinformatics TeamCanes: Sequence Analysis and Functional Prediction Pipeline

Welcome to the official documentation for the **Sequence Analysis and Functional Prediction Pipeline** developed by the Bioinformatics TeamCanes at the Luque Lab. This site provides installation instructions, usage examples, technical details, and contribution guidelines.

---

## Overview

This pipeline is a comprehensive Google Colab-based notebook designed for the analysis of nucleotide sequences. It provides tools for sequence property analysis, visualization, alignments, phylogenetics, and functional prediction using BLAST and HMMER.

**Core Features:**
- Sequence uploading and preprocessing
- GC content and sequence length computation
- Visualization with heatmaps and bar charts
- Pairwise global alignments and percent identity
- Phylogenetic tree construction (nucleotide and protein)
- Functional and organism prediction via BLAST and HMMER
- Directory structure for organized outputs

---

## Installation Instructions

This pipeline is intended to run in [Google Colab](https://colab.research.google.com/). To get started:

1. Go to the [notebook](https://github.com/luquelab/bioinformatics-teamCanes/tree/main) in the GitHub repo.
2. Click `Open in Colab`.
3. Run the first cell to install required packages:
   ```python
   !pip install biopython lxml
   ```

---

## Usage Guide with Examples

### Example Dataset
You can test the pipeline using the included `sequences.fasta` file available in the [GitHub repository](https://github.com/luquelab/bioinformatics-teamCanes/tree/main). This file contains a small test dataset for validating each stage of the pipeline.

### Step 1: Upload Sequences
- Upload your FASTA file (e.g., `sequences.fasta`) using the Colab file upload widget:
  ```python
  from google.colab import files
  uploaded = files.upload()
  ```

### Step 2: Analyze Sequences
- Calculates length, GC content, and translates to protein.
- Saves:
  - `properties.csv`
  - `sequences_translated.faa`
  - Bar plots of length and GC content

### Step 3: Pairwise Alignments
- Performs pairwise global alignments for nucleotide and protein sequences.
- Outputs:
  - Formatted alignments (`.fna` and `.faa`)
  - Percent identity matrix (`sequence_similarities.csv`)

### Step 4: Heatmaps
- Generates similarity matrices and heatmaps:
  - `nucleotide_similarity_heatmap.png`
  - `protein_similarity_heatmap.png`

### Step 5: Phylogenetic Trees
- Constructs NJ trees using calculated distance matrices.
- Outputs:
  - `.nwk` Newick tree files
  - Tree visualizations (PNG)

### Step 6: Functional and Organism Prediction
- Performs online `BLASTx` and HMMER (Pfam):
  - Saves hit results, domain predictions, and organism predictions to CSVs
  - Copies outputs to organized folders for each sequence

### Step 1: Upload Sequences
- Upload your FASTA file (e.g., `sequences.fna`) using the Colab file upload widget.

### Step 2: Analyze Sequences
- Calculates length, GC content, and translates to protein.
- Saves:
  - `properties.csv`
  - `sequences_translated.faa`
  - Bar plots of length and GC content

### Step 3: Pairwise Alignments
- Performs pairwise global alignments for nucleotide and protein sequences.
- Outputs:
  - Formatted alignments (`.fna` and `.faa`)
  - Percent identity matrix (`sequence_similarities.csv`)

### Step 4: Heatmaps
- Generates similarity matrices and heatmaps:
  - `nucleotide_similarity_heatmap.png`
  - `protein_similarity_heatmap.png`

### Step 5: Phylogenetic Trees
- Constructs NJ trees using calculated distance matrices.
- Outputs:
  - `.nwk` Newick tree files
  - Tree visualizations (PNG)

### Step 6: Functional and Organism Prediction
- Performs online `BLASTx` and HMMER (Pfam):
  - Saves hit results, domain predictions, and organism predictions to CSVs
  - Copies outputs to organized folders for each sequence

---

## Technical Details

- **Programming Language:** Python (Biopython, Matplotlib, Numpy, Pandas)
- **Visualization:** Bar charts, heatmaps, phylogenetic trees (via Matplotlib & Biopython Phylo)
- **External APIs:**
  - NCBI BLAST
  - EMBL-EBI HMMER
- **File Structure:**
  ```
project_x_analysis/
    ├── data/
    ├── bin/
    ├── results/
    │   ├── sequence_properties/
    │   ├── alignments/
    │   ├── phylogenetic_tree/
    │   ├── functional_prediction/
    │   └── organism_origin/
  ```

## License

This pipeline is available under the MIT License.


