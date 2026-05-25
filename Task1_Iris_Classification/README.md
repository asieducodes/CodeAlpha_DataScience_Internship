# 🌸 Task 1 — Iris Flower Classification

<div align="center">

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=flat-square&logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-2ECC71?style=flat-square)

</div>

> **CodeAlpha Data Science Internship** · Asiedu Seth Osei · `CA/DF1/63603`

---

## 📌 Objective

Train and evaluate machine learning classification models to accurately identify Iris flower species — **Setosa**, **Versicolor**, and **Virginica** — based on four physical measurements: sepal length, sepal width, petal length, and petal width.

---

## 📂 Folder Structure

```
Task1_Iris_Classification/
├── Task1_Iris_Classification.ipynb   ← Main notebook
├── README.md
├── data/
│   └── Iris.csv
└── outputs/
    ├── eda_iris.png
    ├── correlation_iris.png
    ├── model_results_iris.png
    └── feature_importance_iris.png
```

---

## 📊 Dataset

| Property | Details |
|----------|---------|
| **File** | `Iris.csv` |
| **Source** | UCI Machine Learning Repository |
| **Rows** | 150 |
| **Features** | 4 (SepalLengthCm, SepalWidthCm, PetalLengthCm, PetalWidthCm) |
| **Target** | Species (3 balanced classes — 50 samples each) |
| **Missing Values** | None |

**Class Distribution:**

| Species | Count |
|---------|:-----:|
| Iris-setosa | 50 |
| Iris-versicolor | 50 |
| Iris-virginica | 50 |

**Feature Statistics:**

| Feature | Min | Mean | Max |
|---------|:---:|:----:|:---:|
| Sepal Length (cm) | 4.30 | 5.84 | 7.90 |
| Sepal Width (cm) | 2.00 | 3.05 | 4.40 |
| Petal Length (cm) | 1.00 | 3.76 | 6.90 |
| Petal Width (cm) | 0.10 | 1.20 | 2.50 |

---

## 🔄 Methodology

```
Load Data → EDA → Drop Id Column → LabelEncode Target
→ StandardScaler → Stratified 80/20 Split
→ Train 5 Models → 5-Fold Stratified CV
→ Evaluate → Confusion Matrix → Feature Importance
```

**Preprocessing:**
- Dropped `Id` column (non-informative)
- Stripped `Iris-` prefix from species names
- Applied `StandardScaler` to all 4 features
- Stratified split to preserve class balance across train/test sets

---

## 🤖 Models Trained

| Model | Key Hyperparameters |
|-------|-------------------|
| Logistic Regression | `max_iter=200` |
| K-Nearest Neighbors | `n_neighbors=5` |
| Support Vector Machine | `kernel='rbf'`, `C=1.0` |
| Random Forest | `n_estimators=100` |
| Decision Tree | `max_depth=4` |

All models evaluated using **5-Fold Stratified Cross-Validation** for reliable, unbiased performance estimates.

---

## 📈 Results

| Model | CV Accuracy | CV Std | Test Accuracy |
|-------|:-----------:|:------:|:-------------:|
| Logistic Regression | 95.83% | ±2.64% | 93.33% |
| K-Nearest Neighbors | 95.83% | ±2.64% | 93.33% |
| ⭐ **Support Vector Machine** | **96.67%** | **±1.67%** | **96.67%** |
| Random Forest | 95.00% | ±3.12% | 90.00% |
| Decision Tree | 94.17% | ±2.04% | 93.33% |

**Best Model: Support Vector Machine (RBF Kernel) — 96.67% Test Accuracy**

---

## 🔍 Key Findings

- **Petal length** and **petal width** are the two strongest discriminating features, confirmed by Random Forest feature importance scores
- **Setosa** is linearly separable from the other two species — even simple models classify it perfectly
- **Versicolor** and **Virginica** overlap in sepal measurements, which is why non-linear models (SVM RBF) outperform linear ones
- The **low CV standard deviation (±1.67%)** of SVM confirms consistent, stable performance across all folds

---

## 📊 Output Plots

| Plot | Description |
|------|------------|
| `eda_iris.png` | Scatter pairs + box plots across all 3 species |
| `correlation_iris.png` | Feature-to-feature correlation heatmap |
| `model_results_iris.png` | CV vs test accuracy bar chart + confusion matrix |
| `feature_importance_iris.png` | Random Forest importance ranking |

---

## ▶️ How to Run

```bash
# From the repo root
cd Task1_Iris_Classification
jupyter notebook Task1_Iris_Classification.ipynb
```
Run all cells top to bottom. Plots are automatically saved to `outputs/`.

---

## 🔗 Links

- 📁 [Back to Main Repository](../README.md)
- 🏢 [CodeAlpha](https://www.codealpha.tech)
- 💼 [LinkedIn — Task 1 Video Post](https://www.linkedin.com/posts/asiedu-seth-osei-130b422b0_codealpha-datascience-machinelearning-ugcPost-7464771880533622784-TMrn/?utm_source=share&utm_medium=member_desktop&rcm=ACoAAErrVjQBymG22T14UzHxumhJm30wYe40N9s)