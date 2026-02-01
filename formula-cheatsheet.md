# Excel Formula Quick Reference
A compact reference for commonly used Excel formulas
in reporting, validation, and operational spreadsheets.

## 🔍 Lookup & Reference
```
XLOOKUP(lookup, range, return, [not_found]) // Find anything
VLOOKUP(value, table, col, FALSE) // Classic lookup
INDEX(range, MATCH(value, range, 0)) // Two-way lookup
```
## 📊 Data Analysis
```
SUMIFS(sum_range, criteria_range1, criteria1, ...) // Sum with conditions
COUNTIFS(range1, criteria1, range2, criteria2) // Count with conditions
AVERAGEIFS(avg_range, criteria_range1, criteria1) // Average with conditions
```
## 🔤 Text Manipulation
```
TEXTJOIN(delimiter, ignore_empty, text1, ...) // Combine text
TEXTSPLIT(text, delimiter) // Split text
TRIM(text) // Remove extra spaces
TEXT(value, format) // Format as text
```
## 📅 Date & Time
```
DATEDIF(start, end, "d/m/y") // Date difference
EOMONTH(date, months) // End of month
WORKDAY(start, days) // Workdays from date
NETWORKDAYS(start, end) // Workdays between
TODAY() // Current date
NOW() // Current date/time
```

## ⚡ Logical
```
IF(condition, true, false) // Simple condition
IFS(condition1, result1, condition2, result2) // Multiple conditions
SWITCH(value, val1, result1, val2, result2) // Value matching
FILTER(array, include) // Filter data
AND(logical1, logical2) // Both must be true
OR(logical1, logical2) // Either can be true
```
## 💡 Pro Tips:
```
1. **F4 Key:** Toggle absolute/relative references ($A$1 → A$1 → $A1 → A1)
2. **F2 Key:** Edit formula in cell
3. **Ctrl+Shift+Enter:** Array formulas (if needed)
4. **Named Ranges:** Use for clarity
5. **Error Checking:** Click the green triangle

## Common Errors & Fixes:
- `#N/A`: Value not found → Use `IFERROR(formula, "alternative")`
- `#DIV/0`: Dividing by zero → `IF(denominator=0, 0, numerator/denominator)`
- `#VALUE`: Wrong data type → Check cell formats
- `#REF`: Broken reference → Update range references
```

