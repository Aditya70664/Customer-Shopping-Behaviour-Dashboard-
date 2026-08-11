🛍️ Customer Analytics Dashboard – Retail Customer Behavior & Sales Insights
Analyzing customer shopping behavior, sales performance, subscriptions, and customer preferences using Python, SQL, and Power BI.
---
![Python](https://img.shields.io/badge/Python-3.x-blue)
![SQL](https://img.shields.io/badge/SQL-Analysis-blue)
![PowerBI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)
---
📌 Table of Contents
Section	Link
Overview	Go to Overview
Business Problem	Go to Business Problem
Dataset	Go to Dataset
Tools & Technologies	Go to Tools & Technologies
Project Structure	Go to Project Structure
Data Preparation	Go to Data Preparation
Dashboard	Go to Dashboard
Key Findings	Go to Key Findings
How to Run	Go to How to Run
Recommendations	Go to Recommendations
---
🔗 Quick Project Access
Resource	Open
📊 Power BI Dashboard	`powerbi/Customer_Analytics_Dashboard.pbix`
📓 Python Notebook	`python/Customer_Analytics_Analysis.ipynb`
📘 Project Report	`documentation/Project_Report.pdf`
📄 Business Problem	`documentation/Business_Problem_Statement.pdf`
🖼️ Dashboard Image	`dashboard/Customer_Analytics_Dashboard.png`
---
Overview
This project analyzes customer shopping behavior using a retail dataset containing 3,900 customer purchase records.
The main goal is to understand how customers purchase products and identify useful patterns across:
Customer demographics
Product categories
Subscription status
Seasonal sales
Payment methods
Shipping preferences
Customer ratings
The analysis was carried out using Python and SQL, and the final results were presented through an interactive Power BI dashboard.
---
Business Problem
Retail businesses need to understand customer behavior to make better decisions around products, marketing, subscriptions, and customer service.
This project focuses on questions such as:
What is the overall customer base and average purchase value?
How many customers are subscribed?
Which product categories generate the most revenue?
Which season performs best?
How do sales differ by gender?
Which payment methods are commonly used?
Which shipping options do customers prefer?
What is the overall customer review rating?
---
Dataset
Attribute	Details
Total Records	3,900
Total Columns	18
Average Purchase Amount	$59.76
Average Review Rating	3.75 / 5.00
Main Data Type	Customer shopping transactions
Main Features
Customer ID
Age
Gender
Location
Subscription Status
Item Purchased
Category
Purchase Amount (USD)
Season
Size
Color
Previous Purchases
Payment Method
Frequency of Purchases
Review Rating
Shipping Type
---
Tools & Technologies
Tool / Technology	Purpose
Python	Data cleaning and exploratory analysis
Pandas	Data manipulation and preparation
NumPy	Numerical operations
SQL	Business-oriented data analysis
PostgreSQL	Database analysis
Power BI	Dashboard and visualization
GitHub	Version control and project documentation
---
Project Structure
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
```
---
Data Preparation
The data preparation process included:
Checking the dataset structure and data types
Checking for missing values
Standardizing column names
Handling missing `Review Rating` values
Creating useful derived fields for analysis
Checking duplicate or redundant information
Preparing the cleaned dataset for SQL and Power BI
The cleaned data was then used for further analysis and dashboard development.
---
Dashboard
The Power BI dashboard brings the main findings together in one view.
📊 Dashboard Preview
![Customer Analytics Dashboard](dashboard/Customer_Analytics_Dashboard.png)
Dashboard KPIs
KPI	Value
Number of Customers	3.9K
Average Purchase Amount	$59.76
Average Review Rating	3.75
Dashboard Visuals
Subscription Status – Shows subscribed and non-subscribed customers
Revenue by Season – Compares revenue across Fall, Spring, Winter, and Summer
Revenue by Category – Compares Clothing, Accessories, Footwear, and Outerwear
Sales by Gender – Compares sales between male and female customers
Payment Method Split – Shows the distribution of customer payment methods
Shipping Type Preference – Shows customer preferences across shipping options
---
Key Findings
1. Subscription Status
The dashboard shows approximately 27% of customers as subscribers and 73% as non-subscribers.
This indicates that subscription conversion is an important area for further customer engagement.
2. Revenue by Season
The dashboard shows:
Season	Revenue
Fall	60K
Spring	59K
Winter	59K
Summer	56K
Fall is the strongest season in the dashboard, while Summer has the lowest displayed revenue.
3. Revenue by Category
Category	Revenue
Clothing	104K
Accessories	74K
Footwear	36K
Outerwear	19K
Clothing is the strongest revenue-generating category in the dashboard.
4. Sales by Gender
The dashboard shows approximately:
Male: 158K
Female: 75K
This shows a significant difference in sales contribution between the two groups.
5. Payment Methods
The dashboard shows a relatively balanced distribution across the available payment methods, indicating that customers use multiple payment options rather than relying on one method.
6. Shipping Preferences
The dashboard compares:
Free Shipping
Express
Store Pickup
Standard
2-Day Shipping
Next Day Air
The displayed values are relatively close, suggesting that no single shipping option completely dominates customer preference.
---
How to Run
1. Clone the repository
```bash
git clone <your-github-repository-url>
cd customer-analytics-dashboard
```
2. Install Python libraries
```bash
pip install pandas numpy matplotlib sqlalchemy psycopg2-binary jupyter
```
3. Run the Python Notebook
Open:
```text
python/Customer_Analytics_Analysis.ipynb
```
Run the notebook cells sequentially to perform data preparation and analysis.
4. Run the SQL Analysis
Open:
```text
sql/Customer_Analytics_Queries.sql
```
Run the queries using your PostgreSQL environment.
5. Open the Power BI Dashboard
Open:
```text
powerbi/Customer_Analytics_Dashboard.pbix
```
using Microsoft Power BI Desktop.
---
Recommendations
Based on the dashboard analysis:
Improve subscription conversion by targeting the large non-subscriber customer base.
Prioritize strong categories, especially Clothing and Accessories, when planning inventory and promotions.
Use seasonal trends to support marketing and inventory planning.
Study customer segments to create more relevant offers for different types of buyers.
Review shipping preferences when designing delivery-related promotions.
Monitor customer ratings to understand product satisfaction alongside sales performance.
---
Project Outcome
The final dashboard provides a simple view of customer behavior and sales performance in one place.
The project demonstrates a complete analytics workflow:
Data → Python → SQL → Power BI → Business Insights
It focuses on turning raw customer transaction data into information that can be understood and used for business decisions.
---
Skills Demonstrated
Data Cleaning
Exploratory Data Analysis
SQL Analysis
Data Visualization
Power BI Dashboard Development
Business Analysis
Data Interpretation
GitHub Project Documentation
---
👤 Author
Aditya Sharma
B.Tech CSE Student  
Aspiring Data Analyst & Software Engineer
