# Exercise 11: Shortening the Calculation with Row Operations

### Given Matrix

**Matrix A:**
[  1   2   3 ]
[  1   3   4 ]
[  1   4   6 ][cite: 25]

---

### 1. Operations That Do Not Change the Determinant

* **Core Determinant Property:**
  Performing an **elementary row replacement**—adding or subtracting a scalar multiple of one row to another row—**does NOT change the value of the determinant**[cite: 19, 25]:
  **det(A_new) = det(A_old)**

* **Operations Used in This Solution:**
  1. **R₂ ← R₂ - R₁** (Subtract Row 1 from Row 2)[cite: 25] → *Determinant remains unchanged.*
  2. **R₃ ← R₃ - R₁** (Subtract Row 1 from Row 3)[cite: 25] → *Determinant remains unchanged.*
  3. **R₃ ← R₃ - 2R₂** (Subtract 2 times Row 2 from Row 3)[cite: 25] → *Determinant remains unchanged.*

---

### 2. Step-by-Step Matrix Reduction to Create Zeros

#### Step 1: Create Zero at Position (2,1) using R₂ ← R₂ - R₁

* **Calculation:**
  * Row 1 remains unchanged: [ 1, 2, 3 ][cite: 25]
  * Calculate new Row 2 (R₂ - R₁):
    * Entry (2,1): 1 - 1 = 0
    * Entry (2,2): 3 - 2 = 1
    * Entry (2,3): 4 - 3 = 1
  * Row 3 remains unchanged: [ 1, 4, 6 ][cite: 25]

* **Resulting Matrix A₁:**
  [  1   2   3 ]
  [  0   1   1 ]
  [  1   4   6 ]

* **Effect on Determinant:**
  **det(A) = det(A₁)**[cite: 19, 25]

---

#### Step 2: Create Zero at Position (3,1) using R₃ ← R₃ - R₁

* **Calculation:**
  * Row 1 remains unchanged: [ 1, 2, 3 ][cite: 25]
  * Row 2 remains unchanged: [ 0, 1, 1 ]
  * Calculate new Row 3 (R₃ - R₁):
    * Entry (3,1): 1 - 1 = 0
    * Entry (3,2): 4 - 2 = 2
    * Entry (3,3): 6 - 3 = 3

* **Resulting Matrix A₂:**
  [  1   2   3 ]
  [  0   1   1 ]
  [  0   2   3 ]

* **Effect on Determinant:**
  **det(A) = det(A₁) = det(A₂)**[cite: 19, 25]

---

#### Step 3: Create Zero at Position (3,2) using R₃ ← R₃ - 2R₂

* **Calculation:**
  * Row 1 remains unchanged: [ 1, 2, 3 ][cite: 25]
  * Row 2 remains unchanged: [ 0, 1, 1 ]
  * Calculate new Row 3 (R₃ - 2R₂):
    * Entry (3,1): 0 - 2(0) = 0
    * Entry (3,2): 2 - 2(1) = 0
    * Entry (3,3): 3 - 2(1) = 1

* **Resulting Matrix A₃ (Upper Triangular Form):**
  [  1   2   3 ]
  [  0   1   1 ]
  [  0   0   1 ]

* **Effect on Determinant:**
  **det(A) = det(A₃)**[cite: 19, 25]

---

### 3. Compute det(A)

#### Method 1: Product of Main Diagonal Entries (Upper Triangular Matrix)
* For any upper triangular matrix, the determinant equals the product of its main diagonal entries[cite: 18, 19]:
  det(A) = det(A₃) = (1) × (1) × (1) = **1**

#### Method 2: Cofactor Expansion along Column 1 of Matrix A₂
* Column 1 of Matrix A₂ contains entries [ 1, 0, 0 ][cite: 25]:
  det(A) = 1 × det[ 1, 1 ; 2, 3 ] - 0 + 0
  det(A) = 1 × ((1 × 3) - (1 × 2))
  det(A) = 1 × (3 - 2) = **1**

* **Final Result:**
  **det(A) = 1**[cite: 25]

---

### 4. Mathematical Verification

#### Verification Check: Sarrus' Rule on Original Matrix A
* **Original Matrix A:** [ 1, 2, 3 ; 1, 3, 4 ; 1, 4, 6 ][cite: 25]
* **Down-Right Diagonals (Positive Terms):**
  (1 × 3 × 6) + (2 × 4 × 1) + (3 × 1 × 4) = 18 + 8 + 12 = **38**[cite: 25]
* **Up-Right Diagonals (Negative Terms):**
  (1 × 3 × 3) + (4 × 4 × 1) + (6 × 1 × 2) = 9 + 16 + 12 = **37**[cite: 25]
* **det(A):** 38 - 37 = **1**[cite: 25]

Both methods yield the exact same value (**1**), verifying the calculation[cite: 25].

---

### 5. Detailed Explanation & Linear Algebra Insights

1. **Strategic Planning vs. Mechanical Calculation:**
   * Notice that Column 1 of original Matrix A has identical leading entries: [ 1, 1, 1 ][cite: 25].
   * Recognizing this structure allows us to subtract Row 1 from both Row 2 and Row 3 simultaneously, introducing two zeros in a single step[cite: 25].
   * Reducing the problem to an upper triangular form avoids evaluating six separate multi-digit multiplication terms required by Sarrus' rule[cite: 19, 25].

2. **Cofactor Simplification via Zeros:**
   * Expanding a determinant along a row or column with k zeros eliminates k calculation branches completely.
   * Creating a column with entries [ 1, 0, 0 ] reduces a 3×3 determinant directly to a single 2×2 sub-determinant without altering the overall value[cite: 18, 25].

3. **Invertibility & Geometric Meaning:**
   * Since det(A) = 1 ≠ 0, Matrix A is non-singular and fully **invertible**[cite: 18].
   * Geometrically, Matrix A transforms the 3D unit cube into a parallelepiped with an exact volume of **1 cubic unit**, preserving spatial volume perfectly[cite: 18, 25].
