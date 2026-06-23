# 🛒 Retail Customer Intelligence & Growth Analytics

An end-to-end retail analytics project covering data cleaning, exploratory analysis, customer segmentation, CLV modeling, cohort retention analysis, and executive dashboard development.

---

## 📌 Project Overview

| Detail | Info |
|--------|------|
| **Domain** | Retail & Marketing Analytics |
| **Dataset** | Kaggle Retail Sales Dataset |
| **Records** | 10,000 transactions · 1,986 customers |
| **Period** | January 2022 – February 2023 |
| **Tools** | Python · Power BI · Pandas · Scikit-learn · Matplotlib · Seaborn · Plotly |

---

## 🎯 Business Problem

A multi-channel retail company needed clarity on:
- **Who** their most valuable customers are
- **Why** customers churn and how to retain them
- **Which** product categories and regions drive the most revenue
- **How** to allocate marketing spend more effectively

---

## 📁 Project Structure

```
retail-customer-intelligence/
│
├── data/
│   ├── raw/                        # Original dataset
│   └── processed/                  # Cleaned & transformed data
│
├── notebooks/
│   ├── 01_Data_Acquisition_and_Setup.ipynb
│   ├── 02_Data_Cleaning_Preprocessing.ipynb
│   ├── 03_Exploratory_Data_Analysis.ipynb
│   ├── 04_Customer_Segmentation.ipynb
│   └── 05_KPI_Design_and_Dashboard_Preparation.ipynb
│
├── dashboards/
│   └── power_bi_dashboard.pbix     # Power BI Executive Dashboard
│
├── outputs/
│   ├── figures/                    # 12+ visualizations
│   └── reports/                    # KPI summaries & executive report
│
└── README.md
```

---

## 🔄 Project Workflow

### Notebook 1 — Data Acquisition & Setup
- Downloaded dataset via Kaggle API
- Set up project folder structure
- Performed initial data quality assessment
- Identified 2 columns with missing values (Customer Name: 0.5%, Profit: 0.3%)

### Notebook 2 — Data Cleaning & Preprocessing
- Treated missing values using median imputation and forward fill
- Detected and treated outliers using IQR-based Winsorization:
  - Sales: 328 outliers (3.28%) capped to [−71.87, 275.33]
  - Profit: 87 outliers (0.87%) capped to [−61.87, 101.47]
- Converted date columns to datetime and optimized categorical dtypes
- Engineered 45 features including delivery days, profit margin, net revenue, and time-based variables (quarter, week, weekend flag)

### Notebook 3 — Exploratory Data Analysis
- Univariate and bivariate analysis across sales, profit, region, and segment
- Key findings:
  - **Consumer segment** leads with $537K revenue (vs. Corporate $325K, Home Office $215K)
  - **East region** is top performer at $318K revenue and $59K profit
  - **Electronics** is the highest-grossing category at $328K
  - Average 5.04 purchases per customer

### Notebook 4 — Customer Segmentation & Advanced Analytics
- **RFM Analysis** scored 1,986 customers across Recency, Frequency, and Monetary dimensions

| Segment | Count | Avg Recency (days) | Avg Frequency | Avg Spend ($) |
|---|---|---|---|---|
| Champions | 353 | 19 | 7.70 | 856 |
| Loyal Customers | 401 | 43 | 6.18 | 682 |
| At Risk | 344 | 129 | 5.88 | 634 |
| About to Sleep | 446 | 176 | 2.76 | 297 |
| New Customers | 289 | 38 | 2.98 | 294 |

- **K-Means Clustering (k=5)** applied on RFM features with PCA visualization:

| Cluster | Label | Count | Avg Spend ($) | Avg Frequency |
|---|---|---|---|---|
| 1 | High Value Customers | 291 | 1,010 | 8.69 |
| 2 | Frequent Buyers | 655 | 640 | 5.92 |
| 0 | Regular Customers | 517 | 302 | 3.13 |
| 4 | New / Growing Customers | 331 | 503 | 4.63 |
| 3 | At Risk Customers | 192 | 221 | 2.30 |

- **Cohort Retention Analysis** across 14 monthly cohorts
- **Customer Lifetime Value (CLV)** calculated per customer:
  - Average CLV: **$7,521**
  - High-Value customers (top 25%): **497 customers**
  - CLV range: $254 – $301,695

### Notebook 5 — KPI Design & Dashboard Preparation
- Designed a comprehensive KPI framework for executive reporting

---

## 📊 Key Results

| KPI | Value |
|-----|-------|
| Total Revenue | **$1,078,671** |
| Total Orders | **10,000** |
| Total Customers | **1,986** |
| Average Order Value | **$107.87** |
| Average CLV | **$7,521** |
| High-Value Customers | **497** |
| Repeat Customer Rate | **96.27%** |
| Estimated Churn Rate | **3.73%** |
| Top Product Category | **Electronics ($328K)** |
| Top Region | **East ($318K revenue)** |

---

## 📈 Power BI Executive Dashboard

A 5-page interactive Power BI dashboard built with DAX measures, Power Query transformations, slicers, and drill-through reporting:

- **Page 1 — Executive Overview:** Total Revenue, Orders, Customers, AOV
- **Page 2 — Sales Performance:** Monthly trends, regional breakdown, category analysis
- **Page 3 — Customer Segmentation:** RFM segments, K-Means cluster distribution
- **Page 4 — CLV & Retention:** CLV by segment, cohort retention heatmap
- **Page 5 — Product Analysis:** Category and sub-category performance

---

## 💡 Business Recommendations

1. **Prioritize At-Risk segment (344 customers)** — these are high-frequency buyers showing recency drop; targeted win-back campaigns could recover significant revenue
2. **Double down on Electronics in the East region** — highest revenue combination in the dataset
3. **Invest in High Value Customers (291)** — averaging $1,010 per order with 8.69 purchases; loyalty rewards would protect this revenue
4. **Investigate churn drivers** — though churn is low at 3.73%, the 192 At-Risk cluster customers show early warning signs

---

## 🛠️ Tech Stack

- **Python 3.9+** — Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Plotly, SciPy, Statsmodels
- **Power BI** — DAX, Power Query, Data Modeling
- **Jupyter Notebook / Google Colab**
- **Git & GitHub**

---

## 👩‍💻 Author

**Indu Singh**
Data Analyst | Bioinformatics Researcher
[LinkedIn](https://www.linkedin.com/in/indu-singh-458929365) · [GitHub](https://github.com/iamindusinghds)
