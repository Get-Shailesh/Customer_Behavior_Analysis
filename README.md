# 🛍️ Customer Shopping Behavior Analysis

## 📌 Project Overview
This project analyzes customer shopping behavior using transactional data to extract meaningful insights into customer preferences, spending patterns, product performance, and subscription behavior. The analysis leverages **Python for data preprocessing**, **SQL for business analytics**, and **Power BI for data visualization**, enabling data-driven decision-making for businesses.

---

## 🎯 Objectives
- Analyze customer purchasing patterns
- Understand the impact of discounts and subscriptions
- Identify high-performing products and categories
- Segment customers based on purchase behavior
- Provide actionable business recommendations

---

## 📂 Dataset Description
- **Total Records:** 3,900 customer transactions  
- **Total Columns:** 18  

### Key Features:
- **Customer Demographics:** Age, Gender, Location, Subscription Status  
- **Purchase Details:** Item Purchased, Category, Purchase Amount, Season, Size, Color  
- **Shopping Behavior:** Discount Applied, Review Rating, Shipping Type  
- **Purchase History:** Previous Purchases, Purchase Frequency  

---

## 🧹 Data Cleaning & Feature Engineering (Python)
- Loaded and explored data using `pandas`
- Checked data structure and summary statistics
- Handled missing values in the *Review Rating* column using category-wise median
- Standardized column names using snake_case
- Created new features:
  - `age_group`
  - `purchase_frequency_days`
- Identified and removed redundant columns
- Loaded cleaned data into **PostgreSQL** for SQL-based analysis

---

## 🗄️ SQL Analysis (Business Insights)
Key business questions answered using SQL:

- Revenue contribution by gender
- Spending behavior of discount users
- Top-rated and most purchased products
- Shipping type impact on purchase amount
- Subscribers vs non-subscribers analysis
- Discount-dependent products
- Customer segmentation (New, Returning, Loyal)
- Revenue contribution by age group
- Relationship between repeat purchases and subscriptions

### Example SQL Query
```sql
SELECT subscription_status,
       AVG(purchase_amount) AS avg_spend,
       SUM(purchase_amount) AS total_revenue
FROM customer_data
GROUP BY subscription_status;

