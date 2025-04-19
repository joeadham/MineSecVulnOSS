# MineSecVulnOSS - Data-Driven Software Course Project
Tool to detect and analyze security vulnerabilities in open-source software repositories.

## Overview
This project explores the use of temporal and source code features to predict software vulnerabilities. I implement and compare three approaches:

- **Classical ML models** (Random Forest, Fully Connected Neural Network) trained on:
  - **Temporal features** (commit history statistics)
  - **Code features** (CodeBERT embeddings of function code)
  - **Combined (hybrid)** features
- **Fine-tuned CodeBERT** for sequence classification on function code

## Prerequisites
- Google Colab account with GPU runtime enabled (free tier)
- Google Drive account (to store data files)
- Python 3.x runtime in Colab
- Files:
  - `Data_driven_software_course_project.ipynb` (this notebook)
  - `megavul_simple.json` (dataset downloaded from the provided OneDrive link)

## Setup Instructions

### 1. Upload Files to Google Drive
1. Download `megavul_simple.json` from the OneDrive link:  
   https://1drv.ms/u/c/6CFE4123EACEEBDC/AdzrzuojQf4ggGxzcgAAAAA?e=OOLXLG  
2. Place the `megavul_simple.json` into your Google Drive (e.g., under `MyDrive/`).

### 2. Run the Notebook Cells

If you have correctly uploaded the dataset, and set the runtime to GPU, you can run the notebook cells in order. The notebook is structured as follows:

### Notebook Structure

#### 1. Exploratory Data Analysis (EDA) & Visualization
- Dataset information and summary
- Handling missing values
- Function-length distribution analysis

#### 2. Feature Engineering
- Temporal statistics extraction per file/repository
- Code embeddings generation using CodeBERT
- Dimensionality reduction with PCA

#### 3. Model Training & Evaluation
- Training Random Forest and Fully Connected Neural Network (FCN) models on:
    - Temporal features
    - Code features
    - Combined (hybrid) features
- Fine-tuning CodeBERT for sequence classification

#### 4. Results Comparison
- Evaluation metrics: Precision, Recall, F1-Score, and ROC-AUC
- Comparative analysis of model performance
