### Exercise 4. Matrix Multiplication and Noncommutativity

#### Exercise Reminder

Given the $2\times 2$ matrices

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix},
$$

1. Compute $AB$ and $BA$.
2. Determine whether $AB=BA$.
3. Use this example to explain what noncommutativity of matrix multiplication means.

---

#### Solution

##### 1. Computing $AB$ and $BA$

**Result.**

$$
AB=
\begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix},\qquad BA=
\begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}.
$$

**Main steps.** Both $A$ and $B$ have size $2\times 2$, so both $AB$ and $BA$ are defined and have size $2\times 2$.

To compute $AB$, take the dot product of each row of $A$ with each column of $B$:

$$
AB=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot 2 + 2\cdot 3 & 1\cdot 0 + 2\cdot 1 \\
0\cdot 2 + 1\cdot 3 & 0\cdot 0 + 1\cdot 1 \\
\end{pmatrix}=
\begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix}.
$$

To compute $BA$, take the dot product of each row of $B$ with each column of $A$:

$$
BA=
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
2\cdot 1 + 0\cdot 0 & 2\cdot 2 + 0\cdot 1 \\
3\cdot 1 + 1\cdot 0 & 3\cdot 2 + 1\cdot 1 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}.
$$

**Property / method used.** *Row-by-column matrix multiplication:* for compatible matrices $X$ ($m\times n$) and $Y$ ($n\times p$), the $(i,j)$ entry of the product is given by $(XY)_{ij}=\sum_{k=1}^{n} x_{ik}y_{kj}$.

**Mathematical verification.** For any two square matrices of the same size, their products must share the same trace and determinant even when the matrices themselves differ. Checking both invariants confirms the entries:
- **Trace check:** $\operatorname{tr}(AB) = 8 + 1 = 9$ and $\operatorname{tr}(BA) = 2 + 7 = 9$, so $\operatorname{tr}(AB) = \operatorname{tr}(BA)$.
- **Determinant check:** $\det(A) = 1\cdot 1 - 2\cdot 0 = 1$ and $\det(B) = 2\cdot 1 - 0\cdot 3 = 2$, giving $\det(A)\det(B) = 2$. Computing directly from the products yields $\det(AB) = 8\cdot 1 - 2\cdot 3 = 2$ and $\det(BA) = 2\cdot 7 - 4\cdot 3 = 2$.

##### 2. Equality Check and Meaning of Noncommutativity

**Result.** No, $AB \neq BA$. Noncommutativity of matrix multiplication means that the order in which two matrices are multiplied matters: swapping the left and right factors generally produces a different matrix (or may even make the product undefined).

**Main steps.** Two matrices are equal if and only if they have the same size and identical entries in every $(i,j)$ position. Comparing $AB$ and $BA$ entry by entry shows they disagree in three of the four positions:

$$
AB=
\begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix}
\neq
\begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}=BA.
$$

Specifically, $(AB)_{11}=8 \neq 2=(BA)_{11}$, $(AB)_{12}=2 \neq 4=(BA)_{12}$, and $(AB)_{22}=1 \neq 7=(BA)_{22}$.

**Property / method used.** *Noncommutativity of matrix algebra:* unlike real or complex numbers where $ab = ba$ always holds, matrix multiplication is not commutative ($AB \neq BA$ in general) because $AB$ pairs rows of $A$ with columns of $B$, whereas $BA$ pairs rows of $B$ with columns of $A$.

**Mathematical verification.** Because $AB - BA \neq 0$, the commutator of $A$ and $B$ is nonzero:

$$
[A,B] = AB - BA =
\begin{pmatrix}
8-2 & 2-4 \\
3-3 & 1-7 \\
\end{pmatrix}=
\begin{pmatrix}
6 & -2 \\
0 & -6 \\
\end{pmatrix}
\neq
\begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix},
$$

which directly confirms that $A$ and $B$ do not commute.
