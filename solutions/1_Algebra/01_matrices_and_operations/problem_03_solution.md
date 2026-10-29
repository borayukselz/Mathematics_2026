# Exercise 3: When Can Matrices Be Multiplied?

### Given Matrix Sizes
* Matrix A: 2 × 3[cite: 5]
* Matrix B: 3 × 4[cite: 5]
* Matrix C: 4 × 2[cite: 5]
* Matrix D: 2 × 2[cite: 5]

---

### Core Rule (Dimension Compatibility Condition)
For two matrices to be multiplied together in the order X × Y:
1. **Compatibility Condition:** The number of columns in the first matrix X must equal the number of rows in the second matrix Y (inner dimensions must match)[cite: 5].
2. **Result Size:** If X is (m × n) and Y is (n × p), the product XY is defined and has dimension **m × p** (outer dimensions)[cite: 5].

---

### Analysis of Products

#### 1. Product AB
* **Status:** Defined[cite: 5]
* **Result Size:** 2 × 4[cite: 5]
* **Justification / Steps:** A (2 × 3) and B (3 × 4)[cite: 5].
  * Inner dimensions: Columns of A = 3, Rows of B = 3[cite: 5]. Since 3 = 3, the product is defined.
  * Outer dimensions: Rows of A = 2, Columns of B = 4 → Result size is **2 × 4**.

#### 2. Product BA
* **Status:** Not Defined[cite: 5]
* **Result Size:** N/A[cite: 5]
* **Justification / Steps:** B (3 × 4) and A (2 × 3)[cite: 5].
  * Inner dimensions: Columns of B = 4, Rows of A = 2[cite: 5]. Since 4 ≠ 2, the product cannot be computed.

#### 3. Product BC
* **Status:** Defined[cite: 5]
* **Result Size:** 3 × 2[cite: 5]
* **Justification / Steps:** B (3 × 4) and C (4 × 2)[cite: 5].
  * Inner dimensions: Columns of B = 4, Rows of C = 4[cite: 5]. Since 4 = 4, the product is defined.
  * Outer dimensions: Rows of B = 3, Columns of C = 2 → Result size is **3 × 2**.

#### 4. Product CB
* **Status:** Not Defined[cite: 5]
* **Result Size:** N/A[cite: 5]
* **Justification / Steps:** C (4 × 2) and B (3 × 4)[cite: 5].
  * Inner dimensions: Columns of C = 2, Rows of B = 3[cite: 5]. Since 2 ≠ 3, the product cannot be computed.

#### 5. Product AC
* **Status:** Not Defined[cite: 5]
* **Result Size:** N/A[cite: 5]
* **Justification / Steps:** A (2 × 3) and C (4 × 2)[cite: 5].
  * Inner dimensions: Columns of A = 3, Rows of C = 4[cite: 5]. Since 3 ≠ 4, the product cannot be computed.

#### 6. Product CA
* **Status:** Defined[cite: 5]
* **Result Size:** 4 × 3[cite: 5]
* **Justification / Steps:** C (4 × 2) and A (2 × 3)[cite: 5].
  * Inner dimensions: Columns of C = 2, Rows of A = 2[cite: 5]. Since 2 = 2, the product is defined.
  * Outer dimensions: Rows of C = 4, Columns of A = 3 → Result size is **4 × 3**.

#### 7. Product AD
* **Status:** Not Defined[cite: 5]
* **Result Size:** N/A[cite: 5]
* **Justification / Steps:** A (2 × 3) and D (2 × 2)[cite: 5].
  * Inner dimensions: Columns of A = 3, Rows of D = 2[cite: 5]. Since 3 ≠ 2, the product cannot be computed.

#### 8. Product DA
* **Status:** Defined[cite: 5]
* **Result Size:** 2 × 3[cite: 5]
* **Justification / Steps:** D (2 × 2) and A (2 × 3)[cite: 5].
  * Inner dimensions: Columns of D = 2, Rows of A = 2[cite: 5]. Since 2 = 2, the product is defined.
  * Outer dimensions: Rows of D = 2, Columns of A = 3 → Result size is **2 × 3**.

---

### Summary Table

| Product | Defined? | Inner Dimensions Match? | Resulting Size |
|---------|----------|-------------------------|----------------|
| AB      | Yes      | 3 = 3                   | 2 × 4          |
| BA      | No       | 4 ≠ 2                   | N/A            |
| BC      | Yes      | 4 = 4                   | 3 × 2          |
| CB      | No       | 2 ≠ 3                   | N/A            |
| AC      | No       | 3 ≠ 4                   | N/A            |
| CA      | Yes      | 2 = 2                   | 4 × 3          |
| AD      | No       | 3 ≠ 2                   | N/A            |
| DA      | Yes      | 2 = 2                   | 2 × 3          |
