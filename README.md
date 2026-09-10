E-commerce Customer & Sales Performance Analysis – Excel Project

An end-to-end Excel analysis of a 3,500-order e-commerce dataset — from raw transactional data to enriched records, formula-driven summaries, and a pivot-powered dashboard.

Overview

The workbook starts with three raw tables (Orders, Customers, Products), joins them into a single enriched dataset using lookup formulas, then layers on business logic (value tiers, delivery flags, pending-order flags) before rolling everything up into category, customer, and time-based summaries.

## Dashboard Preview
![Dashboard](images/dashboard.png)

Sheets
Sheet	Purpose
Orders	Raw transaction data — 3,500 orders (Order_ID, Customer_ID, Product_ID, quantity, dates, status, payment mode, order value)
Customer	3,000 customers — name, email, city, state, signup date
Product	3,000 products — category, name, price
Orders_Enriched	Master table joining all three sources, with derived columns: Value_Tier (High Value / Standard), Working_day (delivery turnaround), Order_Month, and flags for priority/review/pending orders
Summary_Analysis	Formula-driven rollups — revenue by category, order counts, average order value
Customer_Analysis	Per-customer totals — order count, total spend, average order value
Lookup_Demo	Side-by-side comparison of VLOOKUP vs INDEX+MATCH for the same lookup, to show both approaches
Dashboard	Chart-based visual summary built on the pivot tables below

Supporting pivot tables (monthly revenue trend, category × status breakdown, payment-mode split, city-wise revenue, value-tier distribution) feed the Dashboard's charts.

Key Techniques Used
Lookup formulas — VLOOKUP and INDEX+MATCH to join Orders with Customer and Product tables
Conditional logic — IF/nested IF for value-tier classification and order flags
Aggregation formulas — SUMIFS, COUNTIFS, AVERAGEIFS for category and customer summaries
Date functions — delivery turnaround (working days), month extraction for trend analysis
PivotTables & PivotCharts — revenue by month, category vs. status, payment mode, city, value tier
Data validation across joined tables to keep the enriched sheet consistent with source data
Key Insight

Order value tiers show a clear split — High Value orders make up a small share of order count but a disproportionately large share of revenue, which is the kind of pattern the Value_Tier flag and Customer_Analysis sheet are built to surface.


Tech Stack
Microsoft Excel — formulas, PivotTables, PivotCharts
