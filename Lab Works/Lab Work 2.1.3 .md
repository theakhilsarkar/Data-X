
# **Lab Work 2.1.3 — COUNTIFS, SUMIFS, AVERAGEIFS**

---

## **Task 1 — Students Scoring Above 80 in Both Subjects**

**Goal:** Count students who scored **above 80 in Math AND Science**.

**Sample Data**

| Student | Math | Science |
| ------- | ---- | ------- |
| Asha    | 85   | 92      |
| Raj     | 81   | 70      |
| Meena   | 78   | 89      |
| Suresh  | 90   | 84      |

**Formula:**

```excel
=COUNTIFS(B2:B5,">80",C2:C5,">80")
```

👉 Counts only rows where **both conditions are true**.
Result = **2** (Asha, Suresh).

---

## **Task 2 — Total Sales for Specific Region & Category (SUMIFS)**

**Goal:** Find **total sales** for a specific **Region + Category**.

**Sample Data**

| Region | Category    | Sales |
| ------ | ----------- | ----- |
| East   | Furniture   | 5000  |
| West   | Electronics | 7000  |
| East   | Electronics | 6000  |
| West   | Furniture   | 4000  |

**Formula (East + Electronics):**

```excel
=SUMIFS(C2:C5,A2:A5,"East",B2:B5,"Electronics")
```

👉 Checks both **Region = East** AND **Category = Electronics**.
Result = **6000**.

---

## **Task 3 — Average Salary (AVERAGEIFS)**

**Goal:** Average salary for employees in **IT department** with **experience > 5 years**.

**Sample Data**

| Employee | Department | Experience | Salary |
| -------- | ---------- | ---------- | ------ |
| Anita    | IT         | 6          | 60000  |
| Raj      | HR         | 7          | 50000  |
| Meena    | IT         | 4          | 45000  |
| Suresh   | IT         | 8          | 70000  |

**Formula:**

```excel
=AVERAGEIFS(D2:D5,B2:B5,"IT",C2:C5,">5")
```

👉 Looks only at **IT + Experience > 5**.
Result = **(60000+70000)/2 = 65000**.

---

## **Task 4 — Orders in January & Completed (COUNTIFS)**

**Goal:** Count how many orders are from **January AND Completed**.

**Sample Data**

| Order | Month    | Status    |
| ----- | -------- | --------- |
| 101   | January  | Completed |
| 102   | January  | Pending   |
| 103   | February | Completed |
| 104   | January  | Completed |

**Formula:**

```excel
=COUNTIFS(B2:B5,"January",C2:C5,"Completed")
```

👉 Filters only **January + Completed**.
Result = **2**.

---

## **Task 5 — Total Revenue >500 in Electronics (SUMIFS)**

**Goal:** Total revenue where **Category = Electronics AND Sales > 500**.

**Sample Data**

| Category    | Sales |
| ----------- | ----- |
| Electronics | 300   |
| Furniture   | 700   |
| Electronics | 800   |
| Electronics | 1200  |

**Formula:**

```excel
=SUMIFS(B2:B5,A2:A5,"Electronics",B2:B5,">500")
```

👉 Checks **Category Electronics + Sales >500**.
Result = **800+1200 = 2000**.
