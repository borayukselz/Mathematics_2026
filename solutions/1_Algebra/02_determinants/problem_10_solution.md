# Exercise 10: Detecting Dependence

### Given Matrix

**Matrix A:**
[  1   2   3 ]
[  2   4   6 ]
[  0   1   5 ][cite: 24]

---

### 1. Identify Specific Dependence Between Rows

* **Result:**
  **Row 2 is a direct scalar multiple of Row 1:**
  **R₂ = 2 × R₁**[cite: 24]

* **Detailed Comparison:**
  * Row 1 (R₁): [ 1, 2, 3 ][cite: 24]
  * Row 2 (R₂): [ 2, 4, 6 ] = 2 × [ 1, 2, 3 ][cite: 24]
  * Row 3 (R₃): [ 0, 1, 5 ][cite: 24]

* **Method & Explanation:**
  Two rows are linearly dependent if one row is an exact scalar multiple of another[cite: 24]. Here, every entry in Row 2 is exactly twice the corresponding entry in Row 1 (2 = 2×1, 4 = 2×2, 6 = 2×3)[cite: 24].

---

### 2. Explain Why det(A) = 0 Without Full Calculation

* **Property Rule:**
  If a square matrix has two proportional (linearly dependent) rows, its determinant is **equal to 0**[cite: 24].

* **Justification via Row Replacement:**
  1. Perform the elementary row replacement **R₂ ← R₂ - 2R₁**[cite: 19].
  2. Adding a scalar multiple of one row to another row **does not change** the value of the determinant[cite: 19].
  3. Calculating the new second row gives:
     [ 2 - 2(1), 4 - 2(2), 6 - 2(3) ] = [ 0, 0, 0 ]
  4. The matrix becomes:
     [  1   2   3 ]
     [  0   0   0 ]
     [  0   1   5 ]
  5. Any matrix containing a row of all zeros has a determinant of **0** (expanding along the zero row yields 0)[cite: 24].

---

### 3. Connect Row Dependence with Noninvertibility

* **Invertibility Criterion:**
  A square matrix is invertible if and only if its determinant is non-zero (**det(A) ≠ 0**)[cite: 18].

* **Connection to Noninvertibility:**
  * **Zero Determinant:** Because row dependence causes **det(A) = 0**, Matrix A is singular and therefore **not invertible**[cite: 18, 24].
  * **Reduced Rank:** Linear dependence means the three rows do not contain three independent directions of information[cite: 24]. Matrix A has rank 2 instead of full rank 3.
  * **Geometric Collapse:** Matrix A maps 3D space onto a 2D plane (collapsing 3D volume to zero)[cite: 18]. Because 3D space collapses onto a flattened plane, multiple distinct points get squished together, making it impossible to uniquely reverse the transformation (noninvertible)[cite: 18, 24].

---

### 4. Mathematical Verification (Quick Check)

* **Verification via Sarrus' Rule:**
  * **Down-Right Diagonals:**
    (1 × 4 × 5) + (2 × 6 × 0) + (3 × 2 × 1) = 20 + 0 + 6 = **26**[cite: 24]
  * **Up-Right Diagonals:**
    (0 × 4 × 3) + (1 × 6 × 1) + (5 × 2 × 2) = 0 + 6 + 20 = **26**[cite: 24]
  * **det(A):** 26 - 26 = **0**[cite: 24]

* **Conclusion:**
  Direct calculation confirms **det(A) = 0**, fully validating the structural row-dependence analysis[cite: 24].
