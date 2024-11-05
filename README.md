# LITA-Capstone-Project-1
Project conducted during LITA Data Analysis training

# Project Title:Sales Performance Analysis for a Retail Store

----

## Table of Contents
1. **Introduction**
   - Project Overview
   - Objectives
2. **Data Collection**
   - Data Sources
   - Data Description
   
3. **Data Preparation**
   - Data Cleaning
   - Data Transformation
4. **Exploratory Data Analysis (EDA)**
   - Descriptive Statistics
   - Visualization
   - Insights
5. **Data Analysis Using SQL**
   - Key Queries
   - Results
6. **Data Visualization with Power BI**
   - Dashboard Creation
   - Key Visuals
7. **Conclusion**
   - Summary of Findings
   - Future Recommendations

     
-----
## Introduction

------
### Project Overview

#### Objectives

This Capstone Project aims to analyze sales performance of a retail store across various regions, product categories, and order dates to identify insights such as top selling products,regional performance and monthly sales trends to optimize sales strategies.

The goals of the project is;
- To understand sales performance over time.
- To identify trends and patterns in sales data.
- To assess the impact of various factors on sales performance.
- To create an interactive Power BI dashboards that highlight these findings.

------
## Data Collection

 ### Data Sources
The datasets used in this project was primarily gotten from an open source online but they were made available to us by our facilitators LITA class.

 ### Data Description
  The datasets used include the following fields:
  - Order ID
  - Customer ID
  - Product Name
  - Region
  - Order date
  - Quantity Sold
  - Unit Price
    
 -----  
 ## Tools Used

- Microsoft Excel [Download Here](https://www.microsoft.com)
  For data cleaning and pivot table analysis.
  
- SQL
  For querying data from the database.
  
- Power BI
  1.For creating interactive dashboards.
  2. For Analysis
  3. For  Visualization
  
- Github for Portfolio building
  
-----
## Data Preparation

### Data Cleaning
- **Handling Missing Values**:Missing data were identified and filled and columns with null datas were removed.
- **Data Types**: In SQL it was ensured that all columns have the correct data types.
- **Outlier Detection**:Outliers were identified  and handled  in the sales data.

### Data Transformation
- **Date Formatting**: `Order Date` were converted to a standard format.
- **Creating New Variables**: Additional columns for year, month, and quarter from `Order Date` were generated for easier analysis.


------
## Exploratory Data Analysis (EDA)

####  Loaded Data into Excel
- Sales datasets were imported into Excel.
- It was ensured that data is structured with the appropriate columns.

####  Data Cleaning
- **Removal Of Duplicates**:  Excel's feature was used to remove the duplicates in datasets
  
- **Formated Data**:It was ensured that  all columns were correctly formatted.

- **Created a Total Sales Column**
- Another new column was added in Excel for Total Sales:
  ```excel
  = Unit Price * Quantity Sold

 (https://github.com/user-attachments/assets/52fbe687-eb59-4adf-a4ad-e31c18d0d07c)

  
-----
## Analysis Using Pivot Tables in Excel

#### Creating Pivot Tables
- **Inserting Pivot Table**: The data range was selected and inserted into a pivot table.
  
####  Key Pivot Table Analyses
1. **Total Sales by  Product**:
    'Products' were dragged to Rows and `Total Sales` to Values.
     
  
2. **Sales by Region**:
   - Region was dragged to Rows.
   - Total Sales was dragged to Values.
  
3. **Sales by Month**:
   - `Region` was dragged to Rows and `Total Sales` to Values.

####  Calculating Measures
- **Average Sales per Product**:
  - It was calculated using this Excel formula;

  = AVERAGEIF(Product column,Product Category,Total Sales)
  ```

- **Total Revenue by Region**:
  This measure was also calculated using the below excel metric

  =SUMIF(Range,Criteria,Sum range)

  PIVOT TABLES

---

## Data Analysis Using SQL

####  Database Setup
- The cleaned datasets were imported into a SQL Server database.

####  SQL Queries Used
- **Total Sales per product**:
  ```sql
  SELECT Product, Sum(Total_sales) AS total_sales
  FROM (dbo).[LITA Capstone Dataset.xlsl-Salesdata]
  Group by Product
  Order by 1 asc
  ```

- **Highest selling product**:
  ```sql
  SELECT top 1 product, SUM(Total_Sales) AS total_sales_per_product
  FROM (dbo).[LITA Capstone Dataset.xlsl-Salesdata]
  GROUP BY product
  ORDER BY 2 DESC;
  ```

- **Monthly Sales total for the current year**:
  ```sql
  SELECT Orderdate, sum (Total_sales) AS [monthly sale for current year]
  FROM (dbo).[LITA Capstone Dataset.xlsl-Salesdata]
  where OrderDate between '2024/01/01' and '2024/12/31'
  Group by OrderDate
  ```


---

###  Data Visualization Using Power BI

####  Importing Data into Power BI
- Connect Power BI to the SQL database or import the Excel file with cleaned data.

####  Visualizations

- **Sales Overview Dashboard**:
  - Bar chart for total sales by category.










  - Line chart for monthly sales trends.
  - Card visuals for total sales and average order value.

#### 5.3. Adding Interactivity
- Add slicers for filtering data by:
  - Category
  - Region
  - Date Range

#### Creating Reports
- Design a report layout that includes:
  - KPIs for sales performance.
  - Visuals showing sales trends and comparisons.

---

### Insights and Recommendations

####  Key Findings
- Identify the top-selling products and categories.
- Highlight seasonal trends and sales patterns.
- Assess the impact of regions on sales performance.

####  Actionable Recommendations
- Suggest inventory management strategies based on sales trends.
- Propose marketing initiatives for underperforming 

---

### Conclusion
This capstone project demonstrates a systematic approach to sales data analysis using pivot tables in Excel, SQL queries for database management, and Power BI for interactive visualizations. The insights derived can significantly impact strategic decision-making and enhance overall sales performance.





## 1. Introduction

### Project Overview
This capstone project aims to analyze sales data from a fictional retail company. By employing too

### Descriptive Statistics
- Calculate mean, median, mode, and standard deviation for numerical columns.
- Frequency distribution of categorical variables.

### Visualization
- **Histograms**: Distribution of `Sales Amount`.
- **Bar Charts**: Total sales by `Category` and `Region`.
- **Line Graphs**: Trends over time for monthly sales.

### Insights
- Identify peak sales periods.
- Analyze best-selling products and categories.
- Explore sales performance across different regions.


### Key Queries
1. **Total Sales by Month

### Results
- Summarize the findings from the SQL queries, including key metrics and any interesting patterns discovered.

## 6. Data Visualization with Power BI

### Dashboard Creation
- Connect Power BI to the sales data source.
- Build a dashboard that includes:
  - Total Sales over Time
  - Top Selling Products
  - Sales by Region
  - Comparison of Sales by Category

### Key Visuals
- Use a combination of line charts, bar graphs, and pie charts.
- Implement slicers for dynamic filtering (e.g., b
