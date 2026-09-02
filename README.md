# Sales Performance Dashboard

A Power BI dashboard designed to analyze sales performance across different time periods, regions, product categories, and customers.

## Dashboard Preview

> Add your dashboard screenshot to the repository and update the image path below.

```text
images/dashboard-preview.png
```

Example Markdown image code:

```markdown

```

## Overview

This interactive Power BI dashboard provides a clear overview of sales performance and helps identify trends, regional results, product-category contributions, and product-level performance.

The report includes a year slicer that allows users to filter results for:

- 2022
- 2023
- 2024

## Key Performance Indicators

| KPI | Value |
|---|---:|
| Total Sales | 2.53M |
| Total Orders | 2K |
| Total Customers | 854 |
| Total Quantity Sold | 10K |
| Average Order Value | 1.26K |

## Dashboard Features

### Monthly Sales Trend

A line chart displays total sales from January to December. It helps identify sales peaks, low-performing periods, and potential seasonal trends.

### Monthly Orders Trend

A second line chart tracks total orders by month, making it possible to compare customer order volume with overall sales revenue.

### Regional Sales Analysis

The dashboard compares total sales across the following regions:

- East
- West
- North
- Central
- South

### Category Sales Analysis

Sales performance is grouped by product category:

- Furniture
- Apparel
- Beauty
- Toys
- Electronics

### Product-Level Performance

A detailed table provides information for each product, including:

- Product Name
- Category
- Total Sales
- Total Quantity Sold

## Data Model

The Power BI report uses the following tables:

| Table | Description |
|---|---|
| `Customers` | Customer-related information |
| `Date_tbl` | Calendar/date table used for time intelligence |
| `Orders` | Sales transactions and order details |
| `Products` | Product and category information |
| `measure` | Reusable DAX measures |

## DAX Measures

Below are example DAX measures used in the report. Update table and column names if they are different in your model.

```DAX
Total Sales =
SUM(Orders[Sales])
```

```DAX
Total Orders =
DISTINCTCOUNT(Orders[OrderID])
```

```DAX
Total Customers =
DISTINCTCOUNT(Customers[CustomerID])
```

```DAX
Total Quantity =
SUM(Orders[Quantity])
```

```DAX
Average Order Value =
DIVIDE([Total Sales], [Total Orders])
```

## Tools and Technologies

- Microsoft Power BI Desktop
- Power Query
- DAX
- Data Modeling
- Data Visualization

## How to Use

1. Clone or download this repository.
2. Open the `.pbix` file using Microsoft Power BI Desktop.
3. Load or refresh the data source, if included.
4. Use the **Year** slicer to filter the dashboard by year.
5. Click charts, categories, regions, or products to interactively cross-filter other visuals.
6. Review the KPI cards, trend charts, regional charts, and product table for insights.

## Project Structure

```text
sales-performance-dashboard/
│
├── README.md
├── Sales_Performance_Dashboard.pbix
├── data/
│   └── sales_data.csv
└── images/
    └── dashboard-preview.png
```

## Business Questions Answered

This dashboard can be used to answer the following questions:

- What is the total sales revenue?
- How many orders were placed?
- How many customers made purchases?
- Which month had the highest sales?
- Which region generated the most sales?
- Which product category performed best?
- Which products generated the highest sales?
- How does total order volume change by month?
- How does sales performance differ across years?

## Future Enhancements

- Add profit and profit-margin analysis.
- Add sales targets versus actual performance.
- Add month-over-month and year-over-year growth metrics.
- Add customer segmentation and customer lifetime value analysis.
- Add product and regional drill-through pages.
- Add forecasting for future sales.
- Connect the report to a live or cloud-based data source.

## Author

Created as a Power BI Sales Performance Dashboard project for data analytics and visualization practice.

## License

This project is intended for educational and portfolio purposes.
