# Retail_Sales_Analysis

📌 Overview

This repository contains a SQL script (Retail_Sales_Analysis.sql) to analyze monthly sales performance from a retail_sales dataset.
The script calculates the average sales per month and identifies the best-selling month for each year.

⚙️ Query Logic

The query performs the following steps:

Extracts Year & Month from sale_date.

Calculates average sales (AVG(total_sale)) for each month.

Uses a window function (RANK()) to rank months within each year based on average sales.

Filters the results to return only the best month (rank = 1) for each year.

🛠️ Requirements

MySQL 8.0+ (for window functions like RANK()).

A table named retail_sales with at least the following columns:

sale_date (DATE/DATETIME) – the date of the sale

total_sale (NUMERIC) – the sale amount

📂 File Description

Retail_Sales_Analysis.sql → Contains the MySQL query to calculate and fetch the best-selling month of each year.

▶️ Usage

Clone the repository:

git clone https://github.com/your-username/Retail-Sales-Analysis.git
cd Retail-Sales-Analysis


Import your retail sales data into MySQL (make sure the table is named retail_sales).

Run the query:

SOURCE Retail_Sales_Analysis.sql;

📊 Example Output
year	month	avg_sale
2022	11	1540.23
2023	07	1892.67
2024	03	2105.50
🔄 MySQL 5.7 Alternative

Since MySQL 5.7 does not support window functions, you can rewrite the query using a subquery + join instead of RANK(). (See documentation in code comments.)
