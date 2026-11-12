### Exercise 6. Transpose

#### Exercise Reminder

Given the matrices

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix},
$$

1. Compute $A^T$, $B^T$, and $AB$.
2. Verify in this example that $(AB)^T = B^T A^T$.

---

#### Solution

##### 1. Computing $A^T$, $B^T$, and $AB$

**Result.**

$$
A^T=
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix},\qquad B^T=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix},\qquad AB=
\begin{pmatrix}
2 & 11 \\
8 & 23 \\
\end{pmatrix}.
$$

**Main steps.** Matrix $A$ has size $2\times 3$, so its transpose $A^T$ has size $3\times 2$ obtained by writing the rows of $A$ as columns:

$$
A^T=
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix}.
$$

Matrix $B$ has size $3\times 2$, so its transpose $B^T$ has size $2\times 3$ obtained by writing the rows of $B$ as columns:

$$
B^T=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}.
$$

Since $A$ has size $2\times 3$ and $B$ has size $3\times 2$, the inner dimensions match ($3=3$), so $AB$ is defined and has size $2\times 2$. Computing the dot products of the rows of $A$ with the columns of $B$ gives

$$
AB=
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot 1 + 2\cdot 2 + 3\cdot (-1) & 1\cdot 0 + 2\cdot 1 + 3\cdot 3 \\
4\cdot 1 + 5\cdot 2 + 6\cdot (-1) & 4\cdot 0 + 5\cdot 1 + 6\cdot 3 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 11 \\
8 & 23 \\
\end{pmatrix}.
$$

**Property / method used.** *Matrix transposition and row-by-column multiplication:* the transpose $M^T$ of an $m\times n$ matrix $M$ is the $n\times m$ matrix defined by interchanging rows and columns,

$$
(M^T)_{ij} = m_{ji},
$$

and matrix multiplication $AB$ computes entry $(i,j)$ as the dot product of row $i$ of $A$ with column $j$ of $B$.

**Mathematical verification.** Applying the transpose twice recovers the original matrices:

$$
(A^T)^T=
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix}=A,\qquad (B^T)^T=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}=B.
$$

Furthermore, computing $AB$ via linear combinations of the columns of $A$ weighted by the columns of $B$ confirms the product:

$$
Ab_1 = 1
\begin{pmatrix}
1 \\
4 \\
\end{pmatrix} + 2
\begin{pmatrix}
2 \\
5 \\
\end{pmatrix} - 1
\begin{pmatrix}
3 \\
6 \\
\end{pmatrix}=
\begin{pmatrix}
2 \\
8 \\
\end{pmatrix},\qquad Ab_2 = 0
\begin{pmatrix}
1 \\
4 \\
\end{pmatrix} + 1
\begin{pmatrix}
2 \\
5 \\
\end{pmatrix} + 3
\begin{pmatrix}
3 \\
6 \\
\end{pmatrix}=
\begin{pmatrix}
11 \\
23 \\
\end{pmatrix}.
$$

##### 2. Verifying $(AB)^T = B^T A^T$

**Result.** Both $(AB)^T$ and $B^T A^T$ evaluate to the same $2\times 2$ matrix, confirming that $(AB)^T = B^T A^T$:

$$
(AB)^T = B^T A^T =
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}.
$$

**Main steps.** First, take the transpose of the product $AB$ found in Part 1:

$$
(AB)^T=
\begin{pmatrix}
2 & 11 \\
8 & 23 \\
\end{pmatrix}^T=
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}.
$$

Second, multiply $B^T$ ($2\times 3$) by $A^T$ ($3\times 2$) in reversed order:

$$
B^T A^T=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot 1 + 2\cdot 2 + (-1)\cdot 3 & 1\cdot 4 + 2\cdot 5 + (-1)\cdot 6 \\
0\cdot 1 + 1\cdot 2 + 3\cdot 3 & 0\cdot 4 + 1\cdot 5 + 3\cdot 6 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}.
$$

Comparing both matrices entry by entry shows $(AB)^T = B^T A^T$.

**Property / method used.** *Transpose of a product (reversal law):* for any compatible matrices $A$ ($m\times n$) and $B$ ($n\times p$), transposing their product reverses the order of the factors:

$$
(AB)^T = B^T A^T.
$$

**Mathematical verification.** Checking the dimensions confirms why the order must reverse: since $AB$ has size $2\times 2$, $(AB)^T$ has size $2\times 2$. Multiplying in reversed order $B^T A^T$ pairs $(2\times 3)(3\times 2)$ to yield the compatible size $2\times 2$, whereas multiplying without reversing ($A^T B^T$) would pair $(3\times 2)(2\times 3)$ and produce a $3\times 3$ matrix of the wrong dimension.
