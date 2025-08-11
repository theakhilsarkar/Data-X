# 📄 Google Sheets Practical Task – Employee Performance & Salary Tracker

## **🎯 Objective**

You are required to create a Google Sheet that tracks **employee details, salaries, and performance**.
This task will test your skills in **data entry, formatting, filtering, and using basic formulas**.

---

## **📝 Task Description**

You must create a Google Sheet with **at least 15 employee records** and the following **10 columns**:

| Column Name           | Data Type / Description                                                                              |
| --------------------- | ---------------------------------------------------------------------------------------------------- |
| **SR NO**             | Number (1, 2, 3...)                                                                                  |
| **EMPLOYEE NAME**     | Text (Full Name of Employee)                                                                         |
| **DEPARTMENT**        | Text (e.g., IT, HR, Sales, Design)                                                                   |
| **DESIGNATION**       | Text (e.g., Developer, Manager)                                                                      |
| **BASIC SALARY**      | Number (₹15,000 – ₹60,000)                                                                           |
| **BONUS**             | Number (₹1,000 – ₹10,000)                                                                            |
| **DEDUCTION**         | Number (₹500 – ₹5,000)                                                                               |
| **TOTAL SALARY**      | Formula (`=BASIC SALARY + BONUS - DEDUCTION`)                                                        |
| **PERFORMANCE SCORE** | Number (1–10)                                                                                        |
| **STATUS**            | Formula (`IF(PERFORMANCE SCORE>=7,"Excellent",IF(PERFORMANCE SCORE>=5,"Good","Needs Improvement"))`) |

---

## **📌 Instructions**

1. **Create the table** in Google Sheets with the above columns.
2. **Enter sample data** for at least **15 employees**.
3. **Apply formatting:**

   * Bold & colored headers.
   * Salary columns should use **currency format (₹)** and be **right-aligned**.
   * Apply alternating row colors.
4. **Apply filters** to:

   * Show only “Excellent” performers.
   * Sort by **TOTAL SALARY** (highest first).
   * Filter by **DEPARTMENT** or **DESIGNATION**.
5. **Conditional Formatting:**

   * Highlight salaries above ₹50,000 in **light green**.
   * Highlight “Needs Improvement” in **red**.
6. **Extra Column (Optional)**:

   * Add **ANNUAL SALARY** column using formula `=TOTAL SALARY * 12`.

---

## **✅ Learning Outcomes**

By completing this task, you will practice:

* **Data entry & organization**
* **Formatting & conditional formatting**
* **Basic formulas**
* **Sorting & filtering**
* **Data presentation for HR/Payroll**
