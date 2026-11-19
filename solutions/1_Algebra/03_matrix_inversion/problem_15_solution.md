### Exercise 15. Two Methods for Solving the Same System

#### Exercise Reminder

For

$$
A =
\begin{pmatrix}
2 & 1 \\
1 & 3
\end{pmatrix},\qquad b =
\begin{pmatrix}
7 \\
8
\end{pmatrix},
$$

solve $Ax = b$ in two ways:
1. using $A^{-1}b$,
2. using Gaussian elimination.

Compare both solutions, the number of essential steps, and state which method was simpler in this example.

---

#### Solution

**Result.** Both methods yield the exact same unique solution vector:

$$
x =
\begin{pmatrix}
\frac{13}{5} \\
\frac{9}{5}
\end{pmatrix}.
$$

In this $2\times 2$ example with a single right-hand side vector $b$, **Gaussian elimination is simpler** because it avoids fractions until the final back-substitution step and requires fewer total arithmetic operations ($9$ operations vs. $13$ operations for $A^{-1}b$).

<br>

**Main steps.**

1. **Method 1 — Using $x = A^{-1}b$:**
   - **Step 1 (Determinant):** Compute $\det A$:

$$
\det A = (2)(3) - (1)(1) = 6 - 1 = 5 \neq 0.
$$

   - **Step 2 (Inverse matrix):** Apply the $2\times 2$ inverse formula:

$$
A^{-1} = \frac{1}{5}
\begin{pmatrix}
3 & -1 \\
-1 & 2
\end{pmatrix}.
$$

   - **Step 3 (Matrix-vector multiplication):** Compute $x = A^{-1}b$:

$$
x = A^{-1}b = \frac{1}{5}
\begin{pmatrix}
3 & -1 \\
-1 & 2
\end{pmatrix}
\begin{pmatrix}
7 \\
8
\end{pmatrix} = \frac{1}{5}
\begin{pmatrix}
3\cdot 7 + (-1)\cdot 8 \\
(-1)\cdot 7 + 2\cdot 8
\end{pmatrix} = \frac{1}{5}
\begin{pmatrix}
21 - 8 \\
-7 + 16
\end{pmatrix} = \frac{1}{5}
\begin{pmatrix}
13 \\
9
\end{pmatrix} =
\begin{pmatrix}
\frac{13}{5} \\
\frac{9}{5}
\end{pmatrix}.
$$

2. **Method 2 — Using Gaussian elimination:**
   - **Step 1 (Augmented matrix & row swap):** Form $[A \mid b]$ and swap rows $R_1 \leftrightarrow R_2$ so the leading $1$ in row $2$ serves as an integer pivot:

$$
[A \mid b] =
\left(
\begin{array}{cc|c}
2 & 1 & 7 \\
1 & 3 & 8
\end{array}
\right)
\xrightarrow{R_1 \leftrightarrow R_2}
\left(
\begin{array}{cc|c}
1 & 3 & 8 \\
2 & 1 & 7
\end{array}
\right).
$$

   - **Step 2 (Forward elimination):** Eliminate the $(2,1)$ entry below the pivot via $R_2 \leftarrow R_2 - 2R_1$:

$$
\left(
\begin{array}{cc|c}
1 & 3 & 8 \\
2 & 1 & 7
\end{array}
\right)
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\left(
\begin{array}{cc|c}
1 & 3 & 8 \\
0 & -5 & -9
\end{array}
\right).
$$

   - **Step 3 (Back-substitution):** Solve from the bottom row upward:

$$
-5x_2 = -9 \implies x_2 = \frac{9}{5}, \qquad x_1 + 3\left(\frac{9}{5}\right) = 8 \implies x_1 = 8 - \frac{27}{5} = \frac{13}{5}.
$$

3. **Comparison of both methods and essential steps:**

| Criterion | Method 1: $x = A^{-1}b$ | Method 2: Gaussian Elimination |
| :--- | :--- | :--- |
| **Solution obtained** | $x = (13/5, \ 9/5)^T$ | $x = (13/5, \ 9/5)^T$ |
| **Essential stages** | $3$ stages ($\det A$, $A^{-1}$, $A^{-1}b$) | $3$ stages (pivot setup, $1$ elimination, back-sub.) |
| **Arithmetic count** | $3$ op. ($\det$) + $4$ op. ($A^{-1}$) + $6$ op. ($A^{-1}b$) = $13$ | $4$ op. (row elim.) + $5$ op. (back-sub.) = $9$ |
| **Best use case** | Multiple systems $Ax = b_k$ with the same $A$ | Single linear system $Ax = b$ |

   - **Which method was simpler:** **Gaussian elimination** was simpler here because a single row swap gave a unit pivot, reducing the system to upper triangular form in one row operation with $4$ fewer scalar calculations than forming $A^{-1}$ and multiplying by $b$.

<br>

**Property / method used.** *Equivalence of inverse-matrix multiplication and Gaussian elimination:* for an invertible matrix $A$, row-reducing $[A \mid b]$ to echelon form and back-substituting solves the exact same system as left-multiplying by $A^{-1}$, while avoiding the extra work of computing all columns of $A^{-1}$.

<br>

**Mathematical verification.** Substituting $x_1 = \frac{13}{5}$ and $x_2 = \frac{9}{5}$ back into $Ax$ confirms that it reproduces $b$:

$$
Ax =
\begin{pmatrix}
2 & 1 \\
1 & 3
\end{pmatrix}
\begin{pmatrix}
\frac{13}{5} \\
\frac{9}{5}
\end{pmatrix} =
\begin{pmatrix}
2\cdot \frac{13}{5} + 1\cdot \frac{9}{5} \\
1\cdot \frac{13}{5} + 3\cdot \frac{9}{5}
\end{pmatrix} =
\begin{pmatrix}
\frac{26 + 9}{5} \\
\frac{13 + 27}{5}
\end{pmatrix} =
\begin{pmatrix}
\frac{35}{5} \\
\frac{40}{5}
\end{pmatrix} =
\begin{pmatrix}
7 \\
8
\end{pmatrix} = b.
$$
