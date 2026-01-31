# Lookup Formulas – Finding Data Efficiently

Lookup formulas are essential when working with large datasets,
reference tables, and system exports.

---

## 1. VLOOKUP (Classic Lookup)
```
=VLOOKUP(A2, Products!$A$2:$C$100, 3, FALSE)
```

**Use case:**

Find product price based on product ID.

**Explanation:**
- A2 → Lookup value
- Products!$A$2:$C$100 → Table range
- 3 → Column containing the result
- FALSE → Exact match only

## 2. XLOOKUP (Modern and Recommended)
```
=XLOOKUP(A2, EmployeeID, EmployeeName, "Not Found")
```

**Use case:**

Find employee name based on employee ID.

**Why XLOOKUP:**
- No column index numbers
- Works left-to-right and right-to-left
- Built-in default value handling

## 3. INDEX / MATCH (Flexible Alternative)
```
=INDEX(DepartmentNames, MATCH(A2, DepartmentIDs, 0))
```

**Use case:**

Lookup department name using department ID.

**Advantages:**
- More flexible than VLOOKUP

- Better performance on large datasets

- Supports multi-directional lookups

## Real Examples
```
// Two-dimensional lookup (row + column)
=INDEX(SalesData,
       MATCH("Product X", ItemList, 0),
       MATCH("Q4", QuarterHeaders, 0))

// Validate if a value exists in a list
=IF(ISNUMBER(MATCH(A2, ValidList, 0)), "Valid", "Invalid")
```

## Quick Comparison
| Task                 | Best Formula |
| -------------------- | ------------ |
| Simple lookup        | XLOOKUP      |
| Legacy files         | VLOOKUP      |
| Two-way lookup       | INDEX/MATCH  |
| Default value needed | XLOOKUP      |
