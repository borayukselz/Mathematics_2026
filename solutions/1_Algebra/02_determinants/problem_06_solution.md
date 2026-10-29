# Exercise 6: Parameter and Invertibility

### Given Family of Matrices

**Matrix A(t):**
[  t   1 ]
[  2   t ][cite: 20]

---

### 1. Compute det(A(t))

* **Result:**
  **det(A(t)) = t² - 2**[cite: 20]

* **Detailed Calculation Steps:**
  * Identify elements of Matrix A(t)[cite: 20]: a = t, b = 1, c = 2, d = t
  * Main diagonal product (a × d): t × t = **t²**
  * Anti-diagonal product (b × c): 1 × 2 = **2**
  * Apply determinant formula det = (a × d) - (b × c)[cite: 18]:
    det(A(t)) = **t² - 2**[cite: 20]

* **Method & Explanation:**
  The determinant of a 2x2 matrix is computed by multiplying the main diagonal elements and subtracting the product of the off-diagonal elements[cite: 18].

---

### 2. Find Values of t for Which A(t) is Not Invertible

* **Result:**
  The matrix A(t) is **not invertible** for **t = √2** and **t = -√2** (or approximately t ≈ 1.414 and t ≈ -1.414)[cite: 20].

* **Detailed Calculation Steps:**
  1. Set the determinant equal to zero[cite: 20]:
     t² - 2 = 0[cite: 20]

  2. Solve the algebraic equation for t:
     t² = 2
     t = ±√2

  3. List the solutions:
     * **t₁ = √2**[cite: 20]
     * **t₂ = -√2**[cite: 20]

---

### 3. Explanation of Relationship to Determinant Being Zero

* **Core Theorem of Invertibility:**
  A square matrix M is **invertible** if and only if its determinant is non-zero (**det(M) ≠ 0**)[cite: 18]. Conversely, a matrix is **not invertible** (singular) if and only if its determinant is equal to zero (**det(M) = 0**)[cite: 18, 20].

* **Direct Relationship in This Problem:**
  * To find the exact parameter values of t that cause Matrix A(t) to lose invertibility, we must solve for where the determinant function collapses to zero[cite: 20].
  * For any value **t ≠ ±√2**, det(A(t)) ≠ 0, meaning the matrix **is invertible**[cite: 18].
  * At the critical parameter values **t = √2** and **t = -√2**, det(A(t)) = 0, meaning the matrix **is not invertible**[cite: 18, 20].

---

### 4. Mathematical Verification

#### Case 1: Plug in t = √2
* **Matrix:**
  A(√2) = [  √2   1 ]
          [   2  √2 ]

* **Determinant:**
  det(A(√2)) = (√2 × √2) - (1 × 2) = 2 - 2 = **0**

* **Row Relationship:**
  Observe that Row 2 is exactly **√2 times Row 1**:
  [ 2, √2 ] = √2 × [ √2, 1 ]
  Because the rows are linearly dependent (proportional), the matrix is singular and not invertible[cite: 18].

---

#### Case 2: Plug in t = -√2
* **Matrix:**
  A(-√2) = [ -√2   1 ]
           [   2 -√2 ]

* **Determinant:**
  det(A(-√2)) = (-√2 × -√2) - (1 × 2) = 2 - 2 = **0**

* **Row Relationship:**
  Observe that Row 2 is exactly **-√2 times Row 1**:
  [ 2, -√2 ] = -√2 × [ -√2, 1 ]
  Because the rows are linearly dependent (proportional), the matrix is singular and not invertible[cite: 18].

---

### 5. Detailed Explanation & Linear Algebra Insights

1. **Why det = 0 Prevents Matrix Inversion (Algebraic Perspective):**
   * The explicit formula for the inverse of a 2x2 matrix A(t) is:
     **A(t)⁻¹ = (1 / det(A(t))) × [ t, -1 ; -2, t ]**
   * If t = ±√2, det(A(t)) = 0, which requires division by zero (1 / 0). Since division by zero is mathematically undefined, the inverse matrix **A(t)⁻¹ cannot exist**.

2. **Loss of Dimension (Geometric Perspective):**
   * The determinant measures how much a linear transformation scales 2D areas.
   * When **t ≠ ±√2**, Matrix A(t) transforms a 2D square into a parallelogram with non-zero area (det = t² - 2), so points can be uniquely mapped backward (reversible)[cite: 18].
   * When **t = ±√2**, the area scaling factor becomes zero (det = 0). The transformation completely collapses 2D space onto a 1D line, destroying dimensional information and making it impossible to undo the operation[cite: 18].

3. **Systems of Linear Equations Perspective:**
   * Consider the system A(t)x = b.
   * If **t ≠ ±√2**, the system has a unique solution for any right-hand vector b.
   * If **t = ±√2**, the system either has infinitely many solutions or no solution at all, depending on vector b.
