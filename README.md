# Tidy Machine Learning Models: Readmission and Stroke Risk Prediction

## Project Overview
This repository contains the implementation and analysis of predictive machine learning models for healthcare applications. The project focuses on:
1. **Predicting hospital readmission risks** within 30 days for diabetic inpatients using clinical data.
2. **Building and evaluating a stroke prediction model** using a similar machine learning workflow.

## Motivation
Hospital readmissions contribute to significant healthcare costs in the U.S., amounting to over $17 billion annually. This project leverages patient data, particularly glycated hemoglobin (HbA1c) levels, to predict readmissions. Additionally, the workflow is extended to analyze stroke prediction, showcasing the versatility of machine learning in healthcare.

---

## Dataset Information

### Readmission Dataset
- **Source**: Visual Automated Disease Analytics (VADA) summer school training, 2018.
- **Data Details**:
  - **Observations**: 69,984 inpatient visits.
  - **Features**: 27, including demographics, HbA1c levels, diagnostic tests, treatments, and outcomes.
  - **Time Period**: 1999–2008.
  - **Objective**: Predict the likelihood of readmissions within 30 days.

### Stroke Dataset
- **Purpose**: Build and evaluate a stroke prediction model.
- **Features**:
  - Numeric: Age, average glucose level, BMI.
  - Categorical: Gender, medical history, lifestyle factors.
  - Target: Stroke (binary).

---

## workflow

1. **Data Exploration and Preprocessing**:
   - Conducted summary statistics and data visualization.
   - Engineered features and transformed data.

2. **Data Splitting**:
   - Split data into training and testing datasets.
   - Applied cross-validation for robust model evaluation.

3. **Recipe Creation**:
   - Normalized numeric predictors.
   - One-hot encoded categorical features.
   - Removed zero-variance predictors.

4. **Model Specification**:
   - Implemented multiple machine learning models:
     - Logistic Regression
     - Decision Tree
     - Naive Bayes
     - Random Forest
     - k-Nearest Neighbors (k-NN)
     - Support Vector Machines (Linear & RBF Kernel)
     - XGBoost

5. **Hyperparameter Tuning**:
   - Performed grid search to optimize model performance.
   - Metrics: Accuracy, F1-score, sensitivity, specificity, ROC AUC.

6. **Model Selection and Evaluation**:
   - Compared model performances.
   - Selected logistic regression for readmission due to its interpretability and reliable metrics.

7. **Finalization and Prediction**:
   - Finalized the best model workflows.
   - Predicted outcomes for new data.

---

## Tools and Technologies
- **Programming Language**: R
- **Libraries**:
  - Data Manipulation and Visualization: `tidyverse`, `ggplot2`, `GGally`
  - Machine Learning: `tidymodels`, `caret`, `glmnet`, `xgboost`, `ranger`, `kernlab`
  - Statistical Analysis: `skimr`, `broom`, `PerformanceAnalytics`

---

## How to Use

### Prerequisites
1. Install R and RStudio.
2. Install the required R packages:
   ```R
   install.packages(c("tidyverse", "tidymodels", "themis", "table1", "ggpubr", "broom", "ggfortify", "GGally", "PerformanceAnalytics", "car", "caret", "skimr", "discrim", "glmnet", "kknn", "naivebayes", "kernlab", "xgboost", "gridExtra"))
   ```

## Results
- **Readmission Prediction**:
  - Logistic regression selected for its simplicity and strong F1-score.
  - Achieved robust performance metrics, ensuring clinical interpretability.
- **Stroke Prediction**:
  - Successfully extended workflow to build a stroke risk prediction model.
  - Demonstrated the adaptability of the `tidymodels` framework for healthcare applications.

---

## References
1. Strack B, DeShazo JP, Gennings C, et al. Impact of HbA1c measurement on hospital readmission rates: Analysis of 70,000 clinical database patient records. *Biomed Res Int.* 2014;2014:781670.
2. Lynam AL, Dennis JM, Owen KR, et al. Logistic regression has similar performance to machine learning models in clinical settings. *Diagn Progn Res.* 2020;4:6.



