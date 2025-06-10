# 🧠 Stroke Prediction: Data Analysis and Preprocessing

![License](https://img.shields.io/badge/License-MIT-yellow.svg)
![Dataset](https://img.shields.io/badge/Dataset-Kaggle-blue.svg)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)

This repository contains a Jupyter Notebook detailing an in-depth exploratory data analysis (EDA) and preprocessing pipeline for the Kaggle Stroke Prediction dataset. The project's mission is to dissect a rich collection of patient information—spanning demographic details, lifestyle habits, and key clinical metrics—to identify the patterns that signal stroke risk and prepare the data for machine learning.

The notebook walks through every step, from initial data inspection to creating a final, model-ready dataset.

---

## 📋 Table of Contents

- [Project Overview](#-project-overview)
- [Dataset](#-dataset)
- [Analysis Workflow](#-analysis-workflow)
- [Key Insights from the Analysis](#-key-insights-from-the-analysis)
- [Dependencies](#-dependencies)
- [License](#-license)

---

## 📝 Project Overview

The primary goal of this analysis is to thoroughly understand the factors contributing to stroke risk. By exploring the relationships between different patient attributes and the final outcome (stroke vs. no stroke), we can derive valuable insights. The project culminates in a meticulously cleaned and preprocessed dataset, which serves as a perfect starting point for building a robust predictive model.

Key areas of focus:

- **Data Quality Assessment**: Handling missing values, outliers, and inconsistencies.
- **Statistical Analysis**: Studying distributions and feature relationships with stroke outcomes.
- **Data Visualization**: Using `matplotlib` and `seaborn` to highlight patterns.
- **Feature Engineering & Preprocessing**: Transforming raw data into machine learning-ready format.

---

## 📊 Dataset

- **Source**: [Kaggle Stroke Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)
- **Size**: 5,110 entries with 12 attributes
- **Key Features**:
  - `gender`, `age`, `hypertension`, `heart_disease`, `ever_married`, `work_type`, `Residence_type`, `avg_glucose_level`, `bmi`, `smoking_status`, and the target variable `stroke`.

---

## ⚙️ Analysis Workflow

### 1. Data Loading and Initial Exploration
- Load dataset using `pandas`
- Inspect shape, data types, missing values
- Summary stats with `.describe()`

### 2. Exploratory Data Analysis (EDA)
- **Target Variable**: Detected ~5% positive stroke cases (severe imbalance)
- **Univariate Analysis**: Visualize feature distributions
- **Bivariate Analysis**: Correlation of features with stroke status
  - Strong links with `age`, `hypertension`, `heart_disease`

### 3. Data Preprocessing
- **Missing Values**: Median imputation for `bmi`
- **Anomalies**: Removed rare category "Other" in `gender`
- **Dropped**: Irrelevant `id` column
- **Encoding**: One-Hot for categorical variables
- **Scaling**: StandardScaler applied to numeric fields

---

## ✨ Key Insights from the Analysis

- **Severe Class Imbalance**: ~5% stroke cases → requires class balancing strategies
- **Age**: Most significant predictor of stroke
- **Co-morbidities**: `hypertension` and `heart_disease` greatly increase stroke risk
- **Glucose & BMI**: Elevated values associated with higher stroke likelihood

---

## 📦 Dependencies

This project uses the following main Python libraries:

- **pandas** – Data manipulation and analysis
- **numpy** – Numerical computing
- **matplotlib** – Data visualization
- **seaborn** – Statistical data visualization
- **scikit-learn** – Machine learning tools for preprocessing and modeling

---


## 📄 License
This project is licensed under the MIT License.
