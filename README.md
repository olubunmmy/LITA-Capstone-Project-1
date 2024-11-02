# LITA-Capstone-Project-1
Project conducted during LITA Data Analysis training

# Project Title:Capstone Project: Sales Data Analysis


### Project Overview
This capstone project aims on performing a sales data analysis using  employing tools like Excel  pivot tables, SQL queries, and Power BI visualizations to derive meaningful insights, calculate key performance metrics, and present findings in an interactive dashboard.

## 3. Data Preparation

### Data Cleaning
- **Handling Missing Values**: Identify and fill or remove missing data.
- **Data Types**: Ensure all columns have the correct data types (e.g., dates, integers).
- **Outlier Detection**: Identify and handle any outliers in the sales data.

### Data Transformation
- **Date Formatting**: Convert `Order Date` to a standard format.
- **Creating New Variables**: Generate additional columns for year, month, and quarter from `Order Date` for easier analysis.

## 4. Exploratory Data Analysis (EDA) using  employing tools like Excel pivot table pivot tables, SQL queries, and Power BI visualizations.By employing tools like Excel, SQL, and Power BI, we will perform exploratory data analysis (EDA) to derive actionable insights that can drive sales strategies. The goal is to derive meaningful insights from sales data, calculate key performance metrics, and present findings in an interactive dashboard.

---

#### Objective:
To analyze sales data across various regions, product categories, and order dates to identify trends and optimize sales strategies.
- To understand sales performance over time.
- To identify trends and patterns in sales data.
- To assess the impact of various factors on sales performance.
- To create visual dashboards for stakeholders.


#### Scope:
- **Data Dimensions**:
  - **Regions**: Examine sales performance across different geographical areas.
  - **Products**: Analyze sales by product categories to determine bestsellers and underperformers.
  - **Order Dates**: Assess sales trends over time to identify seasonal variations and peak sales periods.



### 1. Project Setup

#### 1.1. Data Collection
- **Data Source**: The data used for this project was provided by our facilitator. The dataset include fields like:
  - Order ID
  - Customer ID
  - Product Name
  - Region
  - Order date
  - Quantity Sold
  - Unit Price
  - Total Sales
    
    

#### 1.2. Tools Used
- **Excel**: For data cleaning and pivot table analysis.
- **SQL**: For querying data from the database.
- **Power BI**: For creating interactive dashboards.

---

### 2. Data Preparation
## 3. Data Preparation

### Data Cleaning
- **Handling Missing Values**: Identify and fill or remove missing data.
- **Data Types**: Ensure all columns have the correct data types (e.g., dates, integers).
- **Outlier Detection**: Identify and handle any outliers in the sales data.

### Data Transformation
- **Date Formatting**: Convert `Order Date` to a standard format.
- **Creating New Variables**: Generate additional columns for year, month, and quarter from `Order Date` for easier analysis.

## 4. Exploratory Data Analysis (EDA)

#### 2.1. Loaded Data into Excel
- Imported the sales data into Excel.
- It was ensured that data is structured with the appropriate columns.

#### 2.2. Data Cleaning
- **Removal Of Duplicates**:  Excel's feature was used to remove the duplicates in datasets
- **Handle Missing Values**: Use functions like `IFERROR` or `ISBLANK` to manage missing data.
- **Format Data**: Ensure all columns (especially dates and currencies) are correctly formatted.

#### 2.3. Create a Total Sales Column
- Add a new column in Excel for Total Sales:
  ```excel
  = Unit Price * Quantity Sold
  ```

---

### 3. Analysis Using Pivot Tables in Excel

#### 3.1. Creating Pivot Tables
- **Insert Pivot Table**: Select the data range and insert a pivot table.
  
#### 3.2. Key Pivot Table Analyses
1. **Total Sales by Category**:
   - Drag `Category` to Rows and `Total Sales` to Values.
   - Set Value Field Settings to `SUM`.
  
2. **Monthly Sales Trends**:
   - Drag `Sale Date` to Rows (group by Month).
   - Drag `Total Sales` to Values.
  
3. **Sales by Region**:
   - Drag `Region` to Rows and `Total Sales` to Values.

#### 3.3. Calculating Measures
- **Average Order Value**:
  - Use a calculated field in the pivot table:
  ```excel
  = SUM(Total Sales) / COUNT(Order ID)
  ```

- **Sales Growth Percentage**:
  - Compare sales month-over-month or year-over-year by creating a new column or using calculated fields in your pivot table.

---

### 4. Data Analysis Using SQL

#### 4.1. Database Setup
- Import the cleaned sales data into a SQL database (e.g., MySQL, PostgreSQL).

#### 4.2. Basic SQL Queries
- **Total Sales**:
  ```sql
  SELECT SUM(unit_price * quantity) AS total_sales
  FROM sales_table;
  ```

- **Sales by Category**:
  ```sql
  SELECT category, SUM(unit_price * quantity) AS total_sales
  FROM sales_table
  GROUP BY category
  ORDER BY total_sales DESC;
  ```

