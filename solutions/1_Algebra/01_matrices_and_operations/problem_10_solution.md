# Exercise 10: Columns of a Matrix Product

### Given

**Matrix A:**
[  1   2   0 ]
[  0   1   1 ]

**Matrix B:**
[  1   2 ]
[ -1   0 ]
[  3   1 ]

**Columns of B:**
* **b₁** = [  1, -1,  3 ] (First column of B)[cite: 12]
* **b₂** = [  2,  0,  1 ] (Second column of B)[cite: 12]

---

### 1. Compute Ab₁ and Ab₂

#### A. Compute Ab₁

* **Result:**
  [ -1 ]
  [  2 ]

* **Detailed Calculation Steps:**
  * Top entry (Row 1 of A × b₁):    (1 × 1) + (2 × -1) + (0 × 3) = 1 - 2 + 0 = -1[cite: 12]
  * Bottom entry (Row 2 of A × b₁): (0 × 1) + (1 × -1) + (1 × 3) = 0 - 1 + 3 = 2[cite: 12]

* **Method & Explanation:**
  Multiply matrix A (2 × 3) by the first column vector b₁ (3 × 1)[cite: 12]. Each entry of the resulting 2 × 1 vector is the dot product of a row from A and vector b₁[cite: 12].

* **Mathematical Verification:**
  Re-verify row calculations: 1(1) + 2(-1) + 0(3) = -1, and 0(1) + 1(-1) + 1(3) = 2[cite: 12]. Both values are confirmed.

---

#### B. Compute Ab₂

* **Result:**
  [  2 ]
  [  1 ]

* **Detailed Calculation Steps:**
  * Top entry (Row 1 of A × b₂):    (1 × 2) + (2 × 0) + (0 × 1) = 2 + 0 + 0 = 2[cite: 12]
  * Bottom entry (Row 2 of A × b₂): (0 × 2) + (1 × 0) + (1 × 1) = 0 + 0 + 1 = 1[cite: 12]

* **Method & Explanation:**
  Multiply matrix A (2 × 3) by the second column vector b₂ (3 × 1)[cite: 12]. Each entry of the resulting 2 × 1 vector is the dot product of a row from A and vector b₂[cite: 12].

* **Mathematical Verification:**
  Re-verify row calculations: 1(2) + 2(0) + 0(1) = 2, and 0(2) + 1(0) + 1(1) = 1[cite: 12]. Both values are confirmed.

---

### 2. Compute the Matrix AB

* **Result:**
  [ -1   2 ]
  [  2   1 ]

* **Detailed Calculation Steps:**
  Multiply Matrix A (2 × 3) by Matrix B (3 × 2) to get a 2 × 2 matrix[cite: 12]:
  * **Entry (1,1) [Row 1 of A × Column 1 of B]:** (1 × 1) + (2 × -1) + (0 × 3) = 1 - 2 + 0 = -1
