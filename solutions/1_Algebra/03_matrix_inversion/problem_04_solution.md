### Exercise 4. Gauss–Jordan

#### Exercise Reminder

Find $A^{-1}$ using the Gauss–Jordan method for

$$
A =
\begin{pmatrix}
1 & 2 \\
3 & 5
\end{pmatrix}.
$$

Show the augmented matrix $[A \mid I]$ after successive operations and explain why obtaining $I$ on the left gives the inverse on the right.

---

#### Solution

**Result.**

$$
A^{-1} =
\begin{pmatrix}
-5 & 2 \\
3 & -1
\end{pmatrix}.
$$

<br>

**Main steps.** Form the $2\times 4$ augmented matrix $[A \mid I]$ by adjoining the $2\times 2$ identity matrix $I$ to the right of $A$, and apply elementary row operations to reduce the left block to $I$:

$$
[A \mid I] =
\left(
\begin{array}{cc|cc}
1 & 2 & 1 & 0 \\
3 & 5 & 0 & 1
\end{array}
\right).
$$

1. **Step 1 — Eliminate the $(2,1)$ entry via $R_2 \leftarrow R_2 - 3R_1$:**

$$
\left(
\begin{array}{cc|cc}
1 & 2 & 1 & 0 \\
3 & 5 & 0 & 1
\end{array}
\right)
\xrightarrow{R_2 \leftarrow R_2 - 3R_1}
\left(
\begin{array}{cc|cc}
1 & 2 & 1 & 0 \\
0 & -1 & -3 & 1
\end{array}
\right).
$$

2. **Step 2 — Scale row $2$ to create a leading $1$ in position $(2,2)$ via $R_2 \leftarrow -R_2$:**

$$
\left(
\begin{array}{cc|cc}
1 & 2 & 1 & 0 \\
0 & -1 & -3 & 1
\end{array}
\right)
\xrightarrow{R_2 \leftarrow -R_2}
\left(
\begin{array}{cc|cc}
1 & 2 & 1 & 0 \\
0 & 1 & 3 & -1
\end{array}
\right).
$$

3. **Step 3 — Eliminate the $(1,2)$ entry above the pivot via $R_1 \leftarrow R_1 - 2R_2$:**

$$
\left(
\begin{array}{cc|cc}
1 & 2 & 1 & 0 \\
0 & 1 & 3 & -1
\end{array}
\right)
\xrightarrow{R_1 \leftarrow R_1 - 2R_2}
\left(
\begin{array}{cc|cc}
1 & 0 & -5 & 2 \\
0 & 1 & 3 & -1
\end{array}
\right) = [I \mid A^{-1}].
$$

Reading off the $2\times 2$ block on the right yields

$$
A^{-1} =
\begin{pmatrix}
-5 & 2 \\
3 & -1
\end{pmatrix}.
$$

4. **Why obtaining $I$ on the left gives $A^{-1}$ on the right:** Each elementary row operation corresponds to multiplying the augmented matrix on the left by an elementary matrix $E_k$. If the sequence of row operations $E_1, E_2, \dots, E_m$ transforms $A$ into $I$, let $E = E_m \cdots E_2 E_1$ denote their product. Applying the same operations simultaneously to $[A \mid I]$ computes

$$
E[A \mid I] = [EA \mid EI] = [EA \mid E].
$$

Because the left block becomes $EA = I$, the matrix $E$ satisfies $EA = I$ (and hence $E = A^{-1}$ for square matrices), so the right block $EI = E$ is automatically $A^{-1}$.

<br>

**Property / method used.** *Gauss–Jordan elimination for matrix inversion:* row-reducing $[A \mid I]$ to reduced row echelon form $[I \mid B]$ applies the net invertible row-transformation matrix $E = A^{-1}$ to both blocks simultaneously, yielding $B = A^{-1}I = A^{-1}$.

<br>

**Mathematical verification.** Multiplying $A$ by the computed inverse confirms $A A^{-1} = I$:

$$
A A^{-1} =
\begin{pmatrix}
1 & 2 \\
3 & 5
\end{pmatrix}
\begin{pmatrix}
-5 & 2 \\
3 & -1
\end{pmatrix} =
\begin{pmatrix}
1\cdot (-5) + 2\cdot 3 & 1\cdot 2 + 2\cdot (-1) \\
3\cdot (-5) + 5\cdot 3 & 3\cdot 2 + 5\cdot (-1)
\end{pmatrix} =
\begin{pmatrix}
-5 + 6 & 2 - 2 \\
-15 + 15 & 6 - 5
\end{pmatrix} =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} = I,
$$

which also matches the $2\times 2$ inverse formula since $\det A = 1\cdot 5 - 2\cdot 3 = -1$.
