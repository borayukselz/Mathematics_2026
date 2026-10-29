# Exercise 1: Matrix Size and Entries

### Given Matrices

**Matrix A:**
[  2  -1   3 ]
[  0   4   5 ]

**Matrix B:**
[  1   0 ]
[ -2   3 ]
[  4   1 ]

---

### 1. State the sizes of matrices A and B

* **Result:** Matrix A is **2 × 3** and Matrix B is **3 × 2**.
* **Main Steps:** Count horizontal rows (m), then vertical columns (n).
  * Matrix A: 2 rows, 3 columns → 2 × 3
  * Matrix B: 3 rows, 2 columns → 3 × 2
* **Method & Explanation:** The size (dimension) of a matrix is expressed as m × n, where m is the number of rows and n is the number of columns.
* **Mathematical Verification:** Matrix A has 3 elements horizontally per row, while Matrix B has 3 elements vertically per column, confirming dimensions 2 × 3 and 3 × 2.

---

### 2. Read off the entries a₁₂, a₂₃, b₂₁, and b₃₂

* **Result:**
  * **a₁₂ = -1**
  * **a₂₃ = 5**
  * **b₂₁ = -2**
  * **b₃₂ = 1**
* **Main Steps:** Locate the entry at the intersection of row i and column j:
  * **a₁₂:** Row 1, Column 2 of Matrix A → **-1**
  * **a₂₃:** Row 2, Column 3 of Matrix A → **5**
  * **b₂₁:** Row 2, Column 1 of Matrix B → **-2**
  * **b₃₂:** Row 3, Column 2 of Matrix B → **1**
* **Method & Explanation:** Subscript notation designates the row number first and the column number second.
* **Mathematical Verification:** Cross-referencing position coordinates confirms each selected entry matches its indices.

---

### 3. Write the second row of A and the first column of B as vectors

* **Result:**
  * **Second row of A (Row Vector):**
    [ 0  4  5 ]
  * **First column of B (Column Vector):**
    [  1 ]
    [ -2 ]
    [  4 ]
* **Main Steps:** Extract row 2 of A horizontally into a 1 × 3 vector and column 1 of B vertically into a 3 × 1 vector.
* **Method & Explanation:** A row vector maintains horizontal orientation, whereas a column vector maintains vertical orientation.
* **Mathematical Verification:** Vector dimensions match the respective matrix dimensions (the row vector has 3 elements matching A's column count; the column vector has 3 elements matching B's row count).
