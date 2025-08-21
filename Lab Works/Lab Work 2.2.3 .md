
# **Lab Work 2.2.3 — Date Functions**

---

## **Task 1 — TODAY()**

**Goal:** Show the current date.

**Formula:**

```excel
=TODAY()
```

👉 Result: `21-Aug-2025` (will always update to today’s date automatically).

---

## **Task 2 — EOMONTH()**

**Goal:** Get the last day of a given month.

**Example:** If today is `21-Aug-2025`.

**Formula:**

```excel
=EOMONTH(TODAY(),0)
```

👉 Result: `31-Aug-2025`

*(0 means current month, 1 means next month, -1 means previous month)*

---

## **Task 3 — YEAR()**

**Goal:** Extract the year from a date.

**Sample Data**

| Date        |
| ----------- |
| 15-Jul-2024 |

**Formula:**

```excel
=YEAR(A2)
```

👉 Result: `2024`

---

## **Task 4 — DATEDIF()**

**Goal:** Find difference between two dates.

**Sample Data**

| Start Date  | End Date    |
| ----------- | ----------- |
| 01-Jan-2024 | 21-Aug-2025 |

**Formula (in days):**

```excel
=DATEDIF(A2,B2,"d")
```

👉 Result: `598` days

**Formula (in months):**

```excel
=DATEDIF(A2,B2,"m")
```

👉 Result: `19` months

**Formula (in years):**

```excel
=DATEDIF(A2,B2,"y")
```

👉 Result: `1` year

---

## **Task 5 — DATE()**

**Goal:** Build a date from Year, Month, Day numbers.

**Sample Data**

| Year | Month | Day |
| ---- | ----- | --- |
| 2025 | 1     | 15  |

**Formula:**

```excel
=DATE(A2,B2,C2)
```

👉 Result: `15-Jan-2025`

