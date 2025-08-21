
# Lab Work 1.3.2 – Protecting Sheets & Ranges in Google Sheets

This lab focuses on applying protection to sheets, cells, and workbooks in Google Sheets. Follow the instructions carefully.

---

## **Task 1: Protect a sheet to prevent editing but allow formatting**

### Steps:

1. Open your Google Sheet.
2. Go to the menu → **Data → Protect sheets and ranges**.
3. In the panel, select **Sheet** and choose the sheet you want to protect.
4. Click **Set permissions**.
5. In the dialog box:

   * Choose **Restrict who can edit this range**.
   * Allow **Only you** (or selected users).
   * Check the option **Allow users to format cells**.
6. Click **Done**.

👉 The sheet is now protected from editing but formatting (like colors, fonts, borders) is still allowed.

---

## **Task 2: Unprotect a sheet with a given password**

*(Note: In Google Sheets, protection is based on permissions, not passwords. If a password was set via Excel and imported, follow this logic.)*

### Steps:

1. Go to **Data → Protect sheets and ranges**.
2. In the panel, find the protected sheet.
3. Click the **trash icon (🗑️)** to remove protection.
4. If prompted for a password (Excel import case), enter the password and confirm.
5. The sheet is now unprotected.

👉 You can now freely edit the sheet.

---

## **Task 3: Protect specific cells while keeping other cells editable**

### Steps:

1. Select the range of cells you want to protect (e.g., **A2\:A10**).
2. Right-click → **Protect range** (or use **Data → Protect sheets and ranges**).
3. In the panel, give it a description (optional).
4. Click **Set permissions** → Restrict to **Only you** or selected users.
5. Click **Done**.

👉 Only the selected cells are protected. All other cells in the sheet remain editable.

---

## **Task 4: Apply workbook-level protection to prevent structure changes**

### Steps:

1. Google Sheets does not allow workbook-level password protection like Excel, but you can restrict sharing rights.
2. Go to **File → Share → Share with others**.
3. Set permissions:

   * Give **Viewer/Commenter access** to users who should not edit.
   * Only grant **Editor access** to trusted users.
4. Editors can still edit content, but only the **owner** can:

   * Add or delete sheets.
   * Rename sheets.
   * Change sharing permissions.

👉 This prevents unauthorized users from changing the workbook structure.

---

## **Task 5: Allow specific users to edit ranges in a protected sheet**

### Steps:

1. Protect the entire sheet (see Task 1).
2. Then go to **Data → Protect sheets and ranges**.
3. Select **Range** and define the range that specific users can edit.
4. Click **Set permissions**.
5. Choose **Custom** → Enter the email addresses of the users who should be allowed.
6. Click **Done**.

👉 The sheet stays protected, but the chosen users can edit only their assigned ranges.
