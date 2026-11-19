### Exercise 7. Inverse of a Product

#### Exercise Reminder

For

$$
A =
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix},\qquad B =
\begin{pmatrix}
2 & 0 \\
0 & 3
\end{pmatrix},
$$

compute $(AB)^{-1}$ and $B^{-1}A^{-1}$. Check that the results are the same and explain the meaning of the reversed order.

---

#### Solution

**Result.** Both expressions yield the exact same matrix:

$$
(AB)^{-1} = B^{-1}A^{-1} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3}
\end{pmatrix}.
$$

<br>

**Main steps.**

1. **Compute $(AB)^{-1}$ directly:** First multiply $A$ and $B$:

$$
AB =
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 3
\end{pmatrix} =
\begin{pmatrix}
1\cdot 2 + 1\cdot 0 & 1\cdot 0 + 1\cdot 3 \\
0\cdot 2 + 1\cdot 0 & 0\cdot 0 + 1\cdot 3
\end{pmatrix} =
\begin{pmatrix}
2 & 3 \\
0 & 3
\end{pmatrix}.
$$

Since $\det(AB) = (2)(3) - (3)(0) = 6 \neq 0$, applying the $2\times 2$ inverse formula gives

$$
(AB)^{-1} = \frac{1}{6}
\begin{pmatrix}
3 & -3 \\
0 & 2
\end{pmatrix} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3}
\end{pmatrix}.
$$

2. **Compute $B^{-1}A^{-1}$:** Find the individual inverses of $A$ ($\det A = 1$) and $B$ ($\det B = 6$):

$$
A^{-1} =
\begin{pmatrix}
1 & -1 \\
0 & 1
\end{pmatrix},\qquad B^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & \frac{1}{3}
\end{pmatrix}.
$$

Multiply $B^{-1}$ and $A^{-1}$ in reversed order:

$$
B^{-1}A^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & \frac{1}{3}
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
0 & 1
\end{pmatrix} =
\begin{pmatrix}
\frac{1}{2}\cdot 1 + 0\cdot 0 & \frac{1}{2}\cdot (-1) + 0\cdot 1 \\
0\cdot 1 + \frac{1}{3}\cdot 0 & 0\cdot (-1) + \frac{1}{3}\cdot 1
\end{pmatrix} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3}
\end{pmatrix}.
$$

3. **Comparison and meaning of the reversed order:** Both computations produce the exact same matrix. In the product $(AB)x = A(Bx)$, the transformation $B$ acts on a vector $x$ first and $A$ acts second. To undo the combined operation, one must reverse the steps in last-in, first-out order: first undo $A$ by applying $A^{-1}$, and then undo $B$ by applying $B^{-1}$, which is written as $B^{-1}A^{-1}$.

<br>

**Property / method used.** *Inverse of a matrix product (socks-and-shoes rule):* for any two invertible $n\times n$ matrices $A$ and $B$, the product $AB$ is invertible and its inverse is the product of their inverses in reversed order:

$$
(AB)^{-1} = B^{-1}A^{-1}.
$$

<br>

**Mathematical verification.** Multiplying $AB$ by $B^{-1}A^{-1}$ confirms via associativity that all factors cancel to the identity matrix $I$:

$$
(AB)(B^{-1}A^{-1}) = A(BB^{-1})A^{-1} = AIA^{-1} = AA^{-1} = I.
$$
