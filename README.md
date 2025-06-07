# 🧠 Drug Classification Using Decision Tree

## ✍️ About the Author
> Written by: [*JaberAlJ*](https://github.com/JaberAlJ)

## 1. 🩺 Project Overview
- **Objective**: Predict the most effective drug 💊 (`A`, `B`, `C`, `X`, `Y`) for patients based on health indicators.
- **Context**: Clinical data analysis for personalized medication recommendation.

## 2. 📦 Library Imports
- **Core Libraries**:
  - `numpy`
  - `pandas`
  - `matplotlib.pyplot`
- **Machine Learning Toolkit**:
  - `sklearn.model_selection`: `train_test_split`, `cross_val_score`
  - `sklearn.tree`: `DecisionTreeClassifier`, `plot_tree`
  - `sklearn.metrics`: `confusion_matrix`, `accuracy_score`

## 3. 📊 Dataset Description
- **Source**: `drug_unclnData.csv`
- **Features**:
  - `Age` 📅
  - `Sex` ⚥
  - `Blood Pressure (BP)` 💓
  - `Cholesterol` 🧬
  - `Na_to_K` 🧪 (Sodium to Potassium Ratio)
- **Target Variable**:
  - `Drug` 💊 – The effective medication

## 4. 🔍 Initial Data Assessment
- **Shape**: 200 records × 6 columns
- **Missing Values**:
  - `Age`: 6 missing
  - `Na_to_K`: 5 missing
- **Issues Detected**:
  - Inconsistent casing and extra spaces in categorical data

## 5. 🧹 Data Cleaning
- **Handle Missing Data**:
  - Impute `Age` with mean 🧮
  - Impute `Na_to_K` with mean 🧪
- **Normalize Text Fields**:
  - Trim and capitalize: `Sex`, `BP`, `Cholesterol` ✂️🔠

## 6. 🔢 Data Encoding
- Convert categorical values to numerical format:
  - `Sex`: `M` = 0, `F` = 1 ⚥
  - `BP`: `LOW` = 0, `NORMAL` = 1, `HIGH` = 2 💓
  - `Cholesterol`: `NORMAL` = 0, `HIGH` = 1 🧬

## 7. 🛠️ Data Preparation
- **Feature Set (X)**:
  - Includes: `Age`, `Sex`, `BP`, `Cholesterol`, `Na_to_K`
- **Target (y)**:
  - `Drug` 💊

## 8. 🤖 Model Selection & Evaluation
- **Algorithm**: `DecisionTreeClassifier` 🌳
- **Performance Metrics**:
  - `Accuracy Score` 📈
  - `Confusion Matrix` 🧩
- **Model Visualization**:
  - Decision Tree Plot 🌲
