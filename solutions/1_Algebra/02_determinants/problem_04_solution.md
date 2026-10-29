# Exercise 4: Triangular Matrix

### Given Matrix

**Matrix A:**
[  2   4   1 ]
[  0  -3   5 ]
[  0   0   7 ][cite: 18]

---

### 1. Compute det(A) Without Expanding

* **Result:**
  **det(A) = -42**[cite: 18]

* **Calculation Steps:**
  * Identify the main diagonal entries of Matrix A[cite: 18]: **2**, **-3**, and **7**.
  * Multiply the diagonal entries together[cite: 18]:
    det(A) = 2 × (-3) × 7
    det(A) = -6 × 7 = **-42**

* **Method & Explanation:**
  Because Matrix A is an **upper triangular matrix** (all entries below the main diagonal are zeros), its determinant can be computed directly by taking the product of the entries along the main diagonal, without performing full determinant expansion[cite: 18].

---

### 2. General Rule for an Arbitrary Triangular Matrix

* **Rule Statement:**
  The determinant of any triangular matrix (whether **upper triangular**, **lower triangular**, or **diagonal**) is equal to the **product of its main diagonal entries**[cite: 18].

* **General Formula:**
  For an n × n triangular matrix T with main diagonal entries t₁₁, t₂₂, ..., tₙₙ:
  **det(T) = t₁₁ × t₂₂ × ... × tₙₙ**

---

### 3. Detailed Explanation of the Rule Using This Example

#### A. Algebraic Explanation (via Cofactor Expansion)
To understand why only the main diagonal entries matter, look at what happens when performing cofactor expansion on Matrix A[cite: 18]:

1. **Expand along Column 1:**
   Column 1 contains entries [ 2, 0, 0 ][cite: 18].
   det(A) = 2 × det[ -3, 5 ; 0, 7 ] - 0 × det[ 4, 1 ; 0, 7 ] + 0 × det[ 4, 1 ; -3, 5 ]
   
   Notice that both off-diagonal zeros multiply their respective sub-determinants by 0, eliminating them completely!
   det(A) = 2 × det[ -3, 5 ; 0, 7 ]

2. **Evaluate the 2×2 Sub-Determinant:**
   The sub-matrix [ -3, 5 ; 0, 7 ] is also upper triangular[cite: 18].
   det[ -3, 5 ; 0, 7 ] = (-3 × 7) - (5 × 0) = -3 × 7 = -21

3. **Final Product:**
   det(A) = 2 × (-3) × 7 = **-42**

* **Key Insight:** At every stage of cofactor expansion down the first column (or along the bottom row), every term involving off-diagonal elements vanishes because it is multiplied by zero. The only term that survives at every level is the product of the main diagonal entries[cite: 18]!

---

#### B. Geometric Explanation (Volume Scaling in 3D Space)
* **Axis Scaling vs. Shearing:**
  In Matrix A = [ 2, 4, 1 ; 0, -3, 5 ; 0, 0, 7 ][cite: 18]:
  * The main diagonal entries (2, -3, 7) scale space along the coordinate axes[cite: 18].
  * The upper off-diagonal entries (4, 1, 5) represent **shear transformations** (sliding parallel to coordinate planes)[cite: 18].
* **Volume Invariance under Shearing:**
  Shearing a geometric object (like slanting a stack of paper) changes its shape but **leaves its total enclosed volume completely unchanged**.
* **Conclusion:** The off-diagonal entries (4, 1, 5) do not affect the 3D volume[cite: 18]. Therefore, the volume scaling factor (determinant) depends strictly on the direct scaling factors along the diagonal: **2 × (-3) × 7 = -42**[cite: 18].

---

### 4. Mathematical Verification

* **Check using Sarrus' Rule:**
  * Down-Right Diagonals:
    (2 × -3 × 7) + (4 × 5 × 0) + (1 × 0 × 0) = -42 + 0 + 0 = **-42**[cite: 18]
  * Up-Right Diagonals:
    (0 × -3 × 1) + (0 × 5 × 2) + (7 × 0 × 4) = 0 + 0 + 0 = **0**[cite: 18]
  * det(A) = -42 - 0 = **-42**

* **Conclusion:** Standard computation confirms that det(A) = **-42**, verifying the triangular matrix rule[cite: 18].
