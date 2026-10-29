# Exercise 6: Transpose

### Given Matrices

**Matrix A:**
[ 1  2  3 ]
[ 4  5  6 ]

**Matrix B:**
[  1   0 ]
[  2   1 ]
[ -1   3 ]

---

### 1. Compute Aᵀ and Bᵀ

* **Result:**
  * **Aᵀ (Transpose of A):**
    [ 1  4 ]
    [ 2  5 ]
    [ 3  6 ]

  * **Bᵀ (Transpose of B):**
    [  1   2  -1 ]
    [  0   1   3 ]

* **Main Steps:** Swap rows and columns (Row i becomes Column i)[cite: 8]:
  * For Aᵀ: Row 1 of A [1, 2, 3] becomes Column 1 of Aᵀ; Row 2 of A [4, 5, 6] becomes Column 2 of Aᵀ[cite: 8].
  * For Bᵀ: Row 1 of B [1, 0] becomes Column 1 of Bᵀ; Row 2 [2, 1] becomes Column 2; Row 3 [-1, 3] becomes Column 3[cite: 8].

* **Method & Explanation:** The transpose of a matrix is formed by swapping its rows and columns, turning an (m × n) matrix into an (n × m) matrix[cite: 8].

* **Mathematical Verification:** Check dimensions: Matrix A (2 × 3) transposes to Aᵀ (3 × 2)[cite: 8]. Matrix B (3 × 2) transposes to Bᵀ (2 × 3)[cite: 8].

---

### 2. Compute AB

* **Result:**
  [  2  11 ]
  [  8  23 ]

* **Main Steps:** Multiply rows of A (2 × 3) by columns of B (3 × 2)[cite: 8]:
  * Top-left (1,1):     (1 × 1) + (2 × 2) + (3 × -1) = 1 + 4 - 3 = 2
  * Top-right (1,2):    (1 × 0) + (2 × 1) + (3 × 3)  = 0 + 2 + 9 = 11
  * Bottom-left (2,1):  (4 × 1) + (5 × 2) + (6 × -1) = 4 + 10 - 6 = 8
  * Bottom-right (2,2): (4 × 0) + (5 × 1) + (6 × 3)  = 0 + 5 + 18 = 23

* **Method & Explanation:** Perform standard matrix multiplication by taking the dot product of each row from Matrix A with each column from Matrix B[cite: 8].

* **Mathematical Verification:** Check entry (2,2): (4 × 0) + (5 × 1) + (6 × 3) = 0 + 5 + 18 = 23.

---

### 3. Verify (AB)ᵀ = BᵀAᵀ

* **Result:**
  * **Left Side (AB)ᵀ:**
    Transpose the AB result from Part 2:
    [  2   8 ]
    [ 11  23 ]

  * **Right Side
