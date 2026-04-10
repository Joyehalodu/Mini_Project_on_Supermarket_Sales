# Mini_Project_on_Supermarket_Sales
## Project Overview
This project focuses on analyzing supermarket sales data using SQL to extract meaningful insights that can support business decision-making. The analysis covers customer behavior, product performance, and revenue trends.
## Objectives
The main goals of this project are to:
* Analyze overall sales performance
* Identify top-selling products and categories
* Understand customer purchasing behavior
* Evaluate branch performance
* Examine payment method trends
## Dataset Description
The dataset contains transactional records from a supermarket and includes the following key fields:
* Transaction ID
* CustomerID
* CustomerName 
* ProductCategory
* ProductName
* Unit Price
* Quantity
* Date
* Payment Method
* City
## Key Analysis & Queries
* Total Quantity of items sold

SELECT SUM(Quantity) AS Total_quantity_of_items_sold

FROM dbo.Supermarket

* Total Number of Transactions

SELECT COUNT(TransactionID) as Total_number_of_transactions

FROM dbo.Supermarket

* Average UnitPrice of the products

SELECT Round(AVG(UnitPrice), 2) AS Average_UnitPrice_Of_the_products

FROM dbo.Supermarket

* Total Revenue by each PaymentMethod

SELECT PaymentMethod ,ROUND(SUM(Quantity*UnitPrice),1) AS Total_Revenue

FROM dbo.Supermarket

GROUP BY PaymentMethod

* Total Quantity of top three(3) most sold products

SELECT TOP 3 ProductName, SUM(Quantity) AS Total_Quantity

FROM dbo.Supermarket

GROUP BY ProductName

ORDER BY SUM(Quantity) DESC 

## Key Insights
* The highest revenue was generated from Rice 5kg
* Most Customers preferred using Cash as their PaymentMethod
* Snacks had the highest sales volume

## Recommendations
* Increase stock for high-performing Product Category
* Optimize payment options to match customer preferences
* Focus marketing efforts on top-performing branches
* Introduce promotions during low-sales periods









