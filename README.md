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
 to toggle between metrics.

#########################################################################################################################################

PREVIEW OF SALES TREND OF SHOPIFY USING POWERBI 

<img width="740" height="494" alt="Screenshot 2025-08-13 130026" src="https://github.com/user-attachments/assets/f78483ed-d1a4-4c26-a842-484a4ab67bc2" />
<img width="737" height="495" alt="Screenshot 2025-08-13 130225" src="https://github.com/user-attachments/assets/448b93b4-35dc-4b80-967e-04a9af82ba1d" />

The two data visualizers together provide a comprehensive view of Shopify sales performance. The first visualizer serves as a high-level dashboard, presenting overall transaction metrics, customer behavior, regional sales distribution, sales trends over time, payment method breakdowns, and product-type performance. It also includes interactive filters such as "Select Measure," "Gateway," and "Province" to allow users to customize and drill down into specific aspects of the data. The second visualizer, labeled as the Details Tab, presents a detailed table listing individual customer transactions along with order information, product types, and billing locations. Together, these visualizers support both strategic analysis and detailed operational review.
