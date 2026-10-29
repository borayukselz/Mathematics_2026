# Exercise 15: Associativity of Multiplication and Different Calculation Paths

### Given Matrices

**Matrix A (2 × 3):**
[  1   2   0 ]
[  0   1   1 ]

**Matrix B (3 × 2):**
[  1   0 ]
[  2   1 ]
[ -1   3 ]

**Matrix C (2 × 2):**
[  2   1 ]
[  0  -1 ]

---

### 1. Compute Path 1: (AB)C

#### Step 1A: Compute Intermediate Product AB (Size: 2 × 2)
Multiply Matrix A (2 × 3) by Matrix B (3 × 2)[cite: 17]:

* **Top-left (1,1):**     (1 × 1) + (2 × 2) + (0 × -1) = 1 + 4 + 0 = 5[cite: 17]
* **Top-right (1,2):**    (1 × 0) + (2 × 1) + (0 × 3)  = 0 + 2 + 0 = 2[cite: 17]
* **Bottom-left (2,1):**  (0 × 1) + (1 × 2) + (1 × -1) = 0 + 2 - 1 = 1[cite: 17]
* **Bottom-right (2,2):** (0 × 0) + (1 × 1) + (1 × 3)  = 0 + 1 + 3 = 4[cite: 17]

**Matrix AB:**
[  5   2 ]
[  1   4 ]

* **Operations in Step 1A:**
  * Multiplications: 2 × 2 × 3 = 12
  * Additions: 2 × 2 × 2 = 8

---

#### Step 1B: Multiply (AB) by Matrix C
Multiply intermediate matrix AB (2 × 2) by Matrix C (2 × 2)[cite: 17]:

* **Top-left (1,1):**     (5 × 2) + (2 × 0)  = 10 + 0 = 10[cite: 17]
* **Top-right (1,2):**    (5 × 1) + (2 × -1) = 5 - 2 = 3[cite: 17]
* **Bottom-left (2,1):**  (1 × 2) + (4 × 0)  = 2 + 0 = 2[cite: 17]
* **Bottom-right (2,2):** (1 × 1) + (4 × -1) = 1 - 4 = -3[cite: 17]

**Result for (AB)C:**
[ 10   3 ]
[  2  -3 ]

* **Operations in Step 1B:**
  * Multiplications: 2 × 2 × 2 = 8
  * Additions: 2 × 2 × 1 = 4

* **Total Path 1 Operations:** 20 multiplications, 12 additions (32 total operations).

---

### 2. Compute Path 2: A(BC)

#### Step 2A: Compute Intermediate Product BC (Size: 3 × 2)
Multiply Matrix B (3 × 2) by Matrix C (2 × 2)[cite: 17]:

* **Row 1, Column 1:** (1 × 2) + (0 × 0)  = 2 + 0 = 2[cite: 17]
* **Row 1, Column 2:** (1 × 1) + (0 × -1) = 1 + 0 = 1[cite: 17]
* **Row 2, Column 1:** (2 × 2) + (1 × 0)  = 4 + 0 = 4[cite: 17]
* **Row 2, Column 2:** (2 × 1) + (1 × -1) = 2 - 1 = 1[cite: 17]
* **Row 3, Column 1:** (-1 × 2) + (3 × 0)  = -2 + 0 = -2[cite: 17]
* **Row 3, Column 2:** (-1 × 1) + (3 × -1) = -1 - 3 = -4[cite: 17]

**Matrix BC:**
[  2   1 ]
[  4   1 ]
[ -2  -4 ]

* **Operations in Step 2A:**
  * Multiplications: 3 × 2 × 2 = 12
  * Additions: 3 × 2 × 1 = 6

---

#### Step 2B: Multiply Matrix A by (BC)
Multiply Matrix A (2 × 3) by intermediate matrix BC (3 × 2)[cite: 17]:

* **Top-left (1,1):**     (1 × 2) + (2 × 4) + (0 × -2) = 2 + 8 + 0 = 10[cite: 17]
* **Top-right (1,2):**    (1 × 1) + (2 × 1) + (0 × -4) = 1 + 2 + 0 = 3[cite: 17]
* **Bottom-left (2,1):**  (0 × 2) + (1 × 4) + (1 × -2) = 0 + 4 - 2 = 2[cite: 17]
* **Bottom-right (2,2):** (0 × 1) + (1 × 1) + (1 × -4) = 0 + 1 - 4 = -3
