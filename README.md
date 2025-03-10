# IBM HR Analytics: Employee Attrition & Performance Prediction
# Overview 
This project analyzes employee attrition using the IBM HR Analytics dataset. Various Machine Learning (ML) models are implemented to predict employee attrition based on job-related and personal factors. The best-performing model is identified through hyperparameter tuning and evaluation.

# Dataset Information
**Dataset**: 
IBM HR Analytics Employee Attrition & Performance

 **Target Variable**:
Attrition (0: No, 1: Yes)

**Features**: 
Includes demographics, job roles, salary, satisfaction, performance, work-life balance, etc.

# Data Preprocessing

**Handling Missing Values:** Checked and imputed if necessary.

**Categorical Encoding:**

> **One-Hot Encoding:Applied to Nominal Categorical Features (BusinessTravel, Department, EducationField, Gender, JobRole, MaritalStatus, OverTime).**
> 
> **Label Encoding**:**Applied to Ordinal Categorical Features (Attrition, Education, EnvironmentSatisfaction, JobInvolvement, JobSatisfaction, JobLevel, PerformanceRating, RelationshipSatisfaction, WorkLifeBalance).**

**Feature Scaling:** Applied to numerical features.

**Handling Class Imbalance**: Used SMOTE (Synthetic Minority Over-sampling Technique) to balance the Attrition classes.

# **Machine Learning Models Implemented**

**Logistic Regression (Baseline Model)**

**Decision Tree Classifier**

**Random Forest Classifier**

**XGBoost Classifier (Best Performing Model)**

# Hyperparameter Tuning

Performed RandomizedSearchCV for optimal parameter selection:

Decision Tree & Random Forest: Tuned max_depth, min_samples_split, min_samples_leaf, etc.

XGBoost: Tuned learning_rate, max_depth, n_estimators, subsample, etc

# Model Evaluation

**XGBoost**:86.05%

**Random Forest**:85.03%

**Decision Tree**:73.47%

**Logistic Regression**:59.52%

# Technologies Used

**Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn, XGBoost)**

**Machine Learning (Supervised Learning: Classification)**

**SMOTE for Handling Class Imbalance**

#  How to Run the Project

1. Install required dependencies:
         
        pip install pandas numpy matplotlib seaborn scikit-learn xgboost imbalanced-learn
   
2.Run the Python script:

        python employee_attrition_prediction.py
