# Text Formulas – Cleaning and Formatting Data
Essential for cleaning imported or user-entered data.

---

## 1. TEXTSPLIT
```
=TEXTSPLIT(A2, ",")
```

**Use case:**

Splits structured text into columns automatically.

## 2. CONCAT / TEXTJOIN
```
=TEXTJOIN(" ", TRUE, FirstName, LastName)
```

**Use case:**

Safely combines text while ignoring empty cells.

## 3. TRIM / CLEAN
```
=TRIM(CLEAN(A2))
```

**Use case:**

Removes extra spaces and non-printable characters.

## Real Use Cases
```
// Generate email address
=LOWER(CONCAT(A2, ".", B2, "@company.com"))

// Extract domain
=TEXTAFTER(Email, "@")

// Standardize phone format
=TEXT(PhoneNumber, "(###) ###-####")

// Find and replace specific text
=SUBSTITUTE(A2, "old text", "new text")

// Create IDs
=CONCAT("EMP-", TEXT(ROW(), "0000"))

// Extract text between markers
=TEXTBEFORE(TEXTAFTER(A2, "["), "]")
```
