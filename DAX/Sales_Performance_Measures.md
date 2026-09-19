# Sales Performance Measures

This document contains the DAX measures used to calculate key sales, profitability, and pricing KPIs for the Adidas Sales Analysis Dashboard. These measures support business performance evaluation and decision-making.

---

## 1. Total Sales

```DAX
Total Sales =
SUMX(
    'Data Sales Adidas',
    'Data Sales Adidas'[Price per Unit] *
    'Data Sales Adidas'[Units Sold]
)
```

**Description:** Calculates total sales revenue by multiplying the price per unit by the number of units sold for each transaction and summing the results.

---

## 2. Total Profit

```DAX
Total Profit =
SUM('Data Sales Adidas'[Operating Profit])
```

**Description:** Calculates the total operating profit generated across all sales transactions to evaluate the overall profitability of the business.

---

## 3. Total Units Sold

```DAX
Total Units Sold =
SUM('Data Sales Adidas'[Units Sold])
```

**Description:** Calculates the total number of units sold across all transactions to measure sales volume and product demand.

---

## 4. Average Price Per Unit

```DAX
Avg. Price Per Unit =
AVERAGE('Data Sales Adidas'[Price per Unit])
```

**Description:** Calculates the average selling price per unit across all sales records to understand pricing levels and support product pricing analysis.

---

## 5. Average Profit Margin

```DAX
Avg. Profit Margine =
AVERAGE('Data Sales Adidas'[Operating Margin])
```

**Description:** Calculates the arithmetic average of operating margins across sales records to evaluate the average profitability percentage of individual records.

## 6. Previous Year Sales

```DAX
PreviousYearSales =
CALCULATE(
    [Total Sales],
    DATEADD(
        'Calendar Table'[Date],
        -1,
        YEAR
    )
)
```

**Description:** Calculates total sales for the corresponding period in the previous year using the DATEADD function, enabling year-over-year sales comparisons and performance evaluation.

---

## 7. Previous Year Profit

```DAX
PreviousYearProfit =
CALCULATE(
    [Total Profit],
    DATEADD(
        'Calendar Table'[Date],
        -1,
        YEAR
    )
)
```

**Description:** Calculates total operating profit for the corresponding period in the previous year, supporting year-over-year profitability analysis and evaluation of business performance changes.
