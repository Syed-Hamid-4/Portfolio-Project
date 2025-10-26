# US Regional Sales & Profitability Analysis Dashboard

# Project Overview:
This project is an end-to-end business intelligence solution developed in Power BI. It analyzes transactional sales data for a fictional US-based company to uncover key insights into sales performance, profitability drivers, warehouse efficiency, and the impact of discount strategies.

# Problem Statement:
The primary objective was to transform raw, multi-file sales data into a dynamic, interactive dashboard. The goal is to provide stakeholders with a tool to answer critical business questions, such as:

1) What are the primary drivers of net sales and gross profit?

2) How do sales and profitability trend over time?

3) Which warehouses and sales channels are the top performers?

4) What is the relationship between discounts applied and overall profitability?

# Project Walkthrough:
1. Data Cleaning and Transformation (ETL) The raw transactional data was loaded into Power Query for preparation. The key transformation steps included:

- Data Type Correction: Corrected Unit Cost and Unit Price columns, which were initially imported as text (due to currency symbols), to a decimal number format to enable calculations.

- Column Renaming: Standardized column names for clarity and ease of use in the data model.

- Feature Engineering: Created new calculated columns to enrich the dataset, including:

- Financial Metrics: Net Sales, Total COGS, and Gross Profit.

- Logistical KPIs: Processing Days and Shipping Days to measure order fulfillment efficiency.

2. Data Modeling A simple data model was created in Power BI. The cleaned Sales table was used as the primary fact table. A dedicated calendar table was created using DAX to facilitate robust time-intelligence analysis. A one-to-many relationship was established between the calendar table and the sales table on the date field.

3. DAX Measures and KPIs Core business logic was implemented using DAX measures. Key measures created include:

- Sum of Net Sales

- Sum of Gross Profit

- Gross Profit %

- Average of Processing Days

- Average of Shipping Days

These measures were used to populate the high-level KPI cards at the top of the dashboard, providing an immediate summary of performance.

# Dashboard Design & Key Insights
The final dashboard is a single-page report designed to provide a comprehensive overview of business performance.

<img width="1380" height="809" alt="image" src="https://github.com/user-attachments/assets/031c768c-e500-4a6a-b6fa-6465bc40c777" />


Key Insights from the Dashboard:

- Warehouse Performance: The treemap visual clearly identifies WARE-NMK1003 as the largest contributor to net sales.

- Channel Distribution: The "In-Store" channel accounts for the largest portion of sales distribution, followed by "Online."

- Profitability Analysis: The "Gross Profit % by Discount Applied" chart reveals a strong negative correlation, indicating that as discounts increase, the gross profit percentage sharply declines. This suggests that high discount strategies may be unsustainable and are a key area for further investigation.
