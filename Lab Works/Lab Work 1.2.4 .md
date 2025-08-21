

# Lab Work 1.2.4 – Data Validation in Google Sheets

This lab covers how to use **Data Validation** to control user input and ensure data accuracy. Follow these steps exactly—no alternate methods are required.

---

## **Task 1: Create a drop-down list using Data Validation**

### Steps:

1. Select the cell or range where you want the drop-down list (e.g., **B2\:B10**).
2. Go to the menu → **Data → Data validation**.
3. Under **Criteria**, select **List of items**.
4. Enter the items separated by commas (e.g., `Yes,No,Maybe`).
5. Click **Done**.

👉 A drop-down arrow will appear in the selected cells for choosing values.

---

## **Task 2: Apply Data Validation to restrict numeric input between 1 and 100**

### Steps:

1. Select the target cell(s) (e.g., **C2\:C20**).
2. Go to **Data → Data validation**.
3. Under **Criteria**, choose **Number → between**.
4. Enter **1** and **100** as the range.
5. Click **Done**.

👉 Only numbers between 1 and 100 can be entered in those cells.

---

## **Task 3: Use a formula-based Data Validation rule**

### Steps:

1. Select the cells to apply validation (e.g., **D2\:D20**).
2. Go to **Data → Data validation**.
3. Under **Criteria**, choose **Custom formula is**.
4. Enter your formula. Examples:

   * `=ISODD(D2)` → Allows only odd numbers.
   * `=LEN(D2)=5` → Allows only text with exactly 5 characters.
5. Click **Done**.

👉 This enables custom logic-based validation.

---

## **Task 4: Display a custom error message for invalid data entry**

### Steps:

1. Select the cell(s) with Data Validation already applied.
2. Go to **Data → Data validation**.
3. Check the option **Show validation help text**.
4. Enter your custom message, e.g., *“Enter a value between 1 and 100 only.”*
5. Choose **Reject input** so invalid entries are not accepted.
6. Click **Done**.

👉 Now, if someone enters invalid data, your custom error message will appear.

---

## **Task 5: Allow only unique values in a column using Data Validation**

### Steps:

1. Select the column range (e.g., **E2\:E20**).
2. Go to **Data → Data validation**.
3. Under **Criteria**, choose **Custom formula is**.
4. Enter this formula (assuming your range starts at E2):

   ```
   =COUNTIF($E$2:$E$20,E2)=1
   ```
5. Set action to **Reject input**.
6. Click **Done**.

👉 This ensures that duplicate values cannot be entered in the column.
