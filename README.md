# Decode-Labs-Data-Cleaning

## Project Overview

This project was completed as part of my data analytics internship training at **Decode Labs**.

The focus of this project was to prepare an e-commerce dataset for analysis by checking data quality, identifying potential issues, validating important fields, and making appropriate cleaning decisions.

## Dataset

The dataset contains:

- **1,200 order records**
- **14 columns**
- Order data

The dataset contains information about:

- Orders
- Customers
- Products
- Quantity and pricing
- Shipping
- Payment methods
- Order status
- Tracking information
- Cart information
- Coupon usage
- Referral sources

## Data Cleaning and Validation

The following checks were performed:

### 1. Duplicate Order IDs

The `OrderID` column was checked for duplicate values because it should uniquely identify an order.

**Result:** No duplicate OrderIDs were identified.

### 2. Missing Coupon Codes

Some `CouponCode` entries were blank.

Instead of deleting those records, the blank values were standardized as:

`No Coupon`

This allowed the records to remain in the dataset while making the field easier to analyze.

### 3. Date Validation

The `Date` column was checked and formatted consistently as a date.

### 4. Quantity and Pricing Checks

The `Quantity`, `UnitPrice`, and `TotalPrice` fields were reviewed for missing or invalid values.

### 5. Total Price Validation

The `TotalPrice` field was validated using:

**Quantity × UnitPrice = TotalPrice**

No calculation errors were identified.

### 6. Categorical Consistency

Product, payment method, order status, coupon code, and referral source values were reviewed for consistency.

### 7. Identifier Fields

`OrderID`, `CustomerID`, and `TrackingNumber` were preserved as identifiers rather than being treated as values for mathematical calculations.

## Tools Used

- Microsoft Excel
- Data Cleaning
- Data Validation
- Data Analysis

## Key Learning

This project reinforced an important part of the data analytics process:

Good analysis starts with good data.

Data cleaning is not simply about deleting duplicates or filling blank cells. It requires understanding what each field represents and making decisions that preserve useful information.

## Internship Context

This project is part of my practical learning journey during my **Decode Labs internship training**, where I am developing my skills in Excel, data cleaning, data analysis, and preparing datasets for further analytical work.

## Project Structure

```text
decode-labs-ecommerce-data-cleaning/
│
├── README.md
│
├── data/
│   ├── raw/
│   │   └── Dataset for Data Analytics.xlsx
│   │
│   └── cleaned/
│       └── Dataset for Data Analytics_Cleaned.xlsx
│
└── documentation/
    └── data-cleaning-notes.md
