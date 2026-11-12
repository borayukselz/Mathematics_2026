# EXERCISE 1
# MATRIX SIZE AND ENTRIES

---

## 1. EXERCISE REMINDER

Given the two matrices:

```text
A = [ 2  -1   3 ]
    [ 0   4   5 ]

B = [  1   0 ]
    [ -2   3 ]
    [  4   1 ]
```

where **aᵢⱼ** and **bᵢⱼ** denote the entries in row **i** and column **j** of matrices **A** and **B**, respectively.

**Tasks:**
1. State the sizes of matrices **A** and **B**.
2. Read off the entries **a₁₂**, **a₂₃**, **b₂₁**, and **b₃₂**.
3. Write the second row of **A** and the first column of **B** as vectors.

---

## 2. DEFINITIONS & RULES

- **Matrix Size (Order):** A matrix with **m** horizontal rows and **n** vertical columns has size **m × n** (rows first, columns second).
- **Entry Indexing:** In the notation **xᵢⱼ**, the first index **i** specifies the row (top to bottom) and the second index **j** specifies the column (left to right).
- **Row and Column Vectors:** Row **i** of an **m × n** matrix forms a **1 × n** row vector, while column **j** forms an **m × 1** column vector.

---

## 3. SOLUTIONS

### 3.1. Sizes of Matrices A and B

- **Main Steps:**
  - Count the rows and columns of **A**: it has **2** horizontal rows and **3** vertical columns.
  - Count the rows and columns of **B**: it has **3** horizontal rows and **2** vertical columns.

**RESULT:**
- Size of Matrix A: **2 × 3**
- Size of Matrix B: **3 × 2**

- **Verification:** Multiplying the dimensions gives the total number of entries: **2 · 3 = 6** entries in **A** and **3 · 2 = 6** entries in **B**, matching the 6 numbers displayed in each matrix.

---

### 3.2. Specific Matrix Entries

- **Main Steps:**
  - **a₁₂**: Locate row 1 of **A** (`[ 2  -1  3 ]`) and read its 2nd entry → **-1**
  - **a₂₃**: Locate row 2 of **A** (`[ 0   4  5 ]`) and read its 3rd entry → **5**
  - **b₂₁**: Locate row 2 of **B** (`[ -2  3 ]`) and read its 1st entry → **-2**
  - **b₃₂**: Locate row 3 of **B** (`[  4  1 ]`) and read its 2nd entry → **1**

**RESULT:**
- **a₁₂ = -1**
- **a₂₃ = 5**
- **b₂₁ = -2**
- **b₃₂ = 1**

- **Verification:** Every index pair **(i, j)** satisfies **1 ≤ i ≤ m** and **1 ≤ j ≤ n**, and mapping all entries by position confirms each value:

```text
A = [ a₁₁  a₁₂  a₁₃ ] = [ 2  -1   3 ]
    [ a₂₁  a₂₂  a₂₃ ]   [ 0   4   5 ]

B = [ b₁₁  b₁₂ ] = [  1   0 ]
    [ b₂₁  b₂₂ ]   [ -2   3 ]
    [ b₃₁  b₃₂ ]   [  4   1 ]
```

---

### 3.3. Second Row of A and First Column of B as Vectors

- **Main Steps:**
  - Extract all entries from the 2nd row of **A** in left-to-right order (**a₂₁, a₂₂, a₂₃**) to form a row vector.
  - Extract all entries from the 1st column of **B** in top-to-bottom order (**b₁₁, b₂₁, b₃₁**) to form a column vector.

**RESULT:**

```text
Second row of A (Row Vector):
r₂ = [ 0  4  5 ]

First column of B (Column Vector):
     [  1 ]
c₁ = [ -2 ]
     [  4 ]
```

- **Verification:** Since **A** has **3** columns, **r₂** has size **1 × 3** (3 entries). Since **B** has **3** rows, **c₁** has size **3 × 1** (3 entries). Both dimensions match their parent matrices.

---

## 4. FINAL SUMMARY

| Item | Question | Result | Size / Type |
|:----:|:--------:|:------:|:-----------:|
| 1 | Size of Matrix A | **2 × 3** | 2 rows, 3 columns |
| 1 | Size of Matrix B | **3 × 2** | 3 rows, 2 columns |
| 2 | Entry a₁₂ | **-1** | Row 1, Col 2 of A |
| 2 | Entry a₂₃ | **5** | Row 2, Col 3 of A |
| 2 | Entry b₂₁ | **-2** | Row 2, Col 1 of B |
| 2 | Entry b₃₂ | **1** | Row 3, Col 2 of B |
| 3 | Second row of A | **[ 0  4  5 ]** | 1 × 3 row vector |
| 3 | First column of B | **[ 1, -2, 4 ]ᵀ** | 3 × 1 column vector |

---

## 5. CONCLUSION

Matrix dimensions are always stated in **row × column** order, and individual entries are uniquely identified by their **(row, column)** indices.

Extracting a full row yields a horizontal row vector whose length equals the column count, whereas extracting a full column yields a vertical column vector whose length equals the row count.
