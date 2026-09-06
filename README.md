# Banknote Authentication Analysis

Binary classification benchmark authenticating genuine vs. forged banknotes using continuous wavelet transform features.

---

## Overview

* **Task:** Supervised binary classification on the UCI Banknote Authentication dataset.
* **Dataset:** 1,372 records, 4 continuous numerical features, zero missing cells.
* **Evaluation:** Stratified cross-validation and holdout evaluation against baseline models.
* **Target:** Authentic (0) vs. Forged (1).

---

## Data Summary

* **Source:** [UCI Machine Learning Repository — Banknote Authentication](https://archive.ics.uci.edu/dataset/267/banknote+authentication)
* **Features:**
  * `variance`: Variance of Wavelet Transformed image
  * `skewness`: Skewness of Wavelet Transformed image
  * `curtosis`: Curtosis of Wavelet Transformed image
  * `entropy`: Entropy of image
* **Quality Check:** 1,372 total records, 0 missing values, zero duplicates removed.

---

## Visualizations

| Data Quality & Target | Feature Distributions |
| :---: | :---: |
| ![Data Quality](figures/data-quality.png) | ![Distributions](figures/distributions.png) |

| Feature Correlations | Model Comparison |
| :---: | :---: |
| ![Correlations](figures/correlations.png) | ![Model Comparison](figures/model-comparison.png) |

---

## Repository Structure

```text
├── figures/                   # Diagnostic, distribution, and evaluation plots
├── analysis.ipynb             # Interactive walk-through and evaluation notebook
├── audit.json                 # Run hashes and reproducible environment metadata
├── data_dictionary.csv        # Feature types, boundaries, and descriptions
├── descriptive_statistics.csv # Summary distribution stats per feature
├── feature_importance.csv     # Permutation importance rankings
├── metrics.json               # Full CV and holdout validation scores
└── README.md
