# Exercise 3: When Can Matrices Be Multiplied?

## Exercise Reminder

Given four matrices with the following dimensions:

* Matrix `A`: size `2 × 3`
* Matrix `B`: size `3 × 4`
* Matrix `C`: size `4 × 2`
* Matrix `D`: size `2 × 2`

Consider the eight matrix products:

`AB`, `BA`, `BC`, `CB`, `AC`, `CA`, `AD`, `DA`

For each product:
1. Determine whether the product is defined.
2. If it is defined, state the size of the resulting product matrix.
3. Justify each decision using the dimension compatibility condition for matrix multiplication.

---

## Solution

### Summary of Results

| Product | Left Matrix Size | Right Matrix Size | Inner Dimensions | Status | Resulting Size |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **`AB`** | `2 × 3` | `3 × 4` | `3 = 3` (Match) | **Defined** | **`2 × 4`** |
| **`BA`** | `3 × 4` | `2 × 3` | `4 ≠ 2` (Mismatch) | **Undefined** | — |
| **`BC`** | `3 × 4` | `4 × 2` | `4 = 4` (Match) | **Defined** | **`3 × 2`** |
| **`CB`** | `4 × 2` | `3 × 4` | `2 ≠ 3` (Mismatch) | **Undefined** | — |
| **`AC`** | `2 × 3` | `4 × 2` | `3 ≠ 4` (Mismatch) | **Undefined** | — |
| **`CA`** | `4 × 2` | `2 × 3` | `2 = 2` (Match) | **Defined** | **`4 × 3`** |
| **`AD`** | `2 × 3` | `2 × 2` | `3 ≠ 2` (Mismatch) | **Undefined** | — |
| **`DA`** | `2 × 2` | `2 × 3` | `2 = 2` (Match) | **Defined** | **`2 × 3`** |

---

### Main Steps & Justifications

1. **Product `AB` (`(2 × 3) · (3 × 4)`):**
   * Compare the inner dimensions: `A` has `3` columns and `B` has `3` rows.
   * Since `3 = 3`, the product `AB` is **defined**.
   * Taking the outer dimensions gives a resulting matrix of size **`2 × 4`**.

2. **Product `BA` (`(3 × 4) · (2 × 3)`):**
   * Compare the inner dimensions: `B` has `4` columns and `A` has `2` rows.
   * Since `4 ≠ 2`, the dimension compatibility condition fails, so `BA` is **undefined**.

3. **Product `BC` (`(3 × 4) · (4 × 2)`):**
   * Compare the inner dimensions: `B` has `4` columns and `C` has `4` rows.
   * Since `4 = 4`, the product `BC` is **defined**.
   * Taking the outer dimensions gives a resulting matrix of size **`3 × 2`**.

4. **Product `CB` (`(4 × 2) · (3 × 4)`):**
   * Compare the inner dimensions: `C` has `2` columns and `B` has `3` rows.
   * Since `2 ≠ 3`, the dimension compatibility condition fails, so `CB` is **undefined**.

5. **Product `AC` (`(2 × 3) · (4 × 2)`):**
   * Compare the inner dimensions: `A` has `3` columns and `C` has `4` rows.
   * Since `3 ≠ 4`, the dimension compatibility condition fails, so `AC` is **undefined**.

6. **Product `CA` (`(4 × 2) · (2 × 3)`):**
   * Compare the inner dimensions: `C` has `2` columns and `A` has `2` rows.
   * Since `2 = 2`, the product `CA` is **defined**.
   * Taking the outer dimensions gives a resulting matrix of size **`4 × 3`**.

7. **Product `AD` (`(2 × 3) · (2 × 2)`):**
   * Compare the inner dimensions: `A` has `3` columns and `D` has `2` rows.
   * Since `3 ≠ 2`, the dimension compatibility condition fails, so `AD` is **undefined**.

8. **Product `DA` (`(2 × 2) · (2 × 3)`):**
   * Compare the inner dimensions: `D` has `2` columns and `A` has `2` rows.
   * Since `2 = 2`, the product `DA` is **defined**.
   * Taking the outer dimensions gives a resulting matrix of size **`2 × 3`**.

---

### Property / Method Used

* **Dimension Compatibility Condition for Matrix Multiplication:**
  Let `X` be an `m × n` matrix and `Y` be a `p × q` matrix. The matrix product `XY` is defined **if and only if** the number of columns of the left matrix `X` equals the number of rows of the right matrix `Y` (`n = p`). When `n = p`, the product `XY` has size `m × q` (determined by the outer dimensions):

  `(m × n) · (n × q)  ──►  (m × q)`

* **Row-Column Dot Product Requirement:**
  Each `(i, j)` entry of `XY` is computed as the dot product of row `i` of `X` (which contains `n` entries) and column `j` of `Y` (which contains `p` entries). This dot product is valid only when both vectors have the same length (`n = p`).

---

### Mathematical Verification

* **Vector-Length Check for Defined Products:**
  * In `AB`: every row of `A` has `3` entries and every column of `B` has `3` entries, enabling `2 × 4 = 8` valid dot products.
  * In `BC`: every row of `B` has `4` entries and every column of `C` has `4` entries, enabling `3 × 2 = 6` valid dot products.
  * In `CA`: every row of `C` has `2` entries and every column of `A` has `2` entries, enabling `4 × 3 = 12` valid dot products.
  * In `DA`: every row of `D` has `2` entries and every column of `A` has `2` entries, enabling `2 × 3 = 6` valid dot products (matching the dimension-preserving behavior of left-multiplying a `2 × 3` matrix by a `2 × 2` square matrix).
* **Order-Sensitivity Check (Non-Commutativity of Dimensions):**
  * Notice that `AB`, `BC`, `CA`, and `DA` are all defined, whereas reversing the multiplication order (`BA`, `CB`, `AC`, `AD`) causes the inner dimensions to mismatch in every single case, confirming that matrix multiplication depends strictly on factor order.
