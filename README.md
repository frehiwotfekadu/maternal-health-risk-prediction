# Maternal Health Risk Prediction (Submission Repository)

## Overview
This repository contains the implementation supporting the coursework report on antenatal hypertensive risk stratification using interpretable machine learning.

The primary objective is to predict **maternal high-risk status** using routinely collected physiological variables, with an explicit focus on **recall optimization** and **clinical interpretability**. Logistic Regression is the selected deployment model, benchmarked against a Random Forest to establish a performance ceiling.

---

## Repository Contents
- `maternal_risk_model.ipynb`  
  Submission-safe Jupyter Notebook containing:
  - Data loading and validation
  - Exploratory and bivariate analysis
  - Feature engineering (Mean Arterial Pressure)
  - Logistic Regression model training
  - Threshold optimization (recall-focused)
  - Model evaluation, calibration, and odds ratios
  - Random Forest benchmark (non-deployed comparator)

- `Maternal Health Risk Data Set.csv`  
  Original dataset (Kaggle, 2020), included for reproducibility.

- `README.md`  
  Instructions for running the notebook and interpreting outputs.

---

## Requirements
The notebook was developed using Python 3.10+ with the following core libraries:

- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- scipy
- statsmodels

All libraries are standard within common scientific Python distributions (e.g., Anaconda).

---

## How to Run
1. Clone the repository:
   ```bash
   git clone <https://github.com/frehiwotfekadu/maternal-health-risk-prediction.git>
   cd <maternal-health-risk-prediction>
   ```

2. Open the notebook:
   ```bash
   jupyter notebook maternal_risk_model.ipynb
   ```

3. Run all cells sequentially from top to bottom.
   - No manual parameter tuning is required.
   - All random states are fixed for reproducibility.

---

## Expected Outputs
Running the notebook will produce:

- Dataset summary confirming no missing values (N = 808)
- Class distribution counts (Low vs High risk)
- Correlation heatmap demonstrating BP multicollinearity (r ≈ 0.87)
- Bivariate statistical comparison (High vs Low risk groups)
- Logistic Regression performance metrics:
  - Recall, Precision, Accuracy (default and optimized thresholds)
  - Confusion matrix
  - Calibration curve
- Adjusted Odds Ratios for all predictors
- Random Forest benchmark metrics (training and cross-validation)

All reported figures and statistics in the written report are directly reproducible from this notebook.

---

## Reproducibility Statement
This analysis is fully reproducible. The dataset is included, preprocessing is deterministic, and all models use fixed random seeds. No external data sources or manual interventions are required. Reported numerical results may vary only at the third decimal place due to floating-point precision.

---

## Methodological Notes
- The Random Forest model is included strictly as a **comparative benchmark** and is **not** the selected deployment model.
- Logistic Regression was intentionally chosen to balance predictive performance with global interpretability and clinical auditability.
- Threshold optimization was performed on training data only to avoid test leakage.

---

## Data Source
Maternal Health Risk Data Set. Kaggle (2020).  
Available at: https://www.kaggle.com/datasets/csafrit2/maternal-health-risk-data-set
