 # Coffee Sales Dashboard

## Overview

The Coffee Sales Dashboard is a data analytics project developed to explore coffee shop sales performance and customer ordering patterns. The project uses Power BI to present sales and order data through interactive dashboards, with SQL queries used to investigate key business metrics.

The dashboard provides an overview of revenue, product performance, order volume, and purchasing patterns across different time periods. It is designed to help stakeholders understand business performance and identify areas for further investigation.

**Project type:** Data Analytics  
**Tools:** Microsoft Power BI, SQL Server Management Studio (SSMS)  
**Data coverage:** 2024–2025 (as displayed in the dashboard)  
**Author:** Aiyelero Tobiloba

## Business Problem

Coffee businesses need a clear understanding of which products generate the most revenue, when customers make purchases, and how sales vary across days and months.

Without an organized view of sales data, it can be difficult to identify high-performing products, understand purchasing patterns, and make informed decisions about inventory and business operations.

This project addresses these questions by organizing coffee sales data into visual reports and using SQL queries to examine sales performance across multiple dimensions.

## Objectives

The main objectives of this project were to:

- Analyze total sales revenue and quantity sold.
- Identify the highest- and lowest-revenue coffee products.
- Examine sales and order patterns across different times of the day.
- Compare sales performance across weekdays.
- Explore monthly sales and order trends.
- Analyze payment methods by transaction count and revenue.
- Present key metrics in interactive Power BI dashboards to support business decision-making.

## Dataset

The project uses a coffee sales dataset containing transaction-level information about coffee purchases.

The fields referenced in the SQL queries include:

| Column | Description |
|---|---|
| `date` | Date of the transaction |
| `hour_of_day` | Hour associated with the transaction |
| `coffee_name` | Name of the coffee product |
| `money` | Monetary value recorded for the transaction |
| `cash_type` | Payment method or payment category |
| `time_of_day` | Time-of-day category |
| `weekday` | Day of the week |
| `month_name` | Month associated with the transaction |

The Power BI dashboard also displays unit price, sales, and quantity sold metrics.

**Dataset source:** Kaggle 

**Dataset size:** [3547 rows , 11 Columns]

**Currency:** [Dollars]

## Tools & Technologies

- **Microsoft Power BI Desktop:** Used to build interactive dashboards and visualize sales and order metrics.
- **SQL Server Management Studio (SSMS):** Used to write and execute SQL queries for aggregating and exploring sales data.
- **SQL:** Used for filtering, grouping, sorting, counting transactions, and calculating revenue totals.

## Data Preparation

The SQL analysis references the `Coffee_sales` table and uses its available fields to organize data for reporting.

The documented analytical workflow includes:

- Selecting records from the sales table for inspection.
- Grouping transactions by coffee type, date, month, weekday, and time of day.
- Aggregating monetary values using `SUM()`.
- Counting transactions using `COUNT()`.
- Filtering records by product and reporting period.
- Sorting results to compare product and time-based performance.

**Data cleaning and transformation details:** [Document any missing-value handling, duplicate removal, data type corrections, category standardization, or Power Query transformations performed.]

The extent of data cleaning and transformation should be documented separately from the aggregation steps above.

## Analysis

The project explores several business questions through SQL queries and Power BI visualizations.

### 1. Sales Performance by Coffee Type

Compared revenue across coffee products to identify the products contributing the most and least to recorded sales.

### 2. Sales by Time of Day

Analyzed revenue across morning, afternoon, and night categories to understand how sales are distributed throughout the day.

### 3. Sales by Weekday

Compared revenue across the seven days of the week to identify differences in daily sales performance.

### 4. Monthly Sales Analysis

Examined revenue and order metrics by month to explore sales patterns across the reporting period.

### 5. Order Analysis

Compared order counts across coffee products, months, weekdays, and times of day to understand purchasing activity.

### 6. Payment Method Analysis

Used SQL to calculate transaction counts and revenue by payment category.

### 7. Interactive Dashboard Exploration

The Power BI report includes sales and order dashboards with year and month filters, coffee product filters, and visualizations for comparing performance across products and time periods.

## Key Findings

The following findings are based on the figures displayed in the Power BI dashboard.

### Sales Performance by Coffee Type

