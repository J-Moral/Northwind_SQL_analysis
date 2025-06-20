# Northwind SQL Analysis

## Overview

This project presents an ad-hoc analysis of the Northwind database, a well-known sample dataset that simulates a fictional company specializing in international food and beverage distribution. The analysis was conducted using SQL for querying and Python (pandas and matplotlib) for visualizations and interpretation.

The goal of this repository is to present findings in a format that is accessible to both technical and non-technical audiences. Business professionals, students, and general readers can explore key performance insights about suppliers, products, orders, and customer patterns through clearly presented visuals and summaries.

## About the Market.db File

The Market.db file is a SQLite version of the Northwind database. It contains several relational tables including:

- Products: Details on items sold, including name, price, supplier, and category

- Suppliers: Information about the companies that provide the products

- Orders: Records of each customer transaction

- OrderDetails: Line-item level detail for every order placed

- Customers: Companies or individuals who place orders

These tables are interlinked, enabling us to perform detailed and layered queries that uncover meaningful patterns in the data.

## Understanding the Northwind ER Diagram

The Entity-Relationship Diagram (ERD) visually shows how each table in the database relates to others:

- Each box in the diagram is a table (e.g., Products, Orders)

- Each line shows a relationship between two tables

- Numbers or symbols indicate the nature of the relationship (e.g., one-to-many)

Examples:

- A single supplier can supply many products, but each product is supplied by just one supplier.

- A single order can include many products, and each product in an order is listed individually in OrderDetails.

Reading the ERD allows us to write accurate SQL queries and understand how to join different tables to extract insights.

# Analytical Questions:
1. Which countries have the greatest number of customers? How does this correlate with the number of suppliers by country (i.e. do more customers lead to less or more suppliers)? Which evidence supports your answer?
2. What is the least popular product by order quantity? How does this correlate with revenue (i.e. do less popular products by quantity lead to less or more revenue)? Which evidence supports your answer?
3. Which country has the most orders? How does this correlate with the number of customers who do not order (i.e. do countries with more ordering customers have more or less non-ordering customers)? Which evidence supports your answer?
4. Which supplier has the most orders? Which evidence supports your answer?

## Major Findings

The project answers several business questions using structured SQL queries and visual analysis. Key insights include:

- Top Revenue Supplier: "Aux joyeux ecclésiastiques" generated the highest revenue. "Plutzer Lebensmittelgroßmärkte AG" ranked second, with over 50% of the top supplier’s revenue.

- Product Prices and Quantity Sold: Plutzer offers competitively priced products with strong volume, especially in categories like condiments and beverages. Their pricing strategy helps balance affordability and sales volume.

- Product Count: Plutzer is among the suppliers with the most products offered (five), which supports their broader reach across different customer needs.

- High-Volume Products: Products like "Chartreuse verte" and "Steeleye Stout" recorded the highest order quantities, indicating popular consumer preferences.

- Least Popular Product: Items such as "Laughing Lumberjack Lager" had the lowest order quantities. These products also generated lower revenue, showing that low sales often align with lower financial contribution.

- Revenue vs. Quantity Correlation: Products with higher order volumes generally produced more revenue. However, product price remains a contributing factor.

- roduct Rankings by Quantity: Plutzer’s best-selling products fell within the top 25 to 51 range when ranked across all suppliers, showing strong but not top-tier individual product performance.

- Repeat Order Behavior: Many products had a 100% or higher repeat order rate. For Plutzer, items like "Original Frankfurter grüne Soße" had repeat rates over 100%, reflecting high customer satisfaction.

- Category Distribution: Plutzer’s products span five distinct categories—condiments, beverages, produce, grains/cereals, and meat/poultry—demonstrating diverse offerings.

- Customer Reach: Plutzer serves the highest number of unique customers (32), indicating strong market reach.

- Customer and Supplier Locations: The U.S. and Germany have the largest customer bases. However, countries with more customers don’t necessarily have more suppliers, suggesting a mix of importing and exporting behaviors.

## How to Use This Repository

1. Clone the repository:git clone https://github.com/J-Moral/Northwind_SQL_analysis.git

2. Navigate to the project directory and open adhoc_report.ipynb using Jupyter Notebook.

3. Follow the notebook to explore SQL queries and their resulting insights.

4. Each question is addressed with:

- A clear SQL query

- A pandas DataFrame

- A visual chart (where applicable)

- A written interpretation of the result

No prior programming experience is required to follow the structure of the notebook or the explanations of the results.

## License

This project is intended solely for academic and educational purposes. The Northwind database is a publicly available sample dataset used for learning SQL and database design. The author of this project does not claim ownership of the dataset or its contents.

