# Employee Attrition Prediction

A machine learning project that predicts employee turnover using advanced classification algorithms and feature engineering techniques. This project helps HR departments identify at-risk employees and implement proactive retention strategies.


## Project Overview

Employee attrition refers to the gradual reduction of a company's workforce when employees leave and are not immediately replaced. High turnover increases recruitment costs and reduces productivity. This project builds predictive models to classify employees as likely to leave or stay, enabling HR teams to take preventive action.

### Key Objectives
- Analyze employee demographic, job-related, and satisfaction data
- Build and compare multiple classification models
- Identify key factors influencing employee attrition
- Provide actionable insights for HR decision-making
- Achieve optimal balance between precision and recall for minority class detection

## Dataset

**Source:** [IBM HR Analytics Employee Attrition Dataset](https://www.kaggle.com/pavansubhasht/ibm-hr-analytics-attrition-dataset)

### Dataset Characteristics
- **Total Samples:** 1,470 employees
- **Features:** 35 columns (34 predictors + 1 target)
- **Target Variable:** `Attrition` (Binary: Yes/No)
- **Class Distribution:**
  - No (stayed): 1,233 (83.9%) - Majority class
  - Yes (left): 237 (16.1%) - Minority class
- **Data Type:** Structured tabular data (CSV)
- **Missing Values:** None

### Feature Categories

**Demographic Features:**
- Age, Gender, MaritalStatus, Education, EducationField

**Job-Related Features:**
- Department, JobRole, JobLevel, JobInvolvement, JobSatisfaction, OverTime
- YearsAtCompany, YearsInCurrentRole, YearsWithCurrManager

**Compensation & Performance:**
- MonthlyIncome, PercentSalaryHike, PerformanceRating, StockOptionLevel

**Environment & Satisfaction:**
- DistanceFromHome, EnvironmentSatisfaction, WorkLifeBalance


### Models Implemented
- Logistic Regression
- Random Forest Classifier
- XGBoost Classifier
- Support Vector Machine (SVM)


## Results

### Model Performance Summary (After Tuning)

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|:------|:---------|:----------|:-------|:---------|:--------|
| **XGBoost** | **0.8129** | **0.4231** | **0.4681** | **0.4444** | **0.856** |
| **SVM** | 0.8129 | 0.4394 | 0.6170 | 0.5133 | 0.835 |
| Logistic Regression | 0.7347 | 0.3465 | 0.7447 | 0.4730 | 0.842 |
| Random Forest | 0.8401 | 0.5000 | 0.1277 | 0.2034 | 0.807 |

### Key Findings

**Best Model:** XGBoost achieved the optimal balance between precision and recall, making it the most suitable for predicting employee attrition.

**Top Predictive Features:**
1. OverTime (strong indicator of attrition)
2. MonthlyIncome (compensation matters)
3. JobSatisfaction (low satisfaction → higher attrition)
4. YearsAtCompany (experience and tenure)
5. Age (younger employees more likely to leave)
6. EnvironmentSatisfaction
7. JobLevel
8. YearsInCurrentRole
9. WorkLifeBalance
10. MaritalStatus


## Author

**Lakshmi Mahadevan**
