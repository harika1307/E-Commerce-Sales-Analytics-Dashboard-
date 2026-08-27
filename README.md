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
```
## 🔎 Key Business Insights

- **Technology** is the highest revenue-generating category, making it a major contributor to overall sales.

- **Copiers and Phones** are among the strongest profit-generating sub-categories, indicating strong profitability within these product areas.

- **Tables** show negative overall profitability despite generating substantial revenue, highlighting a potential issue with pricing, discounts, or product costs.

- The **Consumer segment** has the largest customer base and contributes the highest overall revenue, making it the primary customer segment.

- The **Home Office segment** demonstrates a higher profit margin compared with the other segments, indicating potential for profitable growth.

- Revenue is concentrated among a relatively small group of **high-value customers**, highlighting the importance of customer retention and targeted relationship strategies.

- The analysis of **discounts and profit margins** indicates that discounting should be carefully evaluated to ensure that increased sales justify the impact on profitability.

## 💡 Business Recommendations

- Review the pricing, discount, and cost structure of **loss-making sub-categories**, particularly Tables.
- Focus on retaining and developing relationships with **high-value customers**.
- Explore growth opportunities within **high-margin customer segments** such as Home Office.
- Continue leveraging strong-performing categories such as **Technology** while monitoring profitability.
- Evaluate discount strategies based on both **revenue growth and profit margin**, rather than sales volume alone.
