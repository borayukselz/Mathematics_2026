# Exercise 2: Addition and Scalar Multiplication

### Given Matrices

**Matrix A:**
[  1   2 ]
[ -1   3 ]

**Matrix B:**
[  4  -2 ]
[  0   5 ]

---

### 1. Compute A + B

* **Result:**
  [  5   0 ]
  [ -1   8 ]

* **Main Steps:** Add corresponding entries from Matrix A and Matrix B:
  * Top-left:     1 + 4 = 5
  * Top-right:    2 + (-2) = 0
  * Bottom-left:  -1 + 0 = -1
  * Bottom-right: 3 + 5 = 8

* **Method & Explanation:** Matrix addition is performed entry-by-entry (component-wise). You add the entry in row i, column j of A to the entry in row i, column j of B.

* **Mathematical Verification:** Verify using the commutative property (B + A = A + B):
  [4+1, -2+2; 0+(-1), 5+3] = [5, 0; -1, 8], which matches A + B.

---

### 2. Compute A - B

* **Result:**
  [ -3   4 ]
  [ -1  -2 ]

* **Main Steps:** Subtract corresponding entries of B from A:
  * Top-left:     1 - 4 = -3
  * Top-right:    2 - (-2) = 2 + 2 = 4
  * Bottom-left:  -1 - 0 = -1
  * Bottom-right: 3 - 5 = -2

* **Method & Explanation:** Matrix subtraction is performed entry-by-entry. Subtract entry at row i, column j of B from entry at row i, column j of A.

* **Mathematical Verification:** Reconstruct A using (A - B) + B:
  [-3 + 4, 4 + (-2); -1 + 0, -2 + 5] = [1, 2; -1, 3] = Matrix A.

---

### 3. Compute 3A - 2B

* **Result:**
  [ -5  10 ]
  [ -3  -1 ]

* **Main Steps:**
  1. Multiply every entry of Matrix A by scalar 3:
     3A = [ 3(1)  3(2) ] = [  3   6 ]
          [ 3(-1) 3(3) ]   [ -3   9 ]

  2. Multiply every entry of Matrix B by scalar 2:
     2B = [ 2(4)  2(-2) ] = [ 8  -4 ]
          [ 2(0)  2(5)  ]   [ 0  10 ]

  3. Subtract 2B from 3A:
     * Top-left:     3 - 8 = -5
     * Top-right:    6 - (-4) = 6 + 4 = 10
     * Bottom-left:  -3 - 0 = -3
     * Bottom-right: 9 - 10 = -1

* **Method & Explanation:** Scalar multiplication scales every individual entry of a matrix by that scalar number. Linear combinations combine scalar multiplication and entry-wise addition/subtraction.

* **Mathematical Verification:** Verify entry (1,2): 3(2) - 2(-2) = 6 + 4 = 10. Verify entry (2,2): 3(3) - 2(5) = 9 - 10 = -1. All entries match.

---

### 4. Explain why matrix addition is possible only for matrices of the same size

* **Result / Explanation:** Matrix addition is defined strictly as an **entry-by-entry (component-wise)** operation. For the sum (A + B) to exist, every entry at position (i, j) in matrix A must pair with an exact corresponding entry at position (i, j)
