# Date and Time Formulas – Planning and Tracking

---

## 1. DATEDIF
```
=DATEDIF(StartDate, EndDate, "d")
=DATEDIF(StartDate, EndDate, "m")
=DATEDIF(StartDate, EndDate, "y")
```

**Use case:**

Calculate project duration, age or employee tenure.

## 2. EOMONTH
```
=EOMONTH(TODAY(), 0)  // This month end
=EOMONTH(TODAY(), 1)  // Next month end
```

**Use case:**

Finds month-end dates for reporting.

## 3. WORKDAY / NETWORKDAYS
```
=WORKDAY(StartDate, 10)  // 10 workdays from start
=NETWORKDAYS(StartDate, EndDate)  // Workdays between dates
```

**Use case:**

Excludes weekends automatically.


## Practical Examples
```
// Age calculation
=DATEDIF(Birthdate, TODAY(), "y") & " years"

// Payment due date (15 days, skip weekends)
=WORKDAY(InvoiceDate, 15)

// Days until deadline
=NETWORKDAYS(TODAY(), DeadlineDate)

// Fiscal quarter
="Q" & ROUNDUP(MONTH(Date)/3, 0) & "-" & YEAR(Date)
```

**Tips:**

- Excel stores dates as numbers (1 = Jan 1, 1900)

- Use TODAY() for current date

- Use NOW() for current date + time

- Format cells as dates to display correctly
