# Portfolio-Project
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
