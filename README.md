# IRB Credit Risk Modeling – Synthetic PD & LGD Datasets

This repository contains synthetic datasets and notebooks designed to simulate key concepts in IRB credit risk modeling, with a focus on:

- PD (Probability of Default)  
- LGD (Loss Given Default)  

Both are central components in regulatory and internal risk quantification frameworks.

## 1. PD Modeling

The PD dataset (`pd_dataset_easy.csv`) is snapshot-based, with one row per customer per year.  
It is structured to support standard IRB-level PD model development and validation:

- Feature engineering on customer-level attributes  
- Default flag creation  
- Statistical validation: monotonicity, binning, KS tests, and more  

See: `IRB_PD.ipynb`

## 2. LGD Modeling

In progress

## 2. EAD Modeling

In progress
