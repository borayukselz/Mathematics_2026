### Exercise 13. Determinant by Elimination

#### Exercise Reminder

Compute the determinant

$$A= \begin{pmatrix} 1 & 2 & 3 \\ 2 & 5 & 7 \\ 1 & 0 & 2 \\ \end{pmatrix}$$

using elimination. Record the effect of every row operation used on the value of the determinant.

---

#### Solution

**Result.**

$$\det A = 1.$$

<br>

**Main steps.** Reduce $A$ to an upper triangular matrix $U$ via Gaussian elimination while recording the effect of each row operation on the determinant:

1. **Step 1 — Eliminate the $(2,1)$ entry via $R_2 \leftarrow R_2 - 2R_1$:**

$$A= \begin{pmatrix} 1 & 2 & 3 \\ 2 & 5 & 7 \\ 1 & 0 & 2 \\ \end{pmatrix} \xrightarrow{R_2 \leftarrow R_2 - 2R_1} \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 1 & 0 & 2 \\ \end{pmatrix}= A_1.$$

- **Effect on determinant:** **No change** ($\det A_1 = \det A$), because adding a scalar multiple of one row to another row leaves the determinant unchanged.

2. **Step 2 — Eliminate the $(3,1)$ entry via $R_3 \leftarrow R_3 - R_1$:**

$$A_1= \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 1 & 0 & 2 \\ \end{pmatrix} \xrightarrow{R_3 \leftarrow R_3 - R_1} \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & -2 & -1 \\ \end{pmatrix}= A_2.$$

- **Effect on determinant:** **No change** ($\det A_2 = \det A_1 = \det A$), because subtracting $R_1$ from $R_3$ is a row replacement operation.

3. **Step 3 — Eliminate the $(3,2)$ entry via $R_3 \leftarrow R_3 + 2R_2$:**

$$A_2= \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & -2 & -1 \\ \end{pmatrix} \xrightarrow{R_3 \leftarrow R_3 + 2R_2} \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 0 & 1 \\ \end{pmatrix}= U.$$

- **Effect on determinant:** **No change** ($\det U = \det A_2 = \det A$), because adding $2R_2$ to $R_3$ is a row replacement operation.

4. **Step 4 — Evaluate $\det U$ from the upper triangular form:** Since none of the three elimination steps changed the determinant, $\det A = \det U$, which equals the product of the main diagonal entries of $U$:

$$\det A = \det U = 1 \cdot 1 \cdot 1 = 1.$$

<br>

**Property / method used.** *Elimination method for determinants:*
- **Row replacement** ($R_i \leftarrow R_i + cR_j$ for $i \neq j$) preserves the value of the determinant ($\det_{\text{new}} = \det_{\text{old}}$).
- **Upper triangular determinant rule:** once a matrix is reduced to upper triangular form $U$, its determinant equals the product of its diagonal entries $u_{11}u_{22}u_{33}$.

<br>

**Mathematical verification.** Computing $\det A$ directly by Sarrus' rule confirms the elimination result:

$$\det A = (1\cdot 5\cdot 2 + 2\cdot 7\cdot 1 + 3\cdot 2\cdot 0) - (1\cdot 5\cdot 3 + 0\cdot 7\cdot 1 + 2\cdot 2\cdot 2) = (10 + 14 + 0) - (15 + 0 + 8) = 24 - 23 = 1.$$
