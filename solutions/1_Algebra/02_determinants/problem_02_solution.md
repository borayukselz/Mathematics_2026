# Exercise 2: Determinant of a 3x3 Matrix

### Given Matrix

**Matrix A:**
[  1   2  -1 ]
[  0   3   4 ]
[  2   1   5 ][cite: 19]

---

### 1. Compute det(A) Using Sarrus' Rule

* **Result:**
  **det(A) = 33**[cite: 19]

* **Method & Explanation:**
  **Sarrus' Rule** is a visual shortcut designed specifically for 3×3 matrices[cite: 19]. You write down the matrix, repeat the first two columns to the right, calculate the products of the 3 down-right diagonals (and add them), then subtract the products of the 3 up-right diagonals[cite: 19].

* **Detailed Calculation Steps:**

  1. **Set up the extended matrix (repeating Columns 1 and 2):**
     1   2  -1  |  1   2
     0   3   4  |  0   3
     2   1   5  |  2   1

  2. **Calculate Down-Right Diagonal Products (Positive Terms):**
     * Diagonal 1: (1) × (3) × (5)  =  15
     * Diagonal 2: (2) × (4) × (2)  =  16
     * Diagonal 3: (-1) × (0) × (1) =   0
     * **Sum of Positive Terms:** 15 + 16 + 0 = **31**

  3. **Calculate Up-Right Diagonal Products (Negative Terms):**
     * Diagonal 1: (2) × (3) × (-1) =  -6
     * Diagonal 2: (1) × (4) × (1)  =   4
     * Diagonal 3: (5) × (0) × (2)  =   0
     * **Sum of Negative Terms:** (-6) + 4 + 0 = **-2**

  4. **Subtract Negative Sum from Positive Sum:**
     * det(A) = (Sum of Down-Right Diagonals) - (Sum of Up-Right Diagonals)[cite: 19]
     * det(A) = 31 - (-2) = 31 + 2 = **33**[cite: 19]

---

### 2. Verification Check Using Determinant Properties

* **Chosen Properties:**
  1. Adding a scalar multiple of one row to another row (**row replacement**) does not change the value of the determinant[cite: 19].
  2. The determinant of an **upper triangular matrix** equals the product of its main diagonal entries[cite: 19].

* **Check Execution:**
  * **Step 1 (Row replacement R₃ ← R₃ - 2R₁):**
    Matrix A becomes:
    [  1   2  -1 ]
    [  0   3   4 ]
    [  0  -3   7 ]

  * **Step 2 (Row replacement R₃ ← R₃ + R₂):**
    Matrix becomes upper triangular:
    [  1   2  -1 ]
    [  0   3   4 ]
    [  0   0  11 ]

  * **Step 3 (Calculate Product of Diagonal Entries):**
    det(A) = 1 × 3 × 11 = **33**

* **Conclusion:**
  Both Sarrus' Rule and the row-reduction property produce the exact same value (**33**), verifying the computation[cite: 19].

---

### 3. Detailed Explanation & Linear Algebra Insights

1. **Why Sarrus' Rule Works Only for 3×3 Matrices:**
   * Sarrus' Rule captures all 3! = 6 permutations required by the general determinant formula for 3×3 matrices[cite: 19].
   * **Important Note:** Sarrus' Rule does **not** work for 4×4 or larger matrices because a 4×4 determinant requires 4! = 24 terms, whereas extending diagonal lines only yields 8 terms.

2. **Alternative Check via Cofactor Expansion:**
   * Expanding along Column 1 (which already contains a zero) offers another property check[cite: 19]:
     det(A) = 1 × det[ 3, 4 ; 1, 5 ] - 0 + 2 × det[ 2, -1 ; 3, 4 ]
     det(A) = 1 × (15 - 4) + 2 × (8 - (-3))
     det(A) = 1 × 11 + 2 × 11 = 11 + 22 = **33**

3. **Geometric Interpretation in 3D Space:**
   * The value det(A) = 33 means that the three row vectors (or column vectors) of Matrix A span a 3D parallelepiped (a slanted 3D box) with a volume of **33 cubic units**[cite: 19].
   * Because det(A) ≠ 0, the volume is non-zero, proving that Matrix A is non-singular and fully invertible[cite: 18, 19].
