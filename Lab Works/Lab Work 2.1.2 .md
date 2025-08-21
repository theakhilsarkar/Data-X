

# **Lab Work 2.1.2 — IF with AND / OR**

---

## **Task 1 — Student Performance (AND Example)**

**Goal:** Check if a student scored **above 80 in both Math and Science**.

**Sample Data**

| Student | Math | Science | Result            |
| ------- | ---- | ------- | ----------------- |
| Asha    | 85   | 92      | Excellent         |
| Raj     | 81   | 70      | Needs Improvement |
| Meena   | 78   | 89      | Needs Improvement |
| Suresh  | 90   | 84      | Excellent         |

**Formula (in D2):**

```excel
=IF(AND(B2>80,C2>80),"Excellent","Needs Improvement")
```

👉 **AND** checks *both conditions must be TRUE*.

---

## **Task 2 — Free Shipping (OR Example)**

**Goal:** Order qualifies if **Total > 100 OR Membership = Gold**.

**Sample Data**

| Order | Total | Membership | Free Shipping |
| ----- | ----- | ---------- | ------------- |
| 101   | 120   | Silver     | Yes           |
| 102   | 90    | Gold       | Yes           |
| 103   | 95    | Silver     | No            |
| 104   | 150   | Gold       | Yes           |

**Formula (in D2):**

```excel
=IF(OR(B2>100,C2="Gold"),"Yes","No")
```

👉 **OR** means *if any one condition is TRUE → Yes*.

---

## **Task 3 — Employee Bonus (AND Example)**

**Goal:** Eligible if **Sales > 10000 AND Experience > 5 years**.

**Sample Data**

| Employee | Sales | Experience | Bonus Eligible |
| -------- | ----- | ---------- | -------------- |
| Anita    | 12000 | 6          | Yes            |
| Raj      | 9500  | 7          | No             |
| Meena    | 15000 | 4          | No             |
| Suresh   | 18000 | 8          | Yes            |

**Formula (in D2):**

```excel
=IF(AND(B2>10000,C2>5),"Yes","No")
```

---

## **Task 4 — Product Stock Check (OR Example)**

**Goal:** Out of stock if **Stock = 0 OR Status = Discontinued**.

**Sample Data**

| Product | Stock | Status       | Availability |
| ------- | ----- | ------------ | ------------ |
| Laptop  | 0     | Active       | Out of Stock |
| Phone   | 10    | Discontinued | Out of Stock |
| Tablet  | 5     | Active       | Available    |
| TV      | 0     | Discontinued | Out of Stock |

**Formula (in D2):**

```excel
=IF(OR(B2=0,C2="Discontinued"),"Out of Stock","Available")
```

---

## **Task 5 — Candidate Interview (AND Example)**

**Goal:** Qualifies if **Experience > 3 years AND Degree = Yes**.

**Sample Data**

| Candidate | Experience | Degree | Eligible |
| --------- | ---------- | ------ | -------- |
| Asha      | 4          | Yes    | Yes      |
| Raj       | 2          | Yes    | No       |
| Meena     | 6          | No     | No       |
| Suresh    | 5          | Yes    | Yes      |

**Formula (in D2):**

```excel
=IF(AND(B2>3,C2="Yes"),"Yes","No")
```