- **Monthly Sales Trends**:
  ```sql
  SELECT DATE_TRUNC('month', sale_date) AS month, SUM(unit_price * quantity) AS total_sales
  FROM sales_table
  GROUP BY month
  ORDER BY month;
  ```

- **Average Order Value**:
  ```sql
  SELECT AVG(unit_price * quantity) AS average_order_value
  FROM sales_table;
  ```

---

### 5. Data Visualization Using Power BI

#### 5.1. Importing Data into Power BI
- Connect Power BI to the SQL database or import the Excel file with cleaned data.

#### 5.2. Creating Visualizations
- **Sales Overview Dashboard**:
  - Bar chart for total sales by category.
  - Line chart for monthly sales trends.
  - Card visuals for total sales and average order value.

#### 5.3. Adding Interactivity
- Add slicers for filtering data by:
  - Category
  - Region
  - Date Range

#### 5.4. Creating Reports
- Design a report layout that includes:
  - KPIs for sales performance.
  - Visuals showing sales trends and comparisons.

---

### 6. Insights and Recommendations

#### 6.1. Key Findings
- Identify the top-selling products and categories.
- Highlight seasonal trends and sales patterns.
- Assess the impact of regions on sales performance.

#### 6.2. Actionable Recommendations
- Suggest inventory management strategies based on sales trends.
- Propose marketing initiatives for underperforming products.
- Recommend targeted promotions based on regional sales data.

---

### 7. Final Presentation

#### 7.1. Compile Reports
- Create a comprehensive report summarizing methodologies, findings, and visualizations.

#### 7.2. Prepare a Presentation
- Use PowerPoint or similar tools to present key insights to stakeholders.

#### 7.3. Gather Feedback
- Present findings to stakeholders and gather feedback for future iterations or improvements.

---

### Conclusion
This capstone project demonstrates a systematic approach to sales data analysis using pivot tables in Excel, SQL queries for database management, and Power BI for interactive visualizations. The insights derived can significantly impact strategic decision-making and enhance overall sales performance.



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

---

## 1. Introduction

### Project Overview
This capstone project aims to analyze sales data from a fictional retail company. By employing tools like Excel, SQL, and Power BI, we will perform exploratory data analysis (EDA) to derive actionable insights that can drive sales strategies.

### Objectives
- To understand sales performance over time.
- To identify trends and patterns in sales data.
- To assess the impact of various factors on sales performance.
- To create visual dashboards for stakeholders.

## 2. Data Collection

### Data Sources
The dataset will be collected from:
- Company sales records (CSV or Excel format).
- Possible integration with external datasets (e.g., demographic data, economic indicators).

### Data Description
The dataset contains the following columns:
- `Order ID`: Unique identifier for each order.
- `Order Date`: Date of the order.
- `Customer ID`: Unique identifier for customers.
- `Product ID`: Unique identifier for products.
- `Quantity Sold`: Number of units sold.
- `Sales Amount`: Total sales amount for the order.
- `Region`: Geographic area of the sale.
- `Category`: Product category.

## 3. Data Preparation

### Data Cleaning
- **Handling Missing Values**: Identify and fill or remove missing data.
- **Data Types**: Ensure all columns have the correct data types (e.g., dates, integers).
- **Outlier Detection**: Identify and handle any outliers in the sales data.

### Data Transformation
- **Date Formatting**: Convert `Order Date` to a standard format.
- **Creating New Variables**: Generate additional columns for year, month, and quarter from `Order Date` for easier analysis.

## 4. Exploratory Data Analysis (EDA)

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

## 5. Data Analysis Using SQL

### Key Queries
1. **Total Sales by Month**:
   ```sql
   SELECT MONTH(Order_Date) AS Sales_Month, SUM(Sales_Amount) AS Total_Sales
   FROM sales_data
   GROUP BY MONTH(Order_Date)
   ORDER BY Sales_Month;
   ```

2. **Top 10 Products by Sales**:
   ```sql
   SELECT Product_ID, SUM(Sales_Amount) AS Total_Sales
   FROM sales_data
   GROUP BY Product_ID
   ORDER BY Total_Sales DESC
   LIMIT 10;
   ```

3. **Sales by Region**:
   ```sql
   SELECT Region, SUM(Sales_Amount) AS Total_Sales
   FROM sales_data
   GROUP BY Region;
   ```

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
- Implement slicers for dynamic filtering (e.g., by year, region).

## 7. Conclusion

### Summary of Findings
- Present key insights drawn from the EDA and SQL analysis.
- Highlight any trends observed in sales performance and customer behavior.

### Future Recommendations
- Suggest potential marketing strategies based on the analysis (e.g., target high-performing regions).
- Recommend further analysis on customer demographics or product performance.

---

This comprehensive project outline provides a structured approach to analyzing sales data, using powerful tools to extract meaningful insights and present them effectively. You can adapt each section according to the specifics of the dataset you work with and the insights you uncover.
