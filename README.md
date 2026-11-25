# Zepto Grocery Data Analysis Using SQL

## Project Overview

This project focuses on analyzing Zepto grocery inventory and product data using **PostgreSQL**. The objective is to explore product information, clean raw data, and perform SQL-based exploratory data analysis (EDA) to uncover meaningful business insights.

The analysis focuses on product pricing, discount percentages, inventory availability, product categories, and estimated inventory value to support data-driven business decisions.

## Project Objectives

- Explore and understand the grocery product dataset.
- Identify missing values and inconsistent records.
- Clean product pricing data and standardize values.
- Analyze product discounts and pricing patterns.
- Compare in-stock and out-of-stock products.
- Calculate category-wise estimated inventory value.
- Identify high-value products and inventory weight distribution.
- Generate business insights using SQL queries.

## Dataset Description

The dataset contains grocery product information, including:

| Column | Description |
|---|---|
| sku_id | Unique product SKU identifier |
| category | Product category |
| name | Product name |
| mrp | Maximum Retail Price |
| discountPercent | Discount percentage |
| availableQuantity | Available inventory quantity |
| discountedSellingPrice | Discounted selling price |
| weightInGms | Product weight in grams |
| outOfStock | Product availability status |
| quantity | Product quantity |

**Dataset format:** CSV

## Tools & Technologies

- PostgreSQL – Database management and SQL queries
- SQL – Data cleaning, data exploration, and EDA
- GitHub – Project documentation and version control
- CSV – Dataset storage

## Project Workflow

### 1. Database Creation and Data Import

- Created the Zepto database table using PostgreSQL.
- Defined appropriate data types for product attributes.
- Imported the CSV dataset into the database.

### 2. Data Exploration

Performed initial data exploration to understand the dataset:

- Counted total records.
- Retrieved sample records.
- Identified missing or NULL values.
- Explored unique product categories.
- Compared in-stock and out-of-stock products.
- Identified product names appearing under multiple SKUs.

### 3. Data Cleaning

Performed data cleaning operations to improve data quality:

- Identified products with zero MRP or selling price.
- Removed records with zero MRP.
- Converted price values from paise to Indian rupees.
- Checked missing values across important columns.

### 4. Exploratory Data Analysis (EDA)

Performed SQL analysis to answer the following business questions:

| No. | Business Question |
|---|---|
| 1 | What are the top 10 best-value products based on discount percentage? |
| 2 | Which products have a high MRP but are currently out of stock? |
| 3 | What is the estimated inventory value for each product category? |
| 4 | Which products have an MRP greater than ₹500 and a discount below 10%? |
| 5 | Which five categories offer the highest average discount percentage? |
| 6 | What is the price per gram of products weighing at least 100 grams? |
| 7 | How can products be classified into Low, Medium, and Bulk weight categories? |
| 8 | What is the total inventory weight for each product category? |

## Key SQL Concepts Used

- SELECT, DISTINCT, WHERE
- ORDER BY, GROUP BY, HAVING
- Aggregate Functions: COUNT(), SUM(), AVG()
- Filtering and Sorting
- NULL Value Handling
- DELETE and UPDATE
- CASE WHEN Statements
- ROUND() Function
- Primary Keys and SERIAL
- Data Type Selection
- Exploratory Data Analysis (EDA)

## Repository Structure

```text
zepto-sql-data-analysis/
│
├── README.md
│
├── data/
│   └── zepto_v2.csv
│
└── sql/
    └── zepto_analysis.sql
```

## How to Run This Project

1. Download or clone this repository.
2. Install PostgreSQL and open pgAdmin or your preferred SQL editor.
3. Create a database for the project.
4. Execute the table creation query from the SQL script.
5. Import the CSV dataset into the `zepto` table, matching the column order and data types.
6. Execute the data exploration queries.
7. Run the data cleaning operations.
8. Execute the EDA queries to generate business insights.

**Note:** Ensure that the CSV data is imported after table creation and before running the exploration queries. Check the CSV column mapping, especially the auto-generated `sku_id` column.

## Business Applications

The analysis can help grocery businesses:

- Understand product discount strategies.
- Monitor stock availability.
- Identify products with high prices and low discounts.
- Compare inventory value across categories.
- Evaluate product pricing relative to weight.
- Understand category-wise inventory distribution.

## Project Limitations

- The analysis is based on the available dataset and its recorded product information.
- Estimated inventory value is calculated using discounted selling price multiplied by available quantity; it does not represent actual realized sales revenue.
- The analysis does not include customer transactions, orders, or profit and loss information.

## Author

**Manoja Kumar Sahu**

MCA Graduate | Aspiring Data Analyst

- GitHub: [github.com/manojakumarsahu618](https://github.com/manojakumarsahu618)
- LinkedIn: [linkedin.com/in/manoja-kumar-sahu-7477642aa](https://linkedin.com/in/manoja-kumar-sahu-7477642aa)

---

*This project was developed to demonstrate practical SQL skills in data exploration, data cleaning, and business-oriented exploratory data analysis.*
