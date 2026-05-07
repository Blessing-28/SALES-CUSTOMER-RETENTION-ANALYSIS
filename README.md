# SALES-CUSTOMER-RETENTION-ANALYSIS
This analysis evaluates sales performance, customer loyalty, and operational efficiency across 7  interconnected data tables


## Project Overview

This project focuses on performing a comprehensive analysis of the AdventureWorks retail dataset to uncover key drivers of customer loyalty and operational efficiency. By leveraging SQLite, I developed a series of unified reporting views that track the full customer lifecycle—from initial purchase to repeat behavior and eventual returns.


## Key Business Insights
- **High Customer Retention:** Identified a strong brand loyalty with a 86.6% repeat user rate, representing 15,089 returning customers out of a 17,416 total base.
  
- **Category Performance:** Segmented sales data to find that Accessories lead in volume (33,607 orders) and frequency, while Bikes and Clothing show distinct repeat purchase patterns.
  
- **Operational Integrity:** Audited and corrected "many-to-many" join errors in initial reporting that inaccurately inflated return rates, ensuring leadership received validated Portfolio Health metrics.


## Technical Workflow

### 1. Data Cleaning

- Identified and removed null records in customer demographics to ensure demographic accuracy.

- Standardized product categories and subcategories to resolve internal inventory discrepancies, specifically investigating the "Components" category which showed zero retail sales.


### 2. Advanced SQL Implementation

- CTE (Common Table Expressions): Used to modularize complex logic for sales, returns, and repeats into readable, unified tables. 

- Window Functions: Applied SUM() OVER() to calculate precise contribution percentages for user types.

- Conditional Logic: Implemented CASE statements to tier products by price and categorize customer loyalty.


## Repository Structure

- Adventureworks.sqbpro: Full SQLite project file containing all cleaning and analysis scripts.

- /queries: Individual SQL files for retention, regional strategy, and price-tier analysis.

- /visuals: Exported charts representing retention rates and category performance.


## Tools Used

- Database: SQLite / DB Browser for SQLite.

- Languages: SQL.  
