# 🌍 Clean Water & Public Health: Data Analysis and Classification

This project explores the relationships between access to clean water, environmental quality, and public health outcomes across countries using a real-world dataset. It involves exploratory data analysis (EDA), statistical insights, feature engineering, and classification modeling to predict levels of access to clean water.

---

## 📊 Project Overview

### Objectives:
- Understand patterns of clean water access across regions.
- Explore environmental and socio-economic factors affecting water quality and public health.
- Apply machine learning to classify countries by their access to clean water.

---

## 🔍 Dataset

The dataset includes information on:

- **Water Quality Indicators**: pH, nitrate, turbidity, lead, bacterial count, dissolved oxygen.
- **Public Health Metrics**: diarrhea cases, typhoid, cholera, infant mortality.
- **Socioeconomic Features**: GDP per capita, urbanization rate, population density.
- **Target**: `Water_Access_Level` (Low, Medium, High)

Data was filtered for Brazil for some of the analysis and modeling.

---

## 🧪 Exploratory Data Analysis (EDA)

- Distribution and variability of water quality indicators.
- Comparison of public health outcomes across different water source types.
- Correlation matrix and pairwise plots for quantitative features.
- Grouped bar charts and heatmaps to compare countries and regions.

---

## 📈 Statistical Analysis

- Frequency distributions and proportions for categorical variables.
- Mean comparisons and trend analysis across `Water_Access_Level`.
- Investigated potential risk factors related to low access to clean water.

---

## 🤖 Machine Learning Approach

**Model Used:** XGBoost Classifier  
**Goal:** Predict the category of `Water_Access_Level` (Low, Medium, High)

### 🔧 Pipeline & Preprocessing

- Categorical encoding (OneHotEncoder)
- ColumnTransformer to separate numeric and categorical features
- StandardScaler for numeric variables

### 📌 Hyperparameter Tuning

Used `GridSearchCV` with 5-fold cross-validation:
- `learning_rate`
- `n_estimators`
- `max_depth`
- `subsample`
- `colsample_bytree`

### ✅ Best Parameters
```python
{
  'classifier__colsample_bytree': 0.8,
  'classifier__learning_rate': 0.01,
  'classifier__max_depth': 3,
  'classifier__n_estimators': 100,
  'classifier__subsample': 1.0
}

