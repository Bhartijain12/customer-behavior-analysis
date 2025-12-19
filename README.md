
#  Customer Shopping Behavior Analysis

## Project Overview

This project analyzes retail customer shopping behavior using transactional data to uncover patterns in spending, customer segments, product performance, and subscription behavior.

The objective is to convert raw customer data into **business-ready insights** that support decisions related to marketing strategy, customer retention, and product positioning.

The project demonstrates a **complete data analytics workflow** using Python, SQL, and Power BI.

---

## Business Problem

Retail businesses collect large volumes of customer and transaction data but often struggle to identify:

* Which customer segments drive the most revenue
* Whether subscriptions influence purchasing behavior
* Which products and categories perform best
* How customer behavior varies across demographics

This project addresses these challenges by combining data cleaning, structured SQL analysis, and interactive visualization.

---

## Dataset Summary

* **Total Records:** 3,900 transactions
* **Total Columns:** 18

### Key Attributes

* **Customer Demographics:** Age, Gender, Location, Subscription Status
* **Purchase Details:** Item Purchased, Category, Purchase Amount, Season, Size, Color
* **Behavioral Data:** Discount Applied, Previous Purchases, Purchase Frequency, Review Rating, Shipping Type

### Data Quality Notes

* Missing values were found in the *Review Rating* column
* Redundant fields required validation and cleanup

---

## Data Cleaning & EDA (Python)

Data preparation was performed using **pandas** to ensure analytical accuracy.

### Steps Performed

* Loaded and explored data using `df.info()` and `df.describe()`
* Handled missing values in *review_rating* using median imputation per product category
* Standardized column names to `snake_case`
* Created new features:

  * `age_group` using quantile-based binning
* Identified redundancy between `discount_applied` and `promo_code_used` and removed duplicate columns
* Loaded cleaned data into **PostgreSQL** for SQL-based analysis

---

##  Business Analysis Using SQL

PostgreSQL was used to answer key business questions, including:

1. Revenue contribution by gender
2. High-spending customers who used discounts
3. Top 5 products by average review rating
4. Comparison of purchase behavior by shipping type
5. Subscription vs non-subscription spending analysis
6. Products most frequently purchased with discounts
7. Customer segmentation (New, Returning, Loyal)
8. Top 3 products per category using window functions
9. Subscription likelihood among repeat buyers
10. Revenue contribution by age group

---

##  Key SQL Insights (Highlighted)

* **Subscription Impact:**
  Average purchase value is similar for subscribed and non-subscribed customers, indicating subscriptions currently support retention rather than higher transaction size.

* **Product Concentration:**
  A small number of products dominate purchases within each category, highlighting clear customer preferences.

* **Age-Based Revenue:**
  Customers aged **26–35** contribute the highest share of revenue, making them a priority target segment.



##  Power BI Dashboard

An interactive dashboard was created in **Power BI** to visualize insights.

### Dashboard Features

* Revenue and customer distribution
* Subscription behavior comparison
* Product and category performance
* Age group contribution analysis
* Interactive slicers for filtering and exploration

The dashboard focuses on **clarity, minimalism, and business relevance**, avoiding unnecessary visuals.


## Business Recommendations

* **Optimize Subscription Strategy:** Focus on engagement and retention benefits rather than immediate revenue uplift.
* **Strengthen Loyalty Programs:** Encourage repeat buyers to transition into loyal customers.
* **Review Discount Strategy:** Reduce over-dependence on discounts for specific products to protect margins.
* **Product Promotion:** Highlight top-performing and frequently purchased products.
* **Targeted Marketing:** Prioritize high-revenue age groups for campaigns.

## 🛠 Tools & Technologies

* **Python:** pandas, numpy
* **SQL:** PostgreSQL
* **Visualization:** Power BI
* **Version Control:** Git & GitHub

##  Project Status

**Completed**

