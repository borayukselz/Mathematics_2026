# Exercise 4: Matrix Multiplication and Noncommutativity

### Given Matrices

**Matrix A:**
[ 1  2 ]
[ 0  1 ]

**Matrix B:**
[ 2  0 ]
[ 3  1 ]

---

### 1. Compute AB

* **Result:**
  [ 8  2 ]
  [ 3  1 ]

* **Main Steps:** Multiply rows of A by columns of B[cite: 6]:
  * Top-left (1,1):     (1 × 2) + (2 × 3) = 2 + 6 = 8
  * Top-right (1,2):    (1 × 0) + (2 × 1) = 0 + 2 = 2
  * Bottom-left (2,1):  (0 × 2) + (1 × 3) = 0 + 3 = 3
  * Bottom-right (2,2): (0 × 0) + (1 × 1) = 0 + 1 = 1

* **Method & Explanation:** The entry at row i, column j of AB is computed by taking the dot product of row i from Matrix A and column j from Matrix B[cite: 6].

* **Mathematical Verification:** Check individual row-column dot products: (1 × 2 + 2 × 3 = 8) and (0 × 0 + 1 × 1 = 1). All entries match.

---

### 2. Compute BA

* **Result:**
  [ 2  4 ]
  [ 3  7 ]

* **Main Steps:** Multiply rows of B by columns of A[cite: 6]:
  * Top-left (1,1):     (2 × 1) + (0 × 0) = 2 + 0 = 2
  * Top-right (1,2):    (2 × 2) + (0 × 1) = 4 + 0 = 4
  * Bottom-left (2,1):  (3 × 1) + (1 × 0) = 3 + 0 = 3
  * Bottom-right (2,2): (3 × 2) + (1 × 1) = 6 + 1 = 7

* **Method & Explanation:** The entry at row i, column j of BA is computed by taking the dot product of row i from Matrix B and column j from Matrix A[cite: 6].

* **Mathematical Verification:** Check individual row-column dot products: (2 × 1 + 0 × 0 = 2) and (3 × 2 + 1 × 1 = 7). All entries match.

---

### 3. Is AB = BA?

* **Result:** **No, AB ≠ BA[cite: 6].**
* **Justification:**
  * AB = [ 8  2 ; 3  1 ]
  * BA = [ 2  4 ; 3  7 ]
  * Comparing corresponding positions shows that elements differ (for example, top-left entry 8 ≠ 2, top-right entry 2 ≠ 4). Therefore, the resulting matrices are not equal[cite: 6].

---

### 4. Explanation of Noncommutativity

* **Result / Explanation:**
  * **Definition:** Noncommutativity means that changing the order of operands changes the final result[cite: 6]. Unlike regular numbers where multiplication is commutative (for example, 3 × 5 = 5 × 3), matrix multiplication is **noncommutative** (AB ≠ BA in general)[cite: 6].
  * **Reasoning in this example:** Matrix multiplication pairs the **rows** of the left matrix with the **columns** of the right matrix[cite: 6].
    * In **AB**, the rows of A are paired with the columns of B[cite: 6].
    * In **BA**, the rows of B are paired with the columns of A[cite: 6].
  * Because different entries are multiplied together when the order is switched, AB and BA yield completely different matrix outputs[cite: 6].
