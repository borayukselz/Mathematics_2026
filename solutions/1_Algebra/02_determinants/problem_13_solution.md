# Exercise 13: Determinant by Elimination

### Given Matrix

**Matrix A:**
[  1   2   3 ]
[  2   5   7 ]
[  1   0   2 ]

---

### 1. Summary of Elementary Row Operations and Determinant Effects

* **Row Replacement (Rᵢ ← Rᵢ + cRⱼ):** Adding a scalar multiple of one row to another **does not change** the determinant[cite: 19].
* All row operations used below are row replacements, so **det(A_new) = det(A_old)** at every step[cite: 19].

---

### 2. Step-by-Step Elimination to Upper Triangular Form

#### Step 1: Perform R₂ ← R₂ - 2R₁

* **Operation:** Eliminate entry at position (2,1)[cite: 19].
* **Calculation:**
  * Row 1 remains unchanged: [ 1, 2, 3 ]
  * Calculate new Row 2 (R₂ - 2R₁):
    * Entry (2,1): 2 - 2(1) = 0
    * Entry (2,2): 5 - 2(2) = 5 - 4 = 1
    * Entry (2,3): 7 - 2(3) = 7 - 6 = 1
  * Row 3 remains unchanged: [ 1, 0, 2 ]

* **Resulting Matrix A₁:**
  [  1   2   3 ]
  [  0   1   1 ]
  [  1   0   2 ]

* **Effect on Determinant:**
  Row replacement does not change the determinant[cite: 19].
  **det(A) = det(A₁)**[cite: 19]

---

#### Step 2: Perform R₃ ← R₃ - R₁

* **Operation:** Eliminate entry at position (3,1)[cite: 19].
* **Calculation:**
  * Row 1 remains unchanged: [ 1, 2, 3 ]
  * Row 2 remains unchanged: [ 0, 1, 1 ]
  * Calculate new Row 3 (R₃ - R₁):
    * Entry (3,1): 1 - 1 = 0
    * Entry (3,2): 0 - 2 = -2
    * Entry (3,3): 2 - 3 = -1

* **Resulting Matrix A₂:**
  [  1   2   3 ]
  [  0   1   1 ]
  [  0  -2  -1 ]

* **Effect on Determinant:**
  Row replacement does not change the determinant[cite: 19].
  **det(A) = det(A₁) = det(A₂)**[cite: 19]

---

#### Step 3: Perform R₃ ← R₃ + 2R₂

* **Operation:** Eliminate entry at position (3,2)[cite: 19].
* **Calculation:**
  * Row 1 remains unchanged: [ 1, 2, 3 ]
  * Row 2 remains unchanged: [ 0, 1, 1 ]
  * Calculate new Row 3 (R₃ + 2R₂):
    * Entry (3,1): 0 + 2(0) = 0
    * Entry (3,2): -2 + 2(1) = 0
    * Entry (3,3): -1 + 2(1) = -1 + 2 = 1

* **Resulting Matrix A₃ (Upper Triangular Form):**
  [  1   2   3 ]
  [  0   1   1 ]
  [  0   0   1 ]

* **Effect on Determinant:**
  Row replacement does not change the determinant[cite: 19].
  **det(A) = det(A₃)**[cite: 19]

---

### 3. Compute Determinant of the Triangular Matrix

* **Calculation:**
  The determinant of an upper triangular matrix equals the product of its main diagonal entries[cite: 18, 19]:
  det(A₃) = (1) × (1) × (1) = **1**

* **Final Result:**
  Since no row swaps or scaling operations were performed, det(A) = det(A₃):
  **det(A) = 1**

---

### 4. Mathematical Verification

#### Check 1: Sarrus' Rule
* **Down-Right Diagonals (Positive Terms):**
  (1 × 5 × 2) + (2 × 7 × 1) + (3 × 2 × 0) = 10 + 14 + 0 = **24**
* **Up-Right Diagonals (Negative Terms):**
  (1 × 5 × 3) + (0 × 7 × 1) + (2 × 2 × 2) = 15 + 0 + 8 = **23**
* **det(A):** 24 - 23 = **1**

#### Check 2: Cofactor Expansion along Row 3
* Row 3 contains [ 1, 0, 2 ]:
  det(A) = 1 × det[ 2, 3 ; 5, 7 ] - 0 + 2 × det[ 1, 2 ; 2, 5 ]
  det(A) = 1 × ((2 × 7) - (3 × 5)) + 2 × ((1 × 5) - (2 × 2))
  det(A) = 1 × (14 - 15) + 2 × (5 - 4)
  det(A) = 1 × (-1) + 2 × (1) = -1 + 2 = **1**

Both verification methods confirm that **det(A) = 1**.

---

### 5. Detailed Explanation & Linear Algebra Insights

1. **Efficiency of Gaussian Elimination for Determinants:**
   * Converting Matrix A to upper triangular form systematically reduces all entries below the diagonal to zero using row replacements[cite: 19].
   * Because row replacement operations preserve the exact determinant value, the final determinant is read directly off the main diagonal without tracking cumulative sign flips or scaling factors[cite: 18, 19].

2. **Geometric & Structural Meaning:**
   * **Invertibility:** Since det(A) = 1 ≠ 0, Matrix A is non-singular and fully **invertible**[cite: 18].
   * **Volume Preservation:** Geometrically, Matrix A transforms the 3D unit cube into a parallelepiped with an exact volume of **1 cubic unit**, keeping spatial volume completely preserved[cite: 18].
