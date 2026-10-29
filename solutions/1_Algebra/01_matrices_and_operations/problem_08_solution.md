# Exercise 8: Row Operations and Their Reversibility

### Given Initial Matrix A

**Matrix A:**
[  1   2  -1 ]
[  2   4   1 ]
[ -1   1   3 ]

---

### Step-by-Step Row Operations

#### Step 1: Perform R₂ ← R₂ - 2R₁

* **Result Matrix (A₁):**
  [  1   2  -1 ]
  [  0   0   3 ]
  [ -1   1   3 ]

* **Detailed Calculation:**
  * Row 1 (R₁) remains unchanged: [ 1, 2, -1 ]
  * Row 3 (R₃) remains unchanged: [ -1, 1, 3 ]
  * Calculate new Row 2 (R₂ - 2R₁):
    * Entry (2,1):  2 - 2(1)  =  2 - 2 = 0
    * Entry (2,2):  4 - 2(2)  =  4 - 4 = 0
    * Entry (2,3):  1 - 2(-1) =  1 + 2 = 3

* **Method & Explanation:** 
  This operation is an **elementary row replacement**. It eliminates the leading entry in the second row by subtracting twice the first row from the second row. This is a standard step in Gaussian elimination used to create zeros under a pivot element.

* **Reversing Operation:**
  **R₂ ← R₂ + 2R₁**
  * *Detailed Explanation:* To undo the subtraction of 2 times Row 1 from Row 2, you simply add 2 times Row 1 back to the newly modified Row 2.
  * *Verification:* 
    [ 0 + 2(1), 0 + 2(2), 3 + 2(-1) ] = [ 2, 4, 1 ], which restores the original Row 2.

---

#### Step 2: Perform R₃ ← R₃ + R₁

* **Result Matrix (A₂):**
  [  1   2  -1 ]
  [  0   0   3 ]
  [  0   3   2 ]

* **Detailed Calculation:**
  * Row 1 (R₁) remains unchanged: [ 1, 2, -1 ]
  * Row 2 (R₂) remains unchanged: [ 0, 0, 3 ]
  * Calculate new Row 3 (R₃ + R₁):
    * Entry (3,1): -1 + 1  = 0
    * Entry (3,2):  1 + 2  = 3
    * Entry (3,3):  3 + (-1) = 2

* **Method & Explanation:**
  This is another **elementary row replacement**. We add Row 1 to Row 3 to eliminate the negative value in the first column of Row 3, creating another zero in column 1 below the pivot.

* **Reversing Operation:**
  **R₃ ← R₃ - R₁**
  * *Detailed Explanation:* To undo adding Row 1 to Row 3, you subtract Row 1 from the newly modified Row 3.
  * *Verification:*
    [ 0 - 1, 3 - 2, 2 - (-1) ] = [ -1, 1, 3 ], which restores Row 3 of matrix A₁.

---

#### Step 3: Interchange R₂ and R₃ (R₂ ↔ R₃)

* **Result Matrix (A₃):**
  [  1   2  -1 ]
  [  0   3   2 ]
  [  0   0   3 ]

* **Detailed Calculation:**
  * Row 1 (R₁) remains unchanged: [ 1, 2, -1 ]
  * Swap Row 2 and Row 3:
    * New Row 2 becomes old Row 3: [ 0, 3, 2 ]
    * New Row 3 becomes old Row 2: [ 0, 0, 3 ]

* **Method & Explanation:**
  This operation is an **elementary row interchange**. By swapping Row 2 and Row 3, the matrix is brought into **Upper Triangular (Row Echelon) Form**, where all entries below the main diagonal are zeros.

* **Reversing Operation:**
  **Interchange R₂ and R₃ (R₂ ↔ R₃)**
  * *Detailed Explanation:* Row interchange is its own inverse operation. Swapping the second and third rows a second time moves them back to their previous positions.
  * *Verification:*
    Swapping [ 0, 3, 2 ] and [ 0, 0, 3 ] again returns Row 2 to [ 0, 0, 3 ] and Row 3 to [ 0, 3, 2 ], restoring matrix A₂.

---

### Concept Summary & Explanation of Reversibility

1. **What Reversibility Means in Linear Algebra:**
   * Every elementary row operation can be undone by another elementary row operation of the same type[cite: 10].
   * Because every step is reversible, applying row operations to a system of linear equations does not alter or lose any information about the system's solutions[cite: 10].

2. **The Three Fundamental Reversibility Rules:**
   * **Replacement (Rᵢ ← Rᵢ + cRⱼ):** Reversed by performing **Rᵢ ← Rᵢ - cRⱼ**[cite: 10].
   * **Interchange (Rᵢ ↔ Rⱼ):** Reversed by performing the exact same swap **Rᵢ ↔ Rⱼ**[cite: 10].
   * **Scaling (Rᵢ ← cRᵢ, where c ≠ 0):** Reversed by multiplying by the reciprocal **Rᵢ ← (1/c)Rᵢ**.
