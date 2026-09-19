# Calendar Table Measures

This document contains the DAX calculated table and calculated columns used to create the Calendar table. The table serves as the primary date dimension for enabling time intelligence calculations, filtering, and trend analysis across the report.

---

## 1. Calendar Table

```DAX
Calendar Table =
CALENDAR(
    DATE(2020, 1, 1),
    DATE(2021, 12, 31)
)
```

**Description:** Creates a continuous calendar table from **January 1, 2020** to **December 31, 2021**, providing a structured date dimension for time-based analysis.

---

## 2. Year

```DAX
Year =
YEAR('Calendar Table'[Date])
```

**Description:** Extracts the year from each date to support annual sales comparisons, filtering, and year-over-year performance analysis.

---

## 3. Year Month

```DAX
Year Month =
FORMAT('Calendar Table'[Date], "MMM YYYY")
```

**Description:** Combines the month and year into a readable format (e.g., **Jan 2021**) to support monthly reporting and trend analysis.

---

## 4. Quarter

```DAX
Quarter =
"Q" & FORMAT('Calendar Table'[Date], "Q")
```

**Description:** Identifies the quarter of each date (Q1, Q2, Q3, or Q4) to support quarterly sales analysis and seasonal performance evaluation.

---

## 5. Month

```DAX
Month =
MONTH('Calendar Table'[Date])
```

**Description:** Extracts the numeric month (1–12) to support chronological sorting, monthly filtering, and accurate sales comparisons.

---

## 6. Month Name

```DAX
Month Name =
FORMAT('Calendar Table'[Date], "MMM")
```

**Description:** Converts the date into an abbreviated month name (e.g., **Jan**, **Feb**, **Mar**) to improve dashboard readability and monthly trend reporting.

---

## 7. Day Name

```DAX
Day Name =
FORMAT('Calendar Table'[Date], "ddd")
```

**Description:** Extracts the abbreviated weekday name (e.g., **Mon**, **Tue**, **Wed**) to support weekday sales pattern analysis and reporting.

