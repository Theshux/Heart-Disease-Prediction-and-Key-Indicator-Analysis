# Heart-Disease-Prediction-and-Key-Indicator-Analysis

## Table of Contents
1. [Project Summary](#project-summary)
2. [Domain and Dataset](#domain-and-dataset)
3. [Project Objectives](#project-objectives)
4. [Project Process Overview](#project-process-overview)
5. [Step-by-Step Walkthrough](#step-by-step-walkthrough)
6. [Model Evaluation](#model-evaluation)
7. [Comparison to Benchmark](#comparison-to-benchmark)
8. [Visualizations](#visualizations)
9. [Implications](#implications)
10. [Limitations](#limitations)
11. [Future Steps](#future-steps)
12. [Conclusion](#conclusion)

## Project Summary
Our project aimed to analyze the risk factors associated with heart attacks using the "Indicators of Heart Disease (2022 UPDATE)" dataset. We sought to build a classification model for predicting heart attacks and identify key indicators of heart attack risk.

## Domain and Dataset
- **Domain:** Healthcare
- **Dataset:** "Indicators of Heart Disease (2022 UPDATE)" 
- **Source:** [Kaggle](https://www.kaggle.com/datasets/kamilpytlak/personal-key-indicators-of-heart-disease/data)
- **Goal:** Heart Disease Prediction and Identification of Key Risk Indicators

## Project Objectives
- Predict the likelihood of heart attacks using machine learning models.
- Identify key indicators contributing to heart disease risk.
- Enhance current risk assessment methodologies in healthcare through data-driven insights.

## Project Process Overview
We approached the problem by:
1. **Exploratory Data Analysis (EDA):** Identified missing values, outliers, and relationships between variables.
2. **Data Preprocessing:** Handled missing values, encoded categorical variables, and treated outliers.
3. **Model Building:** Built predictive models using various classification algorithms.
4. **Model Evaluation:** Used metrics like recall, AUC-ROC score, and accuracy to assess model performance.
5. **Feature Importance:** Identified key features contributing to heart disease prediction.

## Step-by-Step Walkthrough

### 1. Data Exploration
- **Number of Rows:** 445,132
- **Number of Columns:** 40
- **Categorical Variables:** 34
- **Numeric Variables:** 6
- **Missing Values:** Present in 38 columns, with a maximum of 11.40%.

### 2. Data Preprocessing
- Handled missing values using methods like KNN imputer and median imputation.
- Addressed multicollinearity by dropping variables like height, weight, and sleep that showed high VIF.
- Treated outliers based on analysis, but in final models, outliers were kept as they were essential for prediction.

### 3. Feature Engineering
- Transformed features like BMI from height and weight.
- Reduced categories in variables like Covid status and State for better analysis.

### 4. Model Building
- **Models Tried:** Logistic Regression, Decision Trees, Random Forests, XGBoost, and more.
- **Class Imbalance Treatment:** Used SMOTE with varying strategies to balance the target variable.
- **Final Model:** XGBoost with Sequential Feature Selection.

## Model Evaluation
- **XGBoost Performance:**
  - **Accuracy:** 0.85 on the test dataset.
  - **Recall:** 0.71 for positive cases.
  - **AUC Score:** 0.8757, indicating strong discrimination between positive and negative cases.

## Comparison to Benchmark
- Our XGBoost model outperformed the initial benchmark with an accuracy of 0.85 and a recall of 0.71, significantly improving heart attack risk prediction.

## Visualizations
- **ROC Curve:** Demonstrated the model’s ability to distinguish between positive and negative cases.
- **Feature Importance Plot:** Identified top predictors like 'HadAngina', 'RemovedTeeth', and 'AgeCategory'.
- **Other Visuals:** Histograms, box plots, and correlation matrices were used during EDA.

## Implications
- **Healthcare Practice:** Our model supports proactive measures for heart disease prevention.
- **Policy Making:** Can guide public health campaigns aimed at reducing heart disease incidence.
- **Patient Empowerment:** Provides individuals with insights for making informed lifestyle changes.

## Limitations
- **Data Limitation:** Retrospective data might not capture real-time health changes.
- **Missing Critical Variables:** Lack of information on cholesterol levels and hypertension history.
- **Model Generalizability:** Needs validation across diverse populations.

## Future Steps
- **Feature Engineering:** Introduce new features and improve existing ones.
- **Model Ensemble:** Combine predictions from multiple models for better accuracy.
- **Continuous Monitoring:** Implement ongoing model evaluation and retraining.

## Conclusion
This project provided valuable insights into heart disease risk assessment and demonstrated the importance of thorough EDA, robust preprocessing, and careful model evaluation in building effective healthcare solutions.
