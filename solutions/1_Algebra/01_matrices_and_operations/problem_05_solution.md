# Exercise 5: Matrix Times Vector

### Given

**Matrix A:**
[  2  -1 ]
[  1   3 ]

**Vector x:**
[  4 ]
[  2 ]

---

### 1. Compute Ax

* **Result:**
  [  6 ]
  [ 10 ]

* **Main Steps:** Multiply rows of Matrix A by Vector x[cite: 7]:
  * Top entry (Row 1):    (2 × 4) + (-1 × 2) = 8 - 2 = 6
  * Bottom entry (Row 2): (1 × 4) + (3 × 2)  = 4 + 6 = 10

* **Method & Explanation:** Matrix-vector multiplication using the row dot-product method[cite: 7]. Each element of the resulting vector is the dot product of a row from Matrix A and Vector x[cite: 7].

* **Mathematical Verification:** Check individual calculations: 2(4) - 1(2) = 6, and 1(4) + 3(2) = 10. Both values are correct.

---

### 2. Express Ax as a Linear Combination of the Columns of A

* **Result:**
    4 * [  2 ] + 2 * [ -1 ] = [  6 ]
        [  1 ]       [  3 ]   [ 10 ]

* **Main Steps:**
  1. Identify the columns of Matrix A[cite: 7]:
     * Column 1: [  2 ]
                 [  1 ]
     * Column 2: [ -1 ]
                 [  3 ]
  2. Identify the scalar coefficients from Vector x[cite: 7]:
     * First coefficient (x₁): 4
     * Second coefficient (x₂): 2
  3. Write the linear combination:
     4 * (Column 1) + 2 * (Column 2)[cite: 7]

* **Method & Explanation:** The column-based definition of matrix-vector multiplication states that Ax is a linear combination of the columns of A, where the entries of Vector x serve as the scalar weights (coefficients)[cite: 7].

* **Mathematical Verification:** Multiply out the linear combination:
  * 4 * [ 2, 1 ] = [ 8, 4 ]
  * 2 * [ -1, 3 ] = [ -2, 6 ]
  * Adding them together: [ 8 + (-2), 4 + 6 ] = [ 6, 10 ]
  * This matches the exact result obtained in Part 1.
