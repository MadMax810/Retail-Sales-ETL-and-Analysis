# Retail Sales Data Analysis & Insights

![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)
![Libraries](https://img.shields.io/badge/Libraries-Pandas%20%7C%20Matplotlib%20%7C%20Seaborn-orange.svg)
![Project Status](https://img.shields.io/badge/Status-Completed-green.svg)

A comprehensive data analysis project focused on cleaning, transforming, and analyzing product sales data to uncover key business insights. This project demonstrates a full data analysis workflow, from raw data ingestion to final actionable recommendations, making it a key component of my professional portfolio.

## Table of Contents
- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Dataset](#dataset)
- [Tools and Libraries](#tools-and-libraries)
- [Data Cleaning and Preparation (ETL)](#data-cleaning-and-preparation-etl)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Key Insights & Business Recommendations](#key-insights--business-recommendations)
- [How to Run This Project](#how-to-run-this-project)
- [Contact](#contact)

## Project Overview

In this project, I performed an in-depth analysis of a retail dataset to understand sales performance and customer behavior. The project involved a significant data cleaning and transformation phase, followed by exploratory data analysis to extract meaningful patterns and insights. The final output is a clean, merged dataset and a series of visualizations and findings that could help a business make data-driven decisions.

## Problem Statement

The primary goal of this project was to take raw, messy sales data and transform it into a clean, usable format for analysis. The key objectives were to:
1.  Clean and pre-process data from multiple sources (`orders`, `products`, `customers`).
2.  Merge the datasets to create a single, unified view of sales transactions.
3.  Derive new, meaningful columns, such as `total_price`.
4.  Perform exploratory analysis to answer key business questions like:
    * What are the top-selling and highest-revenue products?
    * Who are the most valuable customers contributing the most to revenue?
    * What is the daily sales trend?

## Dataset

The raw data is contained in three separate CSV files:
* `orders.csv`: Contains transaction data including `order_id`, `date`, `customer_id`, `product_id`, and `qty` (quantity).
* `products.csv`: Contains product details like `product_name` and `price (in INR)`.
* `customers.csv`: Contains customer information, mapping `customer_id` to `customer` name.

## Tools and Libraries

* **Python:** The core programming language for the analysis.
* **Pandas:** Used for data manipulation, cleaning, and merging.
* **Matplotlib & Seaborn:** Used for data visualization to create charts and graphs.
* **Jupyter Notebook:** The environment used for developing, documenting, and sharing the analysis.

## Data Cleaning and Preparation (ETL)

The initial dataset required several cleaning and transformation steps to be ready for analysis. The key steps performed were:
* **Correcting Data Types:** The `qty` column in `orders.csv` contained non-numeric characters (e.g., '8Q'). These were stripped to keep only integer values. A blank `qty` value was found and handled.
* **Handling Inconsistent Casing:** Customer names in `customers.csv` (e.g., 'JaY', 'johN') were standardized to lowercase for consistency.
* **Removing Duplicates:** Checked for and removed duplicate `customer_id` entries in the `customers.csv` file (customer_id 35 appeared twice).
* **Data Enrichment (Joining Tables):** Merged the `orders`, `customers`, and `products` tables based on their respective IDs to create a single, comprehensive DataFrame.
* **Feature Engineering:** Created a new column `total_price` by multiplying the `qty` and the product `price`.
* **Cleaning Price Column:** Removed the '₹' symbol and extra whitespace from the `price (in INR)` column in `products.csv` and converted it to a numeric type.

## Exploratory Data Analysis (EDA)

Several questions were investigated to understand the data:

1.  **Which products generate the most revenue?**
    * **Finding:** An analysis of total sales per product shows that **Chicken and Apple are the top two products**, generating ₹22,750 and ₹21,600 in revenue respectively. This makes them the most critical assets for the business from a revenue standpoint.
    

2.  **Who are the top 5 customers by spending?**
    * **Finding:** The analysis revealed that a small group of customers drives a significant portion of revenue. **Mike is the top customer with ₹10,480 in total spending**, followed by Ravi and Bruce.
   

3.  **What is the overall sales trend?**
    * **Finding:** An analysis of total sales per day shows daily fluctuations, with a **noticeable peak in sales on February 12th, 2023**. Investigating the cause of such peaks could reveal opportunities for event-based promotions.
   

## Key Insights & Business Recommendations

Based on the analysis, the following insights were uncovered:

* **Insight 1: High-Value Products Drive Revenue.** While items like Eggs and Yogurt are sold frequently, high-priced items like **Chicken (₹250)** and **Apples (₹200)** are the main revenue drivers.
    * **Recommendation:** Create targeted marketing campaigns or bundle offers featuring these high-revenue products. For example, "Get 10% off on Apples with every purchase of Chicken."

* **Insight 2: Top Customers are Vital.** The top 3 customers (**Mike, Ravi, and Bruce**) contribute over 45% of the total revenue in this dataset.
    * **Recommendation:** Implement a customer loyalty program to retain these high-value customers. Offer exclusive discounts or early access to new products to enhance their engagement and reward their loyalty.

* **Insight 3: Sales Peaks Suggest Promotion Opportunities.** The spike in sales on Feb 12th indicates that certain days have unusually high activity.
    * **Recommendation:** Analyze the events or promotions that may have occurred on peak sales days. This pattern can be leveraged to plan future marketing calendars and sales events to maximize revenue.

## How to Run This Project

To replicate this analysis, an analyst would typically:
1.  Clone the repository.
2.  Install the required libraries (`pandas`, `matplotlib`, `seaborn`).
3.  Run the analysis script or Jupyter Notebook (`Sales Analysis.ipynb`) to perform the data cleaning and generate the visualizations.

This README summarizes the key findings from that analysis.

## Contact
Abishmita Swain - abishmita13@gmail.com

LinkedIn - www.linkedin.com/in/abishmita-swain-4a0103362
