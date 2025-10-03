# Sales Data Cleaning & Transformation Project


This project showcases a comprehensive data cleaning and transformation process applied to a raw product sales dataset. Developed as a hands-on exercise, it demonstrates critical skills in preparing real-world data for robust analysis. My objective was to resolve various data quality issues, ensuring the dataset's integrity and readiness for downstream analytical tasks and business intelligence reporting. This directly reflects my capability in the crucial **Extract, Transform, Load (ETL)** stage of the data pipeline.

---

## 📊 Dataset Description

The project utilizes a relational dataset composed of three CSV files, simulating a typical e-commerce sales environment:

* `customers.csv`: Contains unique customer identifiers and names.
* `products.csv`: Details product information, including IDs, names, and unit prices.
* `orders.csv`: The transactional core, linking customers to products via order details (order ID, customer ID, product ID, quantity).

**Files in this Repository:**
* `product_sales_raw.csv`: The original, uncleaned dataset with various inconsistencies.
* `product_sales_cleaned.csv`: The final, transformed dataset, ready for analysis.

---

## ✨ Key Data Cleaning & Transformation Steps

This project meticulously addressed several common data quality challenges, employing systematic approaches to ensure data accuracy and consistency:

1.  **Standardizing Text Fields:**
    * Corrected inconsistent capitalization in `customer_name` (e.g., "JaY" to "Jay").
    * Trimmed leading/trailing whitespaces from `product_name` (e.g., "  Apple" to "Apple").
2.  **Validating and Correcting Data Types:**
    * Identified and removed non-numeric characters from the `quantity` column (e.g., "10Q" to "10") to ensure it was purely numeric.
    * Verified `price` columns were correctly formatted as numerical values to support calculations.
3.  **Handling Missing Values (Imputation/Removal):**
    * Strategically addressed null or blank entries in critical columns like `quantity` to prevent errors in aggregations and analyses.
4.  **Identifying and Removing Duplicates:**
    * Implemented logic to detect and eliminate duplicate `order_id` records, maintaining the uniqueness and integrity of transactional data.
5.  **Feature Engineering / Data Enrichment:**
    * Created a new derived column, `total_price`, in the `orders` table by multiplying `price` and `quantity`. This adds immediate analytical value by providing the total value of each order line item.

---

## 🎯 Skills & Technologies Demonstrated

This project showcases the following highly sought-after skills for data roles:

* **Data Cleaning & Preprocessing:** Expertise in identifying and rectifying data inconsistencies, critical for reliable analysis.
* **ETL (Extract, Transform, Load) Principles:** Practical application of data transformation techniques to prepare raw data for a data warehouse or analytical platform.
* **Data Quality Assurance:** Commitment to maintaining high data integrity and accuracy.
* **Problem-Solving & Logical Reasoning:** Ability to systematically approach and resolve data-related challenges.
* **Microsoft Excel Proficiency:** Utilized advanced Excel functions for efficient data manipulation, validation, and transformation (e.g., `TRIM`, `PROPER`, `SUBSTITUTE`, `VALUE`, `REMOVE DUPLICATES`, pivot tables/lookups for validation).
* **Attention to Detail:** Meticulous execution of cleaning steps, ensuring no data errors were overlooked.
* **(Future Scope - highlights proactive learning):** Foundation laid for automating similar processes using Python (Pandas) or structuring data within SQL databases.

---

## 📈 Next Steps & Potential Enhancements

* **Automation with Python:** Implement a Python script using `pandas` to automate the cleaning process, enhancing efficiency and scalability.
* **Database Integration:** Load the cleaned data into an SQL database (e.g., SQLite, PostgreSQL) and perform advanced queries.
* **Exploratory Data Analysis (EDA):** Conduct an in-depth EDA to uncover insights, visualize trends, and generate reports.
* **Dashboard Creation:** Build an interactive dashboard using tools like Power BI or Tableau to visualize key sales metrics.
