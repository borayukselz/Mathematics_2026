# Exercise 5: Row Operations

### Given Matrix

**Matrix A:**
[  1   2   3 ]
[  2   1   0 ]
[ -1   4   2 ][cite: 19]

---

### Core Determinant Rules for Elementary Row Operations

1. **Row Replacement (Rᵢ ← Rᵢ + cRⱼ):**
   Adding a scalar multiple of one row to another row **does not change** the determinant[cite: 19]:
   **det(A_new) = det(A_old)**

2. **Row Interchange (Rᵢ ↔ Rⱼ):**
   Swapping two rows multiplies the determinant by **-1**:
   **det(A_new) = -det(A_old)**

3. **Row Scaling (Rᵢ ← cRᵢ):**
   Multiplying a row by a non-zero scalar c multiplies the determinant by **c** (or factoring out c from a row scales the determinant by c):
   **det(A_old) = c × det(A_factored)**

---

### Step-by-Step Matrix Reduction and Determinant Tracking

#### Step 1: Perform R₂ ← R₂ - 2R₁

* **Operation:** Elementary row replacement to eliminate entry (2,1)[cite: 19].
* **Calculation:**
  * Row 1 remains unchanged: [ 1, 2, 3 ][cite: 19]
  * Calculate new Row 2 (R₂ - 2R₁):
    * Entry (2,1):  2 - 2(1) = 0
    * Entry (2,2):  1 - 2(2) = 1 - 4 = -3
    * Entry (2,3):  0 - 2(3) = 0 - 6 = -6
  * Row 3 remains unchanged: [ -1, 4, 2 ][cite: 19]

* **Resulting Matrix A₁:**
  [  1   2   3 ]
  [  0  -3  -6 ]
  [ -1   4   2 ]

* **Effect on Determinant:**
  Row replacement does not change the determinant[cite: 19].
  **det(A) = det(A₁)**

---

#### Step 2: Perform R₃ ← R₃ + R₁

* **Operation:** Elementary row replacement to eliminate entry (3,1)[cite: 19].
* **Calculation:**
  * Row 1 remains unchanged: [ 1, 2, 3 ][cite: 19]
  * Row 2 remains unchanged: [ 0, -3, -6 ]
  * Calculate new Row 3 (R₃ + R₁):
    * Entry (3,1): -1 + 1 = 0
    * Entry (3,2):  4 + 2 = 6
    * Entry (3,3):  2 + 3 = 5

* **Resulting Matrix A₂:**
  [  1   2   3 ]
  [  0  -3  -6 ]
  [  0   6   5 ]

* **Effect on Determinant:**
  Row replacement does not change the determinant[cite: 19].
  **det(A) = det(A₁) = det(A₂)**

---

#### Step 3: Perform R₃ ← R₃ + 2R₂

* **Operation:** Elementary row replacement to eliminate entry (3,2)[cite: 19].
* **Calculation:**
  * Row 1 remains unchanged: [ 1, 2, 3 ][cite: 19]
  * Row 2 remains unchanged: [ 0, -3, -6 ]
  * Calculate new Row 3 (R₃ + 2R₂):
    * Entry (3,1): 0 + 2(0)  = 0
    * Entry (3,2): 6 + 2(-3) = 6 - 6 = 0
    * Entry (3,3): 5 + 2(-6) = 5 - 12 = -7

* **Resulting Matrix A₃ (Upper Triangular Form):**
  [  1   2   3 ]
  [  0  -3  -6 ]
  [  0   0  -7 ]

* **Effect on Determinant:**
  Row replacement does not change the determinant[cite: 19].
  **det(A) = det(A₃)**

---

### Compute Determinant of the Triangular Matrix

* **Calculation:**
  For an upper triangular matrix, the determinant equals the product of its main diagonal entries[cite: 18, 19]:
  det(A₃) = (1) × (-3) × (-7) = **21**

* **Final Result:**
  Since det(A) = det(A₃), we have:
  **det(A) = 21**[cite: 19]

---

### Verification Checks

#### Check 1: Sarrus' Rule
* **Down-Right Diagonals (Positive Terms):**
  (1 × 1 × 2) + (2 × 0 × -1) + (3 × 2 × 4) = 2 + 0 + 24 = **26**[cite: 19]
* **Up-Right Diagonals (Negative Terms):**
  (-1 × 1 × 3) + (4 × 0 × 1) + (2 × 2 × 2) = -3 + 0 + 8 = **5**[cite: 19]
* **det(A):** 26 - 5 = **21**[cite: 19]

#### Check 2: Alternative Reduction using Row Scaling (Factoring Out Scalars)
* From Matrix A₂: [ 1, 2, 3 ; 0, -3, -6 ; 0, 6, 5 ]
* Factor out -3 from Row 2 (Scaling Row 2 by -1/3):
  det(A) = (-3) × det[ 1, 2, 3 ; 0, 1, 2 ; 0, 6, 5 ]
* Perform R₃ ← R₃ - 6R₂:
  det(A) = (-3) × det[ 1, 2, 3 ; 0, 1, 2 ; 0, 0, -7 ]
* Multiply main diagonal entries:
  det(A) = (-3) × (1 × 1 × -7) = (-3) × (-7) = **21**[cite: 19]

Both verification methods confirm that **det(A) = 21**[cite: 19].

---

### Detailed Explanation & Linear Algebra Insights

1. **Why Row Operations are Powerful for Computing Determinants:**
   * Computing a large determinant via cofactor expansion requires an exponential number of calculations (n! terms).
   * Reducing a matrix to upper triangular form using elementary row operations takes O(n³) operations, making it the primary method used by computer software for high-dimensional matrices.

2. **Summary of Determinant Invariants:**
   * **Row Replacement:** Adding a scalar multiple of one row to another corresponds geometrically to a shear transformation, which preserves the hyper-volume of the parallelepiped defined by the rows.
   * **Row Interchange:** Reverses spatial orientation (changes sign).
   * **Row Scaling:** Stretches or shrinks the matrix along one dimension by scalar factor c (scales determinant by c).
