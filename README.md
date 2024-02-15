# E2E_HeartDisease
End-To-End Heart Disease Classification Using Machine Learning Models
Here is a more detailed README for the heart disease classification project:

## Introduction

Heart disease is a leading cause of mortality worldwide. Machine learning models that can predict heart disease risk can aid early diagnosis and prevention. This project develops a model for classifying heart disease using the Cleveland Clinic Heart Disease dataset.

## Data

The dataset contains 303 patient records with 14 feature columns:

- Demographic: age, sex
- Vitals: blood pressure, cholesterol 
- Electrocardiography: resting blood sugar, resting ECG results
- Heart: maximum heart rate, chest pain type, exercise-induced angina
- Others: peak exercise ST slope, number of major vessels colored, thallium stress test  
- Target variable: heart disease diagnosis (1 if present, 0 if absent)

## Data Preprocessing

- Missing value imputation using mean/median
- Categorical feature encoding using label encoding
- Feature scaling of numeric variables using min-max normalization
- Train/test split: 80% training, 20% holdout set

## Exploratory Data Analysis

- Class imbalance assessment - roughly 55% have heart disease
- Correlation analysis - several redundant highly correlated features identified
- Visualization - scatter plots, histograms to understand relationships 

## Model Development

**Logistic Regression**
- Logistic function to model probability of heart disease based on risk factors
- Learns coefficients through maximum likelihood estimation
- Regularization to prevent overfitting 

**K-Nearest Neighbors**
- Makes prediction by finding closest examples based on distance metrics
- Simple non-parametric approach
- Performance depends heavily on value of k

**Random Forest** 
- Ensemble method combining many decision trees 
- Trees trained on bootstrapped subsets, decorrelated using random subsets of features
- Captures nonlinear relationships and feature interactions
- Hyperparameter tuning required

## Model Evaluation

- Accuracy, precision, recall, F1-score
- Random forest achieved highest accuracy of 85% on test set
- Excellent predictive performance as integrates benefits of bagging, feature randomness, and model averaging

## Feature Importance

Random forest feature importance scores identified maximum heart rate, chest pain type, and exercise-induced angina as top predictors. Provides insight on important risk factors. 

## Conclusion

The random forest model performed the best for heart disease prediction. Next steps are continued model tuning, testing on larger datasets, and integration into clinical decision support systems after further validation.

