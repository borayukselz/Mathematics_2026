# Exercise 2: Addition and Scalar Multiplication

## Exercise Reminder

Given the two `2 × 2` matrices:

**Matrix A:**  
`[  1  2 ]`  
`[ -1  3 ]`

**Matrix B:**  
`[ 4  -2 ]`  
`[ 0   5 ]`

1. Compute the following matrix expressions:
   * `A + B`
   * `A - B`
   * `3A - 2B`
2. Explain why matrix addition is possible only for matrices of the same size.

---

## Solution

### 1. Computing `A + B`, `A - B`, and `3A - 2B`

#### Part (a): `A + B`

* **Result:**  
  `A + B =`  
  `[  5  0 ]`  
  `[ -1  8 ]`

* **Main Steps:**
  1. Confirm dimension compatibility: both `A` and `B` have size `2 × 2`, so their sum is defined and also has size `2 × 2`.
  2. Add corresponding entries `(A + B)ᵢⱼ = aᵢⱼ + bᵢⱼ`:
     * Row 1, Column 1: `1 + 4 = 5`
     * Row 1, Column 2: `2 + (-2) = 0`
     * Row 2, Column 1: `-1 + 0 = -1`
     * Row 2, Column 2: `3 + 5 = 8`

* **Property / Method Used:**
  * **Entrywise Matrix Addition:** For two matrices `A` and `B` of the same size `m × n`, their sum `A + B` is obtained by adding entries that occupy the exact same row and column positions: `(A + B)ᵢⱼ = aᵢⱼ + bᵢⱼ`.

* **Mathematical Verification:**
  * Subtracting `B` from the result `A + B` recovers the original matrix `A`:  
    `[  5 - 4   0 - (-2) ] = [  1  2 ]`  
    `[ -1 - 0      8 - 5 ] = [ -1  3 ] = A`

---

#### Part (b): `A - B`

* **Result:**  
  `A - B =`  
  `[ -3   4 ]`  
  `[ -1  -2 ]`

* **Main Steps:**
  1. Confirm dimension compatibility: both `A` and `B` are `2 × 2` matrices.
  2. Subtract corresponding entries `(A - B)ᵢⱼ = aᵢⱼ - bᵢⱼ`:
     * Row 1, Column 1: `1 - 4 = -3`
     * Row 1, Column 2: `2 - (-2) = 2 + 2 = 4`
     * Row 2, Column 1: `-1 - 0 = -1`
     * Row 2, Column 2: `3 - 5 = -2`

* **Property / Method Used:**
  * **Entrywise Matrix Subtraction:** Matrix difference is defined as `A - B = A + (-1)B`, meaning each entry of `B` is subtracted from the corresponding entry of `A`: `(A - B)ᵢⱼ = aᵢⱼ - bᵢⱼ`.

* **Mathematical Verification:**
  * Adding `B` back to `A - B` recovers `A`:  
    `[ -3 + 4   4 + (-2) ] = [  1  2 ]`  
    `[ -1 + 0     -2 + 5 ] = [ -1  3 ] = A`

---

#### Part (c): `3A - 2B`

* **Result:**  
  `3A - 2B =`  
  `[ -5  10 ]`  
  `[ -3  -1 ]`

* **Main Steps:**
  1. Multiply every entry of `A` by the scalar `3`:  
     `3A =`  
     `[ 3 · 1    3 · 2 ] = [  3  6 ]`  
     `[ 3 · (-1) 3 · 3 ] = [ -3  9 ]`
  2. Multiply every entry of `B` by the scalar `2`:  
     `2B =`  
     `[ 2 · 4   2 · (-2) ] = [ 8  -4 ]`  
     `[ 2 · 0   2 · 5    ] = [ 0  10 ]`
  3. Subtract `2B` from `3A` entry by entry:
     * Row 1, Column 1: `3 - 8 = -5`
     * Row 1, Column 2: `6 - (-4) = 6 + 4 = 10`
     * Row 2, Column 1: `-3 - 0 = -3`
     * Row 2, Column 2: `9 - 10 = -1`

* **Property / Method Used:**
  * **Scalar Multiplication & Linear Combination of Matrices:** Multiplying a matrix `M` by a scalar `c` scales every entry by `c` (`(cM)ᵢⱼ = c · mᵢⱼ`). Combining this with entrywise subtraction yields `(3A - 2B)ᵢⱼ = 3aᵢⱼ - 2bᵢⱼ`.

* **Mathematical Verification:**
  * Rewrite `3A - 2B` using the distributive property as `2(A - B) + A` and verify with the result from Part (b):  
    `2(A - B) + A =`  
    `[ 2 · (-3)  2 · 4    ] + [  1  2 ] = [ -6   8 ] + [  1  2 ] = [ -5  10 ]`  
    `[ 2 · (-1)  2 · (-2) ] + [ -1  3 ] = [ -2  -4 ] + [ -1  3 ] = [ -3  -1 ]`  
  * Both methods produce the identical `2 × 2` matrix.

---

### 2. Why Matrix Addition Requires Matrices of the Same Size

* **Result:**
  * Matrix addition is defined **position-by-position** (`(A + B)ᵢⱼ = aᵢⱼ + bᵢⱼ`), which requires a one-to-one pairing between every entry of `A` and an entry at the exact same `(i, j)` coordinate in `B`. If two matrices have different numbers of rows or columns, at least one entry in one matrix lacks a partner in the other, leaving the sum undefined.

* **Main Steps:**
  1. Recall the definition of matrix addition: for `A` of size `m × n` and `B` of size `p × q`, `(A + B)ᵢⱼ = aᵢⱼ + bᵢⱼ`.
  2. For this sum to be defined across the entire matrix, every row index `i` (`1 ≤ i ≤ m`) and column index `j` (`1 ≤ j ≤ n`) in `A` must also be valid indices in `B` (`1 ≤ i ≤ p` and `1 ≤ j ≤ q`), and vice versa.
  3. Therefore, addition is valid if and only if `m = p` and `n = q` (i.e., `A` and `B` have identical dimensions).

* **Property / Method Used:**
  * **Domain Definition of Matrix Addition:** Addition on matrices is a binary operation closed on the set of `m × n` matrices; differing dimensions violate the index-matching domain requirement.

* **Mathematical Verification:**
  * **Counterexample:** Let `C` be a `2 × 2` matrix (`[ 1  2 ; 3  4 ]`) and `D` be a `2 × 3` matrix (`[ 5  6  7 ; 8  9  10 ]`). Attempting to compute the `(1, 3)` entry of `C + D` requires evaluating `c₁₃ + d₁₃`, which is impossible because `C` has only `2` columns and `c₁₃` does not exist. Thus, `C + D` is undefined.
