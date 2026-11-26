### Exercise 4. Infinitely Many Solutions

#### Exercise Reminder

Solve

$$
\begin{cases}
x + y + z = 2, \\
2x + 2y + 2z = 4, \\
x - y + z = 0.
\end{cases}
$$

Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point really satisfies the system.

---

#### Solution

**Result.** The system has infinitely many solutions. Choosing **$z = t \in \mathbb{R}$ as the free variable**, the general solution in parametric form is

$$
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix} =
\begin{pmatrix}
1 - t \\
1 \\
t
\end{pmatrix} =
\begin{pmatrix}
1 \\
1 \\
0
\end{pmatrix} + t
\begin{pmatrix}
-1 \\
0 \\
1
\end{pmatrix}, \qquad t \in \mathbb{R}.
$$

Choosing the parameter value $t = 2$ gives the specific point $(x, y, z) = (-1, 1, 2)$, which satisfies all three equations.

<br>

**Main steps.**

1. **Form the augmented matrix $[A \mid b]$:**

$$
[A \mid b] =
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 2 \\
2 & 2 & 2 & 4 \\
1 & -1 & 1 & 0
\end{array}
\right).
$$

2. **Eliminate $x$ below the first pivot via $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - R_1$:**

$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 2 \\
2 & 2 & 2 & 4 \\
1 & -1 & 1 & 0
\end{array}
\right)
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 2 \\
0 & 0 & 0 & 0 \\
1 & -1 & 1 & 0
\end{array}
\right)
\xrightarrow{R_3 \leftarrow R_3 - R_1}
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 2 \\
0 & 0 & 0 & 0 \\
0 & -2 & 0 & -2
\end{array}
\right).
$$

3. **Move the zero row to the bottom ($R_2 \leftrightarrow R_3$) and scale row $2$ ($R_2 \leftarrow -\frac{1}{2}R_2$) to obtain reduced row echelon form:**

$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 2 \\
0 & 0 & 0 & 0 \\
0 & -2 & 0 & -2
\end{array}
\right)
\xrightarrow{R_2 \leftrightarrow R_3}
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 2 \\
0 & -2 & 0 & -2 \\
0 & 0 & 0 & 0
\end{array}
\right)
\xrightarrow{R_2 \leftarrow -\frac{1}{2}R_2}
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 2 \\
0 & 1 & 0 & 1 \\
0 & 0 & 0 & 0
\end{array}
\right),
$$

and eliminate above the second pivot via $R_1 \leftarrow R_1 - R_2$:

$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 2 \\
0 & 1 & 0 & 1 \\
0 & 0 & 0 & 0
\end{array}
\right)
\xrightarrow{R_1 \leftarrow R_1 - R_2}
\left(
\begin{array}{ccc|c}
1 & 0 & 1 & 1 \\
0 & 1 & 0 & 1 \\
0 & 0 & 0 & 0
\end{array}
\right).
$$

4. **Identify the free variable and write the parametric solution:**
   - The pivots lie in columns $1$ ($x$) and $2$ ($y$), while column $3$ ($z$) has no pivot. Hence **$z$ is a free variable**; set $z = t$ for any $t \in \mathbb{R}$.
   - Reading the remaining nonzero equations gives $y = 1$ and $x + z = 1 \implies x = 1 - t$.
   - Writing $(x, y, z)^T$ in vector form yields

$$
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix} =
\begin{pmatrix}
1 - t \\
1 \\
t
\end{pmatrix} =
\begin{pmatrix}
1 \\
1 \\
0
\end{pmatrix} + t
\begin{pmatrix}
-1 \\
0 \\
1
\end{pmatrix}, \qquad t \in \mathbb{R}.
$$

<br>

**Property / method used.** *Parametric representation of underdetermined consistent systems:* when reduced row echelon form has $r < n$ pivots and no contradictory row $(0 \ \dots \ 0 \mid c)$ with $c \neq 0$, the $n - r$ non-pivot columns correspond to free parameters, and the solution set forms an $(n - r)$-dimensional affine subspace (here, a line in $\mathbb{R}^3$).

<br>

**Mathematical verification.** Choose $t = 2$, which produces the point $(x, y, z) = (1 - 2, 1, 2) = (-1, 1, 2)$, and substitute it into all three original equations:
- **Equation 1:** $(-1) + 1 + 2 = 2$ (matches $2$).
- **Equation 2:** $2(-1) + 2(1) + 2(2) = -2 + 2 + 4 = 4$ (matches $4$).
- **Equation 3:** $(-1) - 1 + 2 = 0$ (matches $0$).

All three equations are satisfied simultaneously.
