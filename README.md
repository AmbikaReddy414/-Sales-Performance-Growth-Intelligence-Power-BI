# 📊 Sales Performance & Growth Intelligence — Power BI

This repository contains a complete Power BI sales dashboard built to analyze sales performance, growth trends, and profitability using a star schema data model and a dedicated Date dimension.

---

## 📑 Table of Contents

1. Report Pages Overview  
2. Page-wise Explanation  
   - Overview  
   - Product Analysis  
   - Region Analysis  
   - Customer Analysis  
   - Summary & Insights  
3. Steps Taken (Data Cleaning, Modeling & Measures)  
4. Date Dimension (DimDate) Explanation  
5. Measures Used (Conceptual Explanation)  
6. Final Summary  
7. Author  

---

## 1️⃣ Report Pages Overview

The Power BI report is structured into five pages. Each page serves a specific analytical purpose, starting from high-level KPIs and moving toward detailed analysis and final insights.

---

## 2️⃣ Page-wise Explanation

### 📌 Page 1: Overview

This page provides a high-level snapshot of overall business performance.

What is shown:
- KPI cards for Total Sales, Sales YTD, Sales YoY %, and Profit Margin %
- Sales trend over time
- Slicers for Year, Region, and Category

Why this page exists:
To quickly understand how the business is performing and whether it is growing profitably.

---

### 🛒 Page 2: Product Analysis

This page focuses on product and category performance.

What is shown:
- Total Sales by Category
- Profit by Category
- Top products table with sales and profitability metrics

Why this page exists:
To identify which products and categories drive revenue and which need optimization.

---

### 🌍 Page 3: Region Analysis

This page analyzes performance across regions.

What is shown:
- Sales by Region
- Profit by Region
- Sales trend by region over time

Why this page exists:
To compare regional performance and identify high- and low-performing regions.

---

### 👥 Page 4: Customer Analysis

This page focuses on customer-level insights.

What is shown:
- Top customers by Total Sales
- Customer profitability comparison
- Sales vs Profit scatter to identify risky or high-value customers

Why this page exists:
To understand customer contribution, profitability, and revenue concentration risk.

---

### 📌 Page 5: Summary & Insights

This is the final decision-focused page.

What is shown:
- Overall KPI summary
- Category-level performance table
- Relationship between growth and profitability
- Key insights and recommendations

Why this page exists:
To convert analysis into clear, actionable insights.

---

## 3️⃣ Steps Taken (Data Cleaning, Modeling & Measures)

### Data Cleaning
- Renamed columns for clarity
- Corrected data types (dates, numeric fields, text)
- Removed duplicates while creating dimension tables

### Data Modeling
- Created a FactSales table for transactional data
- Created dimension tables: DimDate, DimProduct, DimCustomer, DimRegion
- Implemented a star schema model
- All relationships are one-to-many (1:*) from dimensions to the fact table
- Single-direction filtering from dimensions to fact table

---

## 4️⃣ Date Dimension (DimDate) Explanation

A separate Date table was created to enable time-based analysis.

Why DimDate is needed:
- Enables accurate Year-to-Date (YTD) calculations
- Enables Last Year (LY) and Year-over-Year (YoY) comparisons
- Ensures consistent time filtering across all visuals

Columns included:
- Date: Continuous calendar date
- Year: Used for yearly grouping and YTD reset
- Month: Readable month names
- MonthNumber: Used to sort months correctly
- YearMonth: Used for monthly trend analysis across years

DimDate is marked as the official Date table in Power BI and connected to FactSales using a one-to-many relationship.

---

## 5️⃣ Measures Used (Conceptual Explanation)

Measures were created to support both aggregation and time-based analysis.

Measures include:
- Total Sales: Sum of sales amount
- Sales YTD: Sales from the beginning of the year to the selected date
- Sales LY: Sales for the same period in the previous year
- Sales YoY %: Growth percentage compared to last year
- Profit: Sales minus cost
- Profit Margin %: Profit as a percentage of sales

These measures allow dynamic analysis across time, products, regions, and customers.

---

## 6️⃣ Final Summary

This Power BI report demonstrates a complete analytical workflow:
- Clean data preparation
- Proper star schema modeling with correct relationships
- Use of a Date dimension for time intelligence
- Clear, structured report pages seen in real business dashboards
- Insights focused on performance, growth, and profitability

---

## 👤 Author

Ambika Reddy
