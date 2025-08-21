
# **Lab Work 2.3.1 — VLOOKUP Function**

---

## 🔹 **Understanding VLOOKUP**

* **VLOOKUP** = *Vertical Lookup*
* Used to **search for a value in the first column** of a table and return related information from another column.

**Syntax:**

```excel
=VLOOKUP(lookup_value, table_array, col_index_num, [range_lookup])
```

* `lookup_value` → What you are searching for
* `table_array` → Table range
* `col_index_num` → Column number to return data from
* `[range_lookup]` → FALSE (Exact match) / TRUE (Approximate match)

---

## **Task 1 — Find Price of a Product**

**Sample Data**

| Product ID | Product Name | Price |
| ---------- | ------------ | ----- |
| P101       | Laptop       | 55000 |
| P102       | Phone        | 25000 |
| P103       | Tablet       | 18000 |

**Formula:**

```excel
=VLOOKUP("Phone", A2:C4, 3, FALSE)
```

👉 Result: `25000`

---

## **Task 2 — Retrieve Department of an Employee**

**Sample Data**

| Emp ID | Employee Name | Department |
| ------ | ------------- | ---------- |
| E01    | Rahul Sharma  | IT         |
| E02    | Meena Gupta   | HR         |
| E03    | Arjun Patel   | Sales      |

**Formula:**

```excel
=VLOOKUP("Meena Gupta", A2:C4, 3, FALSE)
```

👉 Result: `HR`

---

## **Task 3 — Find Student Grade**

**Sample Data**

| Marks | Grade |
| ----- | ----- |
| 0     | F     |
| 60    | D     |
| 70    | C     |
| 80    | B     |
| 90    | A     |

**Formula (for marks 85 in D2):**

```excel
=VLOOKUP(D2, A2:B6, 2, TRUE)
```

👉 Result: `B`

*(Here we used `TRUE` for approximate match since grade ranges are given.)*

---

## **Task 4 — Extract Customer Email**

**Sample Data**

| Customer ID | Name        | Email                                   |
| ----------- | ----------- | --------------------------------------- |
| C001        | Riya Singh  | [riya@mail.com](mailto:riya@mail.com)   |
| C002        | Karan Mehta | [karan@mail.com](mailto:karan@mail.com) |
| C003        | Neha Verma  | [neha@mail.com](mailto:neha@mail.com)   |

**Formula:**

```excel
=VLOOKUP("C002", A2:C4, 3, FALSE)
```

👉 Result: `karan@mail.com`

---

## **Task 5 — Get Supplier Name by Product ID**

**Sample Data**

| Product ID | Product Name | Supplier |
| ---------- | ------------ | -------- |
| P5001      | Keyboard     | Dell Ltd |
| P5002      | Mouse        | HP India |
| P5003      | Monitor      | Samsung  |

**Formula:**

```excel
=VLOOKUP("P5003", A2:C4, 3, FALSE)
```

👉 Result: `Samsung`

