# Exercise 9: Composing Transformations

### Given

**Scaling Matrix S (nonuniform scaling - stretches x-axis by factor of 2):**
[  2   0 ]
[  0   1 ]

**Rotation Matrix R (90° counterclockwise rotation):**
[  0  -1 ]
[  1   0 ]

**Vector x:**
[  1 ]
[  2 ]

---

### 1. Compute RSx

* **Result:**
  [ -2 ]
  [  2 ]

* **Detailed Calculation Steps:**
  * **Step 1: Apply Matrix S to Vector x first (Sx)**[cite: 11]
    [  2   0 ]   [  1 ]   [ (2 × 1) + (0 × 2) ]   [ 2 ]
    [  0   1 ] × [  2 ] = [ (0 × 1) + (1 × 2) ] = [ 2 ]

  * **Step 2: Apply Matrix R to the resulting vector (R(Sx))**[cite: 11]
    [  0  -1 ]   [ 2 ]   [ (0 × 2) + (-1 × 2) ]   [ -2 ]
    [  1   0 ] × [ 2 ] = [ (1 × 2) + (0 × 2)  ] = [  2 ]

* **Method & Explanation:**
  Matrix transformation order is read from **right to left**[cite: 11]. In RSx, transformation S acts on vector x first, and then transformation R acts on the resulting vector Sx[cite: 11].

* **Mathematical Verification (via Composite Matrix RS):**
  1. Calculate composite matrix RS = R × S[cite: 11]:
     [  0  -1 ]   [ 2  0 ]   [ (0×2)+(-1×0)  (0×0)+(-1×1) ]   [ 0  -1 ]
     [  1   0 ] × [ 0  1 ] = [ (1×2)+(0×0)   (1×0)+(0×1)  ] = [ 2   0 ]

  2. Multiply composite matrix RS by vector x[cite: 11]:
     [ 0  -1 ]   [ 1 ]   [ (0 × 1) + (-1 × 2) ]   [ -2 ]
     [ 2   0 ] × [ 2 ] = [ (2 × 1) + (0 × 2)  ] = [  2 ]
  *Both methods give the exact same result.*

---

### 2. Compute SRx

* **Result:**
  [ -4 ]
  [  1 ]

* **Detailed Calculation Steps:**
  * **Step 1: Apply Matrix R to Vector x first (Rx)**[cite: 11]
    [  0  -1 ]   [  1 ]   [ (0 × 1) + (-1 × 2) ]   [ -2 ]
    [  1   0 ] × [  2 ] = [ (1 × 1) + (0 × 2)  ] = [  1 ]

  * **Step 2: Apply Matrix S to the resulting vector (S(Rx))**[cite: 11]
    [  2   0 ]   [ -2 ]   [ (2 × -2) + (0 × 1) ]   [ -4 ]
    [  0   1 ] × [  1 ] = [ (0 × -2) + (1 × 1) ] = [  1 ]

* **Method & Explanation:**
  In SRx, transformation R acts on vector x first, and then transformation S acts on the resulting vector Rx[cite: 11].

* **Mathematical Verification (via Composite Matrix SR):**
  1. Calculate composite matrix SR = S × R[cite: 11]:
     [ 2  0 ]   [ 0  -1 ]   [ (2×0)+(0×1)  (2×-1)+(0×0) ]   [ 0  -2 ]
     [ 0  1 ] × [ 1   0 ] = [ (0×0)+(1×1)  (0×-1)+(1×0) ] = [ 1   0 ]

  2. Multiply composite matrix SR by vector x[cite: 11]:
     [ 0  -2 ]   [ 1 ]   [ (0 × 1) + (-2 × 2) ]   [ -4 ]
     [ 1   0 ] × [ 2 ] = [ (1 × 1) + (0 × 0)  ] = [  1 ]
  *Both methods give the exact same result.*

---

### 3. Compare Results

* **Comparison:**
  * **RSx** = [ -2,  2 ][cite: 11]
  * **SRx** = [ -4,  1 ][cite: 11]
* **Conclusion:** **RSx ≠ SRx**[cite: 11]. 
  The order in which geometric transformations are applied produces entirely different final position vectors[cite: 11].

---

### 4. Detailed Geometric Explanation of Why Order Matters

1. **Order of Operation Principle:**
   * Matrix-vector multiplication represents composition of transformations[cite: 11].
   * The matrix written directly adjacent to the vector is executed **first**[cite: 11].

2. **Geometric Breakdown of RSx (Scale First, Then Rotate):**
   * **Initial State:** Start at vector x = [1, 2] in Quadrant I[cite: 11].
   * **First Transformation (S):** Nonuniform scaling stretches the x-axis by a factor of 2[cite: 11]. 
     * The original horizontal distance of 1 doubles to 2[cite: 11].
     * The vertical distance remains 2[cite: 11].
     * Vector becomes **[2, 2]**[cite: 11].
   * **Second Transformation (R):** A 90° counterclockwise rotation rotates the scaled vector [2, 2] around the origin into Quadrant II[cite: 11].
     * The point [2, 2] moves to **[-2, 2]**[cite: 11].

3. **Geometric Breakdown of SRx (Rotate First, Then Scale):**
   * **Initial State:** Start at vector x = [1, 2] in Quadrant I[cite: 11].
   * **First Transformation (R):** A 90° counterclockwise rotation rotates vector [1, 2] into Quadrant II before any scaling happens[cite: 11].
     * The original y-value (2) swings over onto the negative x-axis[cite: 11].
     * The original x-value (1) swings up onto the positive y-axis[cite: 11].
     * Vector becomes **[-2, 1]**[cite: 11].
   * **Second Transformation (S):** Nonuniform scaling stretches whatever component currently lies along the horizontal (x) axis by a factor of 2[cite: 11].
     * Because rotation happened first, the value -2 is now sitting on the x-axis[cite: 11].
     * Scaling doubles this horizontal component from -2 to -4[cite: 11].
     * The vertical component remains 1[cite: 11].
     * Vector becomes **[-4, 1]**[cite: 11].

4. **Why the Results Differ (Core Insight):**
   * Nonuniform scaling Matrix S ONLY modifies coordinates along the horizontal x-axis[cite: 11].
   * Rotating a vector by 90° interchanges its horizontal and vertical components[cite: 11].
   * In **RSx**, Matrix S stretches the **original x-component (1)** into 2 before rotation[cite: 11].
   * In **SRx**, Rotation R moves the **original y-component (2)** onto the x-axis first, so Matrix S ends up stretching that rotated value (2) into 4 instead[cite: 11].
   * Because rotation changes which component sits on the x-axis, applying scaling before versus after rotation affects completely different geometric features of the vector[cite: 11]!
