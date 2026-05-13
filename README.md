# 🛒 Brazilian E-Commerce Sales Analysis

### End-to-End Data Analytics Project | Python · MySQL · Power BI

---

## 📌 Project Overview

An end-to-end sales analysis on the **Olist Brazilian E-Commerce dataset** — 100,000+ real orders placed between 2016 and 2018.

This project covers the complete data analyst workflow:

> **Raw CSV Data → Python (Cleaning & Merging) → MySQL (Business Queries) → Power BI (Dashboard)**

---

## 🎯 Business Questions Answered

| # | Question | Tool |
|---|----------|------|
| 1 | How has monthly revenue trended over time? | MySQL + Power BI |
| 2 | Which states generate the most revenue? | MySQL + Power BI |
| 3 | Which are the top 10 products by revenue? | MySQL |
| 4 | What % of customers are new vs repeat buyers? | MySQL |
| 5 | What is the on-time vs late delivery split? | MySQL + Power BI |
| 6 | What is the average delivery time in days? | MySQL |
| 7 | Which cities generate the most revenue? | MySQL + Power BI |

---

## 📊 Power BI Dashboard

The dashboard file is included as `olist_dashboard.pbix`. Open it in Power BI Desktop to explore the interactive report.

---

## 🗂️ Dataset

**Source:** [Olist Brazilian E-Commerce — Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

| File | Description |
|------|-------------|
| `olist_orders_dataset.csv` | Order status & timestamps |
| `olist_order_items_dataset.csv` | Items, price & freight per order |
| `olist_customers_dataset.csv` | Customer city & state |
| `olist_products_dataset.csv` | Product category & dimensions |
| `olist_order_payments_dataset.csv` | Payment type & value |
| `olist_order_reviews_dataset.csv` | Review scores & comments |

> ⚠️ Raw CSV files are not included due to size limits. Download from the Kaggle link above and place in a `/data/` folder before running the notebook.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| **Python** (Pandas, NumPy, Matplotlib, Seaborn) | Data loading, merging 6 tables, feature engineering |
| **MySQL** | 7 business queries covering revenue, delivery & customers |
| **Power BI** | Interactive 2-page dashboard with KPIs, maps & charts |

---

## 📁 Repository Structure

```
brazilian-ecommerce-analysis/
│
├── olist_analysis.ipynb      ← Python: data cleaning & merging
├── olist_queries.sql         ← MySQL: 7 business analysis queries
├── olist_dashboard.pbix      ← Power BI: interactive dashboard
│
├── screenshots/
│   ├── dashboard_page1.png   ← Sales & revenue overview
│   └── dashboard_page2.png   ← Delivery & customer analysis
│
├── requirements.txt
├── .gitignore
└── README.md
```

---

## 🔍 Python — What Was Done (`olist_analysis.ipynb`)

- Loaded 6 Olist CSV files into Pandas DataFrames
- Checked shape, data types, and null values across all tables
- Merged all 6 tables into one master DataFrame with 40 columns and ~100k rows
- Engineered 3 new features:
  - `Total_Price` — item price + freight value
  - `order_month` — extracted for monthly trend analysis
  - `delivery_days` — number of days from purchase to delivery
- Exported master dataset as `final_dataset.csv` for MySQL import

---

## 🔍 MySQL — Queries Included (`olist_queries.sql`)

| Query | Business Question | SQL Techniques Used |
|-------|-------------------|---------------------|
| 1 | Monthly revenue trend | `DATE_FORMAT`, `GROUP BY`, `ORDER BY` |
| 2 | Revenue by state | Aggregation, `SUM`, `COUNT DISTINCT` |
| 3 | Top 10 products by revenue | `GROUP BY`, `ORDER BY`, `LIMIT` |
| 4 | New vs repeat customers | Subquery, `CASE WHEN` |
| 5 | On-time vs late deliveries | `CASE WHEN`, date comparison |
| 6 | Average delivery days | `AVG()`, `DATEDIFF()` |
| 7 | Top 10 cities by revenue | Aggregation, `LIMIT` |

---

## 🔑 Key Findings

- 📈 **Revenue peaked in November 2017** — driven by Black Friday promotions
- 🗺️ **São Paulo state** generates the highest revenue, accounting for ~40% of total orders
- 🔁 **~97% of customers are one-time buyers** — repeat purchase rate is very low
- 🚚 **Average delivery time is ~12 days** — late deliveries strongly correlate with lower review scores
- 🏙️ **Top city: São Paulo** followed by Rio de Janeiro and Belo Horizonte

---

## ⚙️ How to Run

### Python Notebook
```bash
# 1. Clone the repo
git clone https://github.com/YOUR_USERNAME/brazilian-ecommerce-analysis.git

# 2. Install dependencies
pip install -r requirements.txt

# 3. Download Kaggle CSVs → place all 6 files in a /data/ folder

# 4. Run the notebook
jupyter notebook olist_analysis.ipynb
```

### MySQL
```
1. Open MySQL Workbench
2. Run: CREATE DATABASE PORTFOLIO;
3. Import final_dataset.csv using Table Data Import Wizard
4. Open and run olist_queries.sql
```

### Power BI
```
1. Open olist_dashboard.pbix in Power BI Desktop
2. Update data source path to your local final_dataset.csv
3. Click Refresh
```

---

## 📦 Requirements

```
pandas>=2.0
numpy>=1.24
matplotlib>=3.7
seaborn>=0.12
jupyter>=1.0
```

---

## 🙋 About Me

**[Your Name Here]**
Data Analyst | Python · SQL · Power BI

🔗 [LinkedIn](https://linkedin.com/in/YOUR_LINKEDIN)
🔗 [GitHub](https://github.com/YOUR_USERNAME)

---

*Dataset credit: [Olist](https://olist.com/) via Kaggle. All analysis is original work.*
