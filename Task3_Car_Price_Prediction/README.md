# 🚗 Task 3 — Car Price Prediction with Machine Learning

<div align="center">

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=flat-square&logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-2ECC71?style=flat-square)

</div>

> **CodeAlpha Data Science Internship** · Asiedu Seth Osei · `CA/DF1/63603`

---

## 📌 Objective

Build and evaluate machine learning regression models to predict used car selling prices based on real-world vehicle features including brand, year of manufacture, kilometres driven, fuel type, transmission, and ownership history. Deliver a model capable of reliable price estimation for practical use in automotive market applications.

---

## 📂 Folder Structure

```
Task3_Car_Price_Prediction/
├── Task3_Car_Price_Prediction.ipynb   ← Main notebook
├── README.md
├── data/
│   └── car_data.csv
└── outputs/
    ├── eda_car.png
    ├── car_price_results.png
    └── feature_importance_car.png
```

---

## 📊 Dataset

| Property | Details |
|----------|---------|
| **File** | `car_data.csv` |
| **Rows** | 301 |
| **Features** | 9 (Car_Name, Year, Selling_Price, Present_Price, Driven_kms, Fuel_Type, Selling_type, Transmission, Owner) |
| **Target** | `Selling_Price` (in Indian Lakhs ₹) |
| **Year Range** | 2003 – 2018 |
| **Missing Values** | None |

**Feature Breakdown:**

| Feature | Type | Details |
|---------|------|---------|
| `Car_Name` | Categorical | Brand/model name — dropped after encoding |
| `Year` | Numerical | Manufacture year → engineered to `Car_Age` |
| `Present_Price` | Numerical | Current ex-showroom price (₹ Lakhs) |
| `Driven_kms` | Numerical | Total kilometres driven |
| `Fuel_Type` | Categorical | Petrol (239) · Diesel (60) · CNG (2) |
| `Selling_type` | Categorical | Dealer vs Individual |
| `Transmission` | Categorical | Manual (261) · Automatic (40) |
| `Owner` | Numerical | Number of previous owners |
| `Selling_Price` | **Target** | Used car selling price (₹ Lakhs) |

**Price Statistics:**

| Stat | Value (₹ Lakhs) |
|------|:--------------:|
| Min | 0.10 |
| Mean | 4.66 |
| Median | 3.60 |
| Max | 35.00 |

---

## 🔄 Methodology

```
Load Data → EDA (distributions, scatter, correlations)
→ Drop Car_Name → LabelEncode Categoricals
→ Feature Engineering (Car_Age from Year)
→ StandardScaler → 80/20 Train/Test Split
→ Train 6 Regression Models → Compare Metrics
→ Best Model Analysis → Feature Importance → Price Predictor
```

**Feature Engineering:**
- `Car_Age = 2024 − Year` — captures depreciation as a continuous variable
- Dropped `Car_Name` after encoding (too many unique values, low signal)
- Applied `LabelEncoder` to `Fuel_Type`, `Selling_type`, `Transmission`
- `StandardScaler` applied to all features before model training

---

## 🤖 Models Trained

| Model | Key Hyperparameters |
|-------|-------------------|
| Linear Regression | Default |
| Ridge Regression | `alpha=1.0` |
| Lasso Regression | `alpha=0.01` |
| Decision Tree | `max_depth=6` |
| Random Forest | `n_estimators=100` |
| Gradient Boosting | `n_estimators=100`, `learning_rate=0.1` |

---

## 📈 Results

| Model | MAE (₹L) | RMSE (₹L) | R² Score | Performance |
|-------|:--------:|:---------:|:--------:|:-----------:|
| Linear Regression | 1.222 | 1.879 | 0.8467 | ✅ Good |
| Ridge Regression | 1.223 | 1.882 | 0.8462 | ✅ Good |
| Lasso Regression | 1.222 | 1.882 | 0.8462 | ✅ Good |
| Decision Tree | 0.749 | 1.188 | 0.9387 | ✅ Very Good |
| Random Forest | 0.617 | 0.933 | 0.9622 | ✅ Excellent |
| ⭐ **Gradient Boosting** | **0.556** | **0.891** | **0.9655** | **✅ Best** |

**Best Model: Gradient Boosting Regressor — R² = 0.9655 | MAE = 0.556 ₹L | RMSE = 0.891 ₹L**

---

## 🔍 Key Findings

- **All models performed well (R² ≥ 0.84)** — the engineered `Car_Age` feature and clean preprocessing pipeline gave every model a strong foundation to work from
- **Gradient Boosting** delivered the highest accuracy with R² = 0.9655, meaning it explains over 96.5% of the variance in used car selling prices
- **Linear models achieved R² ≈ 0.846** — significantly better than a naive baseline, but still outperformed by ensemble methods that capture non-linear depreciation curves
- **`Car_Age`** is the strongest price predictor — exponential depreciation dominates all other signals for vehicles older than 5 years
- **`Present_Price`** (ex-showroom value) is the second strongest feature — higher-value brands retain more resale value proportionally
- **Automatic transmission** commands a consistent price premium over manual in the dataset
- **Diesel cars** have a higher median selling price than Petrol, reflecting their lower running costs

---

## 📊 Output Plots

| Plot | Description |
|------|------------|
| `eda_car.png` | Price distribution, fuel-type comparison, year vs price scatter, KM vs price, transmission box plot, correlation heatmap |
| `car_price_results.png` | Actual vs predicted scatter, residual distribution, R² model comparison bar chart |
| `feature_importance_car.png` | Random Forest feature importance horizontal bar chart |

---

## ▶️ How to Run

```bash
# From the repo root
cd Task3_Car_Price_Prediction
jupyter notebook Task3_Car_Price_Prediction.ipynb
```
Run all cells top to bottom. The final cell demonstrates a live price prediction on a sample car. Plots saved automatically to `outputs/`.

---

## 🔗 Links

- 📁 [Back to Main Repository](../README.md)
- 🏢 [CodeAlpha](https://www.codealpha.tech)
- 💼 [LinkedIn — Task 3 Video Post](https://linkedin.com/in/YOUR_PROFILE)