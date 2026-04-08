# Cafe Sales Data Cleaning and Visualization Project

## Project Overview
This project takes a raw cafe sales dataset of 10,000 transaction records
and cleans it fully using Python in Jupyter Notebook. The cleaned data is
then used to build 5 business visuals in Excel.

---

## Files in This Repository

| File | Description |
|------|-------------|
| Cafe_Sales_Final_Cleaned.xlsx | Fully cleaned dataset ready for analysis |
| Cafe_Sales_Report_Final.xlsx | Excel workbook with all 5 charts and pivot tables |

---

## Dataset Overview

The original dataset contained 10,000 rows and 8 columns:

- Transaction ID
- Item
- Quantity
- Price Per Unit
- Total Spent
- Payment Method
- Location
- Transaction Date

---

## Problems Found in the Raw Data

- "UNKNOWN" and "ERROR" values used as fake placeholders in Item,
  Payment Method and Location columns
- Numeric columns stored as text preventing any calculations
- Inconsistent date formats across the Transaction Date column
- Leading and trailing whitespace in text columns causing duplicate categories
- Missing values across all columns totalling thousands of blank cells
- Transaction ID stored as a single string combining prefix and number

---

## Cleaning Steps Performed

1. Loaded and inspected the dataset
2. Audited all missing values and dirty entries
3. Stripped whitespace from all text columns
4. Standardised casing across all text columns
5. Split Transaction ID into TXN_Prefix and TXN_Number columns
6. Replaced UNKNOWN and ERROR values with NaN
7. Replaced all remaining blanks with readable placeholders
8. Converted Quantity, Price Per Unit and Total Spent to numeric format
9. Parsed and standardised Transaction Date to YYYY-MM-DD format
10. Recalculated Total Spent from Quantity times Price Per Unit
11. Filled missing Quantity and Price Per Unit using per-item medians
12. Recalculated Total Spent a second time after median fill
13. Ran final null audit across all columns
14. Verified numeric ranges and category distributions
15. Confirmed all 10 columns present including TXN split columns
16. Exported final cleaned file

---

## Tools Used

- Python 3
- Pandas
- NumPy
- OpenPyXL
- Jupyter Notebook
- Microsoft Excel Online

---

## Visuals Built in Excel

| Visual | Chart Type | Description |
|--------|------------|-------------|
| Sales Revenue by Item | Horizontal Bar | Total revenue per menu item |
| Transaction Volume by Month | Line Chart | Number of transactions per month |
| Payment Method Breakdown | Pie Chart | Split between Cash, Card and Digital Wallet |
| Sales by Location | Column Chart | Revenue from In-Store vs Takeaway |
| Top Items by Quantity Sold | Horizontal Bar | Units sold per menu item ranked highest to lowest |

---

## Key Findings

- The dataset was cleaned from thousands of missing and dirty values
  to a fully complete 10,000 row dataset
- Transaction ID was split into prefix and numeric components
  for easier filtering and sorting
- Total Spent was recalculated from source columns wherever possible
  to avoid estimation
- All 5 visuals are available in the Excel report file ready to view

---

## How to Use This Project

1. Download Cafe_Sales_Final_Cleaned.csv to see the cleaned dataset
2. Download Cafe_Sales_Report_Final.xlsx to view all 5 charts in Excel
3. Open the Jupyter Notebook to follow the full cleaning code step by step

---

## Author
Created as a data cleaning and visualization portfolio project
