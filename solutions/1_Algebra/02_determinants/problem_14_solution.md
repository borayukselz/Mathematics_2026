# Exercise 14: A System of Equations and the Determinant

### Given System and Matrix

**System of Equations:**
Ax = b

**Matrix A:**
[  1   2 ]
[  k   4 ]

**Right-Hand Side Vector b:**
[  b₁ ]
[  b₂ ]

---

### 1. Values of k for Which the System Has Exactly One Solution for Every b

* **Result:**
  The system Ax = b has **exactly one solution for every b** for all real values **k ≠ 2**.

* **Core Theorem:**
  A linear system Ax = b has a unique (exactly one) solution for every right-hand vector b if and only if Matrix A is **invertible**, which requires its determinant to be non-zero (**det(A) ≠ 0**)[cite: 18].

* **Detailed Calculation Steps:**
  1. Calculate det(A) using the 2x2 formula det = (a × d) - (b × c)[cite: 18]:
     det(A) = (1 × 4) - (2 × k)
     **det(A) = 4 - 2k**

  2. Set the condition for invertibility (det(A) ≠ 0)[cite: 18]:
     4 - 2k ≠ 0

  3. Solve for k:
     2k ≠ 4
     **k ≠ 2**

* **Conclusion:**
  When **k ≠ 2**, Matrix A is non-singular, A⁻¹ exists, and the unique solution can always be directly calculated as **x = A⁻¹b** for any vector b[cite: 18].

---

### 2. Analysis of the Remaining Value (k = 2)

When **k = 2**, Matrix A becomes:
[  1   2 ]
[  2   4 ]

Notice that **det(A) = (1 × 4) - (2 × 2) = 4 - 4 = 0**, meaning Matrix A is singular and not invertible[cite: 18].

The linear system Ax = b expands to two scalar equations:
1.  1*x₁ + 2*x₂ = b₁
2.  2*x₁ + 4*x₂ = b₂

Since the left-hand side of Equation 2 is exactly twice the left-hand side of Equation 1 (`2*(x₁ + 2*x₂) = 2x₁ + 4x₂`), consistency depends entirely on whether `b₂ = 2*b₁`.

---

#### A. Example of Vector b for Infinitely Many Solutions

* **Condition for Infinitely Many Solutions:**
  The right-hand side b must be consistent with the row dependence (`b₂ = 2*b₁`), making Equation 2 a redundant duplicate of Equation 1.

* **Chosen Vector b:**
  [  1 ]
  [  2 ]

* **System Calculation:**
  1.  x₁ + 2*x₂ = 1
  2.  2*x₁ + 4*x₂ = 2

* **Verification:**
  Divide Equation 2 by 2:
  (2*x₁ + 4*x₂) / 2 = 2 / 2  →  x₁ + 2*x₂ = 1
  
  Both equations represent the exact same line in 2D space. Expressing x₁ in terms of x₂:
  **x₁ = 1 - 2*x₂**
  
  Since x₂ can be chosen arbitrarily as any real parameter t, there are **infinitely many solutions** of the form:
  **x = [ 1 - 2t ; t ]** for all real numbers t.

---

#### B. Example of Vector b for No Solution

* **Condition for No Solution:**
  The right-hand side b must violate the row relationship (`b₂ ≠ 2*b₁`), causing a mathematical contradiction.

* **Chosen Vector b:**
  [  1 ]
  [  3 ]

* **System Calculation:**
  1.  x₁ + 2*x₂ = 1
  2.  2*x₁ + 4*x₂ = 3

* **Verification:**
  Multiply Equation 1 by 2:
  2*x₁ + 4*x₂ = 2
  
  Compare with Equation 2:
  2*x₁ + 4*x₂ = 3
  
  Subtracting the two equations yields:
  0 = 1 (Contradiction!)
  
  Because 0 can never equal 1, no values of x₁ and x₂ can satisfy both equations simultaneously. Thus, the system has **no solution** (inconsistent).

---

### 3. Summary Table of Solution Cases

| Parameter Value | Determinant | Vector b Condition | System Behavior | Geometric Interpretation |
|-----------------|-------------|--------------------|-----------------|--------------------------|
| **k ≠ 2**       | det(A) ≠ 0  | Any vector b       | **Exactly 1 Solution** | Lines intersect at a single unique point |
| **k = 2**       | det(A) = 0  | b₂ = 2*b₁ (e.g., [ 1 ; 2 ]) | **Infinitely Many Solutions** | Lines are identical (completely overlapping) |
| **k = 2**       | det(A) = 0  | b₂ ≠ 2*b₁ (e.g., [ 1 ; 3 ]) | **No Solution** | Lines are distinct and parallel |

---

### 4. Detailed Explanation & Linear Algebra Insights

1. **The Invertible Matrix Theorem Connection:**
   * The determinant serves as the central indicator for system stability[cite: 18].
   * When det(A) ≠ 0, the columns of Matrix A span all of 2D space (R²), guaranteeing that every target vector b can be reached uniquely[cite: 18].
   * When det(A) = 0, the column space collapses to a 1D line, meaning vector b can only be reached if it happens to lie on that exact 1D line (`b₂ = 2*b₁`)[cite: 18].

2. **Geometric Interpretation in 2D Space:**
   * Each equation in a 2x2 system represents a straight line in the Cartesian plane.
   * **When k ≠ 2:** The slopes of the two lines are different (-1/2 and -k/4), so they cross at exactly one intersection point regardless of b.
   * **When k = 2:** Both lines have the exact same slope (-1/2). They are parallel lines:
     * If they share the same y-intercept (`b₂ = 2*b₁`), they lie on top of each other, yielding infinite intersection points.
     * If they have different y-intercepts (`b₂ ≠ 2*b₁`), they never meet, yielding zero intersection points.
