# Data Analysis Formulas – Summarize and Calculate

These formulas are used for reporting, KPIs, and operational monitoring.

---

## 1. SUMIFS – Conditional Summation
```
=SUMIFS(Sales, Region, "West", Month, "Jan", Amount, ">1000")
```

**Use case:**

Total sales for West region in January over $1000.

## 2. COUNTIFS – Conditional Counting
```
=COUNTIFS(Status, "Complete", Department, "Marketing", DueDate, "<"&TODAY())
```

**Use case:**

Count completed marketing tasks past their deadline.

## 3. AVERAGEIFS – Conditional Average
```
=AVERAGEIFS(Scores, Class, "Math", Grade, "A", Absences, "<=3")
```

**Use case:**

Average score of high-performing students with good attendance.

## Practical Scenarios
```
// Sales commission
=SUMIFS(Sales, Salesperson, A2, Product, "Premium") * 0.15

// Attendance rate
=COUNTIFS(Attendance, "Present") / COUNTA(Attendance)

// Inventory alert
=IF(SUMIFS(Stock, Item, A2) < Minimum, "Reorder", "OK")
```

**Tips:**

- Use named ranges for readability

- Combine multiple criteria safely
