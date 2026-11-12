### Exercise 4. Triangular Matrix

#### Exercise Reminder

Without expanding the determinant, compute

$$
\det
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}.
$$

State the rule for an arbitrary triangular matrix and explain it using this example.

---

#### Solution

##### 1. Computing the Determinant Without Expansion

**Result.**

$$
\det
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}= -42.
$$

<br>

**Main steps.** Let

$$
A=
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}.
$$

Notice that every entry below the main diagonal is zero ($a_{21} = 0$, $a_{31} = 0$, and $a_{32} = 0$), so $A$ is an upper triangular matrix. Identify its three main diagonal entries:

$$
a_{11} = 2,\qquad a_{22} = -3,\qquad a_{33} = 7.
$$

Multiply the diagonal entries directly without performing cofactor expansion or Sarrus' rule:

$$
\det A = a_{11} \cdot a_{22} \cdot a_{33} = 2 \cdot (-3) \cdot 7 = -42.
$$

<br>

**Property / method used.** *Triangular matrix determinant rule:* the determinant of any $n\times n$ triangular matrix (upper triangular, lower triangular, or diagonal) equals the product of its main diagonal entries:

$$
\det T = \prod_{i=1}^{n} t_{ii} = t_{11} t_{22} \cdots t_{nn}.
$$

<br>

**Mathematical verification.** Performing cofactor expansion along the first column (where $a_{21} = a_{31} = 0$) confirms why only the diagonal product survives:

$$
\det A = 2 \cdot \det
\begin{pmatrix}
-3 & 5 \\
0 & 7 \\
\end{pmatrix}- 0 + 0 = 2\bigl((-3)\cdot 7 - 5\cdot 0\bigr) = 2 \cdot (-3) \cdot 7 = -42.
$$

---

##### 2. General Rule and Explanation Using This Example

**Result.** For any arbitrary $n\times n$ triangular matrix $T$, its determinant is the product of all entries along its main diagonal ($\det T = t_{11}t_{22}\cdots t_{nn}$), regardless of the values of the nonzero entries on the opposite side of the diagonal.

<br>

**Main steps.**
1. **Why off-diagonal entries do not affect $\det T$:** In an upper triangular matrix, all entries below the main diagonal are zero ($t_{ij} = 0$ for $i > j$), while the entries above the main diagonal ($t_{ij}$ for $i < j$) can be arbitrary numbers. In this example, the upper-right entries $4$, $1$, and $5$ contribute nothing to $\det A$.
2. **Recursive reduction:** Expanding along column $1$ isolates $t_{11} = 2$ multiplied by the $(n-1)\times(n-1)$ upper triangular submatrix $\begin{pmatrix} -3 & 5 \\ 0 & 7 \end{pmatrix}$, and repeating this step peels off $t_{22} = -3$ and $t_{33} = 7$, leaving solely $2 \cdot (-3) \cdot 7 = -42$.
3. **Symmetry for lower triangular matrices:** Because $\det(L^T) = \det L$ and the transpose of a lower triangular matrix is upper triangular with the exact same diagonal entries, the identical product rule applies to lower triangular matrices as well.

<br>

**Property / method used.** *Inductive cofactor reduction and transpose invariance ($\det(M^T) = \det M$):* zeros below (or above) the main diagonal eliminate every off-diagonal term in the Leibniz permutation expansion except the identity permutation $t_{11}t_{22}\cdots t_{nn}$.

<br>

**Mathematical verification.** Replacing the superdiagonal entries $4, 1, 5$ with zeros forms the diagonal matrix $D = \mathrm{diag}(2, -3, 7)$, which has the exact same determinant:

$$
\det
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 7 \\
\end{pmatrix}= 2 \cdot (-3) \cdot 7 = -42 = \det A,
$$

confirming that the entries above the diagonal have no effect on the determinant.
