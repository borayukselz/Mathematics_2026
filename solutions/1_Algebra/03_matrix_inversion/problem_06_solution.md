### Exercise 6. Solving a System Using the Inverse

#### Exercise Reminder

Solve

$$
Ax = b,
$$

where

$$
A =
\begin{pmatrix}
2 & 1 \\
1 & 3
\end{pmatrix},\qquad b =
\begin{pmatrix}
5 \\
7
\end{pmatrix},
$$

using $x = A^{-1}b$. Then substitute the resulting vector back into the equation and check the result.

---

#### Solution

**Result.**

$$
x =
\begin{pmatrix}
\frac{8}{5} \\
\frac{9}{5}
\end{pmatrix}.
$$

<br>

**Main steps.**

1. **Compute the inverse matrix $A^{-1}$:** First find the determinant of $A$:

$$
\det A = (2)(3) - (1)(1) = 6 - 1 = 5.
$$

Since $\det A = 5 \neq 0$, $A$ is invertible, and the $2\times 2$ inverse formula gives

$$
A^{-1} = \frac{1}{5}
\begin{pmatrix}
3 & -1 \\
-1 & 2
\end{pmatrix} =
\begin{pmatrix}
\frac{3}{5} & -\frac{1}{5} \\
-\frac{1}{5} & \frac{2}{5}
\end{pmatrix}.
$$

2. **Solve for $x$ using $x = A^{-1}b$:** Multiply $A^{-1}$ on the right by the column vector $b$:

$$
x = A^{-1}b = \frac{1}{5}
\begin{pmatrix}
3 & -1 \\
-1 & 2
\end{pmatrix}
\begin{pmatrix}
5 \\
7
\end{pmatrix} = \frac{1}{5}
\begin{pmatrix}
3\cdot 5 + (-1)\cdot 7 \\
(-1)\cdot 5 + 2\cdot 7
\end{pmatrix} = \frac{1}{5}
\begin{pmatrix}
15 - 7 \\
-5 + 14
\end{pmatrix} = \frac{1}{5}
\begin{pmatrix}
8 \\
9
\end{pmatrix} =
\begin{pmatrix}
\frac{8}{5} \\
\frac{9}{5}
\end{pmatrix}.
$$

<br>

**Property / method used.** *Unique solution of a square linear system via the inverse matrix:* if $A$ is an invertible $n\times n$ matrix, then multiplying both sides of $Ax = b$ on the left by $A^{-1}$ yields the unique solution $x = A^{-1}b$.

<br>

**Mathematical verification.** Substitute the computed vector $x$ back into the left-hand side $Ax$ and verify that it equals $b$:

$$
Ax =
\begin{pmatrix}
2 & 1 \\
1 & 3
\end{pmatrix}
\begin{pmatrix}
\frac{8}{5} \\
\frac{9}{5}
\end{pmatrix} =
\begin{pmatrix}
2\cdot \frac{8}{5} + 1\cdot \frac{9}{5} \\
1\cdot \frac{8}{5} + 3\cdot \frac{9}{5}
\end{pmatrix} =
\begin{pmatrix}
\frac{16 + 9}{5} \\
\frac{8 + 27}{5}
\end{pmatrix} =
\begin{pmatrix}
\frac{25}{5} \\
\frac{35}{5}
\end{pmatrix} =
\begin{pmatrix}
5 \\
7
\end{pmatrix} = b.
$$
