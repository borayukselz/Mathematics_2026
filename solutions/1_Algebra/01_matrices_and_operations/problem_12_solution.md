# Exercise 12: Formula for a Matrix Power

### Given Matrix

**Matrix A:**
[  1   1 ]
[  0   1 ]

---

### 1. Compute Successive Powers: A², A³, and A⁴

#### A. Compute A² (A × A)

* **Result:**
  [  1   2 ]
  [  0   1 ]

* **Detailed Calculation Steps:**
  * Top-left entry (1,1):     (1 × 1) + (1 × 0) = 1 + 0 = 1[cite: 14]
  * Top-right entry (1,2):    (1 × 1) + (1 × 1) = 1 + 1 = 2[cite: 14]
  * Bottom-left entry (2,1):  (0 × 1) + (1 × 0) = 0 + 0 = 0[cite: 14]
  * Bottom-right entry (2,2): (0 × 1) + (1 × 1) = 0 + 1 = 1[cite: 14]

* **Method & Explanation:**
  Multiply Matrix A by itself using standard row-by-column multiplication[cite: 14].

---

#### B. Compute A³ (A² × A)

* **Result:**
  [  1   3 ]
  [  0   1 ]

* **Detailed Calculation Steps:**
  * Top-left entry (1,1):     (1 × 1) + (2 × 0) = 1 + 0 = 1[cite: 14]
  * Top-right entry (1,2):    (1 × 1) + (2 × 1) = 1 + 2 = 3[cite: 14]
  * Bottom-left entry (2,1):  (0 × 1) + (1 × 0) = 0 + 0 = 0[cite: 14]
  * Bottom-right entry (2,2): (0 × 1) + (1 × 1) = 0 + 1 = 1[cite: 14]

* **Method & Explanation:**
  Multiply the resulting matrix A² by Matrix A[cite: 14].

---

#### C. Compute A⁴ (A³ × A)

* **Result:**
  [  1   4 ]
  [  0   1 ]

* **Detailed Calculation Steps:**
  * Top-left entry (1,1):     (1 × 1) + (3 × 0) = 1 + 0 = 1[cite: 14]
  * Top-right entry (1,2):    (1 × 1) + (3 × 1) = 1 + 3 = 4[cite: 14]
  * Bottom-left entry (2,1):  (0 × 1) + (1 × 0) = 0 + 0 = 0[cite: 14]
  * Bottom-right entry (2,2): (0 × 1) + (1 × 1) = 0 + 1 = 1[cite: 14]

* **Method & Explanation:**
  Multiply the resulting matrix A³ by Matrix A[cite: 14].

---

### 2. Formulate a Conjecture for Aⁿ

* **Observed Pattern Across Powers:**
  * **A¹:**
    [  1   1 ]
    [  0   1 ]

  * **A²:**
    [  1   2 ]
    [  0   1 ]

  * **A³:**
    [  1   3 ]
    [  0   1 ]

  * **A⁴:**
    [  1   4 ]
    [  0   1 ]

* **Conjecture Statement:**
  For any positive integer n, the matrix power Aⁿ has the general form[cite: 14]:
  [  1   n ]
  [  0   1 ]

  * **Diagonal Entries:** Always remain 1[cite: 14].
  * **Bottom-Left Entry:** Always remains 0[cite: 14].
  * **Top-Right Entry:** Equals the exponent n itself[cite: 14].

---

### 3. Proof by Mathematical Induction

To establish that the conjecture holds for all positive integers n, we use the principle of **Mathematical Induction**[cite: 14].

#### Step 1: Base Case (n = 1)
* For n = 1:
  [  1   1 ]
  [  0   1 ]
  This matches the given Matrix A[cite: 14]. Thus, the base case holds[cite: 14].

#### Step 2: Inductive Hypothesis
* Assume that the formula holds true
