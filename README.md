# 🫀 Predictive Cardiovascular Risk Engine

<p id="badges">
  <img src="https://img.shields.shields.shields.io/badge/python-3.10%2B-blue.svg?style=for-the-badge&logo=python&logoColor=white" alt="Python Version"/>
  <img src="https://img.shields.shields.shields.shields.shields.io/badge/Framework-Scikit--Learn-orange.svg?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Framework"/>
  <img src="https://img.shields.shields.shields.shields.shields.io/badge/Pipeline-Verified-success.svg?style=for-the-badge" alt="Pipeline"/>
</p>

Custom Data Engineering Pipeline & High-Dimensional Predictive Modeling designed to evaluate, preprocess, and optimize patient clinical metrics from the structural Framingham dataset for predicting the 10-year risk of coronary heart disease (CHD).

---

## 🛠️ Core Architecture & High-End Technical Highlights

This repository isolates the foundational data engineering layer required to feed robust machine learning classification algorithms. It implements strict data transformations to ensure maximum algorithmic compatibility and computational efficiency.

* **Deterministic Feature Pruning:** Systematic elimination of low-variance/non-predictive parameters (`education`) to minimize multi-collinearity and optimize model generalization.
* **Structural Feature Re-mapping:** Vectorizing categorical structural variables (`male` $\rightarrow$ `Sex_male`) to establish algorithmic compatibility with advanced distance-based and gradient-boosted classifiers.
* **Stochastic Noise Mitigation:** Implementation of a rigorous row-wise missingness exclusion strategy (`dropna`) to preserve original statistical distribution profiles while eliminating corrupt data points.
* **Exploratory Data Analysis (EDA):** Deep-dive statistical profiling leveraging matrix correlations, feature variance testing, and covariate tracking via optimized Seaborn and Matplotlib pipelines.

---

## 📊 End-to-End Pipeline Blueprint

```text
[ Raw Dataset: framingham.csv ]
               │
               ▼
┌──────────────────────────────────────────────┐
│          Feature Engineering Layer           │
│  • Dimensionality Reduction: Drop education  │
└──────────────────────────────────────────────┘
               │
               ▼
┌──────────────────────────────────────────────┐
│         Structural Realignment Layer         │
│  • Binary Vectorization: male -> Sex_male     │
└──────────────────────────────────────────────┘
               │
               ▼
┌──────────────────────────────────────────────┐
│          Stochastic Cleansing Layer          │
│  • Row-wise NA Elimination                   │
└──────────────────────────────────────────────┘
               │
               ▼
┌──────────────────────────────────────────────┐
│          Downstream Modeling Engine          │
│  • Fully Prepared for RFC, XGBoost, LogReg   │
└──────────────────────────────────────────────┘
