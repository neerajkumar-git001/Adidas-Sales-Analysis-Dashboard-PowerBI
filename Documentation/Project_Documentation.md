# Adidas Sales Analysis Dashboard

![Power BI](https://img.shields.io/badge/Tool-Power%20BI-yellow)
![Power Query](https://img.shields.io/badge/Tool-Power%20Query-blue)
![DAX](https://img.shields.io/badge/Language-DAX-orange)
![Status](https://img.shields.io/badge/Project-Completed-success)

---

## 1. Project Overview

The **Adidas Sales Analysis Dashboard** is an interactive Business
Intelligence project developed using Microsoft Power BI.

The project analyzes Adidas sales performance across products,
regions, states, retailers, sales methods, and time.

The main objective is to transform raw sales data into meaningful
business insights that support data-driven decision-making.

This project demonstrates practical knowledge of:

- Data cleaning and transformation
- Power Query
- DAX calculations
- KPI development
- Time intelligence
- Business analysis
- Interactive dashboard development
- Data storytelling

---


## Dashboard Preview

The following screenshot presents the Adidas Sales Analysis
Dashboard developed in Microsoft Power BI.

The dashboard provides a business-focused overview of:

- Total Sales
- Operating Profit
- Units Sold
- Average Price
- Profit Margin
- Product Performance
- Regional Performance
- Retailer Performance
- Sales Method Analysis
- Business Growth Trends

### Dashboard 

![Adidas Sales Analysis Dashboard](../KPIs%20Image/Adidas_Sales_Analysis_Dashboard_Preview.png)

### Dashboard Purpose

This dashboard helps stakeholders evaluate sales performance,
identify profitable products and regions, compare retailer
contributions, and understand business growth trends.

Interactive filters allow users to analyze performance
across different products, regions, retailers, and sales methods.

--- 
## 3. Business Problem

Adidas sales data contains information about products, retailers,
locations, pricing, units sold, operating profit, operating margin,
and sales methods.

Analyzing this information manually can make it difficult to identify:

- Sales trends
- Profitable products
- High-performing regions
- Retailer performance
- Sales method performance
- Year-over-year growth

This dashboard provides an interactive solution for analyzing
sales performance and identifying business opportunities.

### Business Questions

1. What is the total sales revenue?
2. What is the total operating profit?
3. Which products generate the highest sales?
4. Which regions perform strongly?
5. Which states contribute most to sales?
6. Which retailers contribute most to revenue?
7. Which sales methods are most effective?
8. How are sales and profit changing over time?
9. How does the current year compare with the previous year?
10. Which areas require further business analysis?

---

## 4. Project Objectives

The main objectives of this project are:

- Develop an interactive Power BI dashboard.
- Track important sales and profitability KPIs.
- Analyze product-level performance.
- Analyze regional and state-level performance.
- Compare retailer performance.
- Analyze sales method performance.
- Implement a calendar table for time intelligence.
- Calculate previous-year performance.
- Calculate KPI growth percentages.
- Create business-focused insight cards.
- Support data-driven business decisions.

---

## 5. Dataset Information

### Dataset Name

Adidas US Sales Dataset

### Dataset Period

January 2020 to December 2021

### Dataset Size

- Total records: Approximately 9,653
- Usable records: Approximately 9,648
- Number of columns: 12

### Dataset Columns

| Column | Description |
|---|---|
| Retailer | Name of the retailer |
| Retailer ID | Unique retailer identifier |
| Invoice Date | Date of the transaction |
| Region | Sales region |
| State | State where the sale occurred |
| City | City where the sale occurred |
| Product | Product category |
| Price per Unit | Selling price per unit |
| Units Sold | Number of products sold |
| Operating Profit | Profit generated from sales |
| Operating Margin | Operating margin percentage |
| Sales Method | Method used to complete the sale |

### Total Sales Calculation

The dataset does not contain a separate Total Sales column.

Total Sales is calculated using:

```text
Total Sales = Price per Unit × Units Sold
```

This calculation is implemented using DAX in Power BI.

---

##  6. Tools and Technologies

| Tool | Purpose | Reference |
|---|---|---|
| Microsoft Power BI | Dashboard development and visualization | [Power BI Documentation](https://learn.microsoft.com/en-us/power-bi/) |
| Power Query | Data cleaning and transformation | [Power Query Documentation](https://learn.microsoft.com/en-us/power-query/) |
| DAX | KPI and analytical calculations | [DAX Documentation](https://learn.microsoft.com/en-us/dax/) |
| Microsoft Excel | Dataset review and preparation | [Excel Documentation](https://support.microsoft.com/en-us/excel) |
| GitHub | Version control and project publishing | [GitHub Documentation](https://docs.github.com/en) |

---

## 7. Data Cleaning and Transformation

The dataset was reviewed and prepared before dashboard development.

### Data Cleaning Activities

- Reviewed column names.
- Checked data types.
- Verified invoice date formatting.
- Checked numerical columns.
- Reviewed blank values.
- Checked invalid records.
- Reviewed duplicate or unusable records.
- Standardized categorical values.
- Prepared the dataset for Power BI analysis.

### Power Query Process

The following process was used:

1. Imported the dataset into Power Query.
2. Reviewed the dataset structure.
3. Checked and corrected data types.
4. Verified the invoice date column.
5. Reviewed missing and invalid values.
6. Checked numerical columns.
7. Validated categorical fields.
8. Loaded the prepared data into Power BI.

### Data Validation

The dataset was reviewed to identify usable records before
developing the dashboard.

Approximately 9,648 usable records were used for analysis.

---

## 8. Data Model

The Adidas sales table is used as the primary fact table.

A separate calendar table is used to support time-based analysis.

### Calendar Table Columns

- Date
- Year
- Year-Month
- Quarter
- Month
- Month Name
- Day Name

### Calendar Table Purpose

The calendar table supports:

- Monthly trend analysis
- Previous-year calculations
- Year-over-year comparisons
- Sales growth analysis
- Profit growth analysis
- Units growth analysis
- Price comparisons
- Margin comparisons

### Data Model Relationship

The calendar table is connected to the sales table through
the relevant date column.

The relationship allows DAX time intelligence functions to
calculate previous-year and growth measures.

---

## 9. Key Performance Indicators

The dashboard contains the following KPIs:

| KPI | Description |
|---|---|
| Total Sales | Total revenue calculated from price per unit multiplied by units sold |
| Total Profit | Total operating profit |
| Total Units Sold | Total quantity of products sold |
| Average Price per Unit | Average selling price per unit |
| Average Profit Margin | Average operating margin |

### Overall KPI Summary

| Metric | Approximately Value |
|---|---:|
| Total Sales | $899.90M |
| Total Operating Profit |  $332.13M |
| Total Units Sold |  17.89M |
| Average Price per Unit |  $45.22 |
| Weighted Profit Margin |  36.91% |

**Note:** KPI values may vary depending on filters, data preparation,
and calculation methods.

---

## 10. DAX Measures Documentation

The DAX measures are organized into separate files.

### DAX Documentation Files

- [Calendar Table Measures](../DAX/Calendar_table_Measures.md)
- [Sales Performance Measures](../DAX/Sales_Performance_Measures.md)
- [Growth Analysis Measures](../DAX/Growth_Analysis_Measures.md)
- [Growth Display Measures](../DAX/Growth_Display_Measures.md)

---

## 11. Calendar Table Measures

The calendar table is used for time intelligence and date-based
analysis.

### Main Functions

- Create a continuous date range.
- Extract year information.
- Create year-month values.
- Extract quarter information.
- Extract month information.
- Extract month names.
- Extract day names.

Detailed documentation:

[View Calendar Table Measures](../DAX/Calendar_table_Measures.md)

---

## 12. Sales Performance Measures

Sales performance measures calculate the primary KPIs used
in the dashboard.

### Main Measures

- Total Sales
- Total Profit
- Total Units Sold
- Average Price per Unit
- Average Profit Margin

Detailed documentation:

[View Sales Performance Measures](../DAX/Sales_Performance_Measures.md)

---

## 13. Previous-Year Analysis

Previous-year measures are used to compare current performance
with the corresponding period in the previous year.

### Previous-Year Measures

- Previous Year Sales
- Previous Year Profit

These measures use DAX time intelligence functions to retrieve
historical values.

Detailed documentation:

[View Growth Analysis Measures](../DAX/Growth_Analysis_Measures.md)

---

## 14. Growth Analysis

The dashboard calculates growth for the following KPIs:

- Sales Growth Percentage
- Profit Growth Percentage
- Units Growth Percentage
- Price Growth Percentage
- Margin Growth Percentage

### General Growth Formula

```text
Growth % =
(Current Value - Previous Value) / Previous Value
```

Growth analysis helps identify whether a KPI has increased
or decreased compared with the previous year.

### Growth Indicators

- ▲ represents positive growth.
- ▼ represents negative growth.

Detailed documentation:

[View Growth Analysis Measures](../DAX/Growth_Analysis_Measures.md)

---

## 15. Growth Display Measures

Growth display measures format the calculated growth values
for dashboard presentation.

### Display Features

- Positive growth is displayed using an upward indicator.
- Negative growth is displayed using a downward indicator.
- Growth values are formatted as percentages.
- Absolute values are used for negative display formatting.

Detailed documentation:

[View Growth Display Measures](../DAX/Growth_Display_Measures.md)

---

## 16. Dashboard Features

The dashboard provides an interactive overview of Adidas
sales performance.

### KPI Cards

The dashboard includes KPI cards for:

- Total Sales
- Total Profit
- Total Units Sold
- Average Price per Unit
- Average Profit Margin

### Analytical Visuals

The dashboard includes:

- Monthly sales trend analysis
- Product performance analysis
- Regional sales analysis
- State-level sales analysis
- Retailer performance analysis
- Sales method analysis
- Growth indicators
- Business insight cards

### Interactive Features

- Slicers
- Cross-filtering
- Dynamic KPI updates
- Year selection
- Product selection
- Region selection
- Retailer selection
- Sales method selection

---

## 17. Dashboard Filters

The dashboard provides filters for:

- Year
- Region
- State
- City
- Product
- Retailer
- Sales Method

These filters allow users to analyze specific segments of
the business.

For example, users can select a specific year and region
to analyze the sales performance of that segment.

---

## 18. Conditional Formatting

Conditional formatting is used to highlight KPI growth performance.

### Formatting Logic

| Condition | Color | Hex |
|---|---|---|
| Positive growth | Green | #16A34A |
| Negative growth | Red | #DC2626 |

### Business Purpose

Conditional formatting helps users quickly identify:

- Improving KPIs
- Declining KPIs
- Positive performance
- Negative performance
- Areas requiring additional analysis

The color formatting is applied to growth values and
business insight cards where appropriate.

---

## 19. Dashboard Visual Explanation

### KPI Cards

KPI cards provide a high-level overview of business performance.

They help users quickly understand:

- Total revenue
- Total profit
- Total units sold
- Average selling price
- Average operating margin

### Sales Trend Visual

The sales trend visual displays sales performance over time.

It helps identify:

- Monthly sales patterns
- Seasonal changes
- Increases in sales
- Decreases in sales
- Changes in overall performance

### Product Analysis Visual

The product analysis visual compares sales performance
across different product categories.

It helps identify products that contribute significantly
to overall sales.

### Regional Analysis Visual

The regional analysis visual compares performance across
different regions.

It supports geographic performance analysis and helps
identify high-performing and lower-performing regions.

### Retailer Analysis Visual

The retailer visual compares sales performance across
different retailers.

It helps identify retailers that contribute significantly
to overall revenue.

### Sales Method Visual

The sales method visual compares performance across
different sales channels.

It supports analysis of customer purchasing behavior
and channel contribution.

---

## 20. Business Insights

### Regional Performance

The West region was identified as a leading contributor
to sales in the analyzed dataset.

Regional analysis helps identify geographic demand
and performance differences.

### Product Performance

Men's Street Footwear was identified as a leading
product category by sales.

Product analysis can support inventory planning,
marketing allocation, and product strategy.

### Sales Method Performance

The In-store sales method was identified as a major
contributor to sales.

Sales method analysis helps understand customer
purchasing behavior and channel performance.

### Retailer and Location Analysis

Retailer, state, and city-level analysis helps identify
high-performing markets and locations.

These insights can support regional planning and
retailer management.

### Time-Based Performance

Monthly sales and profit trends help identify
performance changes over time.

Year-over-year analysis provides additional context
for understanding growth and decline.

---

## 21. Business Recommendations

Based on the dashboard analysis, the following actions
can be considered:

- Review high-performing product categories.
- Evaluate product availability in strong markets.
- Analyze leading regions to understand sales drivers.
- Investigate lower-performing regions.
- Compare different sales methods.
- Monitor profit margins along with revenue.
- Review monthly sales trends.
- Track year-over-year growth.
- Analyze retailer performance.
- Use sales insights to support inventory planning.

These recommendations are analytical suggestions based on
the available dataset.

They should be validated using additional business and
operational information before implementation.

---

## 22. Project Limitations

- The dataset covers only the period from 2020 to 2021.
- The analysis is limited to the available dataset columns.
- Customer-level information is not available.
- Marketing expenditure data is not included.
- Inventory data is not included.
- Returns and discounts are not included.
- Logistics costs are not included.
- The dashboard does not establish the cause of sales changes.
- Recommendations require additional business validation.
- Historical data may not represent current business conditions.

---

## 23. Future Improvements

Possible future improvements include:

- Customer segmentation.
- Inventory and stock availability analysis.
- Discount and return analysis.
- Integration of recent sales data.
- Automated data refresh.
- Sales forecasting.
- Marketing campaign analysis.
- Retailer scorecards.
- Territory-level performance analysis.
- Advanced business intelligence reporting.

---

## 24. Project Resources

### Dataset

[Adidas US Sales Dataset](../Dataset/Adidas%20US%20Sales_Datasets.xlsx)

### DAX Documentation

- [Calendar Table Measures](../DAX/Calendar_table_Measures.md)
- [Sales Performance Measures](../DAX/Sales_Performance_Measures.md)
- [Growth Analysis Measures](../DAX/Growth_Analysis_Measures.md)
- [Growth Display Measures](../DAX/Growth_Display_Measures.md)

### Project Documentation

[Project Documentation](./Project_Documentation.md)

### Project README

[README File](../README.md)

### KPI Images

[KPI Images Folder](../KPIs%20Image/)

---

## 25. External References

The following official resources can be used to understand
the tools and concepts applied in this project.

- [Power BI Documentation](https://learn.microsoft.com/en-us/power-bi/)
- [Power Query Documentation](https://learn.microsoft.com/en-us/power-query/)
- [DAX Overview](https://learn.microsoft.com/en-us/dax/dax-overview)
- [DAX Function Reference](https://learn.microsoft.com/en-us/dax/)
- [Power BI Data Modeling](https://learn.microsoft.com/en-us/power-bi/transform-model/)
- [Microsoft Learn](https://learn.microsoft.com/)
- [GitHub Documentation](https://docs.github.com/en)

---

## 26. GitHub Repository Structure

```text
Adidas-Sales-Analysis-Dashboard/
│
├── README.md
│
├── DAX/
│   ├── Calendar_table_Measures.md
│   ├── Growth_Analysis_Measures.md
│   ├── Growth_Display_Measures.md
│   └── Sales_Performance_Measures.md
│
├── Dataset/
│   └── Adidas US Sales_Datasets.xlsx
│
├── Documentation/
│   └── Project_Documentation.md
│
├── KPIs Image/
│   └── KPI Images
│
└── Dashboard Files
```

---

## 27. Project Outcome

This project demonstrates practical knowledge of:

- Data cleaning and transformation
- Power Query
- Power BI dashboard development
- DAX calculations
- KPI development
- Time intelligence
- Growth analysis
- Interactive reporting
- Business insight generation
- Decision-support reporting

The project transforms raw sales data into an interactive
dashboard that supports structured business analysis.

---

## 28. Conclusion

The Adidas Sales Analysis Dashboard provides a consolidated
view of sales, profit, units sold, pricing, margin, products,
regions, retailers, and sales methods.

By combining Power Query, Power BI, and DAX, the project
demonstrates how raw business data can be transformed into
meaningful insights for business analysis and decision-making.

The project also demonstrates the practical application of
Business Intelligence concepts in a sales analytics environment.

---

## Author

**Neeraj Kumar Sahu**

B.Tech Data Science

Interested in Data Analytics, Business Intelligence,
Power BI, and AI-powered analytics.

---
