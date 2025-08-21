
# Lab Work 1.3.3 – Handling Errors in Google Sheets (Beginner Guide)

When we work with formulas in Google Sheets, sometimes mistakes happen, such as dividing by zero, using wrong references, or searching for missing values. These mistakes show up as **errors** (like `#DIV/0!`, `#N/A`, `#VALUE!`).
Google Sheets has special functions to **handle, detect, and classify errors**.

---

## **Task 1: Use IFERROR to replace #DIV/0! errors with a custom message**

* Normally, if you divide a number by zero, you see this error:

  ```
  =10/0
  Result → #DIV/0!
  ```

* To make it user-friendly, we use **IFERROR**.

**Formula:**

```
=IFERROR(10/0, "Division not possible")
```

**Explanation:**

* The first part `10/0` is your calculation.
* If it works, the result will show.
* If it gives an error, the second part `"Division not possible"` will be displayed instead.

👉 Use IFERROR whenever you want to **hide errors** and show a clear message.

---

## **Task 2: Apply ISERROR to identify errors in a dataset**

* Suppose your column looks like this:

| Value | Formula | Result  |
| ----- | ------- | ------- |
| 100   | =A2/10  | 10      |
| 0     | =A3/0   | #DIV/0! |
| Text  | =A4+5   | #VALUE! |

* To check which rows contain errors, use **ISERROR**.

**Formula (in B2):**

```
=ISERROR(A2/10)
```

**Explanation:**

* If the formula works, result = **FALSE** (no error).
* If the formula fails, result = **TRUE** (error).

👉 ISERROR is like a **yes/no test** for errors.

---

## **Task 3: Use the ERROR.TYPE function to classify different types of errors**

* Different errors mean different problems.
* **ERROR.TYPE** tells you *which* error it is by returning a number.

**Example:**
If `=10/0` gives `#DIV/0!`, then:

```
=ERROR.TYPE(10/0)
Result → 2
```

**Common Codes Returned by ERROR.TYPE:**

* `1` → `#NULL!`
* `2` → `#DIV/0!`
* `3` → `#VALUE!`
* `4` → `#REF!`
* `5` → `#NAME?`
* `6` → `#NUM!`
* `7` → `#N/A`

👉 This is useful when you want to **classify errors** and maybe handle them differently.

---

## **Task 4: Fix a #VALUE! error caused by incorrect cell references**

* A `#VALUE!` error usually happens when you try to do math with text.

**Example:**

```
=A2 + "Hello"
Result → #VALUE!
```

**How to Fix:**

1. Make sure the cell contains numbers, not text.
2. If the cell has a number stored as text, convert it:

   ```
   =A2 + VALUE(B2)
   ```

   (If B2 contains "50" as text, VALUE(B2) converts it to number 50).

👉 Always check that **numbers are numbers** before adding, subtracting, multiplying, or dividing.

---

## **Task 5: Use IFNA to handle #N/A errors in a lookup function**

* `#N/A` means “Not Available” (the value was not found).

* Example with **VLOOKUP**:

  ```
  =VLOOKUP("Apple", A2:B10, 2, FALSE)
  ```

  If “Apple” is not in column A, it shows: `#N/A`.

* To handle this nicely, use **IFNA**:

  ```
  =IFNA(VLOOKUP("Apple", A2:B10, 2, FALSE), "Not Found")
  ```

**Explanation:**

* If value is found → Show the result.
* If not found → Show the message “Not Found” instead of an error.

👉 IFNA is like a polite way of saying *“Sorry, that data isn’t here.”*

---

## ✅ Summary of Functions

| Function     | Purpose                                    | Example                                          | Result      |
| ------------ | ------------------------------------------ | ------------------------------------------------ | ----------- |
| `IFERROR`    | Replace any error with a message/value     | `=IFERROR(10/0,"No division")`                   | No division |
| `ISERROR`    | Test if a formula gives error (TRUE/FALSE) | `=ISERROR(A2/B2)`                                | TRUE        |
| `ERROR.TYPE` | Identify type of error (number code)       | `=ERROR.TYPE(10/0)`                              | 2           |
| `VALUE`      | Convert text into number                   | `=VALUE("50")+10`                                | 60          |
| `IFNA`       | Handle only `#N/A` errors                  | `=IFNA(VLOOKUP("X",A2:B10,2,FALSE),"Not Found")` | Not Found   |

