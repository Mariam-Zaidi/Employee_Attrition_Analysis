________________________________________
# 👩‍💼 Employee Attrition Analysis

This project aims to analyze and predict employee attrition using a combination of data preprocessing, feature engineering, exploratory analysis, and machine learning models. The goal is to identify the key drivers of employee churn and help HR teams take proactive action to improve retention.

---

## 📁 Dataset Overview

The dataset includes:
- `general_data.csv`: Demographics, job role, income, performance.
- `in_time.csv` & `out_time.csv`: Employee attendance logs.
- ‘employee_survey_data.csv’ : Environment Satisfaction, Job Satisfaction, Work Life Balance
- ‘manager_survey_data.csv’ : Job Involvement, Performance Rating
- Label: `Attrition` (Yes/No)

---

## 🧠 Objective

- Identify key behavioral and demographic patterns behind employee attrition.
- Build predictive models to classify whether an employee is likely to leave.

---

## 🧹 Data Cleaning & Preparation

1. **Missing Value Treatment**:
   - Replaced or dropped missing values in survey columns.
   - Ensured all employees had matching data across files.

2. **Feature Engineering**:
   - Derived `avg_work_hours` and `absent_days` from in-time/out-time logs.
   - Created binary column `Attrition_bool` for modeling.

3. **Encoding**:
   - Applied label encoding and one-hot encoding on categorical variables.

4. **Multicollinearity**:
   - Checked with VIF (Variance Inflation Factor).
   - Removed features with high VIF if p-values were insignificant.

---

## 📊 Exploratory Data Analysis (EDA)

Visual tools like histograms, barplots, and boxplots and Correlation heatmap
were used to uncover patterns.

### Key Insights:
- Employees with high average work hours showed higher attrition.
- High number of full-day workers left the company possibly due to burn-out. Others left due to very low engagement or absenteeism
- Long gaps since last promotion like at gaps of 3, 10 and 13 years have shown low job satisfaction and were associated with higher attrition.
- Job satisfaction and work-life balance scores were generally lower for those who left.

---

## 🤖 Models Used      	            	
		
Logistic Regression     	            
Decision Tree Classifier	  
Random Forest           	  
XGBoost Classifier      

---

## 📈 Model Evaluation
Models were evaluated using:
- Accuracy
- Precision / Recall
- ROC-AUC
- Confusion Matrix

## HyperParameter Tuning:
Hyperparameter tuning was performed using GridSearchCV and RandomSearchCV to tune the models to obtain best results.

## 🔍 Feature Importance

Top predictive features:
- `avg_work_hours`
- ‘YearsWithCurrManager’
- `JobSatisfaction`
- `EnvironmentSatisfaction`
- `TotalWorkingYears`

---

