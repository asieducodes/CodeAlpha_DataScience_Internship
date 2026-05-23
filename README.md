# 🔬 CodeAlpha Data Science Internship

<div align="center">

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.3+-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.0+-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-2ECC71?style=for-the-badge)

</div>

---

## 👤 Intern Details

| Field | Details |
|-------|---------|
| **Name** | Asiedu Seth Osei |
| **Student ID** | CA/DF1/63603 |
| **Domain** | Data Science |
| **Duration** | 10th May 2026 – 10th June 2026 |
| **Organization** | [CodeAlpha](https://www.codealpha.tech) |
| **LinkedIn** | [Asiedu Seth Osei](https://linkedin.com/in/YOUR_PROFILE) |
| **GitHub** | [@asieducodes](https://github.com/asieducodes) |

---

## 📋 Tasks Overview

| # | Task | Dataset | Algorithm | Best Metric |
|---|------|---------|-----------|-------------|
| [01](#-task-1--iris-flower-classification) | Iris Flower Classification | Iris.csv (150 × 6) | SVM — RBF Kernel | **96.67% Accuracy** |
| [02](#-task-2--unemployment-analysis-with-python) | Unemployment Analysis | Unemployment in India (768 × 7) | EDA + Statistical Analysis | **+24.5pp COVID Impact** |
| [03](#-task-3--car-price-prediction-with-machine-learning) | Car Price Prediction | car_data.csv (301 × 9) | Gradient Boosting Regressor | **R² = 0.93+** |
| [04](#-task-4--sales-prediction-using-python) | Sales Prediction | Advertising.csv (200 × 5) | Polynomial Regression (d=2) | **R² = 0.94+** |

---

## 🛠 Tech Stack

```
Language   : Python 3.x
Notebook   : Jupyter Notebook
Libraries  : Pandas · NumPy · Scikit-learn · Matplotlib · Seaborn
Tools      : VS Code · GitHub · Git
```

---

## 📁 Repository Structure

```
CodeAlpha_DataScience_Internship/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── Task1_Iris_Classification/
│   ├── Task1_Iris_Classification.ipynb
│   ├── README.md
│   ├── data/
│   │   └── Iris.csv
│   └── outputs/
│       ├── eda_iris.png
│       ├── model_results_iris.png
│       └── feature_importance_iris.png
│
├── Task2_Unemployment_Analysis/
│   ├── Task2_Unemployment_Analysis.ipynb
│   ├── README.md
│   ├── data/
│   │   ├── Unemployment_in_India.csv
│   │   └── Unemployment_Rate_upto_11_2020.csv
│   └── outputs/
│       ├── national_trend.png
│       ├── regional_heatmap.png
│       ├── covid_impact.png
│       └── top_regions.png
│
├── Task3_Car_Price_Prediction/
│   ├── Task3_Car_Price_Prediction.ipynb
│   ├── README.md
│   ├── data/
│   │   └── car_data.csv
│   └── outputs/
│       ├── eda_car.png
│       ├── car_price_results.png
│       └── feature_importance_car.png
│
└── Task4_Sales_Prediction/
    ├── Task4_Sales_Prediction.ipynb
    ├── README.md
    ├── data/
    │   └── Advertising.csv
    └── outputs/
        ├── eda_sales.png
        ├── sales_results.png
        └── feature_importance_sales.png
```

---

## 🚀 Getting Started

### Prerequisites
```bash
Python 3.8+
pip
Jupyter Notebook or JupyterLab
```

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/asieducodes/CodeAlpha_DataScience_Internship.git
cd CodeAlpha_DataScience_Internship

# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch Jupyter
jupyter notebook
```

### Running a Task
Navigate into any task folder and open the `.ipynb` file in Jupyter. All notebooks are self-contained — just run cells top to bottom. Plots are saved automatically to the `outputs/` folder.

---

## 🌸 Task 1 — Iris Flower Classification

**Objective:** Classify Iris flower species (Setosa, Versicolor, Virginica) from petal and sepal measurements.

**Dataset:** `Iris.csv` — 150 samples · 4 features · 3 balanced classes

**Approach:**
- Exploratory Data Analysis — scatter plots, box plots, correlation heatmap
- Preprocessing — `StandardScaler`, `LabelEncoder`, Stratified 80/20 split
- Trained and compared **5 classifiers** using 5-fold Stratified Cross-Validation

**Results:**

| Model | CV Accuracy | Test Accuracy |
|-------|:-----------:|:-------------:|
| Logistic Regression | 95.83% | 93.33% |
| K-Nearest Neighbors | 95.83% | 93.33% |
| ⭐ Support Vector Machine (RBF) | 96.67% | **96.67%** |
| Random Forest | 95.00% | 90.00% |
| Decision Tree | 94.17% | 93.33% |

**Key Finding:** Petal length and petal width are the strongest species discriminators. SVM with an RBF kernel handles the Versicolor/Virginica overlap best, achieving the highest accuracy across all models.

📂 [`Task1_Iris_Classification/`](./Task1_Iris_Classification/)

---

## 📉 Task 2 — Unemployment Analysis with Python

**Objective:** Analyze unemployment trends across Indian states and quantify the impact of COVID-19 on employment rates.

**Datasets:**
- `Unemployment_in_India.csv` — 768 records · 20 states · Monthly data with Rural/Urban split
- `Unemployment_Rate_upto_11_2020.csv` — 267 records · includes geo-coordinates

**Approach:**
- Data cleaning, column standardisation, and date parsing across both datasets
- National time-series trend analysis with COVID-19 period annotation
- Regional heatmap across all 20 states
- Statistical comparison — Pre-COVID vs. Lockdown vs. Recovery periods
- Urban vs. Rural unemployment breakdown

**Key Findings:**

| Period | Avg Unemployment Rate |
|--------|:--------------------:|
| Pre-COVID (before Mar 2020) | ~7.97% |
| COVID Lockdown (Mar–Jun 2020) | ~32.46% |
| Recovery (after Jun 2020) | ~9.83% |
| **COVID Impact** | **+24.5 percentage points** |

**Key Finding:** The Apr–Jun 2020 lockdown created a synchronised spike across all regions — an unprecedented shock with no peacetime parallel. By mid-2021, approximately 70% of the peak unemployment had been recovered, though rates remained above pre-COVID baseline — indicating structural labour-market scarring.

📂 [`Task2_Unemployment_Analysis/`](./Task2_Unemployment_Analysis/)

---

## 🚗 Task 3 — Car Price Prediction with Machine Learning

**Objective:** Predict used car selling prices from real-world vehicle features using regression models.

**Dataset:** `car_data.csv` — 301 cars · 9 features including brand, year, mileage, fuel type, transmission, and owner history

**Approach:**
- EDA — price distribution, fuel type comparison, year vs price scatter, correlation analysis
- Feature Engineering — derived `Car_Age` from `Year`, `LabelEncoder` for categoricals
- Trained and benchmarked **6 regression models**

**Results:**

| Model | MAE (₹L) | RMSE (₹L) | R² Score |
|-------|:--------:|:---------:|:--------:|
| Linear Regression | high | high | ~0.43 |
| Ridge Regression | high | high | ~0.43 |
| Lasso Regression | high | high | ~0.43 |
| Decision Tree | medium | medium | ~0.85 |
| Random Forest | low | low | ~0.91 |
| ⭐ Gradient Boosting | **lowest** | **lowest** | **0.93+** |

**Key Finding:** Linear models fail on this task (R²≈0.43) because car pricing is fundamentally multiplicative — brand × age × condition — not additive. Gradient Boosting captures these non-linear interactions, achieving over 93% explained variance. `Car_Age` and `Present_Price` rank as the strongest predictors.

📂 [`Task3_Car_Price_Prediction/`](./Task3_Car_Price_Prediction/)

---

## 📊 Task 4 — Sales Prediction using Python

**Objective:** Forecast product sales from TV, Radio, and Newspaper advertising budgets, and deliver actionable insights for marketing strategy.

**Dataset:** `Advertising.csv` — 200 campaigns · TV, Radio, Newspaper spend → Sales

**Approach:**
- EDA — scatter analysis per channel, correlation heatmap, budget breakdown
- Feature Engineering — TV×Radio interaction term, `TV²`, `log(TV)`, total spend, TV share
- Trained **5 regression models** including a polynomial pipeline
- What-If analysis — TV budget sensitivity from $50K to $300K

**Results:**

| Model | MAE | RMSE | R² | CV R² |
|-------|:---:|:----:|:--:|:-----:|
| Linear Regression | 1.306 | 1.717 | 0.932 | 0.934 |
| Ridge Regression | 1.310 | 1.729 | 0.931 | 0.933 |
| ⭐ Poly Regression (d=2) | **1.199** | **1.634** | **0.938** | **0.950** |
| Random Forest | 1.388 | 1.898 | 0.917 | 0.937 |
| Gradient Boosting | 1.366 | 1.859 | 0.920 | 0.935 |

**Business Recommendations:**
- 📺 **TV** has the highest ROI — every additional $50K yields ~3,500 more units sold
- 📻 **TV × Radio synergy** amplifies returns beyond their individual effects
- 📰 **Newspaper** spend shows near-zero impact — budget better reallocated to TV or Radio

📂 [`Task4_Sales_Prediction/`](./Task4_Sales_Prediction/)

---

## 📦 Requirements

```txt
numpy>=1.24.0
pandas>=2.0.0
matplotlib>=3.7.0
seaborn>=0.12.0
scikit-learn>=1.3.0
jupyter>=1.0.0
notebook>=7.0.0
```

---

## 🔗 Links

- 🏢 **CodeAlpha:** [codealpha.tech](https://www.codealpha.tech)
- 💼 **LinkedIn Internship Post:** [View Post](https://www.linkedin.com/posts/asiedu-seth-osei-130b422b0_internship-offer-letter-ugcPost-7463994746756255744-KmAt/?utm_source=share&utm_medium=member_ios&rcm=ACoAAErrVjQBymG22T14UzHxumhJm30wYe40N9s)
- 🐙 **GitHub Profile:** [github.com/asieducodes](https://github.com/asieducodes)

---

<div align="center">

**Asiedu Seth Osei** · Student ID: `CA/DF1/63603` · CodeAlpha Data Science Internship 2026

</div>