
# Lab Work 1.3.1 – Named Ranges in Google Sheets

This lab explains how to create, use, edit, and manage **Named Ranges** in Google Sheets. Follow the instructions step by step.

---

## **Task 1: Create a named range for a list of product names**

### Steps:

1. Select the range of cells that contain product names (e.g., **A2\:A20**).
2. Go to the menu → **Data → Named ranges**.
3. A side panel will open on the right.
4. Enter a name for the range (e.g., `Products`).

   * Rules: The name must not contain spaces (use underscores if needed).
5. Click **Done**.

👉 Now the selected range has a unique name and can be used in formulas.

---

## **Task 2: Use a named range in a formula to calculate the total sales**

### Steps:

1. Suppose **B2\:B20** contains sales amounts.
2. Create a named range for it (e.g., `Sales`).
3. In a blank cell, enter the formula:

   ```
   =SUM(Sales)
   ```
4. Press **Enter**.

👉 Google Sheets will calculate the total sales using the named range instead of cell references.

---

## **Task 3: Edit an existing named range and update the reference**

### Steps:

1. Go to **Data → Named ranges**.
2. In the panel, select the range you want to edit.
3. Click the **Edit icon (✏️)** next to the named range.
4. Update the reference (e.g., change from `A2:A20` to `A2:A30`).
5. Click **Done**.

👉 Any formulas using that named range will automatically update with the new reference.

---

## **Task 4: Delete a named range and verify if it's removed from formulas**

### Steps:

1. Go to **Data → Named ranges**.
2. Select the named range you want to delete.
3. Click the **Delete (🗑️ trash icon)**.
4. Now check any formulas that were using this name:

   * They will show an error (`#NAME?`) because the named range no longer exists.

👉 This verifies that the named range was successfully deleted.

