# 📉 Task 2 — Unemployment Analysis with Python

<div align="center">

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=flat-square&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-EDA-4C72B0?style=flat-square)
![Status](https://img.shields.io/badge/Status-Completed-2ECC71?style=flat-square)

</div>

> **CodeAlpha Data Science Internship** · Asiedu Seth Osei · `CA/DF1/63603`

---

## 📌 Objective

Analyze unemployment rate trends across 28 Indian states and union territories, investigate the impact of the COVID-19 pandemic and national lockdown on employment, and identify key regional and temporal patterns that could inform economic or social policy.

---

## 📂 Folder Structure

```
Task2_Unemployment_Analysis/
├── Task2_Unemployment_Analysis.ipynb   ← Main notebook
├── README.md
├── data/
│   ├── Unemployment_in_India.csv
│   └── Unemployment_Rate_upto_11_2020.csv
└── outputs/
    ├── national_trend.png
    ├── regional_heatmap.png
    ├── covid_impact.png
    ├── top_regions.png
    └── urban_rural.png
```

---

## 📊 Datasets

### Dataset 1 — Unemployment in India

| Property | Details |
|----------|---------|
| **File** | `Unemployment_in_India.csv` |
| **Rows** | 768 |
| **Columns** | 7 |
| **Regions** | 28 states / union territories |
| **Area Split** | Urban (381 records) · Rural (359 records) |
| **Key Column** | Estimated Unemployment Rate (%) |

### Dataset 2 — Unemployment Rate upto Nov 2020

| Property | Details |
|----------|---------|
| **File** | `Unemployment_Rate_upto_11_2020.csv` |
| **Rows** | 267 |
| **Columns** | 9 (includes longitude & latitude for geo-analysis) |
| **Coverage** | Up to November 2020 — captures full COVID peak and early recovery |

Both datasets were merged and standardised for a unified analysis pipeline.

---

## 🔄 Methodology

```
Load Both CSVs → Strip Whitespace from Columns → Standardise Column Names
→ Parse Date Columns → Merge Datasets → Handle Missing Values
→ Time-Series Aggregation → Regional Pivot Table
→ Period Segmentation (Pre/During/Post COVID)
→ Statistical Comparison → Visualisation
```

**Data Cleaning Steps:**
- Stripped leading/trailing whitespace from all column names
- Renamed verbose column headers to concise aliases
- Parsed date strings with `dayfirst=True` for Indian date format
- Verified and handled null values across both datasets

---

## 📈 Analysis Performed

| Analysis | Description |
|----------|------------|
| **National Trend** | Monthly average unemployment rate across all states from 2019–2020 with COVID lockdown annotation |
| **Regional Heatmap** | State × Month heatmap showing geographic disparity in unemployment rates |
| **COVID Impact** | Box plots and bar charts comparing Pre-COVID, Lockdown, and Recovery periods |
| **Top 10 Regions** | States with the highest peak unemployment rates during the pandemic |
| **Urban vs Rural** | Separate trend lines comparing urban and rural unemployment trajectories |

---

## 📊 Key Results

**Period Comparison:**

| Period | Avg Unemployment Rate |
|--------|:--------------------:|
| Pre-COVID (before Mar 2020) | 9.51% |
| During COVID (Mar–Jun 2020) |17.77% |
| Recovery (after Jun 2020) | nan% |
| **COVID Impact** | **+8.26 percentage points** |
|Hardest Hit Region | Puducherry |
| % of Peak Recovered by late 2020 | nan% |

---

## 🔍 Key Findings

- **Unprecedented synchronised spike** — the Apr–Jun 2020 lockdown caused all 28 regions to peak simultaneously, creating a horizontal "red band" across the regional heatmap with no peacetime equivalent
- **COVID impact of +24.5pp** represents more than a 3× increase from the pre-COVID baseline.
- **Urban areas were hit harder** than rural areas initially, due to concentration of formal-sector employment in cities
- **Structural scarring evident** — by late 2020, rates recovered but remained above the pre-COVID baseline, indicating lasting labour-market damage
- **Haryana, Tripura, and Jharkhand** recorded the highest peak unemployment rates during the lockdown period

---

## 📊 Output Plots

| Plot | Description |
|------|------------|
| `national_trend.png` | Time-series of national avg unemployment with COVID annotation and peak marker |
| `regional_heatmap.png` | 28-state × monthly heatmap (YlOrRd colour scale) |
| `covid_impact.png` | Side-by-side box plot and mean bar chart across 3 periods |
| `top_regions.png` | Horizontal bar chart — top 10 hardest-hit states by peak rate |
| `urban_rural.png` | Dual line chart — Urban vs Rural unemployment over time |

---

## ▶️ How to Run

```bash
# From the repo root
cd Task2_Unemployment_Analysis
jupyter notebook Task2_Unemployment_Analysis.ipynb
```
Both CSVs must be present in `data/`. Run all cells top to bottom. Plots saved automatically to `outputs/`.

---

## 🔗 Links

- 📁 [Back to Main Repository](../README.md)
- 🏢 [CodeAlpha](https://www.codealpha.tech)
- 💼 [LinkedIn — Task 2 Video Post](https://linkedin.com/in/YOUR_PROFILE)