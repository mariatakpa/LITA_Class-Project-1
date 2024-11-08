## Sales Performance Analysis for a Retail Store
---

### Project Overview
---

This project aims at analyzing the sales performance of a retail store. The analysis focuses on uncovering insights such as top-selling products, regional performance , monthly sales trends, and customer purchasing behavior. The goal is to produce an interactive Power BI dashboard that visualizes these insights.

### Project Objective
---

 - To identify trends, understand customer behavior, optimize inventory, and improve revenue.
 - To help the store make data-driven decisions, maximize sales, and increase profitability.
 - To provide a user-friendly interface for generating pivot tables from data sources
 - To develop a Power BI dashboard to visualize key insights.

The project consists of three main phases: 
 1. **Excel Analysis** : Initial data exploration and basic analysis using pivot tables and Excel formulas.
 2. **SQL Queries** : Data extraction and further analysis using SQL queries to answer pecific business questions.
 3. **PowerBI Dashboard** : Visualization of the analysis in an interactive Power BI dashboard.

---
### Project Structure
---
-**data/**: Contains raw sales data files.

-**sql_queries/** :Contains SQL scripts for extracting insights from the data.

-**power_bi/** : Contains the Power BI dashboard files

---
### Instructions
---
1. **Excel**: Open `excel_reports/sales_analysis.xlsx` to explore sales data, create pivot tables, and calculate metrics.
2. **SQL**: Load the data into SQL Server and run the queries in `sql_queries/sales_analysis.sql`to extract insights.
3. **Power BI**: Open `power_bi/dashboard.pbix` to view the interactive dashboard.
   
---

### Project Tools

The following software tools are required for this project:

- **Microsoft Excel** : For initial data exploration and pivot tables.
- **SQL** (Structured Query Language) : To run queries and perform data extraction
- **Power BI** : For creating an interactive dashboard.
- GitHub For Portfolio Building.

---

### Data Cleaning and Preparation
1. Data Collection: Sales data was collected from Microsoft Excel
2. Data Analysis: Excel and SQL were used to analyze sales data
3. Data Visualization: Power BI was used to create interactive dashboards.

---

### Exploratory Data Analysis
EDA involves the exploring of data to answer some questions about the data such as 
- What product are on the peak sales?
- What is the overall sales trend?
- What regions have the highest revenue contribution?

---

### Data Analysis
This is where I included  lines of queries during analysis

```sql
select * from [dbo].[SalesData]

Select product ,sum(Total_sales) as Totalsales from [dbo].[SalesData]
Group by product

Select Region,Count(orderID) as no_off_number from [dbo].[SalesData]
Group by Region

Select product,sum(Total_sales)as Totalsales from [dbo].[SalesData]
Group by product

Select product,sum(Total_sales) as Total_revenue from [dbo].[SalesData]
Group by product

Sum(OrderDate) as sales_month,sum(revenue) as Total_sales from [dbo].[SalesData]
where year(2034-08-11)
Group by OrderDate

Select customer_id, sum(revenue) as total_purchase
from [dbo].[SalesData]
Group by customer_id
order by 2 desc

Select Region,sum(revenue)/(select sum(revenue)
from [dbo].[sales data])* 100 as sales_percentage
from [dbo].[sales data]
group by region
```


---
### Data Visualization

![Power BI Visualization Prj 1](https://github.com/user-attachments/assets/3e724114-b5e1-4e5b-ae36-a8004c8bcd43)

![LITA Capstone Dataset Excel](https://github.com/user-attachments/assets/dff09f93-8c8c-42b8-8512-d0124d800fce)

![Pivot Table Project](https://github.com/user-attachments/assets/a510fce5-ef47-471e-923d-03f916e3e33e)

![Pivot Chart ](https://github.com/user-attachments/assets/c6de666e-273d-4057-8891-6c81fe31e446)




---
### Conclusion
The sales performance analysis project provided insights into top-selling products, regional performances , monthly sales trends. 
The Power BI dashboard enabled interactive visualization of key metrics.

