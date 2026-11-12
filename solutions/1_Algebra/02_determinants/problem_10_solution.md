### Exercise 10. Detecting Dependence

#### Exercise Reminder

Without carrying out a full determinant calculation, explain why

$$\det \begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 0 & 1 & 5 \\ \end{pmatrix}= 0.$$

Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.

---

#### Solution

**Result.** The determinant is $0$ because the second row is an exact scalar multiple of the first row ($R_2 = 2R_1$), making the rows linearly dependent and the matrix singular (not invertible).

<br>

**Main steps.** Let

$$A= \begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 0 & 1 & 5 \\ \end{pmatrix},$$

and denote its rows by $R_1$, $R_2$, and $R_3$.

1. **Identify the specific row dependence:** Compare the entries of row $1$ and row $2$:

$$R_1 = \begin{pmatrix} 1 & 2 & 3 \end{pmatrix},\qquad R_2 = \begin{pmatrix} 2 & 4 & 6 \end{pmatrix}= 2 \begin{pmatrix} 1 & 2 & 3 \end{pmatrix}= 2R_1.$$

Equivalently, $2R_1 - R_2 = \begin{pmatrix} 0 & 0 & 0 \end{pmatrix}$, which is a nontrivial linear dependence relation among the rows of $A$.

2. **Why $\det A = 0$ without full expansion:** Performing the single row replacement $R_2 \leftarrow R_2 - 2R_1$ does not change the determinant and produces a zero row:

$$\det A = \det \begin{pmatrix} 1 & 2 & 3 \\ 0 & 0 & 0 \\ 0 & 1 & 5 \\ \end{pmatrix}= 0,$$

because any square matrix with proportional rows (or a row of zeros) has determinant $0$.

3. **Connection with noninvertibility:** By the Invertible Matrix Theorem, a square matrix $A$ is invertible if and only if $\det A \neq 0$ (equivalently, its rows are linearly independent). Because $R_2 = 2R_1$, the rows of $A$ are linearly dependent ($\mathrm{rank}(A) = 2 < 3$), $\det A = 0$, and $A$ has no inverse $A^{-1}$.

<br>

**Property / method used.** *Proportional-rows determinant property and the Invertible Matrix Theorem:* if one row of a square matrix is a scalar multiple of another row, then $\det A = 0$, and for any $n\times n$ matrix $A$,

$$\text{rows of } A \text{ are linearly dependent} \iff \det A = 0 \iff A \text{ is not invertible.}$$

<br>

**Mathematical verification.** Evaluating $\det A$ directly via Sarrus' rule confirms that all terms cancel to zero:

$$\det A = (1\cdot 4\cdot 5 + 2\cdot 6\cdot 0 + 3\cdot 2\cdot 1) - (0\cdot 4\cdot 3 + 1\cdot 6\cdot 1 + 5\cdot 2\cdot 2) = (20 + 0 + 6) - (0 + 6 + 20) = 26 - 26 = 0.$$
