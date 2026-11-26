### Exercise 5. Row Echelon Form and Number of Solutions

#### Exercise Reminder

For the augmented matrix

$$
\left(
\begin{array}{ccc|c}
1 & 2 & -1 & 3 \\
0 & 1 & 2 & 1 \\
0 & 0 & 0 & 0
\end{array}
\right)
$$

determine the number of solutions and write them in parametric form. Explain how you know how many variables may be chosen freely.

---

#### Solution

**Result.** The system is consistent and has **infinitely many solutions** (a $1$-parameter family). Choosing **$z = t \in \mathbb{R}$ as the single free variable**, the general solution in parametric form is

$$
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix} =
\begin{pmatrix}
1 + 5t \\
1 - 2t \\
t
\end{pmatrix} =
\begin{pmatrix}
1 \\
1 \\
0
\end{pmatrix} + t
\begin{pmatrix}
5 \\
-2 \\
1
\end{pmatrix}, \qquad t \in \mathbb{R}.
$$

<br>

**Main steps.**

1. **Determine consistency and the number of free variables:**
   - The matrix is already in row echelon form with **$n = 3$ unknowns** ($x, y, z$).
   - Row $3$ is $(0 \quad 0 \quad 0 \mid 0)$, which represents the trivial identity $0 = 0$; there is no contradictory row with all zeros on the left and a nonzero constant on the right, so the system is **consistent**.
   - The leading nonzero entries (pivots) sit in column $1$ at row $1$, column $1$ and column $2$ at row $2$, column $2$, giving rank $r = 2$.
   - Because there are $n = 3$ variables and $r = 2$ pivot variables ($x$ and $y$), the number of variables that may be chosen freely is

$$
n - r = 3 - 2 = 1.
$$

   - Column $3$ contains no pivot, so **$z$ is the single free variable**.

2. **Convert the row echelon matrix back into equations and solve for the pivot variables:**
   - Let $z = t \in \mathbb{R}$.
   - From row $2$, $y + 2z = 1 \implies y = 1 - 2t$.
   - From row $1$, $x + 2y - z = 3$; substituting $y = 1 - 2t$ and $z = t$ gives

$$
x + 2(1 - 2t) - t = 3 \implies x + 2 - 5t = 3 \implies x = 1 + 5t.
$$

3. **Write the solution in parametric vector form:**

$$
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix} =
\begin{pmatrix}
1 + 5t \\
1 - 2t \\
t
\end{pmatrix} =
\begin{pmatrix}
1 \\
1 \\
0
\end{pmatrix} + t
\begin{pmatrix}
5 \\
-2 \\
1
\end{pmatrix}, \qquad t \in \mathbb{R}.
$$

<br>

**Property / method used.** *Rank–nullity / pivot-column counting in row echelon form:* for a consistent linear system in $n$ unknowns whose coefficient matrix has rank $r$ (number of pivots), $r$ basic variables are uniquely determined once the remaining $n - r$ non-pivot (free) variables are assigned arbitrary parameter values.

<br>

**Mathematical verification.** Substitute $x = 1 + 5t$, $y = 1 - 2t$, and $z = t$ into the two nonzero rows of the original system to verify that the parameter $t$ cancels out identically:
- **Row 1:** $(1 + 5t) + 2(1 - 2t) - t = 1 + 5t + 2 - 4t - t = 3$ (matches $3$ for all $t \in \mathbb{R}$).
- **Row 2:** $0(1 + 5t) + 1(1 - 2t) + 2(t) = 1 - 2t + 2t = 1$ (matches $1$ for all $t \in \mathbb{R}$).
