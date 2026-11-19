### Exercise 3. When Does the Inverse Not Exist?

#### Exercise Reminder

For

$$
A =
\begin{pmatrix}
2 & 4 \\
1 & 2
\end{pmatrix}
$$

explain in two ways why $A^{-1}$ does not exist: using the determinant and using dependence between the rows.

---

#### Solution

**Result.** The inverse matrix $A^{-1}$ does not exist (so $A$ is singular) because:
1. Its determinant is zero ($\det A = 0$).
2. Its rows are linearly dependent ($R_1 = 2R_2$).

<br>

**Main steps.** Denote the two rows of $A$ by $R_1 = (2 \quad 4)$ and $R_2 = (1 \quad 2)$.

1. **Method 1 — Using the determinant:** Compute $\det A$ using the $2\times 2$ determinant formula $\det M = ad - bc$:

$$
\det A = \det
\begin{pmatrix}
2 & 4 \\
1 & 2
\end{pmatrix} = (2)(2) - (4)(1) = 4 - 4 = 0.
$$

Because an $n\times n$ matrix is invertible if and only if its determinant is nonzero, $\det A = 0$ immediately implies that $A^{-1}$ does not exist (moreover, dividing by $\det A$ in the $2\times 2$ inverse formula would require division by zero).

2. **Method 2 — Using linear dependence between the rows:** Compare the entries of the first and second rows of $A$:

$$
R_1 = (2 \quad 4) = 2(1 \quad 2) = 2R_2,
$$

or equivalently $R_1 - 2R_2 = (0 \quad 0)$. Since one row is an exact scalar multiple of the other, the rows of $A$ are linearly dependent. Applying the elementary row replacement $R_1 \leftarrow R_1 - 2R_2$ reduces $A$ to a matrix with a zero row:

$$
A =
\begin{pmatrix}
2 & 4 \\
1 & 2
\end{pmatrix}
\xrightarrow{R_1 \leftarrow R_1 - 2R_2}
\begin{pmatrix}
0 & 0 \\
1 & 2
\end{pmatrix}.
$$

Because a square matrix with linearly dependent rows cannot be row-reduced to the $2\times 2$ identity matrix $I$, the matrix $A$ is not invertible.

<br>

**Property / method used.** *Invertible Matrix Theorem:* for any $n\times n$ square matrix $A$, the following statements are equivalent:
- $A$ is invertible ($A^{-1}$ exists).
- $\det A \neq 0$.
- The rows of $A$ are linearly independent (equivalently, $\mathrm{rank}(A) = n$).

<br>

**Mathematical verification.** Suppose for contradiction that an inverse matrix

$$
B =
\begin{pmatrix}
x & y \\
z & w
\end{pmatrix}
$$

existed such that $AB = I$. Computing the first column of the product $AB$ gives

$$
AB =
\begin{pmatrix}
2 & 4 \\
1 & 2
\end{pmatrix}
\begin{pmatrix}
x & y \\
z & w
\end{pmatrix} =
\begin{pmatrix}
2x + 4z & 2y + 4w \\
x + 2z & y + 2w
\end{pmatrix} =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}.
$$

Equating the $(1,1)$ and $(2,1)$ entries requires $2x + 4z = 1$ and $x + 2z = 0$. Multiplying the second equation by $2$ yields $2x + 4z = 0$, which contradicts $2x + 4z = 1$. Thus no such inverse matrix $B$ can exist.
