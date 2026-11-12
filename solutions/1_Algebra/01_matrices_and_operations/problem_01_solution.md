# Exercise 1: Matrix Size and Entries

## Exercise Reminder

Given the two matrices:

**Matrix A:**  
`[ 2  -1  3 ]`  
`[ 0   4  5 ]`

**Matrix B:**  
`[  1  0 ]`  
`[ -2  3 ]`  
`[  4  1 ]`

where `aᵢⱼ` and `bᵢⱼ` denote the entries in row `i` and column `j` of matrices `A` and `B`, respectively:

1. State the sizes of matrices `A` and `B`.
2. Read off the entries `a₁₂`, `a₂₃`, `b₂₁`, and `b₃₂`.
3. Write the second row of `A` and the first column of `B` as vectors.

---

## Solution

### 1. Sizes of Matrices A and B

* **Result:**
  * Size of `A`: **2 × 3**
  * Size of `B`: **3 × 2**

* **Main Steps:**
  1. Count the horizontal rows and vertical columns of `A`: it has 2 rows and 3 columns, giving size **2 × 3**.
  2. Count the horizontal rows and vertical columns of `B`: it has 3 rows and 2 columns, giving size **3 × 2**.

* **Property / Method Used:**
  * **Matrix Dimension Convention:** A matrix with `m` horizontal rows and `n` vertical columns has size (order) `m × n`, where the row count `m` is always written first and the column count `n` second.

* **Mathematical Verification:**
  * Multiplying the dimensions gives the total number of entries: `A` contains `2 · 3 = 6` entries and `B` contains `3 · 2 = 6` entries, matching the 6 numbers displayed in each matrix.

---

### 2. Specific Matrix Entries (a₁₂, a₂₃, b₂₁, and b₃₂)

* **Result:**
  * **a₁₂ = -1**
  * **a₂₃ = 5**
  * **b₂₁ = -2**
  * **b₃₂ = 1**

* **Main Steps:**
  1. For `a₁₂`, locate row 1 of `A` (`[ 2  -1  3 ]`) and take its 2nd entry: `-1`.
  2. For `a₂₃`, locate row 2 of `A` (`[ 0   4  5 ]`) and take its 3rd entry: `5`.
  3. For `b₂₁`, locate row 2 of `B` (`[ -2  3 ]`) and take its 1st entry: `-2`.
  4. For `b₃₂`, locate row 3 of `B` (`[  4  1 ]`) and take its 2nd entry: `1`.

* **Property / Method Used:**
  * **Double-Subscript Indexing:** In standard matrix notation `xᵢⱼ`, the first subscript `i` specifies the row index (top to bottom) and the second subscript `j` specifies the column index (left to right).

* **Mathematical Verification:**
  * Every index pair `(i, j)` satisfies `1 ≤ i ≤ m` and `1 ≤ j ≤ n` for its respective matrix, and mapping all entries by position confirms each value:
    * Matrix `A` positions:  
      `[ a₁₁  a₁₂  a₁₃ ] = [ 2  -1  3 ]`  
      `[ a₂₁  a₂₂  a₂₃ ] = [ 0   4  5 ]`
    * Matrix `B` positions:  
      `[ b₁₁  b₁₂ ] = [  1  0 ]`  
      `[ b₂₁  b₂₂ ] = [ -2  3 ]`  
      `[ b₃₁  b₃₂ ] = [  4  1 ]`

---

### 3. Second Row of A and First Column of B as Vectors

* **Result:**
  * **Second row of A (Row Vector):**  
    `r₂ = [ 0  4  5 ]`

  * **First column of B (Column Vector):**  
    `c₁ =`  
    `[  1 ]`  
    `[ -2 ]`  
    `[  4 ]`

* **Main Steps:**
  1. Extract all entries from the 2nd row of `A` in left-to-right order (`a₂₁, a₂₂, a₂₃`) to form the `1 × 3` row vector `[ 0  4  5 ]`.
  2. Extract all entries from the 1st column of `B` in top-to-bottom order (`b₁₁, b₂₁, b₃₁`) to form the `3 × 1` column vector with entries `1`, `-2`, and `4`.

* **Property / Method Used:**
  * **Row and Column Partitioning:** Any row `i` of an `m × n` matrix forms a `1 × n` row vector, and any column `j` forms an `m × 1` column vector.

* **Mathematical Verification:**
  * Since `A` has 3 columns, its second row vector `r₂` must have size `1 × 3` (3 entries), matching `[ 0  4  5 ]`.
  * Since `B` has 3 rows, its first column vector `c₁` must have size `3 × 1` (3 entries), matching the vertical vector with entries `1`, `-2`, and `4`.
