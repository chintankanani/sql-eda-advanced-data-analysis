# SQL Exploratory Data Analysis & Advanced Data Analysis

## Project Overview

This project demonstrates Exploratory Data Analysis (EDA) and Advanced Data Analysis using SQL Server. Using customer, product, and sales data, the project explores business performance, analyses customer purchasing behaviour, evaluates product performance, and generates analytical reports to support data-driven decision-making.

The project contains 13 SQL scripts, progressing from database exploration and business metric analysis to customer and product reporting. It applies SQL techniques to transform raw business data into meaningful insights.

## Objectives

- Explore database structures, dimensions, date ranges, and key business measures.
- Analyse sales magnitude, rankings, and changes over time.
- Perform cumulative, performance, segmentation, and part-to-whole analysis.
- Evaluate customer purchasing behaviour and customer segments.
- Analyse product performance using sales, order volume, quantity, and customer metrics.
- Create customer and product reports with aggregated business metrics and KPIs.

## Tools & Technologies

- **SQL Server** — database querying and analysis.
- **SQL Server Management Studio (SSMS)** — writing and executing SQL queries.
- **SQL** — joins, Common Table Expressions (CTEs), aggregations, conditional logic, date calculations, and analytical reporting.

## Repository Structure

```text
SQL-EDA-Advanced-Data-Analysis/
├── Datasets/
│   ├── dim_customers.csv
│   ├── dim_products.csv
│   └── fact_sales.csv
└── Scripts/
    ├── 01_database_exploration.sql
    ├── 02_dimensions_exploration.sql
    ├── 03_date_range_exploration.sql
    ├── 04_measures_exploration.sql
    ├── 05_magnitude_analysis.sql
    ├── 06_ranking_analysis.sql
    ├── 07_change_over_time_analysis.sql
    ├── 08_cumulative_analysis.sql
    ├── 09_performance_analysis.sql
    ├── 10_data_segmentation.sql
    ├── 11_part_to_whole_analysis.sql
    ├── 12_report_customers.sql
    └── 13_report_products.sql
```

*Note: The folder and dataset filenames above illustrate the structure. Keep the names in this section consistent with the actual names in your GitHub repository.*

## Analysis Workflow

### 1. Database Exploration

The initial scripts examine the database structure and available tables to understand the data before performing detailed analysis.

- Explore database tables and their contents.
- Inspect customer and product dimensions.
- Examine the available date range.
- Identify key business measures.

### 2. Exploratory Data Analysis

The EDA scripts investigate business data from multiple perspectives.

| Script | Analysis |
|---|---|
| `01_database_exploration.sql` | Database exploration |
| `02_dimensions_exploration.sql` | Dimension exploration |
| `03_date_range_exploration.sql` | Date range analysis |
| `04_measures_exploration.sql` | Business measure exploration |
| `05_magnitude_analysis.sql` | Magnitude analysis |
| `06_ranking_analysis.sql` | Ranking analysis |

### 3. Advanced Data Analysis

The advanced analysis scripts apply different analytical techniques to investigate business performance and identify patterns.

| Script | Analysis |
|---|---|
| `07_change_over_time_analysis.sql` | Change-over-time analysis |
| `08_cumulative_analysis.sql` | Cumulative analysis |
| `09_performance_analysis.sql` | Performance analysis |
| `10_data_segmentation.sql` | Data segmentation |
| `11_part_to_whole_analysis.sql` | Part-to-whole analysis |

These techniques help examine trends, compare performance, understand customer and product segments, and evaluate contributions to overall business results.

## Customer Report

**Script:** `12_report_customers.sql`

The customer report consolidates customer-level information and purchasing metrics by joining the sales fact table with the customer dimension.

### Key Metrics

- Customer name and customer number
- Age group
- Customer segment: VIP, Regular, or New
- Last order date and recency in months
- Total orders, total sales, and total quantity purchased
- Number of distinct products purchased
- Customer lifespan in months
- Average order value
- Average monthly spend

### Analytical Logic

The report uses a Common Table Expression (CTE) to retrieve customer and transaction details, followed by customer-level aggregation.

Customer segmentation is based on customer lifespan and total sales:

- **VIP:** Lifespan of at least 12 months and total sales greater than 5,000.
- **Regular:** Lifespan of at least 12 months and total sales less than or equal to 5,000.
- **New:** Lifespan of less than 12 months.

Age groups are also created to support demographic analysis.

### Observations from the Report Output

- The displayed VIP customer records include total sales of approximately 6,400–8,200 and average order values of approximately 2,100–2,700.
- The report includes both VIP and New customers, allowing purchasing activity to be examined across different customer segments.
- Metrics such as recency, lifespan, order frequency, and average monthly spend provide different perspectives on customer purchasing behaviour.

These are examples from the displayed report output rather than overall customer-segment averages.

## Product Report

**Script:** `13_report_products.sql`

The product report consolidates product information and sales metrics by joining the sales fact table with the product dimension.

### Key Metrics

- Product name, category, and subcategory
- Product cost
- Last sale date and recency in months
- Product segment
- Product lifespan in months
- Total orders and total sales
- Total quantity sold
- Number of distinct customers
- Average selling price
- Average order revenue
- Average monthly revenue

### Analytical Logic

The report aggregates sales data at the product level, calculating order counts, sales, quantities, customer counts, and lifespan. It then assigns product segments according to total sales:

- **High-Performer:** Total sales greater than 50,000.
- **Mid-Range:** Total sales from 10,000 to 50,000, inclusive.
- **Low-Performer:** Total sales below 10,000.

The report also calculates recency, average selling price, average order revenue, and average monthly revenue to provide additional performance measures.

### Observations from the Report Output

- The displayed Road-150 Red product variants have total sales exceeding 1 million in the report's sales measure.
- The displayed Mountain Bottle Cage record has 2,025 orders, total sales of 20,340, and 2,004 customers.
- Comparing sales, order counts, quantity, and customer reach helps illustrate differences between higher-value products and lower-priced products with frequent purchases.

These observations describe visible rows in the report output and should not be interpreted as overall category rankings or profitability findings.

## Skills Demonstrated

- SQL querying and database exploration
- Joining fact and dimension tables
- Common Table Expressions (CTEs)
- Aggregation and conditional logic
- Date calculations and time-based analysis
- Ranking and cumulative analysis
- Performance analysis and data segmentation
- Customer behaviour and product performance analysis
- Development of analytical reports and business KPIs

## Datasets

The repository includes three datasets:

- **`dim_customers`** — customer details and demographic attributes.
- **`dim_products`** — product details, categories, subcategories, and costs.
- **`fact_sales`** — sales transactions used to calculate business metrics.

Together, these datasets support customer-level and product-level analysis through SQL queries.

## Learning Outcomes

This project strengthened my ability to use SQL Server for exploratory analysis, advanced analytical queries, and business reporting. It demonstrates how customer, product, and sales data can be combined to calculate KPIs and investigate business performance.

## Author

**Chintankumar Kanani**

Business Analytics | SQL | Data Analysis | Business Intelligence
