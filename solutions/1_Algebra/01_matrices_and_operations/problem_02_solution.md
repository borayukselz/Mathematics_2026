# EXERCISE 2
# ADDITION AND SCALAR MULTIPLICATION

---

## 1. EXERCISE REMINDER

Given the two **2 × 2** matrices:

```text
A = [  1   2 ]      B = [ 4  -2 ]
    [ -1   3 ]          [ 0   5 ]
```

**Tasks:**
1. Compute the matrix expressions:
   - **A + B**
   - **A - B**
   - **3A - 2B**
2. Explain why matrix addition is possible only for matrices of the same size.

---

## 2. DEFINITIONS & RULES

- **Matrix Addition:** For two matrices **A** and **B** of the same size **m × n**, their sum **A + B** is computed entry by entry: **(A + B)ᵢⱼ = aᵢⱼ + bᵢⱼ**.
- **Matrix Subtraction:** Subtracting **B** from **A** subtracts corresponding entries: **(A - B)ᵢⱼ = aᵢⱼ - bᵢⱼ**.
- **Scalar Multiplication:** Multiplying a matrix **M** by a scalar **c** multiplies every entry by **c**: **(cM)ᵢⱼ = c · mᵢⱼ**.
- **Dimension Compatibility for Addition:** Matrix addition and subtraction are defined **if and only if** both matrices have the exact same number of rows and columns (**m × n**).

---

## 3. SOLUTIONS

### 3.1. Compute A + B

- **Main Steps:**
  - Both **A** and **B** have size **2 × 2**, so addition is defined.
  - Add corresponding entries in each position:

```text
A + B = [  1 + 4   2 + (-2) ] = [  5   0 ]
        [ -1 + 0      3 + 5 ]   [ -1   8 ]
```

**RESULT:**

```text
A + B = [  5   0 ]
        [ -1   8 ]
```

- **Verification:** Subtracting **B** from the result recovers the original matrix **A**:

```text
(A + B) - B = [  5 - 4   0 - (-2) ] = [  1   2 ] = A
              [ -1 - 0      8 - 5 ]   [ -1   3 ]
```

---

### 3.2. Compute A - B

- **Main Steps:**
  - Both **A** and **B** have size **2 × 2**, so subtraction is defined.
  - Subtract each entry of **B** from the corresponding entry of **A**:

```text
A - B = [  1 - 4   2 - (-2) ] = [ -3   4 ]
        [ -1 - 0      3 - 5 ]   [ -1  -2 ]
```

**RESULT:**

```text
A - B = [ -3   4 ]
        [ -1  -2 ]
```

- **Verification:** Adding **B** back to the result recovers the original matrix **A**:

```text
(A - B) + B = [ -3 + 4   4 + (-2) ] = [  1   2 ] = A
              [ -1 + 0     -2 + 5 ]   [ -1   3 ]
```

---

### 3.3. Compute 3A - 2B

- **Main Steps:**
  - Multiply every entry of **A** by the scalar **3**:

```text
3A = [ 3 · 1     3 · 2 ] = [  3   6 ]
     [ 3 · (-1)  3 · 3 ]   [ -3   9 ]
```

  - Multiply every entry of **B** by the scalar **2**:

```text
2B = [ 2 · 4   2 · (-2) ] = [ 8  -4 ]
     [ 2 · 0   2 · 5    ]   [ 0  10 ]
```

  - Subtract **2B** from **3A** entry by entry:

```text
3A - 2B = [  3 - 8   6 - (-4) ] = [ -5  10 ]
          [ -3 - 0     9 - 10 ]   [ -3  -1 ]
```

**RESULT:**

```text
3A - 2B = [ -5  10 ]
          [ -3  -1 ]
```

- **Verification:** Rewrite **3A - 2B** as **2(A - B) + A** using the result from **3.2**:

```text
2(A - B) + A = [ -6   8 ] + [  1   2 ] = [ -5  10 ]
               [ -2  -4 ]   [ -1   3 ]   [ -3  -1 ]
```

---

### 3.4. Why Matrix Addition Requires the Same Size

- **Main Steps:**
  - Let **A** have size **m × n** and **B** have size **p × q**.
  - Matrix addition is defined position-by-position via **(A + B)ᵢⱼ = aᵢⱼ + bᵢⱼ**, requiring a one-to-one pairing for every coordinate **(i, j)**.
  - For every entry in **A** to match an entry in the exact same position in **B** (and vice versa), both row counts and column counts must be equal (**m = p** and **n = q**).

**RESULT:**
Matrix addition is possible only for matrices of the **same size** because every entry **aᵢⱼ** in the first matrix must pair with a corresponding entry **bᵢⱼ** at the exact same **(row, column)** position in the second matrix; if the dimensions differ, at least one entry has no partner and the sum is undefined.

- **Verification (Counterexample):** Consider a **2 × 2** matrix **C** and a **2 × 3** matrix **D**:

```text
C = [ 1  2 ]      D = [ 5  6   7 ]
    [ 3  4 ]          [ 8  9  10 ]
```

Attempting to compute **(C + D)₁₃ = c₁₃ + d₁₃** fails because **C** only has 2 columns and **c₁₃** does not exist.

---

## 4. FINAL SUMMARY

| Item | Expression / Question | Result | Size |
|:----:|:---------------------:|:------:|:----:|
| 3.1 | **A + B** | `[ 5  0 ; -1  8 ]` | **2 × 2** |
| 3.2 | **A - B** | `[ -3  4 ; -1  -2 ]` | **2 × 2** |
| 3.3 | **3A - 2B** | `[ -5  10 ; -3  -1 ]` | **2 × 2** |
| 3.4 | Same-size requirement | Entrywise pairing **(i, j)** requires equal dimensions | **m × n** |

---

## 5. CONCLUSION

Matrix addition, subtraction, and linear combinations operate entry by entry on matrices of identical size **m × n**.

Because each operation relies on matching **(row, column)** coordinates, matrices with different dimensions cannot be added or subtracted.
