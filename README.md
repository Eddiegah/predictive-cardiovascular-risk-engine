# 🫀 Predictive Cardiovascular Risk Engine
> High-Dimensional Clinical Data Engineering & Machine Learning Pipeline for 10-Year CHD Risk Stratification.


The **Predictive Cardiovascular Risk Engine** is an enterprise-grade data engineering and predictive modeling framework designed to isolate, preprocess, and optimize patient clinical metrics from the longitudinal Framingham dataset. Its core objective is to deliver structurally pristine data arrays optimized for training high-sensitivity classifiers predicting the 10-year risk of Coronary Heart Disease (CHD).

---

## 🛠️ Core Architecture & Technical Highlights

This system isolates the foundational data engineering layer required to feed robust machine learning classification algorithms, implementing strict mathematical and structural transformations to ensure maximum algorithmic compatibility and computational efficiency.

* **Deterministic Feature Pruning:** Systematic elimination of low-variance/sociodemographic parameters (`education`) to minimize multi-collinearity, prevent overfitting, and optimize model generalization.
* **Structural Feature Re-mapping:** Vectorizing categorical structural variables (`male` $\rightarrow$ `Sex_male`) to establish seamless algorithmic compatibility with advanced distance-based and gradient-boosted classifiers.
* **Stochastic Noise Mitigation:** Implementation of a rigorous row-wise missingness exclusion strategy (`dropna`) to preserve original statistical distribution profiles while eliminating corrupt data vectors.
* **Statistical Profiling (EDA):** Deep-dive exploratory pipelines leveraging matrix correlations, feature variance testing, and covariate tracking via optimized Seaborn and Matplotlib visualization engines.

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
│  • Binary Vectorization: male -> Sex_male    │
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
