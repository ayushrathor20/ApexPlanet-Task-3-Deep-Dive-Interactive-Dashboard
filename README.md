# ApexPlanet Task 3 – Deep-Dive Analysis & Interactive Dashboard

## Overview

This project is part of the **ApexPlanet Software Pvt Ltd Data Analytics Internship – Task 3**.

The objective of this task is to perform a **deep-dive business analysis**, define core KPIs, analyze customer behavior through segmentation, and build an **interactive Power BI dashboard** for business decision-making.

---

## Objectives

The project focuses on:

- Defining 3–5 core business KPIs
- Performing deep-dive customer analysis
- Segmenting customers using business rules
- Identifying important sales and customer insights
- Building an interactive Power BI dashboard
- Presenting findings through a structured deep-dive report

---

## Dataset

The analysis uses the cleaned sales dataset prepared during the previous internship task.

### Dataset Summary

- **Records:** 1,000
- **Unique Orders:** 992
- **Unique Customers:** 947
- **Total Units Sold:** 5,435
- **Total Revenue:** ₹13,93,99,439.65

### Main Fields

- Order_ID
- Customer_ID
- Customer_Name
- Gender
- Age
- City
- Product
- Category
- Quantity
- Unit_Price
- Total_Sales
- Order_Date
- Year
- Month
- Month_Name

---

## Core KPIs

Five core KPIs were defined for the dashboard.

| KPI | Formula | Business Rationale |
|---|---|---|
| Total Revenue | `SUM(Total_Sales)` | Measures overall sales performance |
| Total Orders | `DISTINCTCOUNT(Order_ID)` | Measures order volume |
| Total Customers | `DISTINCTCOUNT(Customer_ID)` | Measures unique customer base |
| Average Order Value | `Total Revenue / Total Orders` | Measures average revenue generated per order |
| Total Units Sold | `SUM(Quantity)` | Measures sales volume in units |

---

## Deep-Dive Analysis: Customer Segmentation

The selected deep-dive business area is **Customer Segmentation**.

The purpose is to understand customer value, purchasing frequency, and recency so that different customer groups can be analyzed separately.

### Customer-Level Metrics

The analysis uses:

- Total Orders per Customer
- Total Revenue per Customer
- Last Order Date
- Recency Days
- Customer Segment

---

## Customer Segmentation Rules

Customers are assigned to segments using business-rule based logic.

| Segment | Definition |
|---|---|
| High Value | Total Revenue ≥ ₹300,000 and Total Orders ≥ 2 |
| Loyal | Total Orders ≥ 2 and Recency ≤ 90 days |
| At Risk | Recency > 180 days |
| New / Recent | Total Orders = 1 and Recency ≤ 90 days |
| Regular | Remaining customers |

These rules are designed to provide an interpretable customer segmentation framework for business analysis.

---

## Power BI Dashboard

The Power BI dashboard contains two major analysis pages.

### Page 1 – Sales Overview

The Sales Overview page includes:

- Total Revenue
- Total Orders
- Total Customers
- Average Order Value
- Total Units Sold
- Revenue by Category
- Monthly Sales Trend
- Product Revenue Ranking
- Revenue by Gender
- Category Filter
- City Filter

### Page 2 – Customer Deep Dive

The Customer Deep Dive page includes:

- Customer Segment Distribution
- Revenue by Customer Segment
- Customer Economics
- Customer Segments by City
- Customer Detail Table
- Customer Segment Filter
- City Filter

---

## Key Business Findings

The analysis identifies several important patterns:

1. **Electronics** is the highest-revenue product category.
2. **Laptop** is the highest-revenue individual product.
3. **March** records the highest monthly revenue.
4. Customer segmentation shows meaningful differences in customer value and recency.
5. Customer-level analysis helps identify high-value, loyal, recent, regular, and at-risk customer groups.

---

## Business Recommendations

Based on the analysis:

- Focus retention efforts on **High Value** customers.
- Develop loyalty strategies for **Loyal** customers.
- Use targeted re-engagement campaigns for **At Risk** customers.
- Improve onboarding and repeat-purchase strategies for **New / Recent** customers.
- Monitor segment performance by city and product category.
- Use KPI and segment filters in the dashboard to support data-driven decision-making.

---

## Project Structure

```text
ApexPlanet-Task-3-Deep-Dive-Interactive-Dashboard/
│
├── data/
│   └── Cleaned_ApexPlanet_Sales_Dataset.xlsx
│
├── report/
│   └── Task_3_Deep_Dive_Report_FINAL.pdf
│
├── powerbi/
│   ├── ApexPlanet_Task3_Interactive_Dashboard.pbix
│   └── ApexPlanet_Task3_PowerBI_CLEAN.zip
│
└── README.md
