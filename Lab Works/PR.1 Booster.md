
# **PR.1 Booster — Expense Tracker 2025**

---

## **1. Navigation & Setup**

**What:** Organise your workbook before entering data.
**Why:** Clean structure makes later tasks easy.

**Steps:**

1. Open Excel/Google Sheets → File → New Workbook.
2. Rename **Sheet1** → Right-click name → Rename → Type `Expense_2025`.
3. Add a new sheet → Click `+` at bottom → Rename to `Summary`.
4. Freeze header row:

   * Go to **View → Freeze Panes → 1 Row**.
   * In Google Sheets: View → Freeze → Up to row 1.

---

## **2. Formatting & Data Input**

**What:** Make your data readable.
**Why:** Formatting helps avoid mistakes and improves presentation.

**Steps:**

1. Enter sample data like:

| Date        | Department | Expense Type | Expense Amount | Payment Mode | Approved |
| ----------- | ---------- | ------------ | -------------- | ------------ | -------- |
| 05-Jan-2025 | Sales      | Travel       | 4500           | Credit Card  | Yes      |
| 08-Jan-2025 | Marketing  | Food         | 1200           | Cash         | No       |

2. Select **Date column** → Right-click → Format Cells → Custom → `DD-MMM-YYYY`.
3. Select **Expense Amount** → Format → Currency → ₹.
4. Select **Department & Payment Mode** → Click **Center Align** (toolbar).
5. Select **Header row** → Bold + Light fill color (light gray).
6. Convert data to **Table**:

   * In Excel: Insert → Table → Check “My table has headers”.
   * In Google Sheets: Select data → Data → Named Ranges (acts like a table).

---

## **3. Paste Special Practice**

**What:** Copy values or formatting without full data.
**Why:** Saves time when working with calculations or styles.

**Steps:**

1. Copy **Expense Amount column** → Right-click where you want → Paste Special → **Values only** → Column will show numbers only.
2. Copy same column again → Paste Special → **Formats only** → Formatting (₹, color) will apply but not values.

---

## **4. Cell References**

**What:** Use formulas with absolute (\$A\$1) and relative (A1) references.
**Why:** Control whether a formula “locks” a cell or adjusts when copied.

**Steps:**

1. In cell A1, type **1.1** (means +10%).
2. In a new column **+10% Hike**, enter formula:
   `=D2 * $A$1`

   * D2 = Expense Amount (changes when copied down → relative).
   * \$A\$1 = 10% hike factor (stays fixed → absolute).
3. Drag formula down → All rows get increased value.

---

## **5. Sorting & Filtering**

**What:** Organize and view only the data you need.
**Why:** Saves time in analysis.

**Steps:**

1. Select dataset → Click **Filter** button.
2. Sorting:

   * Sort Department **A–Z** (alphabetical).
   * Sort Expense Amount **Z–A** (highest first).
3. Filtering:

   * Click dropdown → Select **Approved = Yes**.
   * Then choose **Payment Mode = Credit Card**.

---

## **6. Data Validation**

**What:** Control what users can enter in a cell.
**Why:** Prevents wrong or invalid data entry.

**Steps:**

1. Restrict **Expense Type** → Data → Data Validation → List of items → Type: Travel, Food, Hotel, Misc.
2. Restrict **Date column** → Data Validation → Date → Must be **Before or Equal to =TODAY()**.
3. Custom error message for Expense Amount:

   * Data Validation → Number → Greater than 0.
   * Error Message: *“Expense must be positive!”*.

---

## **7. Named Ranges**

**What:** Give names to ranges of cells.
**Why:** Makes formulas easy to read.

**Steps:**

1. Select Expense Amount column → Data → Named Range → Name it `AllExpenses`.
2. Select only Approved Expenses → Named Range → `ApprovedExpenses`.
3. Try formula:

   * `=SUM(AllExpenses)` → Total expenses.
   * `=AVERAGE(ApprovedExpenses)` → Average approved expenses.

---

## **8. Conditional Formatting**

**What:** Highlight cells automatically based on conditions.
**Why:** Helps spot trends or issues quickly.

**Steps:**

1. Expense Amount > 5000 → Select column → Conditional Formatting → Rule: Greater than 5000 → Orange Fill.
2. Apply **Color Scale** (Green → Red) on Expense Amount.
3. Highlight rows where Approved = No:

   * Select all data → Conditional Formatting → Custom Formula:
     `=$F2="No"` → Apply Light Red.

---

## **9. Handling Formula Errors**

**What:** Prevent formulas from showing confusing error codes.
**Why:** Makes reports clean.

**Steps:**

1. In new column, type `=100/0` → Shows `#DIV/0!`.
2. Use **IFERROR**:
   `=IFERROR(100/0,"Invalid")` → Shows “Invalid”.
3. Use **ISERROR**:
   `=ISERROR(100/0)` → Returns TRUE.

---

## **10. Sheet & Range Protection**

**What:** Protect your important data.
**Why:** Prevent accidental deletion/changes.

**Steps:**

1. Protect Header Row → Select Row 1 → Right-click → Protect Range.
2. Protect Expense Amount column → Same method.
3. Workbook level (Excel only): Review → Protect Workbook → Prevent structure changes.
4. Share workbook with **View Only** permission → Others can see but not edit.
