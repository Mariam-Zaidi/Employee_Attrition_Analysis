# Employee_Attrition_Analysis



---

## 🧠 Problem Statement

The goal is to analyze employee data to understand the key drivers behind attrition and develop predictive models to forecast future attrition. This helps organizations take proactive HR measures.

---

## 📊 Dataset Overview

The dataset includes:
- `general_data.csv`: Demographics, job role, income, performance.
- `in_time.csv` & `out_time.csv`: Employee attendance logs.
- ‘employee_survey_data.csv’ : Environment Satisfaction, Job Satisfaction, Work Life Balance
- ‘manager_survey_data.csv’ : Job Involvement, Performance Rating
- Label: `Attrition` (Yes/No)

---

## 🛠️ Feature Engineering Highlights

Key features created from `in_time.csv` and `out_time.csv`:

| Feature              | Description                            |
|----------------------|----------------------------------------|
| `avg_work_hours`     | Average daily work duration            |
| `std_work_hours`     | Consistency in daily work hours        |
| `num_absent_days`    | Count of days not present              |
| `num_half_days`      | Days with < 8 hrs of work              |
| `num_full_days`      | Days with ≥ 8 hrs of work              |

---

## 🔍 EDA (Exploratory Data Analysis)

Performed detailed visual analysis to understand:
- Attrition distribution by age, role, satisfaction
- Correlation heatmap
- Distribution of work hours and attendance patterns

---

## 🤖 ML Models Used

| Model                  | Notes                              |Accuracy   |Sensitivity |Specificity |Precision |Recall |
|------------------------|------------------------------------|-----------|
| Logistic Regression    | Baseline                           |
| Decision Tree          | Interpretable model                |
| Random Forest          | High accuracy, handles imbalance   |
| XGBoost                | Boosted model for performance      |


---

## 📈 Results Summary

- Best model: ✅ Random Forest (or XGBoost)
- Top predictors:
  - Overtime
  - Job satisfaction
  - Number of projects
  - Avg. work hours

---
