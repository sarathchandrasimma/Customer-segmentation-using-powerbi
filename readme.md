# Dataset Cleaning Process - README

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
