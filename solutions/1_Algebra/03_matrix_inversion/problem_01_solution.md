### Exercise 1. Definition of the Inverse

#### Exercise Reminder

For

$$
A =
\begin{pmatrix}
2 & 1 \\
1 & 1
\end{pmatrix},\qquad B =
\begin{pmatrix}
1 & -1 \\
-1 & 2
\end{pmatrix},
$$

check, without using a formula, whether $B = A^{-1}$. Compute $AB$ and $BA$ and relate the result to the definition of the inverse.

---

#### Solution

**Result.** Yes, $B = A^{-1}$ because both matrix products equal the $2\times 2$ identity matrix:

$$
AB = BA = I =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}.
$$

<br>

**Main steps.** Compute the products $AB$ and $BA$ directly using row-by-column multiplication without invoking any $2\times 2$ inverse formula:

1. **Compute $AB$:**

$$
AB =
\begin{pmatrix}
2 & 1 \\
1 & 1
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
-1 & 2
\end{pmatrix} =
\begin{pmatrix}
2\cdot 1 + 1\cdot (-1) & 2\cdot (-1) + 1\cdot 2 \\
1\cdot 1 + 1\cdot (-1) & 1\cdot (-1) + 1\cdot 2
\end{pmatrix} =
\begin{pmatrix}
2 - 1 & -2 + 2 \\
1 - 1 & -1 + 2
\end{pmatrix} =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} = I.
$$

2. **Compute $BA$:**

$$
BA =
\begin{pmatrix}
1 & -1 \\
-1 & 2
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
1 & 1
\end{pmatrix} =
\begin{pmatrix}
1\cdot 2 + (-1)\cdot 1 & 1\cdot 1 + (-1)\cdot 1 \\
(-1)\cdot 2 + 2\cdot 1 & (-1)\cdot 1 + 2\cdot 1
\end{pmatrix} =
\begin{pmatrix}
2 - 1 & 1 - 1 \\
-2 + 2 & -1 + 2
\end{pmatrix} =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} = I.
$$

3. **Relate to the definition of the inverse:** By definition, an $n\times n$ matrix $A$ is invertible with inverse $B$ if and only if $AB = I$ and $BA = I$. Because both $AB = I$ and $BA = I$ hold, $B$ satisfies the definition of the inverse of $A$, so $B = A^{-1}$.

<br>

**Property / method used.** *Definition of the matrix inverse:* for an $n\times n$ square matrix $A$, if there exists an $n\times n$ matrix $B$ such that $AB = BA = I$, then $A$ is invertible and $A^{-1} = B$ (and the inverse is unique).

<br>

**Mathematical verification.** Checking the action of $AB$ on an arbitrary column vector

$$
x =
\begin{pmatrix}
x_1 \\
x_2
\end{pmatrix}
$$

confirms that applying $B$ followed by $A$ returns the exact input vector:

$$
A(Bx) =
\begin{pmatrix}
2 & 1 \\
1 & 1
\end{pmatrix}
\begin{pmatrix}
x_1 - x_2 \\
-x_1 + 2x_2
\end{pmatrix} =
\begin{pmatrix}
2(x_1 - x_2) + (-x_1 + 2x_2) \\
(x_1 - x_2) + (-x_1 + 2x_2)
\end{pmatrix} =
\begin{pmatrix}
x_1 \\
x_2
\end{pmatrix} = x.
$$
