
# **Lab Work 1.4.1 — IF Functions (Beginner Guide)**

---

## **Task 1 — Simple IF (Pass/Fail)**

**What:** Check if a student scored more than 50.
**Why:** Basic condition handling.

**Example Data**

| Student | Score | Result |
| ------- | ----- | ------ |
| Asha    | 35    | Fail   |
| Raj     | 67    | Pass   |
| Meena   | 50    | Fail   |
| Suresh  | 82    | Pass   |

**Formula (in C2):**

```excel
=IF(B2>50,"Pass","Fail")
```

👉 Copy down for all students.

---

## **Task 2 — Nested IF (Grades A–F)**

**What:** Assign letter grades based on ranges.
**Why:** Multiple conditions in one formula.

**Example Data**

| Student | Score | Grade |
| ------- | ----- | ----- |
| Asha    | 92    | A     |
| Raj     | 81    | B     |
| Meena   | 74    | C     |
| Suresh  | 65    | D     |
| Anita   | 55    | F     |

**Formula (in C2):**

```excel
=IF(B2>=90,"A",IF(B2>=80,"B",IF(B2>=70,"C",IF(B2>=60,"D","F"))))
```

👉 Reads like: If ≥90 → A, else if ≥80 → B, else if ≥70 → C, else if ≥60 → D, else F.

---

## **Task 3 — Weekend or Weekday**

**What:** Identify whether a date falls on weekend.
**Why:** Useful in HR/attendance sheets.

**Example Data**

| Date        | Day Type |
| ----------- | -------- |
| 18-Aug-2025 | Weekday  |
| 23-Aug-2025 | Weekend  |
| 24-Aug-2025 | Weekend  |
| 25-Aug-2025 | Weekday  |

**Formula (in B2):**

```excel
=IF(OR(WEEKDAY(A2)=1,WEEKDAY(A2)=7),"Weekend","Weekday")
```

👉 WEEKDAY returns 1 for Sunday, 7 for Saturday.

---

## **Task 4 — Commission Rate**

**What:** Assign different commission % based on sales.
**Why:** Sales & incentives tracking.

**Example Data**

| Sales | Commission Rate |
| ----- | --------------- |
| 6000  | 5%              |
| 4500  | 3%              |
| 1500  | 1%              |
| 2500  | 3%              |

**Formula (in B2):**

```excel
=IF(A2>5000,"5%",IF(A2>=2000,"3%","1%"))
```

👉 You can also calculate actual commission by multiplying:
`=A2*IF(A2>5000,0.05,IF(A2>=2000,0.03,0.01))`

---

## **Task 5 — Expense Categorization**

**What:** Classify expenses as High, Medium, Low.
**Why:** Expense management.

**Example Data**

| Expense | Category |
| ------- | -------- |
| 1500    | High     |
| 900     | Medium   |
| 400     | Low      |
| 1200    | High     |

**Formula (in B2):**

```excel
=IF(A2>1000,"High",IF(A2>=500,"Medium","Low"))
```
