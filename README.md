# SalesAnalysisProject

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
