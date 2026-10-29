# Exercise 1: Determinant of a 2x2 Matrix

### Given Matrices

**Matrix A:**
[  3  -2 ]
[  5   4 ]

**Matrix B:**
[  1   7 ]
[  2  14 ]

---

### Core Formula for 2x2 Determinant

For any 2x2 matrix M = [ a, b ; c, d ], the determinant is calculated as[cite: 18]:
**det(M) = (a × d) - (b × c)**
(Main diagonal product minus anti-diagonal product)

---

### 1. Compute Determinants

#### A. Compute det(Matrix A)

* **Result:**
  **det(A) = 22**[cite: 18]

* **Detailed Calculation Steps:**
  * Identify elements from Matrix A[cite: 18]: a = 3, b = -2, c = 5, d = 4
  * Main diagonal product (a × d): 3 × 4 = 12
  * Anti-diagonal product (b × c): (-2) × 5 = -10
  * Apply formula: det(A) = 12 - (-10) = 12 + 10 = **22**

* **Method & Explanation:**
  Multiply the top-left element by the bottom-right element, then subtract the product of the top-right and bottom-left elements[cite: 18].

* **Mathematical Verification:**
  3 × 4 - (-2 × 5) = 12 + 10 = 22. Calculation verified.

---

#### B. Compute det(Matrix B)

* **Result:**
  **det(B) = 0**[cite: 18]

* **Detailed Calculation Steps:**
  * Identify elements from Matrix B[cite: 18]: a = 1, b = 7, c = 2, d = 14
  * Main diagonal product (a × d): 1 × 14 = 14
  * Anti-diagonal product (b × c): 7 × 2 = 14
  * Apply formula: det(B) = 14 - 14 = **0**

* **Method & Explanation:**
  Multiply the top-left element by the bottom-right element, then subtract the product of the top-right and bottom-left elements[cite: 18].

* **Mathematical Verification:**
  1 × 14 - 7 × 2 = 14 - 14 = 0. Calculation verified.

---

### 2. Which Matrix is Invertible? Justification

* **Result:**
  **Matrix A is invertible**, while **Matrix B is not invertible** (singular)[cite: 18].

* **Justification:**
  * **Invertibility Criterion:** A square matrix M is invertible if and only if its determinant is non-zero (**det(M) ≠ 0**)[cite: 18].
  * **For Matrix A:** Since **det(A) = 22 ≠ 0**, Matrix A is non-singular and therefore **invertible**[cite: 18].
  * **For Matrix B:** Since **det(B) = 0**, Matrix B is singular and therefore **not invertible**[cite: 18].

---

### 3. Detailed Explanation & Linear Algebra Insights

1. **Why det(M) ≠ 0 Guarantees Invertibility:**
   * The explicit formula for the inverse of a 2x2 matrix M = [ a, b ; c, d ] is:
     **M⁻¹ = (1 / det(M)) × [ d, -b ; -c, a ]**
   * Notice that the formula requires dividing by **det(M)**.
   * If det(M) = 0, division by zero occurs, making the matrix inverse mathematically undefined.
   * **For Matrix A:** A⁻¹ = (1 / 22) × [ 4, 2 ; -5, 3 ] = [ 4/22, 2/22 ; -5/22, 3/22 ].
   * **For Matrix B:** B⁻¹ would require dividing by 0, which is impossible.

2. **Geometric Interpretation of the Determinant:**
   * In 2D space, the absolute value of the determinant |det(M)| represents the **area scaling factor** of the linear transformation defined by matrix M.
   * **For Matrix A (|det(A)| = 22):** A unit square transformed by Matrix A stretches into a parallelogram with an area of 22 square units. Because the area is non-zero, the transformed space occupies 2D area, and the original vectors can be uniquely recovered (reversible).
   * **For Matrix B (det(B) = 0):** A unit square transformed by Matrix B collapses completely into a 1D line segment (area = 0). Because 2D space collapses onto a 1D line, information is lost, making it impossible to undo the transformation (irreversible).

3. **Linear Dependence of Rows and Columns in Matrix B:**
   * Look closely at Matrix B = [ 1, 7 ; 2, 14 ][cite: 18]:
     * Row 2 is a direct scalar multiple of Row 1: **[ 2, 14 ] = 2 × [ 1, 7 ]**[cite: 18].
     * Column 2 is a direct scalar multiple of Column 1: **[ 7, 14 ] = 7 × [ 1, 2 ]**[cite: 18].
   * Whenever rows or columns of a matrix are linearly dependent (proportional), the determinant is always zero, confirming the matrix cannot be inverted[cite: 18].
