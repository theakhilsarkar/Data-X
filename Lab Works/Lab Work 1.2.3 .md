

# Lab Work 1.2.3 – Sorting & Filtering in Google Sheets

This lab covers how to **sort and filter data** effectively in Google Sheets. Each task is explained step by step. No need to use any alternate method—follow only the given instructions.

---

## **Task 1: Sort a dataset in ascending and descending order**

### Steps:

1. Select the dataset range (example: **A1\:D20**).
2. Go to the top menu → **Data → Sort range**.
3. Choose:

   * **Sort A → Z** → Ascending order (smallest to largest / A to Z).
   * **Sort Z → A** → Descending order (largest to smallest / Z to A).

👉 This rearranges your dataset based on the selected column.

---

## **Task 2: Apply multiple column sorting**

### Steps:

1. Select the full dataset (ensure all columns are highlighted).
2. Go to **Data → Sort range → Advanced range sorting options**.
3. In the dialog box:

   * Add the **first column** you want to sort by (e.g., "Department").
   * Then click **Add another sort column** and choose a **second column** (e.g., "Name" or "Marks").
4. Click **Sort**.

👉 The dataset is first sorted by the primary column, then by the secondary column.

---

## **Task 3: Use AutoFilter to display only specific records**

### Steps:

1. Select your dataset including the headers.
2. Go to **Data → Create a filter**.
3. Small **filter icons (▼)** will appear on each column header.
4. Click a filter icon → Choose the specific values you want to display (uncheck the rest).
5. The sheet will hide all rows that do not match your filter.

👉 This helps you view only the data you need without deleting anything.

---

## **Task 4: Apply a custom filter to show data based on a condition**

### Steps:

1. With the filter applied (Task 3), click on the filter icon of a column.
2. Select **Filter by condition**.
3. Choose a condition such as:

   * **Greater than** (e.g., show marks greater than 50).
   * **Text contains** (e.g., show names containing “A”).
4. Enter the condition value and click **OK**.

👉 Now only rows matching the condition will be displayed.

---

## **Task 5: Use Advanced Filtering options for complex data retrieval**

### Steps:

1. Select your dataset with headers.
2. Go to **Data → Create a filter** (if not already applied).
3. Click on a filter icon → Choose **Filter by condition**.
4. Use advanced options such as:

   * **Custom formula is** → Example: `=B2>60` (to show only rows where column B values are greater than 60).
   * **Date is before / after** → Useful for filtering records by date.
   * **Text starts with / ends with** → To filter specific word patterns.
5. Apply and check results.

👉 Advanced filters allow you to handle complex conditions without writing separate formulas.

