
# **Lab Work 2.2.2 — Number Functions**

---

## **Task 1 — ROUND()**

**Goal:** Round a decimal number to 2 decimal places.

**Sample Data**

| Number  |
| ------- |
| 12.3456 |

**Formula:**

```excel
=ROUND(A2,2)
```

👉 Result: `12.35`

*(Rounds normally: if 3rd decimal ≥ 5 → rounds up, else down)*

---

## **Task 2 — CEILING() & FLOOR()**

**Goal:** Round upwards or downwards to nearest multiple.

**Sample Data**

| Number | Multiple |
| ------ | -------- |
| 17     | 5        |

* **CEILING (round up):**

```excel
=CEILING(A2,B2)
```

👉 Result: `20`

* **FLOOR (round down):**

```excel
=FLOOR(A2,B2)
```

👉 Result: `15`

---

## **Task 3 — MOD()**

**Goal:** Find remainder after division.

**Sample Data**

| Dividend | Divisor |
| -------- | ------- |
| 17       | 5       |

**Formula:**

```excel
=MOD(A2,B2)
```

👉 Result: `2`
(Since 17 ÷ 5 = 3 remainder **2**)

---

## **Task 4 — SQRT()**

**Goal:** Calculate square root of a number.

**Sample Data**

| Number |
| ------ |
| 25     |

**Formula:**

```excel
=SQRT(A2)
```

👉 Result: `5`

---

## **Task 5 — ABS()**

**Goal:** Return absolute value (removes negative sign).

**Sample Data**

| Number |
| ------ |
| -45    |
| 78     |

**Formula:**

```excel
=ABS(A2)
```

👉 Result: `45` for `-45`, and `78` for `78`.
