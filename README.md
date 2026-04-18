# 🧬 Integrative Analysis of Gene Expression and Genetic Variants for Lung Cancer Classification

<p align="center">
  <img src="gene.jpeg" alt="Gene Visualization" width="400"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8+-blue.svg"/>
  <img src="https://img.shields.io/badge/Machine%20Learning-Random%20Forest%20%7C%20SVM%20%7C%20LogReg-orange"/>
  <img src="https://img.shields.io/badge/Bioinformatics-GEO%20%7C%20ClinVar-green"/>
</p>

A comprehensive bioinformatics and machine learning pipeline that integrates genetic variant data with gene expression profiles to classify lung normal vs. tumor tissues and discover key biomarker genes.

## 📖 Project Overview

This project bridges rule-based bioinformatics analysis with advanced machine learning to uncover molecular signatures in lung cancer. We analyze gene expression microarray data (GEO) alongside clinically relevant genetic variants (ClinVar) to rank genes based on their mutation risk and expression variation. A suite of machine learning models is then trained to classify patient samples (Tumor vs. Normal) purely based on gene expression profiles.

### ✨ Key Features

- **Interactive Gene Intelligence Dashboard**: Explore a live volcano plot, filterable gene ranking table, and pathway networks with AI-powered clinical context integration.
- **Data Integration Pipeline**: Seamlessly merges GEO expression data (120 samples, 54,675 probes) with ClinVar lung cancer variants.
- **Machine Learning Classification**: Models including Random Forest, Logistic Regression, and Support Vector Machines (SVM) are trained to diagnose tumor samples. 
- **Explainable AI (Feature Importance)**: Extracts exactly *which* genes the model utilized for classification, validating computational results against existing bioinformatics literature.
- **Comprehensive Evaluation**: Includes Confusion Matrices, ROC-AUC Curves, 5-Fold Cross-Validation, and Principal Component Analysis (PCA) for robust validation.

## 🧠 Machine Learning Pipeline

1. **Feature Extraction**: Identification of the top 100 most variable gene probes across the dataset.
2. **Preprocessing**: Normalization using `StandardScaler` and 80/20 train-test splitting.
3. **Model Training**: Comparing Random Forest (primary model), SVM, and Logistic Regression.
4. **Validation**: 5-Fold Cross Validation validates performance reliability.
5. **Dimensionality Reduction**: Visualising sample separation with PCA in 2D space.

## 📂 Repository Structure

- `lung_cancer_with_ML.ipynb` - The core functional Jupyter Notebook containing the full bioinformatics data processing and machine learning pipeline.
- `lung_cancer_dashboard.html` *(Generated)* - Interactive browser dashboard for gene visualisations.
- _Datasets (e.g., GEO matrix and ClinVar datasets) are integrated to provide biologically meaningful inputs._

## 📊 Results & Biological Validation

Our Random Forest classifier successfully learns the distinction between healthy lung tissue and lung tumor tissue. Furthermore, mapping the most "important" features from the Random Forest back to biological genes directly and independently re-discovers clinically significant lung cancer biomarkers.

## 🛠️ Tech Stack & Requirements

- **Language:** Python
- **Data Manipulation:** `pandas`, `numpy`
- **Machine Learning:** `scikit-learn` (`RandomForestClassifier`, `PCA`, etc.)
- **Visualisation:** `matplotlib`, `seaborn`
- **Dashboard:** Interactive HTML/JS generated via Python.

## 🚀 How to Use

1. Clone this repository to your local machine.
2. Ensure you have the necessary dependencies:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn
   ```
3. Open `lung_cancer_with_ML.ipynb` using Jupyter Notebook, JupyterLab, or VS Code.
4. Run all cells sequentially to process the data, evaluate the ML models, and produce the Interactive Dashboard.

---
*Created by [Kumaraswamy](https://github.com/Kumar070204).*
