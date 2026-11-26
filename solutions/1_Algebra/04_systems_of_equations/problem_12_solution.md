### Exercise 12. Homogeneous System

#### Exercise Reminder

Solve

$$
\begin{cases}
x + 2y - z = 0, \\
2x + 4y - 2z = 0, \\
x - y + 2z = 0.
\end{cases}
$$

Give all solutions in parametric form and explain why $(0, 0, 0)$ always satisfies a homogeneous system.

---

#### Solution

**Result.** The homogeneous system has infinitely many solutions (a $1$-dimensional subspace spanned by one vector). Choosing **$z = t \in \mathbb{R}$ as the free variable**, all solutions in parametric form are given by

$$
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix} =
\begin{pmatrix}
-t \\
t \\
t
\end{pmatrix} = t
\begin{pmatrix}
-1 \\
1 \\
1
\end{pmatrix}, \qquad t \in \mathbb{R}.
$$

<br>

**Main steps.**

1. **Form the augmented matrix $[A \mid 0]$ and eliminate $x$ from rows $2$ and $3$ via $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - R_1$:**

$$
[A \mid 0] =
\left(
\begin{array}{ccc|c}
1 & 2 & -1 & 0 \\
2 & 4 & -2 & 0 \\
1 & -1 & 2 & 0
\end{array}
\right)
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\left(
\begin{array}{ccc|c}
1 & 2 & -1 & 0 \\
0 & 0 & 0 & 0 \\
1 & -1 & 2 & 0
\end{array}
\right)
\xrightarrow{R_3 \leftarrow R_3 - R_1}
\left(
\begin{array}{ccc|c}
1 & 2 & -1 & 0 \\
0 & 0 & 0 & 0 \\
0 & -3 & 3 & 0
\end{array}
\right).
$$

2. **Swap rows $2$ and $3$ ($R_2 \leftrightarrow R_3$) and scale row $2$ ($R_2 \leftarrow -\frac{1}{3}R_2$) to reach row echelon form:**

$$
\left(
\begin{array}{ccc|c}
1 & 2 & -1 & 0 \\
0 & 0 & 0 & 0 \\
0 & -3 & 3 & 0
\end{array}
\right)
\xrightarrow{R_2 \leftrightarrow R_3}
\left(
\begin{array}{ccc|c}
1 & 2 & -1 & 0 \\
0 & -3 & 3 & 0 \\
0 & 0 & 0 & 0
\end{array}
\right)
\xrightarrow{R_2 \leftarrow -\frac{1}{3}R_2}
\left(
\begin{array}{ccc|c}
1 & 2 & -1 & 0 \\
0 & 1 & -1 & 0 \\
0 & 0 & 0 & 0
\end{array}
\right).
$$

   Eliminating above the second pivot via $R_1 \leftarrow R_1 - 2R_2$ gives the reduced row echelon form:

$$
\left(
\begin{array}{ccc|c}
1 & 2 & -1 & 0 \\
0 & 1 & -1 & 0 \\
0 & 0 & 0 & 0
\end{array}
\right)
\xrightarrow{R_1 \leftarrow R_1 - 2R_2}
\left(
\begin{array}{ccc|c}
1 & 0 & 1 & 0 \\
0 & 1 & -1 & 0 \\
0 & 0 & 0 & 0
\end{array}
\right).
$$

3. **Write all solutions in parametric form:**
   - The pivots lie in columns $1$ ($x$) and $2$ ($y$), leaving column $3$ ($z$) as the single free variable. Set $z = t \in \mathbb{R}$.
   - Reading the reduced equations gives $y - z = 0 \implies y = t$ and $x + z = 0 \implies x = -t$.
   - Writing $(x, y, z)^T$ in vector form yields

$$
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix} =
\begin{pmatrix}
-t \\
t \\
t
\end{pmatrix} = t
\begin{pmatrix}
-1 \\
1 \\
1
\end{pmatrix}, \qquad t \in \mathbb{R}.
$$

4. **Explain why $(0, 0, 0)$ always satisfies a homogeneous system:**
   - By definition, a homogeneous linear system has the form $Ax = 0$, where every equation has right-hand side $0$:

$$
a_{i1}x + a_{i2}y + a_{i3}z = 0 \qquad (i = 1, 2, 3).
$$

   - Substituting $(x, y, z) = (0, 0, 0)$ into the left-hand side of any linear equation without a constant term gives $a_{i1}(0) + a_{i2}(0) + a_{i3}(0) = 0 + 0 + 0 = 0$, which always equals the right-hand side $0$ (in matrix form, $A\mathbf{0} = \mathbf{0}$ for every matrix $A$). Therefore, the trivial solution $(0, 0, 0)$ is always present, and every homogeneous system is guaranteed to be consistent.

<br>

**Property / method used.** *Null space (kernel) of a homogeneous system $Ax = 0$:* elementary row operations preserve the zero right-hand side column, and the set of all solutions forms the vector subspace $\ker(A) = \mathrm{span}\{(-1, 1, 1)^T\}$ passing through the origin $(0, 0, 0)$ (corresponding to $t = 0$).

<br>

**Mathematical verification.** Substituting $x = -t$, $y = t$, and $z = t$ into all three original equations confirms that every term cancels to $0$ for all $t \in \mathbb{R}$:
- **Equation 1:** $(-t) + 2(t) - t = -t + 2t - t = 0$.
- **Equation 2:** $2(-t) + 4(t) - 2(t) = -2t + 4t - 2t = 0$.
- **Equation 3:** $(-t) - t + 2(t) = -2t + 2t = 0$.
