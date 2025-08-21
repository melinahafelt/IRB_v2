# IRB Credit Risk Modeling – Synthetic PD, LGD & EAD Datasets
This repository contains synthetic datasets and Jupyter notebooks designed to simulate core concepts in **Internal Ratings-Based (IRB)** credit risk modeling.  
It is intnded for educational and demonstration purposes only, showcasing the full lifecycle of model development and validation.

The three core IRB parameters covered are:
- **PD (Probability of Default)**  
- **LGD (Loss Given Default)**  
- **EAD (Exposure at Default)**  
Together, these components form the foundation of regulatory capital estimation under Basel II/III.

## 1. PD Modeling
**Dataset:** `pd_dataset_easy.csv` (snapshot-based, one row per customer per year).  
**Notebook:** `IRB_PD.ipynb`  

Key features:
- Data preparation: missing values, duplicate handling, and risk driver review  
- Feature engineering: categorical encoding, Weight of Evidence (WoE), scaling  
- Statistical validation: monotonicity checks, KS tests, AUROC, calibration analysis  
- Model evaluation with logistic regression, stress testing, and validation "traffic light" summary  

## 2. LGD Modeling
**Notebook:** `IRB_LGD.ipynb` (work in progress)  

Planned scope:
- Recovery rate distributions and transformations  
- Segmentation by collateral and product type  
- Regression-based LGD estimation (e.g., OLS, Beta regression)  
- Validation metrics: RMSE, calibration across buckets, discriminatory power  

## 3. EAD Modeling
**Dataset:** `ead_dataset.csv`  
**Notebook:** `IRB_EAD.ipynb`  

Key features:
- Exploratory analysis of exposure profiles and utilization rates  
- Application of Credit Conversion Factors (CCF)  
- Feature engineering: transformations, scaling, and encoding  
- Regression modeling of EAD (XGBoost regressor)  
- Model diagnostics: prediction error distribution, calibration checks  
- Scenario-based stress testing and average predicted EAD  

---

## <span style="color:red">Disclaimer</span>  
All datasets in this repository are **synthetically generated** for demonstration purposes only.  
They **do not represent any real financial institution’s data** and are not suitable for production use.  
The aim is purely to illustrate the **IRB methodology, data preparation, feature engineering, and validation** steps in a transparent and reproducible way.

---

## Improvement Notes / Prototype Limitations  

In this prototype, certain aspects were **hard-coded** rather than parameterized, which limits the model’s flexibility for repeated validations across multiple years.  

For example:  
- Instead of introducing a configurable variable such as `val_year = 2024` to dynamically control the validation year,  
  the year was hardcoded in parts of the workflow.  
- A more **generalized and modular approach** would have enabled easier reuse of the pipeline for future validation years (2025, 2026, …).  

This was a conscious trade-off made during the prototyping phase, as the focus was on demonstrating the **core IRB methodology and validation flow** rather than full automation.  
However, in a production-ready setting, parameterization should be prioritized to ensure scalability and reusability across different validation cycles.  


All datasets in this repository are **synthetically generated** for demonstration purposes only.  
They **do not represent any real financial institution’s data** and are not suitable for production use.  
The aim is purely to illustrate the **IRB methodology, data preparation, feature engineering, and validation** steps in a transparent and reproducible way.
