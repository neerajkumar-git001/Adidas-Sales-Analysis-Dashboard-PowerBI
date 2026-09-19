# Growth Analysis Measures

This document contains the DAX measures used to calculate year-over-year growth in sales, profit, units sold, average price, and profit margin. These measures help evaluate changes in business performance compared to the previous year.

---

## 1. Sales Growth %

```DAX
Sales Growth % =
VAR CurrentSales =
    [Total Sales]
VAR PreviousSales =
    CALCULATE(
        [Total Sales],
        DATEADD(
            'Calendar Table'[Date],
            -1,
            YEAR
        )
    )
RETURN
    DIVIDE(
        CurrentSales - PreviousSales,
        PreviousSales,
        0
    )
```

**Description:** Calculates the percentage change in total sales compared to the previous year, helping businesses evaluate revenue growth and identify changes in sales performance.

---

## 2. Profit Growth %

```DAX
Profit Growth % =
VAR CurrentProfit =
    [Total Profit]
VAR PreviousProfit =
    CALCULATE(
        [Total Profit],
        DATEADD(
            'Calendar Table'[Date],
            -1,
            YEAR
        )
    )
RETURN
    DIVIDE(
        CurrentProfit - PreviousProfit,
        PreviousProfit,
        0
    )
```

**Description:** Calculates the percentage change in total operating profit compared to the previous year, supporting profitability trend analysis and evaluation of business financial performance.

---

## 3. Units Growth %

```DAX
Units Growth % =
VAR CurrentUnits =
    [Total Units Sold]
VAR PreviousUnits =
    CALCULATE(
        [Total Units Sold],
        DATEADD(
            'Calendar Table'[Date],
            -1,
            YEAR
        )
    )
RETURN
    DIVIDE(
        CurrentUnits - PreviousUnits,
        PreviousUnits,
        0
    )
```

**Description:** Calculates the percentage change in total units sold compared to the previous year, helping businesses evaluate sales volume growth and changes in product demand.

---

## 4. Price Growth %

```DAX
Price Growth % =
VAR CurrentPrice =
    [Avg. Price Per Unit]
VAR PreviousPrice =
    CALCULATE(
        [Avg. Price Per Unit],
        DATEADD(
            'Calendar Table'[Date],
            -1,
            YEAR
        )
    )
RETURN
    DIVIDE(
        CurrentPrice - PreviousPrice,
        PreviousPrice,
        0
    )
```

**Description:** Calculates the percentage change in average price per unit compared to the previous year, supporting pricing trend analysis and evaluation of changes in average selling prices.

---

## 5. Margin Growth %

```DAX
Margin Growth % =
VAR CurrentMargin =
    [Avg. Profit Margine]
VAR PreviousMargin =
    CALCULATE(
        [Avg. Profit Margine],
        DATEADD(
            'Calendar Table'[Date],
            -1,
            YEAR
        )
    )
RETURN
    DIVIDE(
        CurrentMargin - PreviousMargin,
        PreviousMargin,
        0
    )
```

**Description:** Calculates the percentage change in average operating margin compared to the previous year, helping businesses evaluate changes in average profitability levels.

---

## Business Application

These growth measures enable year-over-year performance comparisons across key business metrics, supporting the analysis of revenue trends, profitability, sales volume, pricing, and operating margins.
