### Exercise 11. Shortening the Calculation with Row Operations

#### Exercise Reminder

Compute

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}
$$

by first performing row operations that create as many zeros as possible. State which operations do not change the determinant.

---

#### Solution

**Result.**

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}= 1.
$$

None of the row operations used below change the determinant, because every step is a **row replacement** operation of the form $R_i \leftarrow R_i + cR_j$ ($i \neq j$).

<br>

**Main steps.** Let

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}.
$$

Apply row replacement operations to introduce zeros below the main diagonal (and optionally above it as well):

1. **Create zeros in column $1$ below the $(1,1)$ pivot** via $R_2 \leftarrow R_2 - R_1$ and $R_3 \leftarrow R_3 - R_1$:

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}
\xrightarrow{\substack{R_2 \leftarrow R_2 - R_1 \\ R_3 \leftarrow R_3 - R_1}}
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 2 & 3 \\
\end{pmatrix}= A_1.
$$

2. **Create a zero in column $2$ below the $(2,2)$ pivot** via $R_3 \leftarrow R_3 - 2R_2$:

$$
A_1=
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 2 & 3 \\
\end{pmatrix}
\xrightarrow{R_3 \leftarrow R_3 - 2R_2}
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1 \\
\end{pmatrix}= U.
$$

3. *(Optional)* **Eliminate the entries above the diagonal** via $R_2 \leftarrow R_2 - R_3$, $R_1 \leftarrow R_1 - 3R_3$, and $R_1 \leftarrow R_1 - 2R_2$ to obtain six zeros:

$$
U=
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1 \\
\end{pmatrix}
\xrightarrow{\substack{R_2 \leftarrow R_2 - R_3 \\ R_1 \leftarrow R_1 - 3R_3}}
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}
\xrightarrow{R_1 \leftarrow R_1 - 2R_2}
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}= I_3.
$$

4. **Identify operations that preserve the determinant and evaluate $\det A$:** Every single operation performed above is a row replacement ($R_i \leftarrow R_i + cR_j$ with $i \neq j$), which leaves the determinant completely unchanged ($\det A = \det A_1 = \det U = \det I_3$). Taking the product of the main diagonal entries of the upper triangular matrix $U$ (or $I_3$) gives

$$
\det A = \det U = 1 \cdot 1 \cdot 1 = 1.
$$

<br>

**Property / method used.** *Row replacement invariance and triangular determinant rule:*
- Adding a scalar multiple of one row to a different row ($R_i \leftarrow R_i + cR_j$, $i \neq j$) does not alter the determinant. (By contrast, swapping two rows multiplies $\det$ by $-1$, and scaling a row by $k$ multiplies $\det$ by $k$.)
- The determinant of a triangular matrix equals the product of its main diagonal entries.

<br>

**Mathematical verification.** Computing $\det A$ directly using Sarrus' rule confirms the result:

$$
\det A = (1\cdot 3\cdot 6 + 2\cdot 4\cdot 1 + 3\cdot 1\cdot 4) - (1\cdot 3\cdot 3 + 4\cdot 4\cdot 1 + 6\cdot 1\cdot 2) = (18 + 8 + 12) - (9 + 16 + 12) = 38 - 37 = 1.
$$
