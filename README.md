# Survival Analysis and Machine Learning Predictive Modeling

This repository contains a comprehensive suite of **Survival Analysis** and **Machine Learning** models built to predict time-to-event outcomes and analyze hazard rates. It compares traditional statistical frameworks, parametric Accelerated Failure Time (AFT) models, and modern gradient-boosting machine learning techniques.

## 🛠️ Models Implemented

The project implements and evaluates the following six survival modeling techniques:

* **Kaplan-Meier (KM):** Non-parametric estimator used to estimate the survival function from life-table data and visualize baseline survival curves.
* **Cox Proportional Hazards (Cox PH):** Semi-parametric model targeting how specific covariates multiply the baseline risk/hazard.
* **Weibull AFT:** Parametric Accelerated Failure Time model assuming the baseline hazard follows a Weibull distribution.
* **Log-Logistic AFT:** Parametric model where the hazard rate increases initially and decreases later, useful for non-monotonic hazard shapes.
* **Log-Normal AFT:** Parametric model assuming log-transformed survival times are normally distributed.
* **XGBoost Survival:** Advanced gradient-boosted decision trees optimized for survival data using specialized loss functions (e.g., Cox objective or AFT objective).

## 🚀 Getting Started

### Prerequisites
Ensure you have Python 3.8+ installed. The primary libraries used in this project are `lifelines`, `scikit-survival` (or `xgboost`), `pandas`, and `numpy`.

### Installation
Clone this repository and install the required dependencies:

```bash
git clone https://github.com
cd YOUR_REPOSITORY_NAME
pip install -r requirements.txt
```

## 📊 Model Evaluation Summary

The models are compared using evaluation metrics suitable for censored data, primarily the **Concordance Index (C-index)** and **Brier Score** (where applicable).

| Model Type | Model Name | C-Index (Train) | C-Index (Test) | Key Assumptions / Strengths |
| :--- | :--- | :---: | :---: | :--- |
| **Non-Parametric** | Kaplan-Meier | *N/A* | *N/A* | No assumptions; strictly for baseline visualization. |
| **Semi-Parametric**| Cox Proportional Hazards | `0.XX` | `0.XX` | Assumes constant hazard ratios over time. |
| **Parametric (AFT)**| Weibull AFT | `0.XX` | `0.XX` | Assumes monotonic hazard (either strictly increasing or decreasing). |
| **Parametric (AFT)**| Log-Logistic AFT | `0.XX` | `0.XX` | Handles non-monotonic, unimodal hazard rates. |
| **Parametric (AFT)**| Log-Normal AFT | `0.XX` | `0.XX` | Useful when risk peaks early and degrades slowly. |
| **Machine Learning**| XGBoost Survival | `0.XX` | `0.XX` | Captures complex non-linear relationships and interactions. |

*(Note: Replace `0.XX` with your actual model performance scores.)*

## 📁 Repository Structure

```text
├── data/                  # Dataset directory (raw and processed)
├── notebooks/             # Jupyter notebooks for EDA and model training
├── src/                   # Source code for data preprocessing and utility functions
├── requirements.txt       # Python dependencies
└── README.md              # Project documentation
```

## 📈 Key Insights & Results
* **Best Performing Model:** [Insert model name, e.g., XGBoost Survival] achieved the highest predictive accuracy with a C-index of `0.XX`.
* **Proportional Hazards Check:** [Briefly mention if your data satisfied the Cox PH assumption or if AFT models performed better because of it].
* **Feature Importance:** Top drivers influencing the hazard rate/survival time included `[Feature 1]`, `[Feature 2]`, and `[Feature 3]`.

## 🤝 Contributing
