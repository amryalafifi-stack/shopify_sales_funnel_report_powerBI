This project analyzes Shopify sales data in Power BI to uncover insights into transaction performance, customer purchasing behavior, and long-term customer value.
It delivers an interactive dashboard that allows stakeholders to explore sales trends, customer retention, and revenue patterns dynamically.

The work follows a structured approach from requirement gathering to insight generation, ensuring a business-ready analytical solution.

1. Requirement Gathering / Business Requirements
Reviewed the business needs from the provided documentation.

Defined KPIs and visualization goals based on stakeholder expectations.

Identified data sources, scope, and intended user interactions.

2. Data Walkthrough
Inspected the raw Shopify dataset to understand:

Table structures

Data types (dates, numbers, text)

Missing/duplicate values

Key fields for relationships (Order ID, Customer ID, Product Type, Province, City, Date/Time)

3. Data Connection
Connected the Power BI report to the Shopify data source.

Imported raw data into Power Query for transformation.

4. Data Cleaning / Quality Check
Removed duplicate rows.

Standardized date/time formats.

Ensured numeric columns (Net Sales, Quantity) were correctly typed.

Checked for and addressed missing values in key columns.

Validated data consistency between transactions, customers, and products.

5. Data Modeling
Created a star schema model:

Fact Table: Transactions (sales records with revenue, quantity, timestamps, customer IDs, product types, payment method)

Dimension Tables: Customers, Products, Provinces/Cities, Dates, Payment Methods

Established relationships:

One-to-many from dimension tables to fact table.

Ensured proper cross-filter direction for dashboard interactivity.

6. Data Processing & DAX Calculations
Developed measures for all KPIs required in the business brief:

Transactions Performance
Net Sales – SUM([Net Sales])

Total Quantity – SUM([Quantity])

Net Avg Order Value – DIVIDE([Net Sales], DISTINCTCOUNT([Order ID]))

Customer Purchase Behavior
Total Customers – DISTINCTCOUNT([Customer ID])

Single Order Customers – Customers with Order Count = 1

Repeat Customers – Customers with Order Count > 1

Retention & Value
Lifetime Value (LTV) – Total sales per customer

Repeat Rate – (Repeat Customers / Total Customers) * 100

Purchase Frequency – Average orders per customer

Dynamic Measure Selector
Implemented a parameter table with a disconnected slicer to allow dynamic switching between:

Net Sales

Total Quantity

Total Customers

Repeat Customers

7. Dashboard Layout & Chart Development
1. Regional Overview
Filled Map – Province-level color saturation based on selected KPI.

Bubble/Density Map – City-level bubbles sized by KPI.

City-Level Bar Chart – Sorted by descending KPI, interactive with slicers.

2. Sales Trend Over Time
Area Chart – Daily trend of selected KPI.

Hourly Bar Chart – Sales or customer count by hour (0–23), highlighting peak activity.

3. Gateway Payment Method
Donut chart ranking payment methods by usage and revenue.

4. Product Type
Bar chart comparing product categories by Net Sales and Quantity.

5. Transaction-Level Data
Detail table for drill-through to raw transactions.

Linked from summary visuals for data validation.

8. Interactivity Features
Dynamic KPI measure selector updates all visuals in sync.

Drill-through from maps/charts to detailed order/customer data.

Province/City slicers for geographic filtering.

Date range slicer for custom time-period analysis.

Key Insights
From the dashboard, we can:

Identify top-performing provinces and cities in sales and customer counts.

Track daily and hourly sales patterns to optimize promotions.

Understand payment method preferences across customers.

Highlight high-value customer segments with strong repeat purchase behavior.

Monitor product category performance for inventory and marketing strategies.

Tools & Technologies
Power BI Desktop – Data modeling, DAX, visualization.

Power Query – Data cleaning and transformation.

DAX – KPI calculation and dynamic measure selection.

Repository Structure
yaml
Copy
Edit
├── Shopify Sales Analysis Report.pbix   # Power BI file with full dashboard
├── Shopify Analysis Presentation.pdf    # Project requirements & presentation
├── Screenshot 2025-08-13 130026.png     # Dashboard preview image
├── README.md   



How to Use!!
Open the .pbix file in Power BI Desktop.

Use the KPI selector to toggle between metrics.

Filter by date, region, product type, or payment method.

Drill-through from summary charts to see detailed transaction data.

Potential Next Steps
Integrate with live Shopify API for real-time updates.

Add customer segmentation using RFM analysis.

Incorporate profit margin analysis alongside revenue.

