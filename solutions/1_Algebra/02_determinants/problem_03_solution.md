# Exercise 3: Swapping Two Rows

### Given Matrix

**Matrix A:**
[  1   2   0 ]
[  0   3   1 ]
[  2   1   1 ][cite: 20]

---

### 1. Compute det(A)

* **Result:**
  **det(A) = 6**[cite: 20]

* **Detailed Calculation Steps (via Cofactor Expansion along Column 1):**
  * Column 1 contains [ 1, 0, 2 ][cite: 20]. Expanding along Column 1 minimizes calculations:
    det(A) = 1 × det[ 3, 1 ; 1, 1 ] - 0 × det[ 2, 0 ; 1, 1 ] + 2 × det[ 2, 0 ; 3, 1 ][cite: 20]

  * Compute the 2×2 sub-determinants:
    * det[ 3, 1 ; 1, 1 ] = (3 × 1) - (1 × 1) = 3 - 1 = **2**
    * det[ 2, 0 ; 3, 1 ] = (2 × 1) - (0 × 3) = 2 - 0 = **2**

  * Combine the terms:
    det(A) = 1(2) - 0 + 2(2) = 2 + 4 = **6**

* **Method & Explanation:**
  Cofactor expansion calculates a 3×3 determinant by breaking it down into a weighted sum of smaller 2×2 determinants[cite: 20].

* **Mathematical Verification (via Sarrus' Rule):**
  * Down-Right Diagonals: (1×3×1) + (2×1×2) + (0×0×1) = 3 + 4 + 0 = **7**[cite: 20]
  * Up-Right Diagonals: (2×3×0) + (1×1×1) + (1×0×2) = 0 + 1 + 0 = **1**[cite: 20]
  * det(A) = 7 - 1 = **6**

---

### 2. Form Matrix B and Predict det(B)

#### A. Form Matrix B
Matrix B is formed by swapping Row 1 and Row 2 of Matrix A[cite: 20]:

* **Row 1 of B** = [ 0, 3, 1 ] (Original Row 2 of A)[cite: 20]
* **Row 2 of B** = [ 1, 2, 0 ] (Original Row 1 of A)[cite: 20]
* **Row 3 of B** = [ 2, 1, 1 ] (Original Row 3 of A)[cite: 20]

**Matrix B:**
[  0   3   1 ]
[  1   2   0 ]
[  2   1   1 ][cite: 20]

---

#### B. Predict det(B) Using Determinant Property

* **Determinant Property:**
  Interchanging (swapping) any two rows (or two columns) of a matrix multiplies its determinant by **-1** (it reverses the sign of the determinant)[cite: 20].

* **Prediction:**
  Since Matrix B is derived by performing a single row swap on Matrix A[cite: 20]:
  det(B) = -det(A) = **-6**[cite: 20]

---

### 3. Verify det(B) by Calculation

* **Result:**
  **det(B) = -6**[cite: 20]

* **Detailed Calculation Steps (via Cofactor Expansion along Column 1 of B):**
  * Column 1 of Matrix B contains [ 0, 1, 2 ][cite: 20]:
    det(B) = 0 × det[ 2, 0 ; 1, 1 ] - 1 × det[ 3, 1 ; 1, 1 ] + 2 × det[ 3, 1 ; 2, 0 ][cite: 20]

  * Compute the 2×2 sub-determinants:
    * det[ 3, 1 ; 1, 1 ] = (3 × 1) - (1 × 1) = 3 - 1 = **2**
    * det[ 3, 1 ; 2, 0 ] = (3 × 0) - (1 × 2) = 0 - 2 = **-2**

  * Combine the terms:
    det(B) = 0 - 1(2) + 2(-2) = -2 - 4 = **-6**

* **Conclusion:**
  The direct calculation yields **-6**, which perfectly matches our prediction made using the row swap property[cite: 20]!

---

### 4. Detailed Explanation & Linear Algebra Insights

1. **Why Swapping Rows Changes the Sign:**
   * The formal definition of a determinant sums products over all permutations of matrix indices, weighted by the **sign (parity)** of each permutation.
   * Swapping two rows introduces exactly one additional transposition (swap) into every permutation.
   * Adding one transposition changes the parity of every term from positive to negative (or negative to positive), causing the overall determinant to flip its sign from **det(A)** to **-det(A)**[cite: 20].

2. **Geometric Meaning of Sign Change (Orientation in 3D Space):**
   * The absolute value |det(A)| = 6 represents the **3D volume** spanned by the row vectors of Matrix A.
   * The **sign** (+ or -) represents the **spatial orientation** (handedness) of the coordinate system defined by those vectors (right-handed vs. left-handed system).
   * Swapping two row vectors physically reflects the vector system across a plane, reversing its orientation (from right-handed to left-handed) while leaving the enclosed volume (6 cubic units) completely unchanged.

3. **Connection to Elementary Permutation Matrices:**
   * Swapping Row 1 and Row 2 is equivalent to multiplying Matrix A on the left by an elementary permutation matrix E:
     **E = [ 0, 1, 0 ; 1, 0, 0 ; 0, 0, 1 ]**
   * The determinant of this permutation matrix is **det(E) = -1**.
   * By the multiplicative property of determinants:
     **det(B) = det(E × A) = det(E) × det(A) = (-1) × 6 = -6**[cite: 20].
