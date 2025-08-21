
# **Lab Work 2.2.1 — Text Functions**

---

## **Task 1 — Merge First & Last Name (CONCATENATE / TEXTJOIN)**

**Goal:** Join First Name + Last Name into Full Name.

**Sample Data**

| First Name | Last Name |
| ---------- | --------- |
| Asha       | Patel     |
| Raj        | Kumar     |

**Formula (CONCATENATE):**

```excel
=CONCATENATE(A2," ",B2)
```

**Formula (TEXTJOIN — better):**

```excel
=TEXTJOIN(" ",TRUE,A2,B2)
```

👉 Result: `Asha Patel`, `Raj Kumar`.

---

## **Task 2 — Extract Parts of String (LEFT, RIGHT, MID)**

**Sample Data**

| Code    |
| ------- |
| AB12345 |

* **LEFT** → First 2 letters

```excel
=LEFT(A2,2)
```

Result: `AB`

* **RIGHT** → Last 3 digits

```excel
=RIGHT(A2,3)
```

Result: `345`

* **MID** → Extract 3 digits starting from 3rd character

```excel
=MID(A2,3,3)
```

Result: `123`

---

## **Task 3 — Format Date with TEXT**

**Sample Data**

| Date       |
| ---------- |
| 01-01-2025 |

**Formula:**

```excel
=TEXT(A2,"dddd, mmm d, yyyy")
```

👉 Result: `Wednesday, Jan 1, 2025`

---

## **Task 4 — Format Number as Currency (TEXT)**

**Sample Data**

| Amount |
| ------ |
| 12500  |

**Formula:**

```excel
=TEXT(A2,"₹#,##0.00")
```

👉 Result: `₹12,500.00`

---

## **Task 5 — Extract Last Name (FIND + LEN + MID)**

**Sample Data**

| Full Name  |
| ---------- |
| Asha Patel |
| Raj Kumar  |

**Steps:**

1. Find the position of the space:

```excel
=FIND(" ",A2)
```

👉 Returns `5` (space position in “Asha Patel”).

2. Get text after space using MID:

```excel
=MID(A2,FIND(" ",A2)+1,LEN(A2))
```

👉 Result: `Patel`, `Kumar`.
