# 🛍️ Customer Shopping Behavior Analysis

A end-to-end data analysis project exploring customer purchasing patterns across **3,900 transactions**, combining Python for data wrangling, MYSQL for business queries, and Power BI for interactive dashboards.

## 📌 Project Overview

Ever wonder what makes customers tick — why they buy, how often, and how much they spend? This project digs into those questions using real transactional retail data. The goal was to surface actionable insights around customer segmentation, discount behavior, product performance, and subscription patterns that can guide smarter business decisions.

## 📂 Dataset
1. Total Records = 3,900 purchases.
2. Features  18 columns .
3. Missing Data  37 values in *review_rating* (handled via median imputation)

**Feature categories covered:**
- **Demographics** — Age, Gender, Location, Subscription Status.
- **Purchase Details** — Item, Category, Amount, Season, Size, Color.
- **Behavior** — Discount Applied, Previous Purchases, Purchase Frequency, Review Rating, Shipping Type.

## 🛠️ Tech Stack

1. Python (Pandas) for Data cleaning, feature engineering, EDA.
2. MYSQL for Business-level SQL analysis.
3. Power BI for Interactive dashboard & visualization.

## 🔍 What I Did

### 1. Data Cleaning & Preparation (Python)
- Loaded and explored the dataset using *pandas* (*df.info()*, *df.describe()*).
- Imputed missing *review_rating* values using **median rating per product category**.
- Standardized all column names to *snake_case*.
- Engineered new features:
  - *age_group* — binned customer ages for segment analysis.
  - *purchase_frequency_days* — derived from purchase history.
- Dropped *promo_code_used* after confirming it was redundant with *discount_applied*.
- Loaded the cleaned DataFrame into **MYSQL** for SQL analysis.

### 2. SQL Business Analysis (MYSQL)
Answered 10 key business questions:

1. **Revenue by Gender** — compared male vs. female revenue contribution
2. **High-Spending Discount Users** — customers who used discounts but spent above average
3. **Top 5 Products by Rating** — highest average review-rated items
4. **Shipping Type Comparison** — Standard vs. Express average spend
5. **Subscribers vs. Non-Subscribers** — average spend and total revenue by subscription status
6. **Discount-Dependent Products** — 5 products with highest % of discounted purchases
7. **Customer Segmentation** — classified customers as New, Returning, or Loyal by purchase count
8. **Top 3 Products per Category** — most purchased items within each category
9. **Repeat Buyers & Subscriptions** — do customers with >5 purchases subscribe more?
10. **Revenue by Age Group** — which age segments drive the most revenue

### 3. Power BI Dashboard
Built an interactive dashboard to communicate findings visually — filters, drill-throughs, and KPI cards for stakeholder-friendly exploration.

---

## 💡 Key Business Recommendations

- **Boost Subscriptions** — promote exclusive perks to convert non-subscribers.
- **Loyalty Programs** — incentivize returning customers to reach "Loyal" status.
- **Revisit Discount Policy** — discounts drive volume but may compress margins.
- **Product Spotlighting** — push top-rated and best-selling items in marketing campaigns.
- **Targeted Marketing** — prioritize high-revenue age groups and express-shipping customer.

## 📁 Project Structure

├── data/
│   └── shopping_behavior_raw.csv
├── Jupyter notebook/
│   └── data_cleaning.py
├── Mysql/
│   ├── revenue_by_gender.sql
│   ├── customer_segmentation.sql
│   └── ...
├── dashboard/
│   └── shopping_behavior.pbix
└── README.md
```
