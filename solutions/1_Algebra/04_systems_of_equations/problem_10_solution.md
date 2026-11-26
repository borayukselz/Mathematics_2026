### Exercise 10. A Polynomial Through Three Points

#### Exercise Reminder

Find a polynomial $p(x) = ax^2 + bx + c$ whose graph passes through $(0, 1)$, $(1, 3)$, and $(2, 9)$. Reduce the problem to a system of equations and check the result by substituting all three points.

---

#### Solution

**Result.** The unique quadratic polynomial passing through $(0, 1)$, $(1, 3)$, and $(2, 9)$ is

$$
p(x) = 2x^2 + 1
$$

(with coefficients $a = 2$, $b = 0$, and $c = 1$).

<br>

**Main steps.**

1. **Substitute the three points into $p(x) = ax^2 + bx + c$ to form a $3\times 3$ linear system in $(a, b, c)$:**
   - Passing through $(0, 1)$ requires $p(0) = 1$:

$$
a(0)^2 + b(0) + c = 1 \implies c = 1.
$$

   - Passing through $(1, 3)$ requires $p(1) = 3$:

$$
a(1)^2 + b(1) + c = 3 \implies a + b + c = 3.
$$

   - Passing through $(2, 9)$ requires $p(2) = 9$:

$$
a(2)^2 + b(2) + c = 9 \implies 4a + 2b + c = 9.
$$

   This gives the linear system

$$
\begin{cases}
c = 1, \\
a + b + c = 3, \\
4a + 2b + c = 9.
\end{cases}
$$

2. **Form the augmented matrix $[A \mid d]$ (ordering unknowns as $(a, b, c)$) and solve by Gaussian elimination:**

$$
[A \mid d] =
\left(
\begin{array}{ccc|c}
0 & 0 & 1 & 1 \\
1 & 1 & 1 & 3 \\
4 & 2 & 1 & 9
\end{array}
\right)
\xrightarrow{R_1 \leftrightarrow R_2}
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 3 \\
0 & 0 & 1 & 1 \\
4 & 2 & 1 & 9
\end{array}
\right)
\xrightarrow{R_3 \leftarrow R_3 - 4R_1}
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 3 \\
0 & 0 & 1 & 1 \\
0 & -2 & -3 & -3
\end{array}
\right).
$$

   Swap $R_2 \leftrightarrow R_3$ to place the second pivot in $(2,2)$:

$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 3 \\
0 & 0 & 1 & 1 \\
0 & -2 & -3 & -3
\end{array}
\right)
\xrightarrow{R_2 \leftrightarrow R_3}
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 3 \\
0 & -2 & -3 & -3 \\
0 & 0 & 1 & 1
\end{array}
\right).
$$

3. **Back-substitution for $(a, b, c)$:**
   - From row $3$: $c = 1$.
   - From row $2$: $-2b - 3(1) = -3 \implies -2b = 0 \implies b = 0$.
   - From row $1$: $a + 0 + 1 = 3 \implies a = 2$.
   - Substituting $(a, b, c) = (2, 0, 1)$ into $p(x) = ax^2 + bx + c$ gives $p(x) = 2x^2 + 1$.

<br>

**Property / method used.** *Lagrange / Vandermonde polynomial interpolation reduced to Gaussian elimination:* evaluating a degree-$2$ polynomial at three distinct $x$-coordinates ($x_0 = 0, x_1 = 1, x_2 = 2$) produces an invertible Vandermonde linear system for the unknown coefficients $(a, b, c)$.

<br>

**Mathematical verification.** Substitute $x = 0$, $x = 1$, and $x = 2$ directly into $p(x) = 2x^2 + 1$ to confirm all three points lie on its graph:
- **At $(0, 1)$:** $p(0) = 2(0)^2 + 1 = 0 + 1 = 1$.
- **At $(1, 3)$:** $p(1) = 2(1)^2 + 1 = 2 + 1 = 3$.
- **At $(2, 9)$:** $p(2) = 2(2)^2 + 1 = 8 + 1 = 9$.
