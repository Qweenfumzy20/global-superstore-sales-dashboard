# Global Superstore Sales Dashboard

## Project Overview
Global Superstore Sales Dashboard – This project uses Microsoft Power BI to carry out analysis of Global Superstore dataset and to determine sales trends and areas of profit for individual products and customers

## Project Objective
The project objective was to retail sales data from 2011 - 2014 and answer some of the questions that might arise, such as;
- Which markets generate the highest sales and profit?
- Which products and sub-categories perform best?
- Which countries contribute the most revenue?
- How have sales changed over time?
- What relationship exists between discounts and profit?

- ## Dataset
- The dataset contains more than 51,000 retail transaction records.

Important fields include:
- Order date
- Customer name
- Product name
- Category and sub-category
- Market and country
- Sales
- Profit
- Discount
- Quantity
- Shipping cost

## Tools Used
- Microsoft Excel
- Power Query
- Microsoft Power BI
- DAX

- ## Data Preparation
The dataset was imported and inspected using Power Query.

The preparation process included:
- Checking column data types
- Validating date fields
- Checking for missing values and errors
- Confirming numeric fields such as sales, profit, discount, and shipping cost
- Loading the cleaned data into Power BI
Duplicate order IDs were not removed because one order can contain multiple products.

## DAX Measures
The following measures were created:
```DAX
- Total Sales = SUM(SuperStore_Orders[sales])
- Total Profit = SUM(SuperStore_Orders[profit])
- Total Orders = DISTINCTCOUNT(SuperStore_Orders[order_id])
- Total Customers = DISTINCTCOUNT(SuperStore_Orders[customer_name])
- Profit Margin = DIVIDE([Total Profit], [Total Sales], 0)

# Dashboard Preview

## Page 1 — Executive Overview
This dashboard provides an executive summary of the company's overall performance, including total sales, profit, orders, customers, sales trends, and market performance.

![Executive Overview](Executive Overview)

---

## Page 2 — Product Performance Analysis
This dashboard focuses on product performance, highlighting the best-selling products, the most profitable products, sub-category performance, and the relationship between discounts and profitability.

![Product Performance Analysis](product-performance.png)

---

## Page 3 — Customer & Regional Performance Analysis
This dashboard explores customer and regional performance, identifying the highest-performing countries and markets while allowing users to filter results interactively.

![Customer & Regional Performance Analysis](customer-regional-performance.png)

