# Logical Formulas – Decision Making in Excel

These formulas are used for reporting, KPIs, and operational monitoring.

---

## IF
```
=IF(Score >= 70, "Pass", "Fail")
```

## IFS
```
=IFS(
    Score>=90,"A",
    Score>=80,"B",
    Score>=70,"C",
    TRUE,"F"
)
```

## SWITCH
```
=SWITCH(Code,
    "A","Active",
    "I","Inactive",
    "P","Pending",
    "Unknown"
)
```

## FILTER
```
=FILTER(Data, (Department="Sales")*(Region="East"))
```

**Use case:**

Creates dynamic reports without PivotTables.


## Examples:
```
// Nested IF for complex logic
=IF(AND(Score>=70, Attendance>=80%), "Pass", "Review")

// Calculate bonus with IFS
=IFS(
    Sales > 100000, Sales*0.1,
    Sales > 50000, Sales*0.05,
    TRUE, 0
)

// Priority based on multiple factors
=SWITCH(TRUE,
    AND(Urgent, Impact="High"), 1,
    Impact="High", 2,
    Urgent, 3,
    4
)
```
