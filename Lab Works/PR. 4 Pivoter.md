

# 📘 **PR. Pivoter – Final Project Guide for Google Sheets**

This guide will help you complete all the tasks in Google Sheets for your final project. Follow each step carefully, and you will learn how to create advanced reports, charts, dashboards, and use formulas effectively. Every option, menu, and formula is explained clearly.

---

## ✅ **PHASE 1: DATA SETUP AND NAMED RANGES**

### Step 1 – Create Named Ranges

1. Open your Google Sheet with the dataset.
2. Select the data section you want to name (for example, select all rows and columns for sales data).
3. Click **Data** → **Named ranges**.
4. In the right sidebar:

   * Enter the name like `SalesData`
   * Ensure the correct cell range is selected (for example: `A1:E100`)
   * Click **Done**
5. Similarly create these named ranges:

   * `EmployeeList` → Employee details table
   * `SalesAmounts` → Column where sales values are present
   * `Regions` → Column with region names
   * `Departments` → Column with department names

### Step 2 – Test Named Ranges

1. In any empty cell, type:

   ```excel
   =SUM(SalesAmounts)
   ```
2. Press **Enter** → It should calculate the total sales.
3. You can also test:

   ```excel
   =SUMIF(Regions, "North America", SalesAmounts)
   ```

   → It will sum sales from "North America".

---

## ✅ **PHASE 2: CONDITIONAL FORMATTING**

### Step 1 – Format `Performance_Rating` column

1. Select the `Performance_Rating` column.
2. Click **Format** → **Conditional formatting**.
3. Under “Format rules”:

   * Apply rule: **Text is exactly** → type "Excellent" → choose green fill color → Click **Done**
   * Add another rule → Text is exactly → "Good" → yellow fill → Done
   * Add another rule → Text is exactly → "Average" → red fill → Done

### Step 2 – Format `Total_Sales` with Color Scale

1. Select the `Total_Sales` column.
2. Format → Conditional formatting → Color scale tab
3. Set **Min value** to lowest sales → choose red
4. Set **Max value** to highest sales → choose green → Done

### Step 3 – Highlight Top 10% of performers

1. Select `Total_Sales` column
2. Format → Conditional formatting → Format rules →

   * “Custom formula is” → type:

     ```excel
     =B2>=PERCENTILE($B$2:$B$100,0.9)
     ```
   * Set highlight style → Done

### Step 4 – Add Data Bars in `Units_Sold` column

1. Select `Units_Sold` column
2. Format → Conditional formatting → Color scale
3. Choose gradient → Done

### Step 5 – Format `Salary` column

1. Select `Salary` column
2. Format → Number → Currency
3. Add a custom rule:

   * “Less than” → set low salary → red
   * “Greater than” → set high salary → green

---

## ✅ **PHASE 3: IF FORMULAS AND LOGICAL FUNCTIONS**

### Step 1 – Commission Calculation

1. In the new column “Commission”, type:

   ```excel
   =IF(Total_Sales>10000, Total_Sales*0.2, 0)
   ```
2. Drag the formula down to apply to all rows.

### Step 2 – Performance Bonus

1. In “Performance Bonus” column:

   ```excel
   =IF(Performance_Rating="Excellent", 5000, IF(Performance_Rating="Good", 2000, 0))
   ```

### Step 3 – Sales Category

1. Type in “Sales Category”:

   ```excel
   =IF(AND(Total_Sales>15000, Performance_Rating="Excellent"), "Top Performer", IF(OR(Total_Sales>10000, Performance_Rating="Good"), "Good Performer", "Needs Improvement"))
   ```

### Step 4 – Quarter Performance Status

1. In “Quarter Status”:

   ```excel
   =IF(AND(Quarter="Q1", Total_Sales>8000), "Q1 Target Met", IF(AND(Quarter="Q2", Total_Sales>10000), "Q2 Target Met", IF(AND(Quarter="Q3", Total_Sales>12000), "Q3 Target Met", "Target Missed")))
   ```

---

## ✅ **PHASE 4: STATISTICAL FUNCTIONS**

### Create Summary Table

**Total Sales by Region:**

```excel
=SUMIFS(SalesAmounts, Regions, "North America")
```

**Count of Excellent Performers:**

```excel
=COUNTIFS(Performance_Rating, "Excellent")
```

**Average Sales by Department:**

```excel
=AVERAGEIFS(SalesAmounts, Departments, "Sales")
```

### Multi-criteria Example

**Sales count for Q1 Electronics:**

```excel
=COUNTIFS(Quarter, "Q1", Product, "Electronics")
```

**Revenue for Sales department in North America:**

```excel
=SUMIFS(SalesAmounts, Departments, "Sales", Regions, "North America")
```

---

## ✅ **PHASE 5: TEXT AND MATH FUNCTIONS**

**Full Name:**

```excel
=A2 & " " & B2
```

**Initials:**

```excel
=LEFT(A2,1) & LEFT(B2,1)
```

**Email addresses in lowercase:**

```excel
=LOWER(A2 & "." & B2 & "@company.com")
```

**Years of service:**

```excel
=DATEDIF(Hire_Date, TODAY(), "Y")
```

**Round commission to 2 decimals:**

```excel
=ROUND(Commission, 2)
```

**Employee codes:**

```excel
=UPPER(LEFT(Department, 3) & "-" & RIGHT(Employee_ID, 3))
```

---

## ✅ **PHASE 6: DATE AND TIME FUNCTIONS**

**Days since hire:**

```excel
=TODAY() - Hire_Date
```

**Extract hire month:**

```excel
=MONTH(Hire_Date)
```

**Sales month as text:**

```excel
=TEXT(Sales_Date, "MMMM")
```

**Age group based on hire date:**