- **Latte** recorded the highest displayed sales, at approximately 393K.
- **Americano with Milk** followed at approximately 338K.
- **Cappuccino** generated approximately 261K in sales.
- **Espresso** recorded the lowest displayed sales, at approximately 37K.

### Sales by Time of Day

| Time of day | Recorded sales |
|---|---:|
| Night | 732.34K |
| Afternoon | 537.49K |
| Morning | 337.31K |

Night recorded the highest sales among the three time-of-day categories, followed by afternoon and morning.

### Sales by Weekday

| Weekday | Approximate sales |
|---|---:|
| Tuesday | 262K |
| Monday | 245K |
| Thursday | 240K |
| Friday | 235K |
| Wednesday | 226K |
| Saturday | 207K |
| Sunday | 193K |

Tuesday recorded the highest displayed weekday sales, while Sunday recorded the lowest.

### Overall Dashboard Metrics

The dashboard displays the following headline metrics:

- **Sum of unit price:** approximately 112K.
- **Sum of sales:** approximately 2M.
- **Total quantity sold:** 3,547.

These values are reported as displayed in the dashboard. The underlying metric definitions, currency, and aggregation logic should be verified before using them for financial reporting.

## Business Recommendations

Based on the observed patterns, the following actions could be considered:

1. **Review inventory allocation:** Evaluate stock availability for Latte and Americano with Milk, which recorded the highest displayed sales.
2. **Assess staffing by time of day:** Investigate whether staffing and preparation capacity align with the higher sales recorded at night.
3. **Review lower-performing products:** Examine Espresso and other lower-revenue products to determine whether pricing, demand, product positioning, or customer preferences explain their performance.
4. **Plan weekday operations:** Use weekday sales patterns to inform staffing and inventory planning, while considering operating costs and demand variability.
5. **Investigate monthly performance:** Compare monthly results over time to identify recurring patterns and possible seasonal effects.
6. **Monitor payment methods:** Use transaction counts and revenue by payment method to understand payment preferences and support operational planning.

These recommendations are based on descriptive analysis. Their effectiveness would need to be evaluated using additional business context and subsequent sales data.

## Limitations

- The dataset source, collection method, and full reporting period have not yet been documented in this README.
- The displayed figures are descriptive and do not establish the causes of observed sales patterns.
- Revenue and quantity metrics depend on the underlying data definitions and aggregation methods.
- The dashboard's displayed values are rounded, so exact totals may differ from the underlying data.
- Profitability cannot be assessed without product costs, operating expenses, and other relevant financial information.
- Customer demographics, repeat-purchase behaviour, and individual customer preferences are not covered by the documented analysis.
- The SQL script includes exploratory queries whose aggregation logic should be validated before treating every result as a reliable order count.

## Project Structure

The following is a suggested repository structure. Update the filenames to match the files included in your GitHub repository.

```text
coffee-sales-dashboard/
├── README.md
├── dashboard/
│   └── [Coffee Sales dashboard ].pbix
├── sql/
│   └── [Coffee Sales Query].sql
├── images/
│   └── [dashboard screenshot].png
└── data/
    └── [Kaggle]
```

**Note:** Only include files and folders that are actually present in your repository. If the dataset cannot be redistributed, provide its source or instructions for obtaining it instead.

## How to Reproduce the Analysis

1. **Obtain the dataset.** Download or access the coffee sales dataset from [Kaggle].
2. **Set up the database.** Import the dataset into SQL Server and create or identify the `Coffee_sales` table.
3. **Run the SQL queries.** Open the SQL script in SQL Server Management Studio and execute the relevant queries.
4. **Open the Power BI report.** Use Power BI Desktop to open the `.pbix` file.
5. **Connect the data source.** If required, update the data connection to match your local database or dataset location.
6. **Explore the dashboards.** Use the available filters and visuals to examine sales and order performance by product, month, weekday, and time of day.

**Prerequisites:** SQL Server, SQL Server Management Studio, Power BI Desktop, and access to the source dataset.

## Key Skills Demonstrated

- SQL querying and aggregation
- Data exploration and descriptive analysis
- Revenue and transaction analysis
- Grouping, filtering, and sorting data
- Business intelligence reporting
- Power BI dashboard development
- Data visualization and KPI presentation
- Translating business questions into analytical queries
- Communicating data-driven business observations
- Developing practical recommendations from descriptive findings

---





