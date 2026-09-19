# Growth Display Measures

These DAX measures format year-over-year growth percentages into readable text indicators using upward and downward arrows. They improve KPI readability by displaying positive growth with an upward arrow and negative growth with a downward arrow.

---

## 1. Sales Growth Display

```DAX
Sales Growth Display =
VAR Growth =
    [Sales Growth %]
RETURN
    IF(
        Growth >= 0,
        "▲ " & FORMAT(Growth, "0.0%"),
        "▼ " & FORMAT(ABS(Growth), "0.0%")
    )
```

**Description:** Formats the sales growth percentage into a readable indicator with upward or downward arrows, enabling users to quickly identify changes in revenue performance.

---

## 2. Profit Growth Display

```DAX
Profit Growth Display =
VAR Growth =
    [Profit Growth %]
RETURN
    IF(
        Growth >= 0,
        "▲ " & FORMAT(Growth, "0.0%"),
        "▼ " & FORMAT(ABS(Growth), "0.0%")
    )
```

**Description:** Formats the profit growth percentage with directional arrows, helping users quickly interpret changes in operating profitability compared to the previous year.

---

## 3. Units Growth Display

```DAX
Units Growth Display =
VAR Growth =
    [Units Growth %]
RETURN
    IF(
        Growth >= 0,
        "▲ " & FORMAT(Growth, "0.0%"),
        "▼ " & FORMAT(ABS(Growth), "0.0%")
    )
```

**Description:** Formats the units growth percentage with directional arrows, making changes in sales volume easier to interpret in the dashboard.

---

## 4. Price Growth Display

```DAX
Price Growth Display =
VAR Growth =
    [Price Growth %]
RETURN
    IF(
        Growth >= 0,
        "▲ " & FORMAT(Growth, "0.0%"),
        "▼ " & FORMAT(ABS(Growth), "0.0%")
    )
```

**Description:** Formats the average price growth percentage with directional arrows, supporting the visual interpretation of year-over-year pricing changes.

---

## 5. Margin Growth Display

```DAX
Margin Growth Display =
VAR Growth =
    [Margin Growth %]
RETURN
    IF(
        Growth >= 0,
        "▲ " & FORMAT(Growth, "0.0%"),
        "▼ " & FORMAT(ABS(Growth), "0.0%")
    )
```
## 6. Conditional Formatting for KPI Display

The Growth Display measures use upward (▲) and downward (▼) arrows to represent positive and negative performance changes. Conditional formatting can be applied to the Callout Value and Insight Card visuals to improve KPI readability and highlight performance direction.

Conditional Formatting Logic
Green: Positive growth (Growth ≥ 0)
```
color = #16A34A
```
Red: Negative growth (Growth < 0)
```
color = #DC2626
```

**Description:** Formats the profit margin growth percentage with directional arrows, helping users identify changes in average operating margin compared to the previous year.

---

## Business Application

These display measures improve KPI readability by converting numerical growth percentages into intuitive visual indicators, allowing users to quickly interpret year-over-year performance changes across sales, profit, units, price, and margin.

