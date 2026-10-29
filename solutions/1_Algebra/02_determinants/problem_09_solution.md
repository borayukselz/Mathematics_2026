# Exercise 9: Area and the Determinant

### Given Vectors

**Vector u:**
[  3 ]
[  1 ][cite: 23]

**Vector v:**
[  1 ]
[  4 ][cite: 23]

---

### Core Formula for Area of a Parallelogram

In 2D space, the geometric area of the parallelogram spanned by two vectors u and v is equal to the **absolute value of the determinant** of the 2x2 matrix formed by placing the vectors as columns (or rows)[cite: 18, 23]:
**Area = | det([ u  v ]) |**

---

### 1. Compute Area Using Matrix M = [ u  v ]

* **Result:**
  **Determinant:** det(M) = 11[cite: 23]
  **Area:** Area = 11 square units[cite: 23]

* **Detailed Calculation Steps:**
  1. Construct Matrix M with vector u as Column 1 and vector v as Column 2[cite: 23]:
     M = [  3   1 ]
         [  1   4 ][cite: 23]

  2. Compute determinant using the 2x2 formula det = (a × d) - (b × c)[cite: 18]:
     det(M) = (3 × 4) - (1 × 1)
     det(M) = 12 - 1 = **11**[cite: 23]

  3. Compute physical area by taking the absolute value:
     Area = | det(M) | = | 11 | = **11**[cite: 23]

* **Method & Explanation:**
  The determinant calculates the signed area scaled by the linear transformation mapping standard unit vectors to u and v[cite: 23].

* **Mathematical Verification:**
  Re-verify arithmetic: (3 × 4) - (1 × 1) = 12 - 1 = 11. Absolute value is 11. Calculation confirmed.

---

### 2. Reverse Vector Order: Matrix M' = [ v  u ]

* **Result:**
  **Determinant:** det(M') = -11[cite: 23]
  **Area:** Area = 11 square units[cite: 23]

* **Detailed Calculation Steps:**
  1. Construct Matrix M' with vector v as Column 1 and vector u as Column 2[cite: 23]:
     M' = [  1   3 ]
          [  4   1 ][cite: 23]

  2. Compute determinant:
     det(M') = (1 × 1) - (3 × 4)
     det(M') = 1 - 12 = **-11**[cite: 23]

  3. Compute physical area by taking the absolute value:
     Area = | det(M') | = | -11 | = **11**[cite: 23]

---

### 3. Summary: What Changes vs. What Does Not Change

| Property | Original Order [ u  v ] | Reversed Order [ v  u ] | Effect of Reversing Order |
|----------|-------------------------|-------------------------|---------------------------|
| **Determinant Value** | +11 | -11 | **Sign changes** (+ to -)[cite: 20, 23] |
| **Parallelogram Area** | 11 | 11 | **Does NOT change** (remains 11)[cite: 23] |

---

### 4. Detailed Explanation & Linear Algebra Insights

1. **What Changes in the Determinant (The Sign & Orientation):**
   * **Column Swap Property:** Swapping the two columns of a matrix multiplies its determinant by **-1**[cite: 20].
   * **Geometric Meaning of the Sign:**
     * In **det([ u  v ]) = +11**, the positive sign indicates that rotating vector u into vector v through the smaller angle follows a **counterclockwise** (right-handed) orientation[cite: 23].
     * In **det([ v  u ]) = -11**, the negative sign indicates that rotating vector v into vector u follows a **clockwise** (left-handed) orientation[cite: 23].
   * Reversing the vector order flips the geometric orientation, which causes the determinant to change its sign from +11 to -11[cite: 20, 23].

2. **What Does NOT Change in the Area (Geometric Magnitude):**
   * **Physical Parallelogram Area:** The geometric shape and physical space enclosed by two vectors depend strictly on their lengths and the angle between them, regardless of which vector is ordered first or second[cite: 23].
   * **Absolute Value Function:** Because physical area cannot be negative, area is defined as **Area = | det |**[cite: 18, 23]. Taking the absolute value removes the sign/orientation component, ensuring the computed area remains strictly **11 square units** under both ordering paths[cite: 23].

3. **Alternative Geometric Calculation Check (Base × Height Formula):**
   * Length of base vector u: ||u|| = √(3² + 1²) = √10.
   * Angle θ between u and v: cos(θ) = (u · v) / (||u|| × ||v||) = (3×1 + 1×4) / (√10 × √(1² + 4²)) = 7 / (√10 × √17) = 7 / √170.
   * sin(θ) = √(1 - cos²(θ)) = √(1 - 49/170) = √(121/170) = 11 / √170.
   * Area = ||u|| × ||v|| × sin(θ) = √10 × √17 × (11 / √170) = √170 × (11 / √170) = **11**.
   * The classical geometric base-times-height formula yields 11 square units, matching the determinant result exactly!
