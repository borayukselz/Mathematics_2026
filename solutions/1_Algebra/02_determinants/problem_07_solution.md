
# Exercise 7: Using Properties Instead of Recomputing

### Given

* **Matrix Dimension:** 3 × 3 (n = 3)[cite: 21]
* **Determinant:** det(A) = -4[cite: 21]

---

### 1. Compute det(2A)

* **Result:**
  **det(2A) = -32**[cite: 21]

* **Property Used:**
  For an n × n matrix A and scalar c:
  **det(cA) = cⁿ × det(A)**

* **Detailed Calculation Steps:**
  1. Identify matrix dimension: n = 3 (since A is a 3 × 3 matrix)[cite: 21]
  2. Identify scalar factor: c = 2[cite: 21]
  3. Apply general formula: det(2A) = 2³ × det(A)[cite: 21]
  4. Substitute det(A) = -4: det(2A) = 8 × (-4) = **-32**[cite: 21]

* **Method & Explanation:**
  Multiplying an entire 3 × 3 matrix by scalar 2 multiplies every entry in every row by 2[cite: 21]. Factoring 2 out of each of the 3 rows scales the determinant by 2 three separate times (2 × 2 × 2 = 2³ = 8)[cite: 21].

---

### 2. Compute det(Aᵀ)

* **Result:**
  **det(Aᵀ) = -4**[cite: 21]

* **Property Used:**
  The determinant of a matrix transpose equals the determinant of the original matrix:
  **det(Aᵀ) = det(A)**

* **Detailed Calculation Steps:**
  * Substitute det(A) = -4 directly:
    det(Aᵀ) = **-4**[cite: 21]

* **Method & Explanation:**
  Transposing a matrix swaps its rows and columns[cite: 8]. Because row operations and column operations affect determinants in identical ways, taking the transpose never changes the value of a square matrix's determinant[cite: 21].

---

### 3. Compute det(A²)

* **Result:**
  **det(A²) = 16**[cite: 21]

* **Property Used:**
  The determinant of a product of matrices equals the product of their individual determinants (Multiplicative Property):
  **det(AB) = det(A) × det(B)**
  For integer powers: **det(Aᵏ) = (det(A))ᵏ**

* **Detailed Calculation Steps:**
  1. Apply multiplicative property for k = 2:
     det(A²) = det(A × A) = det(A) × det(A) = (det(A))²[cite: 21]
  2. Substitute det(A) = -4:
     det(A²) = (-4)² = **16**[cite: 21]

* **Method & Explanation:**
  Because the determinant function is multiplicative, squaring a matrix simply squares its scalar determinant value[cite: 21].

---

### 4. Compute det(-A)

* **Result:**
  **det(-A) = 4**[cite: 21]

* **Property Used:**
  Negating a matrix is equivalent to multiplying by scalar c = -1 for an n × n matrix:
  **det(-A) = (-1)ⁿ × det(A)**

* **Detailed Calculation Steps:**
  1. Identify matrix dimension: n = 3 (odd dimension)[cite: 21]
  2. Calculate scale factor: (-1)³ = -1
  3. Apply formula: det(-A) = (-1)³ × det(A) = -1 × det(A)[cite: 21]
  4. Substitute det(A) = -4:
     det(-A) = -1 × (-4) = **4**[cite: 21]

* **Method & Explanation:**
  Negating a 3 × 3 matrix multiplies all 3 rows by -1[cite: 21]. Each row negation multiplies the overall determinant by -1. Three sign changes yield (-1) × (-1) × (-1) = -1, which reverses the negative sign of det(A)[cite: 21].

---

### Summary Table of Results

| Target Expression | Property Rule / Formula | Substitution / Calculation | Final Value |
|-------------------|-------------------------|----------------------------|-------------|
| det(2A)           | 2³ × det(A)             | 8 × (-4)                   | -32         |
| det(Aᵀ)           | det(A)                  | -4                         | -4          |
| det(A²)           | (det(A))²               | (-4)²                      | 16          |
| det(-A)           | (-1)³ × det(A)          | -1 × (-4)                  | 4           |

---

### Detailed Explanation & Linear Algebra Insights

1. **Scaling a Single Row vs. Scaling an Entire Matrix:**
   * Scaling **one row** of an n × n matrix by scalar c scales the determinant by **c**[cite: 19].
   * Scaling the **entire matrix** by c scales all n rows simultaneously, scaling the determinant by **cⁿ**[cite: 21].
   * This is why det(2A) = 2³ × det(A) = -32, NOT 2 × (-4) = -8[cite: 21]!

2. **Odd vs. Even Matrix Dimensions for Matrix Negation:**
   * For an **even-dimensional** matrix (e.g., 2 × 2 or 4 × 4), det(-A) = (-1)ⁿ det(A) = det(A).
   * For an **odd-dimensional** matrix (e.g., 3 × 3 or 5 × 5), det(-A) = (-1)ⁿ det(A) = -det(A)[cite: 21].
   * Because Matrix A is 3 × 3 (odd), det(-A) flips sign from -4 to +4[cite: 21].

3. **Geometric Volume Interpretation:**
   * A determinant det(A) = -4 means Matrix A transforms 3D space by scaling volumes by a factor of 4 while reversing spatial orientation[cite: 19, 21].
   * Scaling all 3 spatial directions by a factor of 2 (matrix 2A) expands 3D volume by 2 × 2 × 2 = 8 times, giving a total volume factor of 8 × 4 = 32 (with reversed orientation, resulting in -32)[cite: 21].

```
