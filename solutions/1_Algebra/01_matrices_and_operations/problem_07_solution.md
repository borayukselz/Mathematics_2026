# Exercise 7: Identity Matrix, Zero Matrix, and Powers

### Given Matrix

**Matrix A:**
[  2   1 ]
[  0   2 ]

---

### 1. Compute AI, IA, A + 0, A², and A³

* **AI (A × Identity Matrix):**
  [  2   1 ] × [  1   0 ] = [  2   1 ]
  [  0   2 ]   [  0   1 ]   [  0   2 ]
  * **Result:** Same as Matrix A[cite: 9].

* **IA (Identity Matrix × A):**
  [  1   0 ] × [  2   1 ] = [  2   1 ]
  [  0   1 ]   [  0   2 ]   [  0   2 ]
  * **Result:** Same as Matrix A[cite: 9].

* **A + 0 (A + Zero Matrix):**
  [  2   1 ] + [  0   0 ] = [  2   1 ]
  [  0   2 ]   [  0   0 ]   [  0   2 ]
  * **Result:** Same as Matrix A[cite: 9].

* **A² (A × A):**
  [  2   1 ] × [  2   1 ] = [  4   4 ]
  [  0   2 ]   [  0   2 ]   [  0   4 ]
  * **Main Steps:**
    * Top-left:     (2 × 2) + (1 × 0) = 4 + 0 = 4
    * Top-right:    (2 × 1) + (1 × 2) = 2 + 2 = 4
    * Bottom-left:  (0 × 2) + (2 × 0) = 0 + 0 = 0
    * Bottom-right: (0 × 1) + (2 × 2) = 0 + 4 = 4

* **A³ (A² × A):**
  [  4   4 ] × [  2   1 ] = [  8  12 ]
  [  0   4 ]   [  0   2 ]   [  0   8 ]
  * **Main Steps:**
    * Top-left:     (4 × 2) + (4 × 0) = 8 + 0 = 8
    * Top-right:    (4 × 1) + (4 × 2) = 4 + 8 = 12
    * Bottom-left:  (0 × 2) + (4 × 0) = 0 + 0 = 0
    * Bottom-right: (0 × 1) + (4 × 2) = 0 + 8 = 8

---

### 2. Roles of the Matrices I and 0

* **Identity Matrix (I):**
  * Serves as the **multiplicative identity** (analogous to the number 1 in regular multiplication)[cite: 9].
  * Multiplying any compatible matrix by I leaves the matrix unchanged: **AI = IA = A**[cite: 9].

* **Zero Matrix (0):**
  * Serves as the **additive identity** (analogous to the number 0 in regular addition)[cite: 9].
  * Adding 0 to any matrix of the same size leaves the matrix unchanged: **A + 0 = A**[cite: 9].

---

### 3. Pattern in Successive Powers of A

* **Observed Pattern:**
  * **A¹:**
    [  2¹  (1 × 2⁰) ] = [ 2  1 ]
    [  0       2¹   ]   [ 0  2 ]

  * **A²:**
    [  2²  (2 × 2¹) ] = [ 4  4 ]
    [  0       2²   ]   [ 0  4 ]

  * **A³:**
    [  2³  (3 × 2²) ] = [ 8 12 ]
    [  0       2³   ]   [ 0  8 ]

* **General Rule for Aⁿ (where n is the power):**
  [ 2ⁿ   n × 2ⁿ⁻¹ ]
  [ 0    2ⁿ       ]

  1. **Diagonal entries:** Equal to **2ⁿ**.
  2. **Bottom-left entry:** Always remains **0**.
  3. **Top-right entry:** Equal to **n × 2ⁿ⁻¹**.
