# Predictive Modeling of Customer Churn with Explainable Machine Learning

This project presents an end-to-end machine learning workflow for predicting
customer churn using supervised classification models. The analysis focuses not
only on predictive performance, but also on model interpretability and informed
model selection.

---

## Project Overview

Customer churn prediction is a classic binary classification problem with strong
business relevance. The goal of this project is to identify customers who are
likely to leave a service, while maintaining a clear understanding of the factors
driving these predictions.

The project follows a structured analytical pipeline:
- exploratory data analysis
- feature engineering and preprocessing
- baseline and advanced model training
- model explainability
- comparative model evaluation

---

## Dataset

The project uses the **Telco Customer Churn Dataset** provided by IBM and publicly
available on Kaggle.

The dataset is not included in this repository. Download instructions are provided
in:

data/requirements.txt


After downloading, the dataset should be placed at:


data/raw_data.csv


---

## Project Structure


notebooks/
01_eda.ipynb - Exploratory data analysis and hypothesis generation
02_feature_engineering.ipynb - Data preprocessing and feature engineering
03_logistic_regression.ipynb - Baseline linear model
04_gradient_boosting.ipynb - Non-linear ensemble model
05_random_forest.ipynb - Alternative ensemble approach
06_explainability_logistic.ipynb - Model interpretability analysis (logistic regression)
07_model_comparison_and_explainability.ipynb - Comparative analysis and final model selection


---

## Models Evaluated

The following models were trained and evaluated using the same preprocessing
pipeline and data split:

- Logistic Regression (baseline, high interpretability)
- Gradient Boosting (non-linear ensemble model)
- Random Forest (tree-based ensemble model)

---

## Evaluation Metrics

Due to class imbalance, model performance is primarily evaluated using:
- ROC-AUC (primary metric)
- Recall for churned customers
- Precision and accuracy for additional context

---

## Key Results

| Model               | ROC-AUC | Recall (Churn) | Accuracy |
|---------------------|--------:|---------------:|---------:|
| Logistic Regression | 0.842   | 0.56           | 0.81     |
| Gradient Boosting   | 0.846   | 0.51           | 0.80     |
| Random Forest       | 0.829   | 0.49           | 0.80     |

Gradient Boosting achieves the best overall discriminative performance, while
Logistic Regression provides the highest interpretability and a strong baseline.

---

## Model Explainability

Model interpretability is addressed through coefficient analysis for Logistic
Regression and comparative discussion across all evaluated models.

Key churn drivers identified include:
- contract type (short-term contracts increase churn risk)
- customer tenure (longer tenure reduces churn probability)
- pricing-related variables

The analysis highlights the trade-off between predictive power and transparency
when selecting models for real-world deployment.

---

## Conclusion

This project demonstrates a structured and interpretable approach to customer
churn prediction, emphasizing both model performance and explainability.

Gradient Boosting is selected as the preferred model based on ROC-AUC, while
Logistic Regression remains essential for transparent interpretation and business
communication.

---

## Future Work

Potential extensions include:
- probability threshold tuning to optimize churn recall
- advanced explainability techniques (e.g., SHAP) for ensemble models
- cost-sensitive evaluation aligned with business objectives

---

## Requirements

All Python dependencies are listed in:

requirements.txt
