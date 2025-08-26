
# **Lab Work 2.4.1 — INDEX + MATCH Functions**

---

## 🔹 **Understanding INDEX + MATCH**

* **INDEX** → Returns the value from a specific row & column of a given range.
* **MATCH** → Returns the *position* of a value in a row/column.
* Together → More powerful alternative to **VLOOKUP/HLOOKUP** since they:

  * Work both *horizontally & vertically*.
  * Don’t require the lookup value to be in the first column/row.

**Syntax:**

```excel
=INDEX(array, row_num, [column_num])
=MATCH(lookup_value, lookup_array, [match_type])
```

👉 Combined Formula:

```excel
=INDEX(return_range, MATCH(lookup_value, lookup_range, 0))
```

---

## **Task 1 — Find Salary of an Employee by ID**

**Sample Data**

| Emp ID | 101 | 102 | 103 | 104 |
| ------ | --- | --- | --- | --- |
| Salary | 30K | 40K | 35K | 50K |

**Formula (for Emp ID 103):**

```excel
=INDEX(B2:E2, MATCH(103, B1:E1, 0))
```

👉 Result: `35K`

---

## **Task 2 — Retrieve Customer City**

**Sample Data**

| Cust ID | C001  | C002   | C003 | C004    |
| ------- | ----- | ------ | ---- | ------- |
| City    | Delhi | Mumbai | Pune | Chennai |

**Formula (for Cust ID C003):**

```excel
=INDEX(B2:E2, MATCH("C003", B1:E1, 0))
```

👉 Result: `Pune`

---

## **Task 3 — Find Sales Amount for Salesperson**

**Sample Data**

| Salesperson | John | Mary | Alex | Sara |
| ----------- | ---- | ---- | ---- | ---- |
| Sales (\$)  | 5000 | 7000 | 6500 | 8000 |

**Formula (for Alex):**

```excel
=INDEX(B2:E2, MATCH("Alex", B1:E1, 0))
```

👉 Result: `6500`

---

## **Task 4 — Lookup Stock Quantity of Product**

**Sample Data**

| Product  | Laptop | Phone | Tablet | TV |
| -------- | ------ | ----- | ------ | -- |
| Quantity | 20     | 50    | 35     | 15 |

**Formula (for Phone):**

```excel
=INDEX(B2:E2, MATCH("Phone", B1:E1, 0))
```

👉 Result: `50`

---

## **Task 5 — Extract Student Name by Roll Number**

**Sample Data**

| Roll No | 1   | 2    | 3    | 4     |
| ------- | --- | ---- | ---- | ----- |
| Name    | Raj | Neha | Amit | Priya |

**Formula (for Roll No 4):**

```excel
=INDEX(B2:E2, MATCH(4, B1:E1, 0))
```

👉 Result: `Priya`

---

⚡ With **INDEX + MATCH**, you can perform *flexible lookups* without the limitations of VLOOKUP/HLOOKUP.
