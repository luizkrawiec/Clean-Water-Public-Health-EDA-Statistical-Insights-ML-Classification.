# 🌍 Clean Water Access & Public Health – Statistical Analysis and Machine Learning Classification

This project explores the relationship between access to clean water and public health, environmental, and socioeconomic indicators across different countries. Using a dataset with over 3,000 records and various qualitative and quantitative variables, we performed a complete analysis involving:

- 📊 **Exploratory Data Analysis (EDA)**
- 📈 **Descriptive statistics and bivariate analysis**
- 🧠 **Predictive modeling with machine learning algorithms**
- 🧪 **Hyperparameter optimization and model evaluation**

---

## 🔍 Objective

To investigate how environmental factors (such as water contamination, pH levels, and bacterial presence), socioeconomic indicators (GDP per capita, population density), and health metrics relate to the level of access to clean water in different countries.

---

## 🧬 Project Pipeline

1. **Data loading and cleaning**
2. **Transformations and creation of the target variable (`Water_Access_Level`)**
3. **Descriptive and inferential statistical analysis**
4. **Feature engineering and data preparation for machine learning**
5. **Building a pipeline with `XGBoostClassifier`**
6. **Hyperparameter tuning using `GridSearchCV` (testing 243 combinations)**
7. **Model evaluation with confusion matrix and classification report**

---

## 🛠️ Technologies and Libraries

- Python (pandas, numpy, seaborn, matplotlib)
- Scikit-learn
- XGBoost
- Jupyter Notebook / Google Colab

---

## 📈 Results

The final model (using `XGBoost` with hyperparameter optimization) achieved the following results on the test set:

- 🎯 Accuracy: **0.3977**
- 🎯 Best parameters:
  ```python
  {
    'classifier__colsample_bytree': 0.8,
    'classifier__learning_rate': 0.01,
    'classifier__max_depth': 3,
    'classifier__n_estimators': 100,
    'classifier__subsample': 1.0
  }

## 📉 Most challenging class: low performance in predicting the "Low Access to Clean Water" class, highlighting potential class imbalance or intrinsic complexity in the data.

## 📚 Key Learnings

    The importance of statistical analysis before machine learning modeling

    Challenges of working with real-world environmental and social datasets

    Practical experience with ML pipelines and cross-validation

    Understanding evaluation metrics beyond accuracy (f1-score, recall)
