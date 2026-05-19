# 🫀 Predictive Cardiovascular Risk Engine

[![Python Version](https://img.shields.shields.shields.shields.shields.shields.io/badge/python-3.10%2B-blue.svg)](https://www.python.org/)
[![Framework](https://img.shields.shields.shields.shields.shields.shields.io/badge/Framework-Scikit--Learn-orange.svg)](https://scikit-learn.org/)
[![Pipeline](https://img.shields.shields.shields.shields.shields.shields.io/badge/Pipeline-Verified-success.svg)]()

A high-performance, end-to-end data engineering and predictive modeling architecture designed to evaluate, preprocess, and predict the 10-year risk of coronary heart disease (CHD) utilizing clinical patient metrics from the structural Framingham dataset.

---

## 🛠️ Core Architecture & Technical Highlights

This repository isolates the foundational data engineering layer required to feed robust machine learning classification algorithms. 

* **Deterministic Feature Pruning:** Systematic elimination of low-variance/non-predictive parameters (`education`) to minimize multi-collinearity and optimize computational efficiency.
* **Structural Feature Re-mapping:** Vectorizing categorical structural variables (`male` $\rightarrow$ `Sex_male`) to establish algorithmic compatibility with advanced distance-based and gradient-boosted classifiers.
* **Missing Data Mitigation:** Implementation of a rigorous row-wise missingness exclusion strategy (`dropna`) to preserve statistical distribution profiles while eliminating stochastic noise.
* **Statistical Visualization:** Deep-dive exploratory data analysis (EDA) leveraging matrix correlations, feature distributions, and variance testing via optimized Seaborn pipelines.

---

## 📊 Pipeline Blueprint

```text
[Raw Dataset: framingham.csv] 
          │
          ▼
[Feature Engineering Layer] ──► Drop 'education' (Dimensionality Reduction)
          │
          ▼
[Structural Realignment]   ──► Map 'male' to 'Sex_male' (Binary Vectorization)
          │
          ▼
[Stochastic Cleansing]     ──► Row-wise NA Elimination (Variance Preservation)
          │
          ▼
[Downstream Modeling]      ──► Engine Ready for Training (RFC, XGBoost, LogReg)
git clone [https://github.com/Eddiegah/predictive-cardiovascular-risk-engine.git](https://github.com/Eddiegah/predictive-cardiovascular-risk-engine.git)
cd predictive-cardiovascular-risk-engine
pip install -r requirements.txt
jupyter notebook Heart_Disease_Detection.ipynb
'docs:upgrade docomentation to enterprise standard' as the commit message
