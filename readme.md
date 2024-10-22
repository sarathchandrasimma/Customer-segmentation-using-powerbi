# Dataset Cleaning Process - README

## Overview
This document provides a detailed step-by-step explanation of the data cleaning process applied to the customer dataset. The dataset contains columns such as `CustomerID`, `Email`, `updated_phone_number`, `City`, `State`, `Country`, `Gender`, `Age`, `Updated_Joined_date`, `updated_last_purchase_date`, `TotalSpent`, `LoyaltyPoints`, `PurchaseFrequency`, `CustomerSegment`, `PreferredPaymentMethod`, `MaritalStatus`, `Updated_Account_creation_date`, `AccountStatus`, `LastUpdated`, `Updated_Referrer_Id`, `FeedbackRating`, `Domain of mail`, and `country_code`.

The data cleaning was performed in **Power BI** using Power Query Editor.

## Cleaning Steps

### 1. **Import Data**
- Open Power BI Desktop.
- Import the CSV file containing the raw data by selecting `Get Data` > `Text/CSV`.

### 2. **Data Transformation**
Once the data is loaded into Power BI, open Power Query Editor by clicking on `Transform Data`.

### 3. **Remove Invalid Email Domains**
- Filter the `Email` column to find any invalid entries (e.g., `alyssa.rodriguez@None`).
- Remove or replace invalid emails as needed.

### 4. **Standardize Phone Numbers**
- Clean the `updated_phone_number` column to ensure a consistent format.
- Replace inconsistent characters (e.g., replace `x` with `-`).
- Ensure that phone numbers are in international formats (e.g., `+1-123-456-7890`).

### 5. **Handle Missing Values**
- Check for missing values across relevant columns, especially `Gender`, `Age`, `MaritalStatus`, etc.
- Use the `Fill Down` option to fill missing values or manually input missing values based on logical assumptions.
- Impute missing numerical values (e.g., `Age`) by using the median or mean value.

### 6. **Correct Data Types**
- Ensure each column has the correct data type:
  - `Email` and `City` as **Text**.
  - `Age` and `TotalSpent` as **Number**.
  - Date columns such as `Updated_Joined_date`, `updated_last_purchase_date`, and `Updated_Account_creation_date` as **Date**.
- Adjust data types using the `Data Type` option in Power Query.

### 7. **Extract Email Domains**
- In the `Email` column, split the data by `@` to extract the domain of the email.
- Use `Split Column` > `By Delimiter` (`@`) to create a new `Domain of mail` column (e.g., `gmail.com`, `yahoo.com`).

### 8. **Create Derived Columns**
- Add a new column for customer classification based on the combination of `TotalSpent` and `LoyaltyPoints`.
- Use the "Add Column" feature to create conditional logic (e.g., customers with high spending and loyalty points are classified as `Gold`, `Platinum`, etc.).

### 9. **Clean Date Formats**
- Standardize the date formats across all date columns (`Updated_Joined_date`, `updated_last_purchase_date`, etc.).
- Ensure consistent format, e.g., `dd-mm-yyyy`, and replace any inconsistent formats using the `Replace Values` feature.

### 10. **Standardize Country Codes**
- Verify the `country_code` column for uniformity.
- Add or adjust country codes to maintain consistency (e.g., adding `+` to international codes).
- Use the `Replace Values` feature to format the country codes appropriately.

### 11. **Save and Load Data**
- After completing the cleaning process, click on `Close & Apply` to apply all the transformations.
- The cleaned dataset will be loaded into Power BI for further analysis.

## Final Cleaned Data Structure
After cleaning, the dataset will contain the following key columns:
- `CustomerID`
- `Email`
- `updated_phone_number`
- `City`
- `State`
- `Country`
- `Gender`
- `Age`
- `Updated_Joined_date`
- `updated_last_purchase_date`
- `TotalSpent`
- `LoyaltyPoints`
- `PurchaseFrequency`
- `CustomerSegment`
- `PreferredPaymentMethod`
- `MaritalStatus`
- `Updated_Account_creation_date`
- `AccountStatus`
- `LastUpdated`
- `Updated_Referrer_Id`
- `FeedbackRating`
- `Domain of mail`
- `country_code`

## Conclusion
The dataset has been successfully cleaned and is now ready for analysis. All missing values have been handled, phone numbers standardized, email domains extracted, and data types corrected. This cleaned dataset will ensure accurate insights during analysis.
