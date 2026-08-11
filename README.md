##🛍️ Consumer Retail Analysis – Customer Behavior & Sales Insights

_Analyzing customer shopping behavior and retail trends to drive strategic business decisions using Python, SQL, and Power BI._

---

![Python](https://img.shields.io/badge/Python-3.11-blue)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-blue)
![PowerBI](https://img.shields.io/badge/PowerBI-Dashboard-yellow)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

---

## 📌 Table of Contents

| Section | Link |
|---|---|
| Overview | [Go to Overview](#overview) |
| Business Problem | [Go to Business Problem](#business-problem) |
| Dataset | [Go to Dataset](#dataset) |
| Tools & Technologies | [Go to Tools & Technologies](#tools--technologies) |
| Project Structure | [Go to Project Structure](#project-structure) |
| Data Cleaning & Preparation | [Go to Data Cleaning & Preparation](#data-cleaning--preparation) |
| Exploratory Data Analysis | [Go to EDA](#exploratory-data-analysis-eda) |
| Research Questions & Key Findings | [Go to Findings](#research-questions--key-findings) |
| Dashboard | [Go to Dashboard](#dashboard) |
| How to Run This Project | [Go to Setup Guide](#how-to-run-this-project) |
| Final Recommendations | [Go to Recommendations](#final-recommendations) |
| Author & Contact | [Go to Contact](#author--contact) |
---


## 🔗 Quick Project Access

| Resource | Open |
|---|---|
| 📊 Power BI Dashboard | [Open Dashboard](Consumer%20Retail%20Analysis%20Dashboard.pbix) |
| 📓 Jupyter Notebook | [Open Notebook](Consumer%20Retail%20Analysis%20notebook.ipynb) |
| 📘 Project Report | [Open Report](Consumer%20Retail%20Analysis%20Project%20Report.pdf) |

---

## Overview

This project analyzes customer shopping behavior using transactional retail data from **3,900 purchases** across multiple product categories. The goal is to uncover actionable insights into spending patterns, customer segmentation, product preferences, seasonal trends, and subscription behavior — all to support smarter, data-driven retail decisions.

A complete data pipeline was built using **Python** for data cleaning and EDA, **PostgreSQL** for structured SQL analysis, and **Power BI** for interactive dashboard visualization.

---

## Business Problem

Understanding what drives customer spending is critical for any retail business. This project aims to:

- Identify high-value customer segments and their purchasing patterns
- Understand the impact of discounts and promo codes on revenue
- Analyze product category performance across demographics and seasons
- Investigate the gap between loyal buyers and subscription conversion
- Support strategic marketing, pricing, and inventory decisions

---

## Dataset

| Attribute | Details |
|---|---|
| Total Rows | 3,900 |
| Total Columns | 18 |
| Missing Values | 37 values in `Review Rating` column |
| Average Purchase Amount | $59.76 |
| Average Review Rating | 3.75 / 5.00 |

**Key Features:**
- **Customer Demographics** – Age, Gender, Location, Subscription Status
- **Purchase Details** – Item Purchased, Category, Purchase Amount, Season, Size, Color
- **Shopping Behavior** – Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type

---

## Tools & Technologies

| Tool / Technology | Purpose |
|---|---|
| Python (Pandas, NumPy) | Data loading, cleaning, feature engineering |
| PostgreSQL | Database storage and SQL-based analysis |
| SQLAlchemy | Python-to-PostgreSQL integration |
| Power BI | Interactive dashboard and report visualization |
| Microsoft Excel | Additional dashboard development and KPI cards |
| pgAdmin / psql | SQL query execution and database management |

---

## Project Structure

```
consumer-retail-analysis/
│
├── README.md
├── Business Problem Document.pdf          # Problem statement and objectives
├── Consumer Retail Analysis Project Report.pdf  # Full project report
│
├── Consumer Retail Analysis notebook.ipynb     # EDA + SQL analysis notebook
│
├── Consumer_Retail_Analysis.xlsx              # Raw dataset (Excel)
│
├── data/                                      # Supporting data files
│   └── (CSV files used for analysis)
│
└── images/                                    # Dashboard screenshots
    └── Consumer Retail Analysis Dashboard.png
```

> **Note:** The Power BI dashboard file (`Consumer Retail Analysis Dashboard.pbix`) is included for interactive exploration of all visualizations.

---

## Data Cleaning & Preparation

- **Missing Values**: Imputed missing `Review Rating` values using the median rating per product category
- **Column Standardization**: Renamed all columns to `snake_case` for consistency and readability
- **Feature Engineering**:
  - Created `age_group` column by binning customer ages (Young Adult, Adult, Middle-aged, Senior)
  - Created `purchase_frequency_days` column derived from purchase history
- **Redundancy Check**: Verified that `discount_applied` and `promo_code_used` were redundant; dropped `promo_code_used`
- **Database Integration**: Loaded the cleaned DataFrame into PostgreSQL via SQLAlchemy for SQL-based analysis

---

## Exploratory Data Analysis (EDA)

**Summary Statistics:**
- Purchase Amount Range: $20 – $100 (Mean: $59.76)
- Age Range: 18 – 70 years (Mean: 44 years)
- Review Rating Range: 2.5 – 5.0 (Mean: 3.75)

**Key Observations:**
- Most frequent category: **Clothing** (Blouse was the most purchased item)
- Most common location: **Montana**
- Payment methods were nearly evenly distributed across PayPal, Credit Card, Cash, Debit Card, Venmo, and Bank Transfer
- **73% of customers are non-subscribers**, presenting a major conversion opportunity

---

## Research Questions & Key Findings

1. **Revenue by Gender** – Male customers contributed ~$157,890 vs. ~$75,191 from female customers — a **2.1× difference**

2. **High-Spending Discount Users** – **839 customers** used discounts but still spent above the average purchase amount

3. **Top 5 Products by Rating**:
   | Item | Avg. Rating |
   |---|---|
   | Gloves | 3.86 |
   | Sandals | 3.84 |
   | Boots | 3.82 |
   | Hat | 3.80 |
   | Skirt | 3.78 |

4. **Shipping Type Comparison** – Express shipping users averaged **$60.48** vs. Standard at **$58.46**

5. **Subscribers vs. Non-Subscribers** – Subscribers (1,053) averaged $59.49/transaction; Non-subscribers (2,847) averaged $59.87 with significantly higher total revenue ($170,436)

6. **Discount-Dependent Products**:
   | Item | Discount Rate |
   |---|---|
   | Hat | 50.00% |
   | Sneakers | 49.66% |
   | Coat | 49.07% |
   | Sweater | 48.17% |
   | Pants | 47.37% |

7. **Customer Segmentation**:
   | Segment | Customers |
   |---|---|
   | Loyal (>10 purchases) | 3,116 |
   | Returning (2–10 purchases) | 701 |
   | New (1 purchase) | 83 |

8. **Top 3 Products Per Category** – Clothing: Blouse, Pants, Shirt | Accessories: Jewelry, Sunglasses, Belt | Footwear: Sandals, Shoes, Sneakers | Outerwear: Jacket, Coat

9. **Repeat Buyers & Subscriptions** – 2,518 repeat buyers (>5 purchases) have **no subscription**, revealing a large untapped loyalty-to-subscription conversion gap

10. **Revenue by Age Group**:
    | Age Group | Total Revenue |
    |---|---|
    | Young Adult | $62,143 |
    | Middle-aged | $59,197 |
    | Adult | $55,978 |
    | Senior | $55,763 |

---

## 📊 Dashboard

The Power BI dashboard provides a complete visual analysis of customer behavior, category performance, subscription trends, payment preferences, and seasonal sales insights.

### ✨ Dashboard Features
- KPI Cards for Total Customers, Average Purchase Amount & Review Rating
- Subscription Analysis
- Revenue & Sales Trends
- Age Group Insights
- Payment Method Distribution
- Shipping Preference Analysis
- Seasonal Revenue Trends

---

## 🖼️ Dashboard Preview

![Consumer Retail Insights Dashboard](Consumer%20Retail%20Analysis%20Dashboard%20Image.png)

---

## 🚀 Interactive Dashboard

To explore the dashboard interactively:

1. Download or clone this repository
2. Open:
```text
Consumer Retail Analysis Dashboard.pbix
```
3. Launch using Microsoft Power BI Desktop
4. Use slicers, filters, and visuals to interact with the dashboard dynamically

### 📌 Interactive Features

✔ Dynamic Filtering  
✔ Cross-Chart Highlighting  
✔ KPI Tracking  
✔ Category-Level Drilldown  
✔ Seasonal Trend Analysis  
✔ Customer Segment Insights
---

## How to Run This Project

1. **Clone the repository:**
```bash
git clone https://github.com/AbhisekChandra-SenGupta1/Consumer-Retail-Analysis---SQL-Python-Power-BI.git
cd Consumer-Retail-Analysis---SQL-Python-Power-BI
```

2. **Install required Python libraries:**
```bash
pip install pandas numpy matplotlib seaborn sqlalchemy psycopg2 jupyter
```

3. **Open the dataset:**
   - The raw data is available in `Consumer_Retail_Analysis.xlsx`
   - Load it in the notebook using `pandas.read_excel()`

4. **Run the Jupyter Notebook:**
   - Open `Consumer Retail Analysis notebook.ipynb` in Jupyter or VS Code
   - Run all cells sequentially — the notebook covers data loading, cleaning, feature engineering, EDA, and SQL-based analysis

5. **View the Power BI Dashboard:**
   - Open `Consumer Retail Analysis Dashboard.pbix` in **Power BI Desktop**
   - All visuals are pre-built and interactive — no additional setup needed

6. **Read the full report:**
   - Open `Consumer Retail Analysis Project Report.pdf` for a complete walkthrough of methodology, findings, and recommendations
   - Refer to `Business Problem Document.pdf` for the original problem statement and objectives

---

## Final Recommendations

- **Boost Subscription Conversion** – Target 2,518 loyal non-subscribers with exclusive discounts and early access offers to convert them into subscribers
- **Leverage Male Customer Segment** – With 2× higher revenue, personalized campaigns and loyalty rewards for male demographics can maximize returns
- **Capitalize on Young Adult Spending** – Young Adults contribute the highest total revenue ($62,143); prioritize digital-first, trend-driven campaigns for this segment
- **Promote Express Shipping** – Express shipping correlates with higher order values ($60.48); limited-time express discounts could lift average order value across all segments
- **Review Discount Policy** – High discount dependency on items like Hat (50%) and Sneakers (49.66%) risks margin erosion; shift toward tiered or loyalty-based discounts
- **Seasonal Marketing Push** – Fall is the peak revenue season; pre-fall inventory scaling and email campaigns can maximize seasonal revenue capture
- **Highlight Top-Rated Products** – Feature Gloves, Sandals, and Boots prominently in banners and category pages to improve conversion rates

---

## Author & Contact

**Abhisek Chandra Sen Gupta**  
B.Tech CSE Student | Siliguri Institute of Technology  
Aspiring Data Analyst & Software Engineer

📧 Email: abhisekchandrasengupta@gmail.com  
📞 Phone: +91-9382933694  
🔗 [LinkedIn](https://www.linkedin.com/in/abhisek-chandra-sen-gupta-573987289/)  
🔗 [GitHub](https://github.com/AbhisekChandra-SenGupta1)
