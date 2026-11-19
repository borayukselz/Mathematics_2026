### Exercise 9. Matrix Equation

#### Exercise Reminder

Given

$$
A =
\begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix},\qquad B =
\begin{pmatrix}
3 & 1 \\
2 & 4
\end{pmatrix},
$$

solve the equation $AX = B$ for $X$. Before calculating, decide on which side of the equation $A^{-1}$ must be used. Then check the result by computing $AX$.

---

#### Solution

**Result.** Multiply both sides on the **left** by $A^{-1}$, giving

$$
X = A^{-1}B =
\begin{pmatrix}
-1 & -7 \\
2 & 4
\end{pmatrix}.
$$

<br>

**Main steps.**

1. **Decide which side to multiply by $A^{-1}$:** In the equation $AX = B$, the unknown matrix $X$ is multiplied by $A$ on its *left*. Because matrix multiplication is generally noncommutative, multiplying on the right would produce $AXA^{-1}$, which does not simplify to $X$. Instead, we must multiply both sides on the **left** by $A^{-1}$:

$$
A^{-1}(AX) = A^{-1}B \implies (A^{-1}A)X = A^{-1}B \implies IX = A^{-1}B \implies X = A^{-1}B.
$$

2. **Compute $A^{-1}$:** First evaluate $\det A$:

$$
\det A = (1)(1) - (2)(0) = 1.
$$

Since $\det A = 1 \neq 0$, $A$ is invertible, and the $2\times 2$ inverse formula yields

$$
A^{-1} = \frac{1}{1}
\begin{pmatrix}
1 & -2 \\
0 & 1
\end{pmatrix} =
\begin{pmatrix}
1 & -2 \\
0 & 1
\end{pmatrix}.
$$

3. **Compute $X = A^{-1}B$:** Multiply $A^{-1}$ on the left by $B$ on the right:

$$
X = A^{-1}B =
\begin{pmatrix}
1 & -2 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
3 & 1 \\
2 & 4
\end{pmatrix} =
\begin{pmatrix}
1\cdot 3 + (-2)\cdot 2 & 1\cdot 1 + (-2)\cdot 4 \\
0\cdot 3 + 1\cdot 2 & 0\cdot 1 + 1\cdot 4
\end{pmatrix} =
\begin{pmatrix}
3 - 4 & 1 - 8 \\
0 + 2 & 0 + 4
\end{pmatrix} =
\begin{pmatrix}
-1 & -7 \\
2 & 4
\end{pmatrix}.
$$

<br>

**Property / method used.** *Left-cancellation in matrix equations and associativity:* for an invertible square matrix $A$, multiplying $AX = B$ on the left by $A^{-1}$ isolates $X = A^{-1}B$ via $(A^{-1}A)X = IX = X$.

<br>

**Mathematical verification.** Substitute the computed matrix $X$ back into the left-hand side $AX$ and confirm that it reproduces $B$:

$$
AX =
\begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
-1 & -7 \\
2 & 4
\end{pmatrix} =
\begin{pmatrix}
1\cdot (-1) + 2\cdot 2 & 1\cdot (-7) + 2\cdot 4 \\
0\cdot (-1) + 1\cdot 2 & 0\cdot (-7) + 1\cdot 4
\end{pmatrix} =
\begin{pmatrix}
-1 + 4 & -7 + 8 \\
0 + 2 & 0 + 4
\end{pmatrix} =
\begin{pmatrix}
3 & 1 \\
2 & 4
\end{pmatrix} = B.
$$
