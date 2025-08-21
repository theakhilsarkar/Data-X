

# **Lab Work 2.2.4 — Time Functions**

---

## **Task 1 — NOW()**

**Goal:** Show the current **date & time**.

**Formula:**

```excel
=NOW()
```

👉 Result: `21-Aug-2025 10:35 AM` *(updates automatically whenever the sheet refreshes)*

---

## **Task 2 — HOUR()**

**Goal:** Extract the **hour** from a time.

**Sample Data**

| Time     |
| -------- |
| 14:45:30 |

**Formula:**

```excel
=HOUR(A2)
```

👉 Result: `14` (represents 2 PM in 24-hour format).

---

## **Task 3 — TIME()**

**Goal:** Convert numbers into a valid time format.

**Example:** Suppose we want to create `2:30:45` (2 hours, 30 minutes, 45 seconds).

**Formula:**

```excel
=TIME(2,30,45)
```

👉 Result: `2:30:45 AM`

---

## **Task 4 — Difference Between Two Times (TEXT)**

**Goal:** Calculate the difference between two times and display it in `hh:mm:ss` format.

**Sample Data**

| Start Time | End Time |
| ---------- | -------- |
| 08:15:00   | 11:45:30 |

**Formula:**

```excel
=TEXT(B2-A2,"hh:mm:ss")
```

👉 Result: `03:30:30`

*(3 hours, 30 minutes, 30 seconds difference)*

---

## **Task 5 — MINUTE() and SECOND()**

**Goal:** Extract **minute** and **second** from a time.

**Sample Data**

| Time     |
| -------- |
| 09:22:45 |

**Formula (Minute):**

```excel
=MINUTE(A2)
```

👉 Result: `22`

**Formula (Second):**

```excel
=SECOND(A2)
```

👉 Result: `45`

