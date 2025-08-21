

# **Lab Work 1.4.1 – Project: Sheet Smart Tracker**

This project is about creating a **Performance Tracker Workbook** in Google Sheets. You’ll design a dataset, apply formatting, use formulas, data validation, and protection tools to analyze employee performance.

---

## **Task 1: Create a sheet with the required columns + sample dataset**

### Columns Needed:

* Employee ID
* Full Name
* Department
* Joining Date
* Monthly Sales
* Target Sales
* Performance Rating
* Review Comments

### Example Dataset (First 10 rows shown – you’ll extend to 50 rows)

| Employee ID | Full Name    | Department | Joining Date | Monthly Sales | Target Sales | Performance Rating | Review Comments         |
| ----------- | ------------ | ---------- | ------------ | ------------- | ------------ | ------------------ | ----------------------- |
| E001        | Ramesh Gupta | Sales      | 12-Jan-2021  | 55000         | 50000        | 95.00              | Excellent work          |
| E002        | Priya Sharma | Marketing  | 03-Feb-2022  | 43000         | 45000        | 88.00              | Meets expectations      |
| E003        | Aditya Mehta | IT         | 20-Mar-2020  | 39000         | 50000        | 78.00              | Needs improvement       |
| E004        | Neha Patil   | Support    | 05-Apr-2021  | 27000         | 40000        | 67.00              | Training required       |
| E005        | Arjun Singh  | Sales      | 11-Jul-2022  | 62000         | 60000        | 102.00             | Outstanding performance |
| E006        | Kavita Joshi | Sales      | 14-Aug-2020  | 30000         | 40000        | 75.00              |                         |
| E007        | Rajesh Kumar | IT         | 09-Oct-2019  | 45000         | 50000        | 90.00              | Great progress          |
| E008        | Sneha Reddy  | Marketing  | 22-Sep-2021  | 51000         | 55000        | 92.73              | Exceeds expectations    |
| E009        | Vivek Nair   | Support    | 15-Dec-2020  | 32000         | 40000        | 80.00              | Reliable contributor    |
| E010        | Meera Desai  | Sales      | 18-Jun-2018  | 70000         | 65000        | 107.69             | Top performer           |

👉 Extend this dataset to at least **50 employees** with varied departments, dates, and sales figures.

---

## **Task 2: Workbook & Sheets Setup**

1. Create a workbook named **Performance Tracker**.
2. Rename **Sheet1 → Jan\_Data**.
3. Duplicate it → rename copies as **Feb\_Data** and **Mar\_Data**.

---

## **Task 3: Calculate Performance %**

Formula for Performance %:

```
=Monthly Sales / Target Sales
```

* Example in row 2:

  ```
  =E2/F2
  ```

👉 Use **relative reference** (E2/F2) for each row.
👉 If Target Sales is a constant (e.g., always 50000), use **absolute reference**:

```
=E2/$F$2
```

---

## **Task 4: Formatting the Sheet**

* Header row → **Bold + Center Alignment + Light Blue Background**.
* Joining Date column → Format as **DD-MMM-YYYY**.
* Performance Rating column → Format as **0.00** (two decimals).

👉 Example formatted header:

\| **Employee ID** | **Full Name** | **Department** | **Joining Date** | **Monthly Sales** | **Target Sales** | **Performance Rating** | **Review Comments** |

---

## **Task 5: Paste Special**

1. Copy the calculated **Performance % column**.
2. Right-click → **Paste special → Paste values only** into a new column (`Performance Rating`).
3. Copy the formatted header row.
4. Right-click a blank row → **Paste special → Paste format only**.

---

## **Task 6: Convert to Table with Filters**

1. Select the dataset.
2. Go to **Format → Table** (or apply filter with **Data → Create a filter**).
3. Name the range **EmployeeData**.
4. Now you can filter/sort easily.

---

## **Task 7: Sorting & Filtering**

* Sort by **Monthly Sales (Z → A)** to see top performers first.
* Apply filter on **Department** → Show only **Sales employees**.

---

## **Task 8: Data Validation**

* Department column: Add **drop-down list** with options → Sales, Marketing, Support, IT.
* Review Comments column:

  * Go to **Data → Data Validation**.
  * Criteria → **Text length ≤ 200**.

---

## **Task 9: Create Named Ranges**

* Select `Monthly Sales` column → Name it **MonthlySales**.
* Select `Target Sales` column → Name it **TargetSales**.
* Select `Performance Rating` column → Name it **PerformanceRating**.

👉 You can now use formulas like:

```
=SUM(MonthlySales)
```

---

## **Task 10: Protect Columns**

* Protect **Performance Rating** column → Only the owner can edit.
* Allow only specific users (e.g., Managers) to edit **Review Comments**.

---

## **Task 11: Use IFERROR for Safety**

* Update formulas with IFERROR:

  ```
  =IFERROR(E2/F2, "No Target")
  ```

👉 If Target Sales is 0, instead of error `#DIV/0!`, it shows **No Target**.

---

## **Task 12: Conditional Formatting**

* Apply these rules to **Performance % column**:

  * ≥ 90% → Green Fill
  * 70–89% → Yellow Fill
  * < 70% → Red Fill
* Highlight empty **Review Comments** with Pink Fill:

  * Custom formula:

    ```
    =ISBLANK(H2)
    ```

---

## ✅ Final Result Snapshot

When complete, your sheet will look like this (colors added for visual clarity):

| Employee ID | Full Name    | Department | Joining Date | Monthly Sales | Target Sales | Performance %    | Review Comments         |
| ----------- | ------------ | ---------- | ------------ | ------------- | ------------ | ---------------- | ----------------------- |
| E001        | Ramesh Gupta | **Sales**  | 12-Jan-2021  | 55000         | 50000        | **110% (Green)** | Excellent work          |
| E004        | Neha Patil   | Support    | 05-Apr-2021  | 27000         | 40000        | **67% (Red)**    | Training required       |
| E006        | Kavita Joshi | Sales      | 14-Aug-2020  | 30000         | 40000        | **75% (Yellow)** | *(Blank – Highlighted)* |


