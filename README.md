# Week 1: Data Acquisition and Preprocessing

## Project Overview
This repository contains the revised submission for **Week 1** of the Data Science virtual internship at **Yuva Intern**. The objective is to design and execute a robust data acquisition, cleaning, missing value imputation, outlier mitigation, and feature engineering pipeline on the authentic **Titanic passenger manifest dataset**.

---

## Technical Highlights
* **Ingestion & Profiling:** Ingested 891 records across 12 raw features, documenting multi-modal distributions and target imbalances (61.6% perished vs 38.4% survived).
* **Advanced Imputation:** Replaced global mean imputation with conditional grouped medians based on passenger class (`Pclass`) and honorific title (`Title`). Mode imputation was applied for departure port (`Embarked`).
* **Sparsity Handling:** Transformed the sparse `Cabin` attribute (77.1% missing) into an informative binary indicator (`Has_Cabin`).
* **Outlier Mitigation:** Evaluated skewed expenditures via Interquartile Range (IQR threshold = 65.63). Mitigated extreme variance via 99th percentile Winsorization and natural logarithmic scaling (`Fare_Log = ln(1 + Fare)`).
* **Matrix Preparation:** Encoded nominal attributes with dummy indicators (`drop_first=True`) and applied `StandardScaler` to continuous dimensions.

---

## Repository Files
```text
├── data_preprocessing.py        # Complete end-to-end Python pipeline
├── preprocessing_eda_plots.png  # Exploratory and distribution diagnostic plots
└── README.md                    # Technical documentation
