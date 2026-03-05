# SalesAnalysisProject
This project is a sales analytics dashboard created to visualize key business insights from a sales dataset. Using data aggregation and analysis, the dashboard highlights top-performing products, sales performance by region, category distribution, and customer segments. The visualizations help identify trends, high-revenue products, and regional performance to support data-driven decision making. This project demonstrates skills in data analysis, SQL aggregation, and data visualization.
Used DB Drowser for SQLite
########################################
Sales by Category
SELECT
    category,
    SUM(sales) AS total_sales
FROM sales
GROUP BY category
ORDER BY total_sales DESC;
########################################
Sales by Region
SELECT
    region,
    SUM(sales) AS total_sales
FROM sales
GROUP BY region
ORDER BY total_sales DESC;
########################################
Sales by Segment
SELECT
    segment,
    SUM(sales) AS total_sales
FROM sales
GROUP BY segment
ORDER BY total_sales DESC;
########################################
Top Products by Sales
SELECT
    product_name,
    SUM(sales) AS total_sales
FROM sales
GROUP BY product_name
ORDER BY total_sales DESC
LIMIT 10;
########################################
