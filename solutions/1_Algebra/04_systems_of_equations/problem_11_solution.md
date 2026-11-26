### Exercise 11. A Parameter in a System of Three Equations

#### Exercise Reminder

Analyze the number of solutions depending on $t$:

$$
\begin{cases}
x + y + z = 1, \\
x + ty + z = 2, \\
x + y + tz = 3.
\end{cases}
$$

Use elimination and separately analyze the parameter values for which a standard calculation step ceases to be valid.

---

#### Solution

**Result.**
- **For $t \neq 1$:** The system has **exactly one unique solution**:

$$
(x, y, z) = \left(1 - \frac{3}{t - 1}, \ \frac{1}{t - 1}, \ \frac{2}{t - 1}\right) = \left(\frac{t - 4}{t - 1}, \ \frac{1}{t - 1}, \ \frac{2}{t - 1}\right).
$$

- **For $t = 1$:** Dividing by $t - 1$ during back-substitution ceases to be valid ($t - 1 = 0$); the system reduces to contradictory equations ($0 = 1$ and $0 = 2$) and has **no solution** (inconsistent).
- **Infinitely many solutions:** Never occurs for any $t \in \mathbb{R}$.

<br>

**Main steps.**

1. **Form the augmented matrix $[A \mid b]$ and eliminate $x$ from rows $2$ and $3$ via $R_2 \leftarrow R_2 - R_1$ and $R_3 \leftarrow R_3 - R_1$:**

$$
[A \mid b] =
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 1 \\
1 & t & 1 & 2 \\
1 & 1 & t & 3
\end{array}
\right)
\xrightarrow{R_2 \leftarrow R_2 - R_1}
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 1 \\
0 & t - 1 & 0 & 1 \\
1 & 1 & t & 3
\end{array}
\right)
\xrightarrow{R_3 \leftarrow R_3 - R_1}
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 1 \\
0 & t - 1 & 0 & 1 \\
0 & 0 & t - 1 & 2
\end{array}
\right).
$$

   Notice that the matrix is already in upper triangular form without requiring any division by $t - 1$ during forward elimination:

$$
\begin{cases}
x + y + z = 1, \\
(t - 1)y = 1, \\
(t - 1)z = 2.
\end{cases}
$$

2. **Identify where standard back-substitution ceases to be valid ($t - 1 = 0 \iff t = 1$):**
   - Standard back-substitution solves $(t - 1)z = 2$ and $(t - 1)y = 1$ by dividing both sides by $t - 1$.
   - This division is valid if and only if $t - 1 \neq 0$ (i.e., $t \neq 1$). When $t = 1$, $t - 1 = 0$ and division by zero is undefined.

3. **Case 1 — $t \neq 1$ (valid division by $t - 1$):**
   - From row $3$: $(t - 1)z = 2 \implies z = \frac{2}{t - 1}$.
   - From row $2$: $(t - 1)y = 1 \implies y = \frac{1}{t - 1}$.
   - From row $1$: $x + y + z = 1 \implies x = 1 - \frac{1}{t - 1} - \frac{2}{t - 1} = 1 - \frac{3}{t - 1} = \frac{t - 4}{t - 1}$.
   - Every variable is uniquely determined, yielding **exactly one solution**.

4. **Case 2 — $t = 1$ (separate analysis of the singular parameter value):**
   - Substituting $t = 1$ directly into the reduced augmented matrix gives

$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 1 \\
0 & 0 & 0 & 1 \\
0 & 0 & 0 & 2
\end{array}
\right).
$$

   - Rows $2$ and $3$ read $0 = 1$ and $0 = 2$, both of which are contradictions (geometrically, the three equations become $x + y + z = 1$, $x + y + z = 2$, and $x + y + z = 3$, representing three distinct parallel planes with no common point).
   - Hence, for $t = 1$, the system is inconsistent and has **no solution**.

<br>

**Property / method used.** *Parametric Gaussian elimination with singular-pivot case splitting:* forward row replacement reduces the system cleanly to triangular form with diagonal pivots $1$, $t - 1$, and $t - 1$ (determinant $\det A = (t - 1)^2$); separating the root $t = 1$ of the pivot factor $t - 1$ prevents illegal division by zero and distinguishes the unique-solution regime ($t \neq 1$) from the inconsistent regime ($t = 1$).

<br>

**Mathematical verification.** For any $t \neq 1$, substituting $x = \frac{t - 4}{t - 1}$, $y = \frac{1}{t - 1}$, and $z = \frac{2}{t - 1}$ into all three original equations confirms consistency:
- **Equation 1:** $\frac{t - 4}{t - 1} + \frac{1}{t - 1} + \frac{2}{t - 1} = \frac{t - 4 + 1 + 2}{t - 1} = \frac{t - 1}{t - 1} = 1$.
- **Equation 2:** $\frac{t - 4}{t - 1} + \frac{t}{t - 1} + \frac{2}{t - 1} = \frac{2t - 2}{t - 1} = \frac{2(t - 1)}{t - 1} = 2$.
- **Equation 3:** $\frac{t - 4}{t - 1} + \frac{1}{t - 1} + \frac{2t}{t - 1} = \frac{3t - 3}{t - 1} = \frac{3(t - 1)}{t - 1} = 3$.
