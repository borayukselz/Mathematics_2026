### Exercise 12. A Parameter Revealed by a Row Operation

#### Exercise Reminder

For

$$
A(t)=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & t \\
0 & 1 & 1 \\
\end{pmatrix},
$$

1. Perform the row operation $R_2 \leftarrow R_2 - 2R_1$ before computing the determinant and use the resulting structure to find the values of $t$ for which the matrix is not invertible.
2. Explain what special thing happens to the rows for the value of the parameter found.

---

#### Solution

##### 1. Performing $R_2 \leftarrow R_2 - 2R_1$ and Finding Where $A(t)$ Is Not Invertible

**Result.** After applying $R_2 \leftarrow R_2 - 2R_1$, the matrix becomes

$$
A_1(t)=
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & t - 6 \\
0 & 1 & 1 \\
\end{pmatrix},
$$

giving $\det A(t) = 6 - t$. Therefore, $A(t)$ is not invertible solely for

$$
t = 6.
$$

<br>

**Main steps.**

1. **Apply the row replacement $R_2 \leftarrow R_2 - 2R_1$:** Subtract $2$ times row $1$ from row $2$:

$$
A(t)=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & t \\
0 & 1 & 1 \\
\end{pmatrix}
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & t - 6 \\
0 & 1 & 1 \\
\end{pmatrix}= A_1(t).
$$

Because $R_2 \leftarrow R_2 - 2R_1$ is a row replacement operation, it leaves the determinant unchanged: $\det A(t) = \det A_1(t)$.

2. **Use the resulting structure to compute $\det A(t)$:** Swapping rows $2$ and $3$ ($R_2 \leftrightarrow R_3$) transforms $A_1(t)$ into an upper triangular matrix $U(t)$ while multiplying the determinant by $-1$:

$$
A_1(t)=
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & t - 6 \\
0 & 1 & 1 \\
\end{pmatrix}
\xrightarrow{R_2 \leftrightarrow R_3}
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & t - 6 \\
\end{pmatrix}= U(t).
$$

Multiplying the main diagonal entries of $U(t)$ and accounting for the sign flip from the single row swap yields

$$
\det A(t) = \det A_1(t) = -\det U(t) = -\bigl(1 \cdot 1 \cdot (t - 6)\bigr) = -(t - 6) = 6 - t.
$$

3. **Find the noninvertible parameter value:** A square matrix is not invertible if and only if its determinant equals zero:

$$
\det A(t) = 0 \implies 6 - t = 0 \implies t = 6.
$$

<br>

**Property / method used.** *Row operation invariance, alternating row-swap property, and singularity criterion:*
- Row replacement ($R_2 \leftarrow R_2 - 2R_1$) preserves the determinant.
- Interchanging two rows ($R_2 \leftrightarrow R_3$) reverses the sign of the determinant.
- A square matrix $A(t)$ fails to be invertible if and only if $\det A(t) = 0$.

<br>

**Mathematical verification.** Expanding $\det A(t)$ directly via Sarrus' rule confirms the determinant formula independently:

$$
\det A(t) = (1\cdot 4\cdot 1 + 2\cdot t\cdot 0 + 3\cdot 2\cdot 1) - (0\cdot 4\cdot 3 + 1\cdot t\cdot 1 + 1\cdot 2\cdot 2) = (4 + 0 + 6) - (0 + t + 4) = 10 - t - 4 = 6 - t.
$$

---

##### 2. What Happens to the Rows When $t = 6$

**Result.** When $t = 6$, the second row of $A(6)$ becomes an exact scalar multiple of the first row ($R_2 = 2R_1$), so the rows of $A(6)$ are linearly dependent and the row operation $R_2 \leftarrow R_2 - 2R_1$ produces an entire row of zeros.

<br>

**Main steps.** Substitute $t = 6$ into both the original matrix $A(t)$ and the reduced matrix $A_1(t)$:

$$
A(6)=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 1 \\
\end{pmatrix},\qquad A_1(6)=
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}.
$$

1. **Proportional rows in $A(6)$:** In $A(6)$, the first row is $(1, 2, 3)$ and the second row is $(2, 4, 6) = 2(1, 2, 3)$, meaning $R_2 = 2R_1$.
2. **Zero row after elimination:** Because $R_2$ is twice $R_1$, subtracting $2R_1$ from $R_2$ annihilates the entire second row in $A_1(6)$, leaving $(0, 0, 0)$ and reducing the rank of the matrix from $3$ to $2$.

<br>

**Property / method used.** *Linear dependence of rows and rank deficiency:* when two rows of a $3\times 3$ matrix are proportional, the rows span at most a $2$-dimensional subspace ($\mathrm{rank}(A) < 3$), forcing $\det A = 0$ and making $A$ noninvertible.

<br>

**Mathematical verification.** The nontrivial linear combination $2R_1 - R_2 + 0R_3 = (0, 0, 0)$ holds among the rows of $A(6)$, directly verifying that the rows are linearly dependent and that $A(6)x = 0$ has infinitely many nonzero solutions (for example, $x = (1, 1, -1)^T$).
