# Quality control, Filtering, and Clustering of Single-cell RNA data

## Introduction

Here we will take a hands-on approach and start with some of the first steps when working with single cell RNA sequencing data, in this case from the 10X platform.

## Data
We will be using publicly available data from the ['gut cell atlas'](https://www.gutcellatlas.org/#datasets), starting after the raw reads are converted into per-cell transcript counts via the 10X platform software. That earlier step (raw reads to the matrix) is done in a completely automated manner. It is interesting in and of itself (particularly when your experiment requires detection of non-standard genes, like transgenes or viral transcripts during an infection experiment). But we will start one step after that one, where things are decidedly less automated.

## Objective
For CD45+ preselected fraction cells, identify the cell types present.

## Learning Objectives
- Become familiar with accessing data via code
- Become familiar with 'big data' stored in the anndata format.
- Become familiar with filtering data via slicing of matricies.
- Get hands-on experience with the nuances of processing single cell data, including aspects that have subjective components.


## How to rerun it yourself:

### Prerequisites:
- A relatively recent version of python 3 (3.10 or later is best)

### Installation steps:
1. clone or download this repository.
If you have git installed you can do so in a terminal window via:
`git clone https://github.com/jgolob/immuno-850-scrna/`

2. Download the data files from the gut cell atlas and place them into the `jupyter/data` directory
- [Colon_cell_atlas.h5ad](https://cellgeni.cog.sanger.ac.uk/gutcellatlas/Colon_cell_atlas.h5ad)
- [Colon_immune_counts.mtx](https://cellgeni.cog.sanger.ac.uk/gutcellatlas/Colon_immune_counts.mtx)
- [Colon_immune_gene_names.csv](https://cellgeni.cog.sanger.ac.uk/gutcellatlas/Colon_immune_gene_names.csv)
- [Colon_immune_metadata.csv](https://cellgeni.cog.sanger.ac.uk/gutcellatlas/Colon_immune_metadata.csv)

3. Create a python virtual environment and install the needed packages
`python3 -m venv scrna`
`source scrna/bin/activate`
`pip3 install -r requirements.txt`

4. Go to the `jupyter` directory and activate the notebook
`jupyter notebook`



