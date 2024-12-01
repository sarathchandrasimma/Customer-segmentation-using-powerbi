# Customer Insights Power BI Dashboard
## Overview
This Power BI dashboard provides actionable insights into customer behavior and business performance. The dashboard includes metrics such as New Customer Acquisition, Sales Growth, Customer Segments Distribution, and other KPIs like Customer Lifetime Value (CLV), Purchase Frequency, and RFM analysis to aid marketing and operational strategies.

## Features
Key Metrics and Visuals
Number of New Customers by Year

Identifies customers who made purchases for the first time in a specific year.
Excludes customers who made purchases in prior years.
Sales Growth Rate

Tracks year-over-year (YoY) sales growth.
Helps assess business performance trends.
Sales by Product Category

Breaks down sales contributions by product categories.
Enables targeted marketing strategies for high-performing categories.
Quantity Sold

Displays the total number of units sold across all categories.
Customer Lifetime Value (CLV)

Measures the total revenue generated from a customer during their relationship with the company.
Purchase Frequency (PF)

Tracks how often customers make purchases over a defined period.
RFM Analysis (Recency, Frequency, Monetary)

Recency: How recently a customer made a purchase.
Frequency: How often a customer makes purchases.
Monetary: How much a customer spends.
Includes customer ranking based on RFM scores.
Returned Orders Analysis

Visualizes the count and value of returned orders by product category and region.
Geographic Distribution of Customers

Map-based visualization showing customer distribution across regions.
Profitability Metrics

Tracks total profit by region, segment, and product categories.
## Data Sources
### Orders
Contains details of transactions, including sales, profit, and customer information.

Columns: Order ID, Customer ID, Order Date, Product Category, Sales, Profit, etc.
### Returns
Contains information about returned orders.

Columns: Returned, Order ID.
### DimDate
A date dimension table created to enable time-based analysis.

## Key DAX Measures
New Customers by Year

Identifies first-time customers in each year using DAX filters.
YoY Sales Growth

Measures sales performance year-over-year using the SAMEPERIODLASTYEAR function.
CLV Calculation

Sum of total sales per customer over their entire transaction history.
RFM Scoring

Combines recency, frequency, and monetary value to rank customers.
Returned Orders Count

Counts the total number of returned orders.
## How to Use
Open the Power BI file.
Interact with slicers to filter by year, region, or product category.
Hover over visualizations for detailed insights into each metric.
Use the map visualization to analyze customer distribution geographically.
Installation
Import the dataset files (Orders.csv, Returns.csv) into Power BI.
Create a DimDate table by generating a list of dates spanning the transaction period.
Load the prepared dataset into Power BI and refresh the data model.
Future Improvements
Add Churn Rate Analysis to track customer retention trends.
Include additional KPIs like Customer Acquisition Cost (CAC).
Implement real-time data updates.
## Contact
For further queries or support, contact:
Email: [your.sarathchandrasimma04@gmail.com]
GitHub: [(https://github.com/sarathchandrasimma)]


## milesotne-1
## Dataset Cleaning Process - README

### Overview

This document provides a detailed step-by-step explanation of the data cleaning process applied to the customer, products, regions, and transactions datasets. Each dataset underwent cleaning in Power BI using the Power Query Editor to ensure uniformity, consistency, and accuracy.

## Datasets:

## Customer Dataset

## Products Dataset

## Regions Dataset

## Transactions Dataset

## 1. Customer Dataset Cleaning Process

Columns:
CustomerID, Email, updated_phone_number, City, State, Country, Gender, Age, Updated_Joined_date, updated_last_purchase_date, TotalSpent, LoyaltyPoints, PurchaseFrequency, CustomerSegment, PreferredPaymentMethod, MaritalStatus, Updated_Account_creation_date, AccountStatus, LastUpdated, Updated_Referrer_Id, FeedbackRating, Domain of mail, country_code.

### Cleaning Steps

Import Data: Imported the dataset into Power BI via Get Data > Text/CSV.
Remove Invalid Email Domains: Cleaned the Email column to remove invalid domains.
Standardize Phone Numbers: Ensured consistent formatting of phone numbers (e.g., +1-123-456-7890).
Handle Missing Values: Filled or imputed missing values logically.
Correct Data Types: Ensured proper data types for each column (e.g., Date, Number, Text).
Extract Email Domains: Created a new Domain of mail column.
Create Derived Columns: Added customer classifications based on TotalSpent and LoyaltyPoints.
Standardize Date Formats: Applied consistent date formatting across columns.
Standardize Country Codes: Ensured uniform country code formatting (e.g., adding +).

## 2. Products Dataset Cleaning Process

Columns:
ProductID, ProductName, Category, Price, StockStatus, Supplier, Updated_Price, Updated_StockStatus, LastUpdated, Discontinued.

### Cleaning Steps

Remove Duplicates: Checked and removed duplicate entries based on ProductID.
Handle Missing Values: Imputed missing values in the Price and StockStatus columns.
Standardize Price Formats: Ensured consistent currency formatting (e.g., $100.00).
Correct Data Types: Standardized column types, ensuring Price is a number and ProductName is text.
Update Discontinued Products: Marked products as Discontinued where applicable.

## 3. Regions Dataset Cleaning Process

Columns:
RegionID, RegionName, Country, State, Updated_RegionName, LastUpdated, CountryCode.

### Cleaning Steps

Remove Invalid Regions: Filtered out incomplete or invalid RegionName entries.
Standardize Country Codes: Ensured uniformity in CountryCode (e.g., +1 for US).
Handle Missing Values: Addressed missing region or country data using fill down logic.
Correct Data Types: Ensured text formatting for RegionName and number formatting for CountryCode.

## 4. Transactions Dataset Cleaning Process

Columns:
TransactionID, CustomerID, ProductID, TransactionDate, Quantity, TotalAmount, PaymentMethod, DiscountApplied, LastUpdated.

### Cleaning Steps

Remove Duplicates: Ensured that TransactionID is unique and removed any duplicates.
Handle Missing Data: Imputed or removed missing entries for Quantity and TotalAmount.
Correct Data Types: Applied appropriate data types, ensuring TransactionDate is in a date format and TotalAmount is a number.
Standardize Payment Methods: Ensured uniformity in the PaymentMethod column (e.g., Credit Card, Paypal).
Update Discounts: Checked for consistent values in the DiscountApplied column.

### Conclusion

The datasets have been successfully cleaned and standardized. Each dataset now contains consistent, error-free, and well-structured data that can be used for analysis and reporting in Power BI.

