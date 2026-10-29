# Exercise 11: When Do Matrices Commute?

### Given

**Matrix A:**
[  1   1 ]
[  0   1 ]

**Matrix B:**
[  a   b ]
[  c   d ]

---

### 1. Compute Matrix Product AB

* **Result:**
  [  a + c   b + d ]
  [    c       d   ]

* **Detailed Calculation Steps:**
  * Top-left entry (1,1):     (1 × a) + (1 × c) = a + c[cite: 13]
  * Top-right entry (1,2):    (1 × b) + (1 × d) = b + d[cite: 13]
  * Bottom-left entry (2,1):  (0 × a) + (1 × c) = c[cite: 13]
  * Bottom-right entry (2,2): (0 × b) + (1 × d) = d[cite: 13]

* **Method & Explanation:**
  Multiply row i of Matrix A by column j of Matrix B using standard row-column dot products[cite: 13].

---

### 2. Compute Matrix Product BA

* **Result:**
  [  a   a + b ]
  [  c   c + d ]

* **Detailed Calculation Steps:**
  * Top-left entry (1,1):     (a × 1) + (b × 0) = a[cite: 13]
  * Top-right entry (1,2):    (a × 1) + (b × 1) = a + b[cite: 13]
  * Bottom-left entry (2,1):  (c × 1) + (d × 0) = c[cite: 13]
  * Bottom-right entry (2,2): (c × 1) + (d × 1) = c + d[cite: 13]

* **Method & Explanation:**
  Multiply row i of Matrix B by column j of Matrix A using standard row-column dot products[cite: 13].

---

### 3. Determine Conditions on a, b, c, d for AB = BA

* **System of Equations:**
  Set AB equal to BA by equating entries in corresponding positions[cite: 13]:
  [  a + c   b + d ]   =   [  a   a + b ]
  [    c       d   ]       [  c   c + d ]

  1. **Entry (1,1):**  a + c = a        →  **c = 0**[cite: 13]
  2. **Entry (1,2):**  b + d = a + b    →  **d = a**[cite: 13]
  3. **Entry (2,1):**  c = c            →  Always true[cite: 13]
  4. **Entry (2,2):**  d = c + d        →  c = 0  (confirms condition 1)[cite: 13]

* **Summary of Conditions:**
  * **c = 0:** Matrix B must be upper triangular[cite: 13].
  * **a = d:** The main diagonal entries of Matrix B must be equal[cite: 13].
  * **b:** Can be any real number (free parameter)[cite: 13].
  * **a:** Can be any real number (free parameter)
