
# 📘 Google Sheets Formulas & Basic Concepts — Lecture Documentation

This guide summarizes the **core formulas and concepts** we’ve learned so far, with explanations, uses, and examples.

---

## 🧾 1. Cell References

| Reference Type        | Example | Meaning                   | Behavior on Copy                        |
| --------------------- | ------- | ------------------------- | --------------------------------------- |
| **Relative**          | `A1`    | Refers to column A, row 1 | Changes when copied (e.g., `A1` → `A2`) |
| **Absolute**          | `$A$1`  | Locks column and row      | Always stays at `A1`                    |
| **Mixed (row fixed)** | `A$1`   | Column changes, row fixed | Copy → row remains 1                    |
| **Mixed (col fixed)** | `$A1`   | Column fixed, row changes | Copy → column stays A, row shifts       |

---

## 🧾 2. Basic Functions

| Formula           | Use                  | Example              | Result |
| ----------------- | -------------------- | -------------------- | ------ |
| `=SUM(A1:A5)`     | Adds numbers         | `=SUM(10,20,30)`     | **60** |
| `=AVERAGE(A1:A5)` | Finds mean           | `=AVERAGE(10,20,30)` | **20** |
| `=MIN(A1:A5)`     | Smallest value       | `=MIN(10,5,30)`      | **5**  |
| `=MAX(A1:A5)`     | Largest value        | `=MAX(10,5,30)`      | **30** |
| `=COUNT(A1:A5)`   | Counts numbers only  | `=COUNT(10,"x",20)`  | **2**  |
| `=COUNTA(A1:A5)`  | Counts all non-empty | `=COUNTA(10,"x","")` | **2**  |

---

## 🧾 3. Logical Functions

| Formula                                         | Use                           | Example                     | Result                |
| ----------------------------------------------- | ----------------------------- | --------------------------- | --------------------- |
| `=IF(condition, value_if_true, value_if_false)` | Returns based on condition    | `=IF(A1>=50,"Pass","Fail")` | If `A1=60` → **Pass** |
| `=AND(condition1, condition2)`                  | Checks if all conditions true | `=AND(A1>10,B1<5)`          | **TRUE** if both true |
| `=OR(condition1, condition2)`                   | Checks if any condition true  | `=OR(A1>10,B1<5)`           | **TRUE** if any true  |
| `=IF(AND(A1>10,B1<5),"Yes","No")`               | IF with AND                   | If both true → "Yes"        |                       |
| `=IF(OR(A1>10,B1<5),"Yes","No")`                | IF with OR                    | If any true → "Yes"         |                       |

---

## 🧾 4. Error Handling

| Formula                                         | Use                | Example                      | Result |
| ----------------------------------------------- | ------------------ | ---------------------------- | ------ |
| `=IFERROR(A1/B1,"Invalid")`                     | Replaces error     | If `5/0` → **Invalid**       |        |
| `=ISERROR(A1)`                                  | Checks if error    | If `#DIV/0!` → **TRUE**      |        |
| `=ERROR.TYPE(A1)`                               | Returns error code | If `#DIV/0!` → **2**         |        |
| `=IFNA(VLOOKUP("X",A1:B5,2,FALSE),"Not Found")` | Handles #N/A       | If not found → **Not Found** |        |

---

## 🧾 5. Text & Validation Functions

| Formula             | Use                  | Example                  | Result                  |
| ------------------- | -------------------- | ------------------------ | ----------------------- |
| `=LEN(A1)`          | Length of text       | `=LEN("Google")`         | **6**                   |
| `=PROPER(A1)`       | Capitalize each word | `=PROPER("hello world")` | **Hello World**         |
| `=LOWER(A1)`        | Convert to lowercase | `"HELLO"` → **hello**    |                         |
| `=UPPER(A1)`        | Convert to uppercase | `"hello"` → **HELLO**    |                         |
| **Data Validation** | Restrict inputs      | Numeric between 1–100    | Blocks invalid entry    |
| **Unique Values**   | Validation → Custom  | Ensure no duplicates     | Prevents repeated input |

---

## 🧾 6. Counting & Summing with Conditions

| Formula                                               | Use                              | Example                  | Result |
| ----------------------------------------------------- | -------------------------------- | ------------------------ | ------ |
| `=COUNTIF(A1:A10,">=30")`                             | Count with 1 condition           | Count ages ≥30           |        |
| `=COUNTIFS(A1:A10,">=30",B1:B10,"Male")`              | Count with multiple conditions   | Count Male ≥30           |        |
| `=SUMIF(A1:A10,">=50",B1:B10)`                        | Sum values meeting criteria      | Sum marks ≥50            |        |
| `=SUMIFS(C1:C10,A1:A10,"East",B1:B10,"Approved")`     | Sum with multiple conditions     | Sales from East Approved |        |
| `=AVERAGEIF(A1:A10,">=50",B1:B10)`                    | Average with one condition       | Avg marks ≥50            |        |
| `=AVERAGEIFS(C1:C10,A1:A10,"East",B1:B10,"Approved")` | Average with multiple conditions | Avg sales East Approved  |        |

---

## 🧾 7. Conditional Formatting

| Task                       | Rule                                       | Example              |
| -------------------------- | ------------------------------------------ | -------------------- |
| Highlight numbers >5000    | Custom rule                                | `=A1>5000`           |
| Highlight duplicates       | Built-in → Format rules → “Custom formula” | `=COUNTIF(A:A,A1)>1` |
| Highlight cells with “Bad” | `=A1="Bad"`                                | Colors bad feedback  |

---

## 🧾 8. Named Ranges

| Named Range        | Use                                              | Example                      |
| ------------------ | ------------------------------------------------ | ---------------------------- |
| `AllExpenses`      | Select full Expense column → Data → Named ranges | Use `=SUM(AllExpenses)`      |
| `ApprovedExpenses` | Filter Approved rows only                        | Use `=SUM(ApprovedExpenses)` |
| `ProductNames`     | Name product list                                | Use in validation dropdown   |

---

# 🎯 Summary

* **Absolute (`$A$1`) vs Relative (`A1`)** references decide formula behavior when copied.
* **Basic functions** (SUM, AVERAGE, COUNT, MIN, MAX) build foundation.
* **Logical functions** (IF, AND, OR, Nested IF) add decision-making.
* **Error functions** (IFERROR, ISERROR, IFNA) make sheets more user-friendly.
* **Conditional counting (COUNTIF/IFS)** and **summing (SUMIF/IFS)** handle multiple conditions.
* **Conditional formatting + Named ranges** improve visualization and usability.
