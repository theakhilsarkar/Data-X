

# **Lab Work 2.3.2 — HLOOKUP Function**

---

## 🔹 **Understanding HLOOKUP**

* **HLOOKUP** = *Horizontal Lookup*
* Used to **search for a value in the first row** of a table and return related information from another row.

**Syntax:**

```excel
=HLOOKUP(lookup_value, table_array, row_index_num, [range_lookup])
```

* `lookup_value` → What you are searching for
* `table_array` → Table range
* `row_index_num` → Row number to return data from
* `[range_lookup]` → FALSE (Exact match) / TRUE (Approximate match)

---

## **Task 1 — Find Sales Figures for a Specific Month**

**Sample Data**

|       | Jan  | Feb  | Mar  | Apr  |
| ----- | ---- | ---- | ---- | ---- |
| Sales | 5000 | 7000 | 6500 | 8000 |

**Formula (for March sales):**

```excel
=HLOOKUP("Mar", A1:E2, 2, FALSE)
```

👉 Result: `6500`

---

## **Task 2 — Retrieve Tax Rate for an Income Bracket**

**Sample Data**

| Income Bracket | 0-2L | 2-5L | 5-10L | 10L+ |
| -------------- | ---- | ---- | ----- | ---- |
| Tax Rate       | 0%   | 5%   | 20%   | 30%  |

**Formula (for 5-10L bracket):**

```excel
=HLOOKUP("5-10L", A1:E2, 2, FALSE)
```

👉 Result: `20%`

---

## **Task 3 — Find Discount Percentage for Product Category**

**Sample Data**

| Category   | Electronics | Clothing | Furniture | Grocery |
| ---------- | ----------- | -------- | --------- | ------- |
| Discount % | 10%         | 20%      | 15%       | 5%      |

**Formula (for Furniture):**

```excel
=HLOOKUP("Furniture", A1:E2, 2, FALSE)
```

👉 Result: `15%`

---

## **Task 4 — Extract Currency Exchange Rates**

**Sample Data**

| Country | USA | UK  | Japan | India |
| ------- | --- | --- | ----- | ----- |
| Rate    | 1.0 | 0.8 | 110   | 74    |

**Formula (for India):**

```excel
=HLOOKUP("India", A1:E2, 2, FALSE)
```

👉 Result: `74`

---

## **Task 5 — Find Passing Percentage from Horizontal Scale**

**Sample Data**

| Exam      | Math | Science | English | History |
| --------- | ---- | ------- | ------- | ------- |
| Passing % | 35   | 40      | 33      | 30      |

**Formula (for Science):**

```excel
=HLOOKUP("Science", A1:E2, 2, FALSE)
```

👉 Result: `40`

