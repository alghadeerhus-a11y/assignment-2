# ARTI 308 – Machine Learning Lab 2
## Dataset & Problem Summary

---

## Dataset Information

| Field | Details |
|-------|---------|
| **Dataset Name** | Pima Indians Diabetes Dataset |
| **Source** | [Kaggle](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database) / UCI ML Repository |
| **Format** | CSV |
| **Size** | 768 rows × 9 columns |

---

## Dataset Description

The Pima Indians Diabetes Dataset contains medical records for female patients of Pima Indian heritage. Each record includes diagnostic measurements used to predict whether a patient has diabetes. The dataset was originally collected by the National Institute of Diabetes and Digestive and Kidney Diseases.

### Features (Input Variables)

| Column | Description | Type |
|--------|-------------|------|
| `Pregnancies` | Number of times pregnant | Numerical |
| `Glucose` | Plasma glucose concentration (2-hour oral glucose tolerance test) | Numerical |
| `BloodPressure` | Diastolic blood pressure (mm Hg) | Numerical |
| `SkinThickness` | Triceps skin fold thickness (mm) | Numerical |
| `Insulin` | 2-hour serum insulin (mu U/ml) | Numerical |
| `BMI` | Body mass index (weight in kg / height in m²) | Numerical |
| `DiabetesPedigreeFunction` | Diabetes pedigree function (genetic likelihood) | Numerical |
| `Age` | Age in years | Numerical |
| `Outcome` | **Target variable** – 1 = Diabetic, 0 = Not Diabetic | Binary |

---

## Machine Learning Problem Definition

### Problem Type: **Classification (Binary)**

This is a **binary classification** problem. The goal is to predict whether a patient will be diagnosed with diabetes (`Outcome = 1`) or not (`Outcome = 0`) based on the provided medical features.

### Why Classification?
- The target variable (`Outcome`) is **categorical** with two discrete values: 0 or 1
- The model must learn to separate patients into two distinct classes
- This is **not** regression (no continuous output) and **not** clustering (we have labeled data)

### Problem Statement

> Given a set of medical diagnostic measurements for a female patient (including glucose levels, BMI, age, and other clinical features), predict whether the patient has diabetes (1) or not (0).

### Target Variable
- **Column:** `Outcome`
- **Type:** Binary (0 = No Diabetes, 1 = Diabetes)
- **Distribution:** ~65% Non-diabetic (500 cases), ~35% Diabetic (268 cases)

---

## Methodology Overview

The project follows a standard supervised machine learning pipeline:

1. **Dataset Selection** → Pima Diabetes CSV dataset
2. **Data Loading** → Load with Pandas, inspect shape and types
3. **Data Preprocessing** → Handle missing/zero values, normalize features
4. **Train/Test Split** → 80% training, 20% testing
5. **Model Training** → Train classification models (e.g., Logistic Regression, Random Forest)
6. **Model Evaluation** → Measure Accuracy, Precision, Recall, F1-Score
7. **Results** → Compare model performance and select the best model

---

*ARTI 308 – Machine Learning | Academic Year 2025/2026 – 2nd Semester*
