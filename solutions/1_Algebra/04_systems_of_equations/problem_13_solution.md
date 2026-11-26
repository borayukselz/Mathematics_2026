### Exercise 13. Does Every Equation Add New Information?

#### Exercise Reminder

Consider the system

$$
x_1 + x_2 = 10, \qquad x_2 + x_3 = 8, \qquad x_1 - x_3 = 2.
$$

Solve it and check whether all three equations are independently necessary to describe the solution set. If one follows from the others, show this by calculation.

---

#### Solution

**Result.** The system is consistent and has **infinitely many solutions** (a $1$-parameter family). Choosing **$x_3 = t \in \mathbb{R}$ as the free variable**, the solution set is

$$
\begin{pmatrix}
x_1 \\
x_2 \\
x_3
\end{pmatrix} =
\begin{pmatrix}
2 + t \\
8 - t \\
t
\end{pmatrix} =
\begin{pmatrix}
2 \\
8 \\
0
\end{pmatrix} + t
\begin{pmatrix}
1 \\
-1 \\
1
\end{pmatrix}, \qquad t \in \mathbb{R}.
$$

**Redundancy check:** **No**, not all three equations are independently necessary—any two equations determine the exact same solution set, and the third equation is a redundant linear combination of the first two (specifically, Equation $3$ equals Equation $1$ minus Equation $2$).

<br>

**Main steps.**

1. **Form the augmented matrix $[A \mid b]$ and eliminate $x_1$ from row $3$ via $R_3 \leftarrow R_3 - R_1$:**

$$
[A \mid b] =
\left(
\begin{array}{ccc|c}
1 & 1 & 0 & 10 \\
0 & 1 & 1 & 8 \\
1 & 0 & -1 & 2
\end{array}
\right)
\xrightarrow{R_3 \leftarrow R_3 - R_1}
\left(
\begin{array}{ccc|c}
1 & 1 & 0 & 10 \\
0 & 1 & 1 & 8 \\
0 & -1 & -1 & -8
\end{array}
\right).
$$

2. **Eliminate $x_2$ from row $3$ via $R_3 \leftarrow R_3 + R_2$:**

$$
\left(
\begin{array}{ccc|c}
1 & 1 & 0 & 10 \\
0 & 1 & 1 & 8 \\
0 & -1 & -1 & -8
\end{array}
\right)
\xrightarrow{R_3 \leftarrow R_3 + R_2}
\left(
\begin{array}{ccc|c}
1 & 1 & 0 & 10 \\
0 & 1 & 1 & 8 \\
0 & 0 & 0 & 0
\end{array}
\right).
$$

3. **Write the parametric solution:**
   - There are $n = 3$ variables and $r = 2$ pivots (in columns $1$ and $2$), leaving $3 - 2 = 1$ free variable: set $x_3 = t \in \mathbb{R}$.
   - From row $2$: $x_2 + x_3 = 8 \implies x_2 = 8 - t$.
   - From row $1$: $x_1 + x_2 = 10 \implies x_1 = 10 - (8 - t) = 2 + t$.
   - In vector form:

$$
\begin{pmatrix}
x_1 \\
x_2 \\
x_3
\end{pmatrix} =
\begin{pmatrix}
2 + t \\
8 - t \\
t
\end{pmatrix} =
\begin{pmatrix}
2 \\
8 \\
0
\end{pmatrix} + t
\begin{pmatrix}
1 \\
-1 \\
1
\end{pmatrix}, \qquad t \in \mathbb{R}.
$$

4. **Show by explicit calculation that the third equation follows from the first two:**
   - Subtracting Equation $2$ ($x_2 + x_3 = 8$) directly from Equation $1$ ($x_1 + x_2 = 10$) gives

$$
(x_1 + x_2) - (x_2 + x_3) = 10 - 8 \implies x_1 + (x_2 - x_2) - x_3 = 2 \implies x_1 - x_3 = 2,
$$

     which is identically Equation $3$.
   - Equivalently, in augmented row vector form, $R_3 = R_1 - R_2$:

$$
(1 \quad 0 \quad -1 \mid 2) = (1 \quad 1 \quad 0 \mid 10) - (0 \quad 1 \quad 1 \mid 8).
$$

   - Because Equation $3$ is automatically satisfied by every triple $(x_1, x_2, x_3)$ that satisfies the first two equations, removing Equation $3$ leaves the solution set completely unchanged.

<br>

**Property / method used.** *Linear dependence of equations (redundant constraints):* when an augmented row in $[A \mid b]$ is a linear combination of the other augmented rows, Gaussian elimination reduces it to a zero row $(0 \ \dots \ 0 \mid 0)$, meaning the constraint adds no new restriction to the solution set.

<br>

**Mathematical verification.** Substituting $x_1 = 2 + t$, $x_2 = 8 - t$, and $x_3 = t$ into all three original equations confirms consistency for every $t \in \mathbb{R}$:
- **Equation 1:** $(2 + t) + (8 - t) = 10$.
- **Equation 2:** $(8 - t) + t = 8$.
- **Equation 3:** $(2 + t) - t = 2$.