```excel
=IF(Hire_Date<DATE(2021,1,1), "Veteran", IF(Hire_Date<DATE(2023,1,1), "Experienced", "New"))
```

**Quarterly sales date:**

```excel
=EOMONTH(Sales_Date, 2)
```

---

## ✅ **PHASE 7: VLOOKUP AND HLOOKUP**

**Employee Lookup:**

```excel
=VLOOKUP(Employee_ID, EmployeeList, 2, FALSE)
```

**Salary Lookup:**

```excel
=VLOOKUP(Employee_ID, EmployeeList, 3, FALSE)
```

**Commission Rate Lookup with error handling:**

```excel
=IFERROR(VLOOKUP(Department, CommissionTable, 2, FALSE), 0)
```

**HLOOKUP for product categories:**

```excel
=HLOOKUP(ProductCode, CategoryTable, 2, FALSE)
```

**Approximate match for performance tiers:**

```excel
=VLOOKUP(Total_Sales, PerformanceTable, 2, TRUE)
```

---

## ✅ **PHASE 8: INDEX AND MATCH**

**Replace VLOOKUP with INDEX/MATCH:**

```excel
=INDEX(EmployeeList, MATCH(Employee_ID, INDEX(EmployeeList,,1), 0), 2)
```

**Highest Sales Performer:**

```excel
=INDEX(EmployeeList, MATCH(MAX(SalesAmounts), SalesAmounts, 0), 2)
```

**Dynamic Column Lookup:**

```excel
=INDEX(SalesData, ROW_NUMBER, MATCH(UserInput, HeaderRow, 0))
```

---

## ✅ **PHASE 9: FILTER FUNCTION**

**Filter top performers:**

```excel
=FILTER(EmployeeList, SalesAmounts>15000)
```

**Filter by multiple criteria:**

```excel
=FILTER(SalesData, SalesAmounts>10000, Regions="North America")
```

**Filter sales above threshold:**

```excel
=FILTER(SalesData, SalesAmounts>15000)
```

**Dropdown selection dynamic filter:**

1. Use **Data → Data validation** → Criteria → List from a range or list of items → create dropdown.

**Combine FILTER with other functions:**

```excel
=SUM(FILTER(SalesAmounts, Regions="North America"))
```

---

## ✅ **PHASE 10: CHART CREATION**

**Column Chart – Monthly sales by region:**

1. Select pivot table → Insert → Chart → Column Chart
2. Customize → Add axis titles, labels, colors → Done

**Pie Chart – Sales distribution by department:**

1. Insert → Chart → Pie Chart
2. Show percentages → Customize → Slice labels → Percentages → Done

**Bar Chart – Top 10 employees by total sales:**

1. Sort data descending → Insert → Chart → Bar
2. Add data labels → Customize → Series → Data labels → On → Done

**Line Chart – Sales trends by quarter:**

1. Insert → Chart → Line Chart
2. Add trendlines → Customize → Series → Trendline → On → Done

---

## ✅ **PHASE 11: PIVOT TABLES**

**Employee Performance Pivot:**

1. Insert → Pivot table → Rows = Employee Name, Department
2. Columns = Quarter
3. Values = Sum of Total Sales, Average of Performance Rating
4. Apply formatting → Bold headers

**Regional Analysis Pivot:**

1. Rows = Region, Product Category
2. Values = Count of Sales, Sum of Revenue

**Time-based Analysis Pivot:**

1. Rows = Month (from Sales\_Date)
2. Columns = Customer Type
3. Values = Sum of Units Sold

**Calculated fields:**

1. Pivot table → Add → Calculated field → Create formulas using fields → Done

---

## ✅ **PHASE 12: CHARTS FROM PIVOT TABLES**

**Column Chart from Employee Pivot:**

1. Select pivot → Insert → Chart → Column

**Pie Chart from Regional Analysis:**

1. Insert → Chart → Pie → Customize labels and colors

**Line Chart from Time-based Analysis:**

1. Insert → Chart → Line → Add trendlines and axis labels

**Consistent styling:**

* Chart editor → Customize → Apply same fonts, colors, and labels across all charts

**Add interactive filters:**

1. Insert → Slicer → Choose fields like Region, Department
2. Link slicers to pivot charts → Done

---

## ✅ **PHASE 13: DASHBOARD CREATION**

**Step 1 – Design layout:**

1. Create a new sheet → Name it “Dashboard”
2. Insert tables, charts, and metrics in clean sections

**Step 2 – KPI Summary:**

* Total Revenue:

  ```excel
  =SUM(SalesAmounts)
  ```
* Average Sale:

  ```excel
  =AVERAGE(SalesAmounts)
  ```
* Top Performer:

  ```excel
  =INDEX(EmployeeList, MATCH(MAX(SalesAmounts), SalesAmounts, 0), 2)
  ```
* Best Region:

  ```excel
  =INDEX(Regions, MATCH(MAX(SUMIFS(SalesAmounts, Regions, Regions)), Regions, 0))
  ```

**Step 3 – Add dropdown filters:**

1. Data → Data validation → List from a range or items → Select categories → Done

**Step 4 – Link charts to filters:**

1. Click chart → Setup → Filter → Connect to slicer fields → Done

**Step 5 – Executive summary:**

* Use text boxes → Insert → Drawing → Text box
* Write key insights like “North America is the top-performing region.”

**Step 6 – Professional formatting:**

1. Adjust fonts → Format → Text → Bold
2. Apply borders → Format → Borders
3. Use corporate colors → Format → Fill color

---

## ✅ Final Notes

* Always save your work regularly.
* Use the Explore feature (bottom right corner) if you need suggestions.
* Check formulas by pressing Enter and reviewing results.
* Explore **Help → Function list** if unsure about syntax.


