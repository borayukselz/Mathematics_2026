### Exercise 5. Row Operations

#### Exercise Reminder

For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2 \\
\end{pmatrix},
$$

find $\det A$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

---

#### Solution

**Result.**

$$
\det A = 21.
$$

<br>

**Main steps.** Reduce $A$ to an upper triangular matrix $U$ using elementary row operations while tracking the effect of each operation on the determinant:

1. **Step 1 — Eliminate the $(2,1)$ entry via $R_2 \leftarrow R_2 - 2R_1$:**

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2 \\
\end{pmatrix}
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
-1 & 4 & 2 \\
\end{pmatrix}= A_1.
$$

- **Effect on determinant:** **Does not change** ($\det A_1 = \det A$), because adding a scalar multiple of one row to another row leaves the determinant unchanged.

2. **Step 2 — Eliminate the $(3,1)$ entry via $R_3 \leftarrow R_3 + R_1$:**

$$
A_1=
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
-1 & 4 & 2 \\
\end{pmatrix}
\xrightarrow{R_3 \leftarrow R_3 + R_1}
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 6 & 5 \\
\end{pmatrix}= A_2.
$$

- **Effect on determinant:** **Does not change** ($\det A_2 = \det A_1 = \det A$), because this is again a row replacement operation.

3. **Step 3 — Eliminate the $(3,2)$ entry via $R_3 \leftarrow R_3 + 2R_2$:**

$$
A_2=
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 6 & 5 \\
\end{pmatrix}
\xrightarrow{R_3 \leftarrow R_3 + 2R_2}
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 0 & -7 \\
\end{pmatrix}= U.
$$

- **Effect on determinant:** **Does not change** ($\det U = \det A_2 = \det A$), because adding $2R_2$ to $R_3$ is a row replacement operation.

4. **Step 4 — Compute $\det U$ from the upper triangular form:**

$$
\det A = \det U = 1 \cdot (-3) \cdot (-7) = 21.
$$

<br>

**Property / method used.** *Gaussian elimination for determinants:*
- **Row replacement** ($R_i \leftarrow R_i + cR_j$ for $i \neq j$): preserves the determinant ($\det_{\text{new}} = \det_{\text{old}}$).
- **Row swap** ($R_i \leftrightarrow R_j$): multiplies the determinant by $-1$ (not needed here because all pivots are nonzero).
- **Row scaling** ($R_i \leftarrow kR_i$): multiplies the determinant by $k$ (not needed here).
- **Upper triangular determinant:** once reduced to upper triangular form $U$, $\det U$ equals the product of the main diagonal entries.

<br>

**Mathematical verification.** Computing $\det A$ directly by Sarrus' rule confirms the result:

$$
\det A = \bigl(1\cdot 1\cdot 2 + 2\cdot 0\cdot (-1) + 3\cdot 2\cdot 4\bigr) - \bigl((-1)\cdot 1\cdot 3 + 4\cdot 0\cdot 1 + 2\cdot 2\cdot 2\bigr) = (2 + 0 + 24) - (-3 + 0 + 8) = 26 - 5 = 21.
$$
