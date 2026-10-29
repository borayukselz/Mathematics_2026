# Exercise 13: A Recurrence Written in Matrix Form

### Given Matrix

**Matrix F:**
[  1   1 ]
[  1   0 ]

---

### 1. Compute Matrix Powers: F², F³, F⁴, and F⁵

#### A. Compute F² (F × F)

* **Result:**
  [  2   1 ]
  [  1   1 ]

* **Detailed Calculation Steps:**
  * Top-left entry (1,1):     (1 × 1) + (1 × 1) = 1 + 1 = 2[cite: 15]
  * Top-right entry (1,2):    (1 × 1) + (1 × 0) = 1 + 0 = 1[cite: 15]
  * Bottom-left entry (2,1):  (1 × 1) + (0 × 1) = 1 + 0 = 1[cite: 15]
  * Bottom-right entry (2,2): (1 × 1) + (0 × 0) = 1 + 0 = 1[cite: 15]

---

#### B. Compute F³ (F² × F)

* **Result:**
  [  3   2 ]
  [  2   1 ]

* **Detailed Calculation Steps:**
  * Top-left entry (1,1):     (2 × 1) + (1 × 1) = 2 + 1 = 3[cite: 15]
  * Top-right entry (1,2):    (2 × 1) + (1 × 0) = 2 + 0 = 2[cite: 15]
  * Bottom-left entry (2,1):  (1 × 1) + (1 × 1) = 1 + 1 = 2[cite: 15]
  * Bottom-right entry (2,2): (1 × 1) + (1 × 0) = 1 + 0 = 1[cite: 15]

---

#### C. Compute F⁴ (F³ × F)

* **Result:**
  [  5   3 ]
  [  3   2 ]

* **Detailed Calculation Steps:**
  * Top-left entry (1,1):     (3 × 1) + (2 × 1) = 3 + 2 = 5[cite: 15]
  * Top-right entry (1,2):    (3 × 1) + (2 × 0) = 3 + 0 = 3[cite: 15]
  * Bottom-left entry (2,1):  (2 × 1) + (1 × 1) = 2 + 1 = 3[cite: 15]
  * Bottom-right entry (2,2): (2 × 1) + (1 × 0) = 2 + 0 = 2[cite: 15]

---

#### D. Compute F⁵ (F⁴ × F)

* **Result:**
  [  8   5 ]
  [  5   3 ]

* **Detailed Calculation Steps:**
  * Top-left entry (1,1):     (5 × 1) + (3 × 1) = 5 + 3 = 8[cite: 15]
  * Top-right entry (1,2):    (5 × 1) + (3 × 0) = 5 + 0 = 5[cite: 15]
  * Bottom-left entry (2,1):  (3 × 1) + (2 × 1) = 3 + 2 = 5[cite: 15]
  * Bottom-right entry (2,2): (3 × 1) + (2 × 0) = 3 + 0 = 3[cite: 15]

---

### 2. Comparison with the Sequence 0, 1, 1, 2, 3, 5, 8, ...

#### A. The Fibonacci Sequence
The given sequence **0, 1, 1, 2, 3, 5, 8, ...** is the **Fibonacci Sequence** (denoted by f_n)[cite: 15]:
* f₀ = 0[cite: 15]
* f₁ = 1[cite: 15]
* f₂ = 1[cite: 15]
* f₃ = 2[cite: 15]
* f₄ = 3[cite: 15]
* f₅ = 5[cite: 15]
* f₆ = 8[cite: 15]

---

#### B. Observed Relationship

When comparing the entries of matrix powers Fⁿ with the Fibonacci terms:

* **F¹:**
  [ 1  1 ] = [ f₂  f₁ ]
  [ 1  0 ]   [ f₁  f₀ ][cite: 15]

* **F²:**
  [ 2  1 ] = [ f₃  f₂ ]
  [ 1  1 ]   [ f₂  f₁ ][cite: 15]

* **F³:**
  [ 3  2 ] = [ f₄  f₃ ]
  [ 2  1 ]   [ f₃  f₂ ][cite: 15]

* **F⁴:**
  [ 5  3 ] = [ f₅  f₄ ]
  [ 3  2 ]   [ f₄  f₃ ][cite: 15]

* **F⁵:**
  [ 8  5 ] = [ f₆  f₅ ]
  [ 5  3 ]   [ f₅  f₄ ][cite: 15]

* **General Formula:**
  For any positive integer n:
  **Fⁿ = [ f_(n+1)   f_n     ]**
         **[ f_n       f_(n-1) ]**[cite: 15]

Every entry in the matrix Fⁿ is a specific term from the Fibonacci sequence![cite: 15]

---

### 3. Compute Matrix-Vector Multiplication: F × [ a ; b ]

* **Result:**
  [ a + b ]
  [   a   ][cite: 15]

* **Detailed Calculation Steps:**
  * Top entry:    (1 × a) + (1 × b) = **a + b**[cite: 15]
  * Bottom entry: (1 × a) + (0 × b) = **a**[cite: 15]

---

### 4. Detailed Explanation: How This Multiplication Performs a Recurrence Step

1. **Understanding the Recurrence Formula:**
   * The Fibonacci sequence is defined by the linear recurrence relation:
     **f_(k+1) = f_k + f_(k-1)**
   * To calculate the next number in the sequence, you must know the **two preceding consecutive terms**.

2. **How Matrix F Transforms State Vectors:**
   * Imagine a vector holding two consecutive terms of the sequence:
     Input Vector = [  a  ] = [ f_k     ]  (Current term)
                    [  b  ]   [ f_(k-1) ]  (Previous term)[cite: 15]

   * When you multiply this vector by Matrix F:
     F × [  a  ] = [ 1  1 ] × [  a  ] = [ a + b ]
         [  b  ]   [ 1  0 ]   [  b  ]   [   a   ][cite: 15]

3. **Role of the Two Rows:**
   * **Row 1 (Sum Creation):** Compute `a + b`[cite: 15]. Since `a = f_k` and `b = f_(k-1)`, `a + b` calculates the **new next term** `f_(k+1)`[cite: 15].
   * **Row 2 (Memory / Shift):** Keeps `a` unchanged[cite: 15]. The previous larger term (`f_k`) becomes the new lower entry, preserving it for the subsequent step[cite: 15].

4. **Output Vector:**
   Output Vector = [ a + b ] = [ f_(k+1) ]  (New term)
                   [   a   ]   [ f_k     ]  (Updated previous term)[cite: 15]

5. **Key Takeaway:**
   * Multiplying by Matrix F acts as a **single time step forward** in the recurrence[cite: 15].
   * Multiplying by Fⁿ advances the recurrence by **n steps simultaneously**!
   * This is why matrix powers allow us to compute extremely large Fibonacci numbers efficiently without calculating every intermediate number sequentially.
