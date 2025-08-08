# 🎓 **Lecture 1: Kickstart with Google Sheets for Data Analysis**

> Welcome to your **first step into Data Analysis!** In this session, you’ll learn how to navigate Google Sheets like a pro, understand how data flows in spreadsheets, and apply core concepts like cell referencing, formatting, and basic data input.

---

## 📍 Learning Objectives

By the end of this lecture, you'll be able to:
✅ Understand what Google Sheets is and why it's used in data analysis
✅ Navigate sheets, workbooks, and ranges like a pro
✅ Differentiate between **Relative** and **Absolute** cell references
✅ Format data smartly and input formulas
✅ Build your **first mini-data tracker**

---

## 🧠 1. What is Google Sheets & Why Use It?

**Google Sheets** is a free online spreadsheet tool that helps you:

* Organize & clean data
* Perform calculations with functions
* Visualize patterns using charts
* Build reports & dashboards
* Collaborate in real-time with teams

🎯 **Use Case in Data Analysis**:

> You collect sales, survey, attendance, or feedback data → Analyze trends → Make decisions
> Google Sheets = Your *starting tool for analysis journey!*

---

## 🗂️ 2. Workbooks, Sheets, Cells & Navigation

| Term         | Definition                               | Example                      |
| ------------ | ---------------------------------------- | ---------------------------- |
| **Workbook** | A file containing one or more **sheets** | `Sales_Q1_2025.xlsx`         |
| **Sheet**    | A tab within the workbook                | "January Sales", "Dashboard" |
| **Cell**     | Single box that holds data               | `A1`, `B3`, `C2`             |
| **Range**    | A selection of multiple cells            | `A1:A10`, `B2:D6`            |

### 💡 Pro Tips:

* Press `Ctrl + Arrow Keys` to jump to data edges
* Click `+` to add new sheets
* Use **Named Ranges** to make formulas readable

---

## 🔁 3. Relative vs Absolute Cell References

One of the **most important concepts** in spreadsheets — understanding how cell references behave when you copy formulas.

| Type     | Format       | Example Formula | Behavior when copied      |
| -------- | ------------ | --------------- | ------------------------- |
| Relative | `A1`         | `=A1+B1`        | Adjusts to new row/column |
| Absolute | `$A$1`       | `=$A$1+$B$1`    | Locked on exact cell      |
| Mixed    | `A$1`, `$A1` | `=A$1+B2`       | Row or column locked      |

📘 **Example:**
Imagine you have:

* Unit Price in column C
* Quantity in column D
* Tax rate in cell `F1` (say 10%)

You want to calculate Total = `(C2 × D2) + Tax`
👉 Use: `=(C2*D2) + (C2*D2*$F$1)`

Why `$F$1`? Because you want the **same cell reference** (tax rate) every time.

---

## 🎨 4. Formatting & Data Input

### ✅ Why Formatting Matters:

Good formatting makes your data clean, readable, and easier to analyze.

| Task                       | Where to Find It                | Example               |
| -------------------------- | ------------------------------- | --------------------- |
| Bold headers               | Toolbar → Bold (B)              | `Product`, `Price`    |
| Currency Format            | Format → Number → Currency      | ₹10.00 or \$10.00     |
| Conditional Formatting     | Format → Conditional Formatting | Highlight Total > 100 |
| Data Validation (Dropdown) | Data → Data validation          | Limit to item list    |

📌 **Pro Tip**: Use keyboard shortcuts like `Ctrl + B`, `Ctrl + Shift + 1` for fast formatting.

---

## 🧪 5. Practical Example

Let’s create your first **Sales Tracker**:

### 🗃️ Step 1: Enter this Data

| Date       | Product | Price | Quantity | Total    |
| ---------- | ------- | ----- | -------- | -------- |
| 2025-08-01 | Pen     | 10    | 5        | `=C2*D2` |
| 2025-08-01 | Pencil  | 5     | 3        | `=C3*D3` |
| 2025-08-01 | Eraser  | 3     | 4        | `=C4*D4` |

---

### 🛠️ Step 2: Apply Formatting

* Bold the headers
* Format **Price** and **Total** as currency
* Apply **conditional formatting** to Total if value > 30

---

### 🧩 Step 3: Add Dropdown Validation

* Select Product cells → Data → Data Validation
* Enter list: `Pen, Pencil, Eraser`

---

## ✍️ 6. Practice Task

Create a **Mini Expense Tracker**:

| Date       | Category  | Amount | Description      |
| ---------- | --------- | ------ | ---------------- |
| 2025-08-01 | Food      | 200    | Lunch at café    |
| 2025-08-01 | Transport | 50     | Auto fare        |
| 2025-08-02 | Utilities | 150    | Electricity bill |
