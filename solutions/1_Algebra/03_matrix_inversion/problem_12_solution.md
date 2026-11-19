### Exercise 12. Finding Inverses Without Starting from Scratch

#### Exercise Reminder

It is known that

$$
A^{-1} =
\begin{pmatrix}
2 & -1 \\
-3 & 2
\end{pmatrix}.
$$

Without finding $A$, compute $(3A)^{-1}$, $(A^T)^{-1}$, and $(A^2)^{-1}$. Justify each result using the appropriate property.

---

#### Solution

**Result.**

$$
(3A)^{-1} =
\begin{pmatrix}
\frac{2}{3} & -\frac{1}{3} \\
-1 & \frac{2}{3}
\end{pmatrix},\qquad (A^T)^{-1} =
\begin{pmatrix}
2 & -3 \\
-1 & 2
\end{pmatrix},\qquad (A^2)^{-1} =
\begin{pmatrix}
7 & -4 \\
-12 & 7
\end{pmatrix}.
$$

<br>

**Main steps.** Use algebraic inverse properties to express each target inverse directly in terms of the known matrix $A^{-1}$ without ever computing $A$:

1. **Compute $(3A)^{-1}$:** Apply the scalar-multiple inverse rule $(cA)^{-1} = \frac{1}{c}A^{-1}$ with $c = 3$:

$$
(3A)^{-1} = \frac{1}{3}A^{-1} = \frac{1}{3}
\begin{pmatrix}
2 & -1 \\
-3 & 2
\end{pmatrix} =
\begin{pmatrix}
\frac{2}{3} & -\frac{1}{3} \\
-1 & \frac{2}{3}
\end{pmatrix}.
$$

   - **Justification:** Because $(3A)\left(\frac{1}{3}A^{-1}\right) = \left(3\cdot \frac{1}{3}\right)(AA^{-1}) = 1\cdot I = I$, scaling a matrix by a nonzero constant $c$ scales its inverse by $\frac{1}{c}$.

2. **Compute $(A^T)^{-1}$:** Apply the transpose-inverse rule $(A^T)^{-1} = (A^{-1})^T$:

$$
(A^T)^{-1} = (A^{-1})^T =
\begin{pmatrix}
2 & -1 \\
-3 & 2
\end{pmatrix}^T =
\begin{pmatrix}
2 & -3 \\
-1 & 2
\end{pmatrix}.
$$

   - **Justification:** Taking the transpose of $AA^{-1} = I$ gives $(A^{-1})^T A^T = I^T = I$ (and similarly $A^T (A^{-1})^T = I$), so transposition and inversion commute.

3. **Compute $(A^2)^{-1}$:** Apply the power-inverse rule $(A^k)^{-1} = (A^{-1})^k$ for $k = 2$:

$$
(A^2)^{-1} = (A^{-1})^2 =
\begin{pmatrix}
2 & -1 \\
-3 & 2
\end{pmatrix}
\begin{pmatrix}
2 & -1 \\
-3 & 2
\end{pmatrix} =
\begin{pmatrix}
2\cdot 2 + (-1)\cdot (-3) & 2\cdot (-1) + (-1)\cdot 2 \\
(-3)\cdot 2 + 2\cdot (-3) & (-3)\cdot (-1) + 2\cdot 2
\end{pmatrix} =
\begin{pmatrix}
4 + 3 & -2 - 2 \\
-6 - 6 & 3 + 4
\end{pmatrix} =
\begin{pmatrix}
7 & -4 \\
-12 & 7
\end{pmatrix}.
$$

   - **Justification:** By associativity of matrix multiplication (and the product rule $(AB)^{-1} = B^{-1}A^{-1}$ with $B = A$), $A^2 (A^{-1})^2 = A(AA^{-1})A^{-1} = AIA^{-1} = I$.

<br>

**Property / method used.** *Algebraic rules for matrix inverses:* for any invertible $n\times n$ matrix $A$, nonzero scalar $c \neq 0$, and positive integer $k \ge 1$:
- $(cA)^{-1} = c^{-1}A^{-1}$,
- $(A^T)^{-1} = (A^{-1})^T$,
- $(A^k)^{-1} = (A^{-1})^k$.

<br>

**Mathematical verification.** As an independent consistency check, recovering $A = (A^{-1})^{-1}$ from $\det(A^{-1}) = 2\cdot 2 - (-1)(-3) = 1$ gives

$$
A =
\begin{pmatrix}
2 & 1 \\
3 & 2
\end{pmatrix}.
$$

Multiplying each transformed matrix by its computed inverse directly confirms the identity matrix $I$ in all three cases:

$$
(3A)(3A)^{-1} = 3
\begin{pmatrix}
2 & 1 \\
3 & 2
\end{pmatrix}
\cdot \frac{1}{3}
\begin{pmatrix}
2 & -1 \\
-3 & 2
\end{pmatrix} =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} = I,
$$

$$
A^T (A^T)^{-1} =
\begin{pmatrix}
2 & 3 \\
1 & 2
\end{pmatrix}
\begin{pmatrix}
2 & -3 \\
-1 & 2
\end{pmatrix} =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} = I,
$$

$$
A^2 (A^2)^{-1} =
\begin{pmatrix}
7 & 4 \\
12 & 7
\end{pmatrix}
\begin{pmatrix}
7 & -4 \\
-12 & 7
\end{pmatrix} =
\begin{pmatrix}
49 - 48 & -28 + 28 \\
84 - 84 & -48 + 49
\end{pmatrix} =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} = I.
$$
