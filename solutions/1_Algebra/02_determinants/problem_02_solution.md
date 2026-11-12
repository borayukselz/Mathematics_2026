### Exercise 2. Determinant of a $3\times 3$ Matrix

#### Exercise Reminder

For

$$A= \begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 4 \\ 2 & 1 & 5 \\ \end{pmatrix},$$

1. Compute $\det A$ using Sarrus' rule.
2. Perform one simple check using a chosen property of the determinant.

---

#### Solution

##### 1. Computing $\det A$ Using Sarrus' Rule

**Result.**

$$\det A = 33.$$

<br>

**Main steps.** Write the matrix $A$ and repeat its first two columns to the right:

$$\begin{array}{ccc\|cc} 1 & 2 & -1 & 1 & 2 \\ 0 & 3 & 4 & 0 & 3 \\ 2 & 1 & 5 & 2 & 1 \end{array}$$

1. **Sum of the three downward-right diagonal products:**

$$D_{\text{down}} = (1\cdot 3\cdot 5) + (2\cdot 4\cdot 2) + \bigl((-1)\cdot 0\cdot 1\bigr) = 15 + 16 + 0 = 31.$$

2. **Sum of the three upward-right diagonal products:**

$$D_{\text{up}} = (2\cdot 3\cdot (-1)) + (1\cdot 4\cdot 1) + (5\cdot 0\cdot 2) = -6 + 4 + 0 = -2.$$

3. **Subtract the upward sum from the downward sum:**

$$\det A = D_{\text{down}} - D_{\text{up}} = 31 - (-2) = 31 + 2 = 33.$$

<br>

**Property / method used.** *Sarrus' rule for $3\times 3$ determinants:* expanding the $3\times 3$ matrix by repeating columns $1$ and $2$ on the right allows computing $\det A$ as the sum of the three main (top-left to bottom-right) diagonal products minus the sum of the three anti-diagonal (bottom-left to top-right) products.

<br>

**Mathematical verification.** Expanding $\det A$ by cofactors along the first column (which contains a zero entry in row $2$) gives an independent check:

$$\det A = 1\cdot \det \begin{pmatrix} 3 & 4 \\ 1 & 5 \\ \end{pmatrix}- 0\cdot \det \begin{pmatrix} 2 & -1 \\ 1 & 5 \\ \end{pmatrix}+ 2\cdot \det \begin{pmatrix} 2 & -1 \\ 3 & 4 \\ \end{pmatrix}= 1(15 - 4) + 2\bigl(8 - (-3)\bigr) = 11 + 22 = 33.$$

---

##### 2. Simple Check Using a Determinant Property

**Result.** Reducing $A$ to an upper triangular matrix $U$ via row replacements gives

$$\det A = \det U = 1 \cdot 3 \cdot 11 = 33,$$

which confirms $\det A = 33$.

<br>

**Main steps.** Apply two elementary row replacement operations to eliminate the entries below the main diagonal without changing the determinant:

1. **Eliminate the $(3,1)$ entry** via $R_3 \leftarrow R_3 - 2R_1$:

$$A= \begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 4 \\ 2 & 1 & 5 \\ \end{pmatrix} \xrightarrow{R_3 \leftarrow R_3 - 2R_1} \begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 4 \\ 0 & -3 & 7 \\ \end{pmatrix}.$$

2. **Eliminate the $(3,2)$ entry** via $R_3 \leftarrow R_3 + R_2$:

$$\begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 4 \\ 0 & -3 & 7 \\ \end{pmatrix} \xrightarrow{R_3 \leftarrow R_3 + R_2} \begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 4 \\ 0 & 0 & 11 \\ \end{pmatrix}= U.$$

3. **Compute the determinant of the triangular matrix $U$:**

$$\det U = 1 \cdot 3 \cdot 11 = 33.$$

<br>

**Property / method used.** *Row replacement invariance and triangular determinant property:*
- Adding a scalar multiple of one row to another row ($R_i \leftarrow R_i + cR_j$ for $i \neq j$) leaves the determinant unchanged.
- The determinant of an upper triangular matrix equals the product of its main diagonal entries.

<br>

**Mathematical verification.** Since neither $R_3 \leftarrow R_3 - 2R_1$ nor $R_3 \leftarrow R_3 + R_2$ alters the determinant, we have $\det A = \det U = 33$, matching the value obtained from Sarrus' rule in Part 1.
