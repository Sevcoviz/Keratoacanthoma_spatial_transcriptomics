# Keratoacanthoma Spatial Transcriptomics Analysis

This repository contains code and resources for my diploma thesis project on spatial transcriptomics analysis of human skin tissue. 

## Project Overview
The goal of this project is to preprocess, visualize, and perform exploratory analysis of spatial transcriptomics data to investigate spatial gene expression patterns in keratoacanthoma in comparison to cutaneous squanous cell carcinoma and healthy tissue. 

## Current work
- analysis of Xenium In Situ Gene Expression data for adult human skin sections using the Xenium Human Multi-Tissue and Cancer Panel publicaly available at: https://www.10xgenomics.com/datasets/human-skin-data-xenium-human-multi-tissue-and-cancer-panel-1-standard
  * see notebooks/00_initial_look_at_dataset.ipynb
- notes for latest articles
  * ~/docs/theory/articles/01_Prakrithi2025/notes_01.md, see https://skincanceratlas.com/
  * ~/docs/theory/articles/03_Veenstra2023/Veenstra2023.md, Comparison of Keratoacanthoma and cSCC using single-cell spatial pathology
- dataset loading and preprocessing (see ~/notebooks/00_initial_look_at_dataset.ipynb)

## Planned Features
- **Data analysis from the 01_Prakrithi2025 article**, see: https://www.ebi.ac.uk/biostudies/ArrayExpress/studies/E-MTAB-11932?query=skin
- Utilize Python and also R 
- Additional analyses as the project develops 

## How to Use
Clone the repository:
```bash
git clone https://github.com/Sevcoviz/Keratoacanthoma_spatial_transcriptomics.git
cd Keratoacanthoma_spatial_transcriptomics
