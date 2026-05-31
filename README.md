# Global Layoffs Data Cleaning Project

## Project Overview

This project focuses on cleaning and preparing a real-world layoffs dataset using SQL. The goal was to improve data quality by removing duplicates, standardizing values, handling missing data, converting data types, and preparing the dataset for analysis.

## Dataset

Global Layoffs Dataset

Fields included:
- Company
- Location
- Industry
- Total Laid Off
- Percentage Laid Off
- Date
- Stage
- Country
- Funds Raised (Millions)

## Tools Used

- MySQL
- SQL
- Window Functions
- Data Cleaning Techniques

## Skills Demonstrated

### Data Cleaning
- Removed duplicate records
- Standardized text values
- Handled missing and blank values
- Converted date formats
- Deleted unusable records

### SQL Techniques
- ROW_NUMBER()
- Common Table Expressions (CTEs)
- UPDATE statements
- DELETE statements
- JOIN operations
- ALTER TABLE
- Data type conversion

## Cleaning Process

### 1. Created a Staging Table
Created a copy of the raw dataset to preserve original data.

### 2. Removed Duplicates
Used ROW_NUMBER() to identify duplicate records and removed them from the dataset.

### 3. Standardized Data
- Trimmed company names
- Standardized industry labels
- Corrected country formatting

### 4. Converted Data Types
Converted date fields from text format to SQL DATE format.

### 5. Handled Missing Values
- Replaced blank values with NULL
- Populated missing industry values using matching company records

### 6. Removed Invalid Records
Deleted rows where both:
- Total Laid Off = NULL
- Percentage Laid Off = NULL

### 7. Final Cleanup
Removed temporary columns used during the cleaning process.

## Key SQL Concepts Used

```sql
ROW_NUMBER() OVER (
PARTITION BY company, location, industry
)
```

```sql
STR_TO_DATE(date, '%m/%d/%Y')
```

```sql
UPDATE table
SET column = value
```

```sql
DELETE
FROM table
WHERE condition
```

## Results

- Removed duplicate records
- Standardized inconsistent text values
- Corrected date formatting
- Filled missing industry information
- Removed unusable records
- Produced an analysis-ready dataset

## Files

- Data Cleaning.sql
- layoffs.csv
- README.md

## Author

Tejasvee Williams

Aspiring Data Analyst | Healthcare Data Analyst
