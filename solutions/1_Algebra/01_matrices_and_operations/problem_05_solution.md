### Exercise 5. Matrix Times Vector

#### Exercise Reminder

Let

$$
A=
\begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix},\qquad x=
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix}.
$$

1. Compute $Ax$.
2. Express $Ax$ as a linear combination of the columns of $A$, with coefficients coming from the vector $x$.

---

#### Solution

##### 1. Computing $Ax$

**Result.**

$$
Ax=
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}.
$$

**Main steps.** Matrix $A$ has size $2\times 2$ and column vector $x$ has size $2\times 1$. Since the number of columns of $A$ ($2$) equals the number of rows of $x$ ($2$), the product $Ax$ is defined and has size $2\times 1$.

Take the dot product of each row of $A$ with the vector $x$:

$$
Ax=
\begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix}=
\begin{pmatrix}
2\cdot 4 + (-1)\cdot 2 \\
1\cdot 4 + 3\cdot 2 \\
\end{pmatrix}=
\begin{pmatrix}
8 - 2 \\
4 + 6 \\
\end{pmatrix}=
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}.
$$

**Property / method used.** *Row-by-column matrix-vector multiplication:* for an $m\times n$ matrix $A$ and an $n\times 1$ vector $x$, the $i$-th component of $Ax$ is the dot product of row $i$ of $A$ with $x$.

**Mathematical verification.** Using the standard basis vectors $e_1 = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$ and $e_2 = \begin{pmatrix} 0 \\ 1 \end{pmatrix}$, we can decompose $x = 4e_1 + 2e_2$. By linearity of matrix multiplication,

$$
Ax = A(4e_1 + 2e_2) = 4Ae_1 + 2Ae_2 = 4
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix} + 2
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}=
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix},
$$

which confirms the result.

##### 2. Expressing $Ax$ as a Linear Combination of the Columns of $A$

**Result.**

$$
Ax = 4
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix} + 2
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix} =
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}.
$$

**Main steps.** Partition $A$ into its two column vectors $a_1$ and $a_2$, and read the scalar weights $x_1$ and $x_2$ from $x$:

$$
a_1=
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix},\qquad a_2=
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix},\qquad x_1 = 4,\qquad x_2 = 2.
$$

Multiply each column vector of $A$ by its corresponding entry from $x$ and add the resulting vectors:

$$
Ax = x_1 a_1 + x_2 a_2 = 4
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix} + 2
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix} =
\begin{pmatrix}
8 \\
4 \\
\end{pmatrix} +
\begin{pmatrix}
-2 \\
6 \\
\end{pmatrix} =
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}.
$$

**Property / method used.** *Column-picture of matrix-vector multiplication:* if $A = \begin{pmatrix} a_1 & a_2 & \cdots & a_n \end{pmatrix}$ and $x = \begin{pmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{pmatrix}$, then the product $Ax$ is the linear combination of the columns of $A$ weighted by the entries of $x$:

$$
Ax = x_1 a_1 + x_2 a_2 + \cdots + x_n a_n.
$$

**Mathematical verification.** Comparing the vector obtained from the column-wise linear combination in Part 2 with the vector computed via row-by-column dot products in Part 1 shows that both methods produce the exact same column vector $\begin{pmatrix} 6 \\ 10 \end{pmatrix}$.
