# Exercise 12: A Parameter Revealed by a Row Operation

### Given Family of Matrices

**Matrix A(t):**
[  1   2   3 ]
[  2   4   t ]
[  0   1   1 ][cite: 26]

---

### 1. Perform Row Operation R₂ ← R₂ - 2R₁

* **Operation:**
  Elementary row replacement subtracting 2 times Row 1 from Row 2[cite: 26].

* **Detailed Calculation Steps:**
  * Row 1 remains unchanged: [ 1, 2, 3 ][cite: 26]
  * Calculate new Row 2 (R₂ - 2R₁):
    * Entry (2,1): 2 - 2(1) = 2 - 2 = 0
    * Entry (2,2): 4 - 2(2) = 4 - 4 = 0
    * Entry (2,3): t - 2(3) = t - 6
  * Row 3 remains unchanged: [ 0, 1, 1 ][cite: 26]

* **Resulting Transformed Matrix A₁(t):**
  [  1   2    3  ]
  [  0   0   t-6 ]
  [  0   1    1  ]

* **Effect on Determinant:**
  Adding a scalar multiple of one row to another **does not change** the determinant[cite: 19].
  **det(A(t)) = det(A₁(t))**[cite: 19]

---

### 2. Compute det(A(t)) Using the Resulting Structure

#### Method A: Row Swap to Upper Triangular Form
1. Swap Row 2 and Row 3 of Matrix A₁(t):
   * Swapping two rows multiplies the determinant by **-1**[cite: 20].

   [  1   2    3  ]
   [  0   1    1  ]
   [  0   0   t-6 ]

2. The matrix is now in **Upper Triangular Form**[cite: 18]. The determinant of an upper triangular matrix equals the product of its main diagonal entries[cite: 18]:
   det(Triangular) = 1 × 1 × (t - 6) = **t - 6**

3. Account for the row swap sign change[cite: 20]:
   det(A(t)) = -1 × (t - 6) = **6 - t**

#### Method B: Cofactor Expansion along Row 2
* Row 2 of A₁(t) contains two zeros: [ 0, 0, t - 6 ].
* Expand along Row 2:
  det(A(t)) = (t - 6) × (-1)²⁺³ × det[ 1, 2 ; 0, 1 ]
  det(A(t)) = (t - 6) × (-1) × ((1 × 1) - (2 × 0))
  det(A(t)) = -(t - 6) = **6 - t**

* **Final Determinant Formula:**
  **det(A(t)) = 6 - t**

---

### 3. Find Values of t for Which Matrix A(t) is Not Invertible

* **Result:**
  Matrix A(t) is **not invertible** when **t = 6**[cite: 26].

* **Detailed Calculation Steps:**
  1. A matrix is non-invertible (singular) if and only if its determinant equals zero (**det = 0**)[cite: 18, 20].
  2. Set the determinant equal to 0:
     6 - t = 0
  3. Solve for t:
     **t = 6**

---

### 4. What Special Thing Happens to the Rows when t = 6?

* **Row Structure at t = 6:**
  When t = 6, substitute t = 6 back into the original Matrix A(6)[cite: 26]:
  [  1   2   3 ]
  [  2   4   6 ]
  [  0   1   1 ]

* **Special Properties of the Rows:**
  1. **Direct Proportionality / Row Dependence:**
     Row 2 becomes an exact scalar multiple of Row 1:
     **Row 2 = 2 × Row 1** ([ 2, 4, 6 ] = 2 × [ 1, 2, 3 ])[cite: 24].

  2. **Creation of a Zero Row:**
     In the transformed matrix A₁(6), the entire second row collapses to zeros:
     Row 2 = [ 0, 0, 6 - 6 ] = **[ 0, 0, 0 ]**.

  3. **Linear Dependence & Rank Loss:**
     Because Row 2 is linearly dependent on Row 1, the matrix loses full row rank (rank becomes 2 instead of 3)[cite: 24]. The three row vectors span a 2D plane instead of 3D space, collapsing the 3D volume to zero and making the transformation non-invertible[cite: 18, 24].

---

### 5. Verification Checks

#### Check 1: Sarrus' Rule on Original Matrix A(t)
* **Original Matrix A(t):** [ 1, 2, 3 ; 2, 4, t ; 0, 1, 1 ][cite: 26]
* **Down-Right Diagonals (Positive Terms):**
  (1 × 4 × 1) + (2 × t × 0) + (3 × 2 × 1) = 4 + 0 + 6 = **10**
* **Up-Right Diagonals (Negative Terms):**
  (0 × 4 × 3) + (1 × t × 1) + (1 × 2 × 2) = 0 + t + 4 = **t + 4**
* **det(A(t)):** 10 - (t + 4) = **6 - t**

#### Check 2: Cofactor Expansion along Column 1 of Original Matrix A(t)
* Column 1 contains entries [ 1, 2, 0 ][cite: 26]:
  det(A(t)) = 1 × det[ 4, t ; 1, 1 ] - 2 × det[ 2, 3 ; 1, 1 ] + 0
  det(A(t)) = 1 × (4 - t) - 2 × (2 - 3)
  det(A(t)) = (4 - t) - 2 × (-1) = 4 - t + 2 = **6 - t**

Both verification methods confirm that **det(A(t)) = 6 - t** and **t = 6** causes non-invertibility[cite: 18, 26].

---

### 6. Detailed Explanation & Linear Algebra Insights

1. **Why Performing a Row Operation First Makes the Problem Easier:**
   * Performing `R₂ ← R₂ - 2R₁` creates two zeros in Row 2 simultaneously: `[ 0, 0, t - 6 ]`[cite: 26].
   * This immediately reveals the critical parameter value (t = 6) by inspection, showing where Row 2 becomes all zeros without needing a lengthy determinant formula[cite: 26].

2. **Parameter Dependence in Matrix Families:**
   * For any value **t ≠ 6**, det(A(t)) ≠ 0, so Matrix A(t) is non-singular and fully invertible[cite: 18].
   * At the unique critical point **t = 6**, det(A(6)) = 0, causing the matrix to become singular and non-invertible[cite: 18, 26].
