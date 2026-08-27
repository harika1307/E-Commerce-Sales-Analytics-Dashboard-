# E-Commerce Sales & Profitability Analysis

An interactive Power BI dashboard designed to analyze e-commerce sales performance, profitability, product performance, customer behavior, and regional trends.

## 📌 Project Overview

This project analyzes historical e-commerce transaction data to understand overall business performance and identify key opportunities for improving revenue and profitability.

The dashboard was built using **Power BI, Power Query, DAX, and data modeling** and provides interactive analysis across sales, products, customers, segments, and regions.

## 🎯 Business Objectives

- Analyze overall sales and profitability performance
- Track revenue and profit trends over time
- Identify top-performing products and sub-categories
- Analyze customer and segment performance
- Compare profitability across regions
- Understand the relationship between discounts and profitability
- Identify high-value customers
- Identify areas of weak or negative profitability

## 🛠️ Tools & Technologies

- **Power BI** – Dashboard development and visualization
- **Power Query** – Data cleaning and transformation
- **DAX** – Measures and calculated tables
- **Data Modeling** – Relationships between fact and dimension tables

## 📊 Dashboard Pages

### 1. Executive Sales Overview

Provides a high-level view of business performance.

**Key KPIs:**
- Total Revenue
- Total Profit
- Total Orders
- Average Order Value
- Profit Margin %

**Analysis:**
- Monthly revenue trends
- Revenue by category
- Profit by region
- Interactive Year and Region filters

### 2. Product & Profitability Analysis

Focuses on product and profitability performance.

**Analysis:**
- Top 10 products by revenue
- Revenue and profit margin by customer segment
- Profit by sub-category
- Revenue vs. profit by sub-category
- Discount vs. profit margin

### 3. Customer Analysis

Analyzes customer value and behavior.

**Key KPIs:**
- Total Customers
- Revenue per Customer
- Orders per Customer

**Analysis:**
- Top 10 customers by revenue
- Revenue vs. profit for top customers
- Customer distribution by segment
- Customer revenue by segment

## 🧹 Data Preparation

The dataset was prepared using Power Query.

Key preparation steps included:

- Promoting headers
- Correcting column data types
- Validating column quality
- Checking for errors and missing values
- Removing unnecessary columns
- Reviewing duplicate Order IDs based on transaction-level data
- Preparing tables for data modeling

## 🧩 Data Model

The project uses a relational data model consisting of:

- Orders
- Returns
- People
- Date Table
- Order-related dimension data

A dedicated Date Table was created using DAX to support time-based analysis.

The Date Table contains:

- Date
- Year
- Month
- Month Number
- Quarter
- Year Month

The Date Table is related to the Orders table through the Order Date field.

## 📐 Key DAX Measures

Some of the key measures created include:

```DAX
Total Revenue =
SUM(Orders[Sales])

Total Profit =
SUM(Orders[Profit])

Total Orders =
DISTINCTCOUNT(Orders[Order ID])

Profit Margin % =
DIVIDE([Total Profit], [Total Revenue])

Average Order Value =
DIVIDE([Total Revenue], [Total Orders])
