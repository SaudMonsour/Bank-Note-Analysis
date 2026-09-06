# Banknote Authentication Analysis

**Binary Classification · Machine Learning Benchmark**

Supervised learning analysis to authenticate genuine vs. forged banknotes using statistical continuous wavelet transform features.

---

## Overview

* **Objective:** Classify banknote authenticity based on wavelet transform variance, skewness, kurtosis, and entropy.
* **Dataset:** 1,372 records, 4 continuous features.
* **Evaluation:** Stratified train/test holdout evaluated against baseline classifiers.
* **Key Artifacts:** Preprocessing pipeline, cross-validation metrics, and permutation importance.

---

## Data Summary

* **Source:** UCI Machine Learning Repository (Banknote Authentication)
* **Features:**
  * `variance`: Variance of Wavelet Transformed image
  * `skewness`: Skewness of Wavelet Transformed image
  * `curtosis`: Curtosis of Wavelet Transformed image
  * `entropy`: Entropy of image
* **Class Balance:** Binary distribution (Genuine vs. Forged) with zero missing entries.

---

## Visualizations

| Target & Distributions | Correlation Matrix |
| :---: | :---: |
| ![Distributions](figures/distributions.png) | ![Correlations](figures/correlations.png) |

| Model Performance | Error / Diagnostics |
| :---: | :---: |
| ![Model Comparison](figures/model-comparison.png) | ![Error Analysis](figures/error-analysis.png) |

---

## Repository Structure

```text
├── figures/                   # Distribution, correlation, and model plots
├── analysis.ipynb             # End-to-end interactive exploration notebook
├── audit.json                 # Pipeline metadata and reproducibility hash
├── data_dictionary.csv        # Column specifications and descriptive ranges
├── descriptive_statistics.csv # Summary statistics for each predictor
├── error_analysis.csv         # Holdout predictions and misclassification logs
├── feature_importance.csv     # Model-level permutation importance
├── metrics.json               # Full evaluation scores
└── README.md
