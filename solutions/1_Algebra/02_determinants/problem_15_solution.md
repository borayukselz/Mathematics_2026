# Exercise 15: Combining Determinant Properties

### Given Data

* **Matrix Dimensions:** 2 × 2 square matrices A and B[cite: 20]
* **Invertibility:** Both A and B are invertible[cite: 20]
* **Determinant of A:** det(A) = -2[cite: 20]
* **Determinant of B:** det(B) = 3[cite: 20]

---

### 1. Determinant Properties Used (In Order)

To compute det(B⁻¹ Aᵀ B), we apply three fundamental determinant properties sequentially[cite: 20]:

1. **Multiplicative Property of Determinants:**
   The determinant of a product of square matrices equals the product of their individual determinants:
   det(X Y Z) = det(X) × det(Y) × det(Z)

2. **Determinant of an Inverse Matrix:**
   If a matrix B is invertible (det(B) ≠ 0), the determinant of its inverse is the reciprocal of its determinant:
   det(B⁻¹) = 1 / det(B)

3. **Determinant of a Transpose Matrix:**
   Transposing a matrix does not change its determinant:
   det(Aᵀ) = det(A)

---

### 2. Step-by-Step Computation of det(B⁻¹ Aᵀ B)

* **Result:**
  **det(B⁻¹ Aᵀ B) = -2**[cite: 20]

* **Detailed Calculation Steps:**

  1. **Apply the Multiplicative Property:**
     det(B⁻¹ Aᵀ B) = det(B⁻¹) × det(Aᵀ) × det(B)

  2. **Apply Inverse and Transpose Properties:**
     * Replace det(B⁻¹) with (1 / det(B))
     * Replace det(Aᵀ) with det(A)
     det(B⁻¹ Aᵀ B) = (1 / det(B)) × det(A) × det(B)

  3. **Substitute Given Numerical Values:**
     * Substitute det(A) = -2 and det(B) = 3:
     det(B⁻¹ Aᵀ B) = (1 / 3) × (-2) × (3)

  4. **Perform Scalar Arithmetic:**
     det(B⁻¹ Aᵀ B) = (-2 × 3) / 3 = -6 / 3 = **-2**

---

### 3. Why the Factors Involving B Eventually Cancel

* **Commutativity of Scalar Multiplication:**
  While matrix multiplication is generally non-commutative (M N ≠ N M), taking the determinant converts matrix expressions into single real numbers (scalars)[cite: 20]. Multiplication of real numbers is commutative[cite: 20].

* **Algebraic Derivation of Cancellation:**
  Rearranging the scalar terms yields:
  det(B⁻¹ Aᵀ B) = (1 / det(B)) × det(Aᵀ) × det(B)
  det(B⁻¹ Aᵀ B) = [ (1 / det(B)) × det(B) ] × det(Aᵀ)
  det(B⁻¹ Aᵀ B) = (1) × det(Aᵀ) = det(A)

Because (1 / det(B)) × det(B) = 1 for any non-zero scalar det(B), the terms involving Matrix B completely cancel out, leaving the result dependent only on Matrix A[cite: 20].

---

### 4. Summary Table of Properties & Calculation

| Step | Rule / Property | Expression Form | Substitution | Result |
|------|-----------------|-----------------|--------------|--------|
| Step 1 | Multiplicative Rule | det(B⁻¹) × det(Aᵀ) × det(B) | — | — |
| Step 2 | Inverse & Transpose Rules | (1 / det(B)) × det(A) × det(B) | — | — |
| Step 3 | Numerical Substitution | (1 / 3) × (-2) × 3 | (1 / 3) × (-6) | **-2**[cite: 20] |

---

### 5. Detailed Explanation & Linear Algebra Insights

1. **Similarity Transformations Preserve Determinants:**
   * An expression of the form B⁻¹ M B is called a **similarity transformation** (or conjugate) of matrix M.
   * Similar matrices represent the exact same linear transformation under a change of basis (defined by B).
   * Because changing coordinate basis does not alter the fundamental geometric volume scaling factor of a transformation, **similar matrices always have identical determinants**:
     det(B⁻¹ M B) = det(M)
   * Setting M = Aᵀ gives det(B⁻¹ Aᵀ B) = det(Aᵀ) = det(A) = **-2**.

2. **Role of Invertibility:**
   * The problem specifies that B is invertible[cite: 20].
   * This guarantees that det(B) ≠ 0 (since det(B) = 3 ≠ 0), ensuring that division by det(B) is fully valid and defined[cite: 20].
