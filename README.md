# E-Commerce-Sales-Data-Cleaning-Transformation
A complete Power Query data cleaning and transformation project on a messy e-commerce sales dataset

**Project Overview**

This project documents the complete data cleaning and transformation of a three-file e-commerce sales dataset using Microsoft Power Query (Excel). It was completed as part of the GIFT 1 Case Study for the Excel Study Group.

**Files**

<img width="436" height="234" alt="image" src="https://github.com/user-attachments/assets/116969e9-1f60-4a42-b8db-6918dbf9b871" />


<img width="442" height="214" alt="image" src="https://github.com/user-attachments/assets/7fd3f7a5-ba7f-42fa-b852-810af20b9c22" />


<img width="436" height="213" alt="image" src="https://github.com/user-attachments/assets/fc343980-5968-4be7-be81-0566f6ec2f6e" />




•	Messy_List_of_Orders.csv — ~508 rows of order headers

•	Messy_Order_Details.csv — ~1,506 rows of line-item detail

•	Messy_Sales_Target.csv — 44 rows of monthly targets by category



**Key Transformations Applied**


**List of Orders**

•	Removed Notes and Sales_Rep columns

•	Trimmed leading/trailing whitespace from Order ID and Customer Name

•	Fixed leading zeros in Order ID

•	Standardised four date formats (DD-MM-YYYY, MM/DD/YYYY, YYYY-MM-DD, text) into one

•	Standardised state names using a mapping table (e.g., "Maharastra", "MAHARASHTRA", "MP" → "Maharashtra")

•	Applied Proper Case to city names

•	Removed exact and near-duplicates

•	Handled null Customer Name and State values


**Order Details**

•	Removed currency symbols and converted Amount to decimal

•	Converted parenthetical negatives in Profit column to signed numbers

•	Removed percentage signs from Profit values

•	Fixed negative Quantity entries

•	Removed rows with missing Order ID

•	Standardised Category and Sub-Category names (e.g., "Hankerchief" → "Handkerchief")

•	Removed Discount column and blank rows


**Sales Target**

•	Normalised month formats (Apr-18, April 2018, 4/2018) to a single date standard

•	Cleaned Target column of ₹, Rs., commas, and text placeholders

•	Removed duplicate rows, blank rows, and the Region column

•	Corrected one row with swapped Category and Month values


**Advanced Techniques**

•	Custom M function for reusable currency cleaning

•	Conditional column for Profit Status (Profit / Loss / Break-even)

•	Calculated column for Revenue per Unit

•	Year and Month extraction from Order Date

•	Merge of Orders + Order Details with aggregation by Order ID

•	Merge of Sales Targets with Actual Sales for variance analysis

•	Fuzzy matching for state name standardisation

•	Query dependency documentation and organisation


**Cleaned Data file**

 <img width="530" height="304" alt="image" src="https://github.com/user-attachments/assets/7ef55c4e-2687-4081-842e-63fc4245f37a" />
 
<img width="505" height="257" alt="image" src="https://github.com/user-attachments/assets/d6531270-9eae-4929-8869-e49375f3558d" />

<img width="490" height="271" alt="image" src="https://github.com/user-attachments/assets/f9172cdd-5919-4fec-aeaa-99cad89a7155" />


**Validation Results**

All quality checks passed: row counts, data types, null checks, duplicate checks, referential integrity, and business logic validation.

**Tools Used:**

Microsoft Excel · Power Query · M Language


