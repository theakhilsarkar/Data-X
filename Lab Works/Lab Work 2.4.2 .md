# **Lab Work 2.4.2 — FILTER Function**

---

## 🔹 **Understanding FILTER()**

* **FILTER()** → Returns an array that meets the criteria you specify.
* Super useful for **dynamic filtering** without manually applying filters.

**Syntax:**

```excel
=FILTER(array, include, [if_empty])
```

* `array` → The range of cells to filter.
* `include` → The condition(s) to apply.
* `[if_empty]` → Optional value if no results are found.

---

## **Task 1 — Extract Values Greater than 50**

**Sample Data**

| Values |
| ------ |
| 30     |
| 60     |
| 45     |
| 80     |

**Formula:**

```excel
=FILTER(A2:A5, A2:A5>50, "No values > 50")
```

👉 Result: `60, 80`

---

## **Task 2 — Show Sales Above Threshold**

**Sample Data**

| Sales |
| ----- |
| 5000  |
| 3000  |
| 7000  |
| 2000  |

**Formula (threshold = 4000):**

```excel
=FILTER(A2:A5, A2:A5>4000, "No sales above 4000")
```

👉 Result: `5000, 7000`

---

## **Task 3 — Display Records by Category**

**Sample Data**

| Category    | Item   |
| ----------- | ------ |
| Grocery     | Rice   |
| Electronics | Laptop |
| Grocery     | Oil    |
| Clothing    | Shirt  |

**Formula (Category = Grocery):**

```excel
=FILTER(B2:B5, A2:A5="Grocery", "No records found")
```

👉 Result: `Rice, Oil`

---

## **Task 4 — Filter + Sort Together**

**Sample Data**

| Product | Price |
| ------- | ----- |
| A       | 150   |
| B       | 90    |
| C       | 200   |
| D       | 120   |

**Formula (Price > 100, sorted ascending):**

```excel
=SORT(FILTER(B2:B5, C2:C5>100), 1, TRUE)
```

👉 Result: `120, 150, 200`

---

## **Task 5 — Filter with Multiple Conditions**

**Sample Data**

| Category    | Product | Price |
| ----------- | ------- | ----- |
| Electronics | Laptop  | 1200  |
| Grocery     | Rice    | 60    |
| Electronics | Phone   | 800   |
| Clothing    | Shirt   | 400   |

**Formula (Price > 100 AND Category = Electronics):**

```excel
=FILTER(B2:B5, (C2:C5>100)*(A2:A5="Electronics"), "No match")
```

👉 Result: `Laptop, Phone`

---

⚡ **Key Advantage:** Unlike `VLOOKUP`, `FILTER()` is **dynamic** → if new data is added, results auto-update.
