# Exercise 8: Determinant of a Product

### Given

* **det(A) = 3**[cite: 22]
* **det(B) = -5**[cite: 22]
* **A and B are square matrices of the same size**[cite: 22]

---

### 1. Compute det(AB)

* **Result:**
  **det(AB) = -15**[cite: 22]

* **Property Used:**
  The determinant of a product of matrices equals the product of their individual determinants (Multiplicative Property of Determinants):
  **det(AB) = det(A) × det(B)**[cite: 22]

* **Detailed Calculation Steps:**
  1. Apply multiplicative property: det(AB) = det(A) × det(B)[cite: 22]
  2. Substitute given values: det(AB) = (3) × (-5)[cite: 22]
  3. Calculate product: det(AB) = **-15**[cite: 22]

* **Method & Explanation:**
  Matrix multiplication preserves volume scaling. The combined scaling factor of transformation B followed by transformation A is simply the product of their individual volume scaling factors.

---

### 2. Compute det(BA)

* **Result:**
  **det(BA) = -15**[cite: 22]

* **Property Used:**
  **det(BA) = det(B) × det(A)**[cite: 22]

* **Detailed Calculation Steps:**
  1. Apply multiplicative property: det(BA) = det(B) × det(A)[cite: 22]
  2. Substitute given values: det(BA) = (-5) × (3)[cite: 22]
  3. Calculate product: det(BA) = **-15**[cite: 22]

* **Method & Explanation:**
  Even though applying transformation A before B produces a different resulting matrix than applying B before A, both combined transformations scale overall space by the exact same total factor.

---

### 3. Compute det(A⁻¹B)

* **Existence Check:**
  * Matrix A is **invertible** if and only if **det(A) ≠ 0**.
  * Since **det(A) = 3 ≠ 0**, the inverse matrix **A⁻¹ exists**[cite: 22].
  * Therefore, the matrix product **A⁻¹B exists** and its determinant is defined[cite: 22].

* **Result:**
  **det(A⁻¹B) = -5/3** (or approx. -1.667)[cite: 22]

* **Property Used:**
  1. Determinant of an inverse matrix: **det(A⁻¹) = 1 / det(A)**
  2. Multiplicative property: **det(A⁻¹B) = det(A⁻¹) × det(B) = (1 / det(A)) × det(B)**[cite: 22]

* **Detailed Calculation Steps:**
  1. Compute det(A⁻¹):
     det(A⁻¹) = 1 / det(A) = 1 / 3
  2. Multiply by det(B):
     det(A⁻¹B) = (1 / 3) × (-5) = **-5/3**[cite: 22]

* **Method & Explanation:**
  The inverse operation undoes the scaling of A (scaling by 1/3). Combining A⁻¹ with B multiplies the scaling factor 1/3 by the scaling factor -5 of B.

---

### 4. Explain Why det(AB) = det(BA) Even Though AB ≠ BA

* **Key Distinction:**
  * **Matrix Multiplication is Non-Commutative:** In general, **AB ≠ BA** because matrix operations depend on the order in which individual components are transformed[cite: 22].
  * **Scalar Multiplication is Commutative:** The determinant map converts square matrices into single real numbers (scalars)[cite: 22].

* **Algebraic Explanation:**
  1. By the multiplicative property:
     * det(AB) = det(A) × det(B)[cite: 22]
     * det(BA) = det(B) × det(A)[cite: 22]
  2. Since det(A) and det(B) are ordinary real numbers, scalar multiplication is commutative:
     **det(A) × det(B) = det(B) × det(A)**
  3. Therefore, **det(AB) = det(BA)** always holds for any square matrices A and B, even when AB ≠ BA[cite: 22].

* **Geometric Explanation:**
  * Matrix AB and matrix BA perform geometric transformations in different sequence orders, resulting in different final orientations/configurations.
  * However, the **total volume change** (and orientation sign) caused by applying both transformations depends only on the combined magnitude of both scaling factors, which is independent of sequence order.

---

### Summary Table of Results

| Target Expression | Property / Formula used | Substitution & Calculation | Final Value |
|-------------------|-------------------------|----------------------------|-------------|
| det(AB)           | det(A) × det(B)         | (3) × (-5)                 | -15         |
| det(BA)           | det(B) × det(A)         | (-5) × (3)                 | -15         |
| det(A⁻¹B)         | det(B) / det(A)         | (-5) / (3)                 | -5/3        |
