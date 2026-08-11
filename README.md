# 🛍️ Customer Analytics Dashboard – Retail Customer Behavior & Sales Insights

_Analyzing customer shopping behavior, sales performance, subscriptions, and customer preferences using Python, SQL, and Power BI._

---

![Python](https://img.shields.io/badge/Python-3.x-blue)
![SQL](https://img.shields.io/badge/SQL-Analysis-blue)
![PowerBI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow)
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
| Data Preparation | [Go to Data Preparation](#data-preparation) |
| Dashboard | [Go to Dashboard](#dashboard) |
| Key Findings | [Go to Key Findings](#key-findings) |
| How to Run | [Go to How to Run](#how-to-run) |
| Recommendations | [Go to Recommendations](#recommendations) |

---

## 🔗 Quick Project Access

| Resource | File |
|---|---|
| 📊 Power BI Dashboard | `powerbi/Customer_Analytics_Dashboard.pbix` |
| 📓 Python Notebook | `python/Customer_Analytics_Analysis.ipynb` |
| 📘 Project Report | `documentation/Project_Report.pdf` |
| 📄 Business Problem | `documentation/Business_Problem_Statement.pdf` |
| 🖼️ Dashboard Image | `dashboard/Customer_Analytics_Dashboard.png` |

---

## Overview

This project analyzes customer shopping behavior using a retail dataset containing **3,900 customer purchase records**.

The main goal is to understand customer purchasing patterns and identify useful insights across:

- Customer demographics
- Product categories
- Subscription status
- Seasonal sales
- Payment methods
- Shipping preferences
- Customer ratings

The analysis was carried out using **Python and SQL**, and the results were presented through an interactive **Power BI dashboard**.

---

## Business Problem

Retail businesses need to understand customer behavior to make better decisions around products, marketing, subscriptions, and customer service.

This project focuses on questions such as:

- What is the overall customer base and average purchase value?
- How many customers are subscribed?
- Which product categories generate the most revenue?
- Which season performs best?
- How do sales differ by gender?
- Which payment methods are used by customers?
- Which shipping options do customers prefer?
- What is the overall customer review rating?

---

## Dataset

| Attribute | Details |
|---|---|
| Total Records | 3,900 |
| Average Purchase Amount | $59.76 |
| Average Review Rating | 3.75 / 5.00 |
| Main Data Type | Customer shopping transactions |

### Main Features

- Customer ID
- Age
- Gender
- Location
- Subscription Status
- Item Purchased
- Category
- Purchase Amount (USD)
- Season
- Size
- Color
- Previous Purchases
- Payment Method
- Frequency of Purchases
- Review Rating
- Shipping Type

---

## Tools & Technologies

| Tool / Technology | Purpose |
|---|---|
| Python | Data cleaning and exploratory analysis |
| Pandas | Data manipulation and preparation |
| NumPy | Numerical operations |
| SQL | Data analysis |
| PostgreSQL | Database analysis |
| Power BI | Dashboard and visualization |
| GitHub | Version control and documentation |

---

## Project Structure

```text
customer-analytics-dashboard/
│
├── README.md
│
├── data/
│   └── customer_shopping_behavior.csv
│
├── python/
│   └── Customer_Analytics_Analysis.ipynb
│
├── sql/
│   └── Customer_Analytics_Queries.sql
│
├── powerbi/
│   └── Customer_Analytics_Dashboard.pbix
│
├── documentation/
│   ├── Business_Problem_Statement.pdf
│   └── Project_Report.pdf
│
└── dashboard/
    └── Customer_Analytics_Dashboard.png
