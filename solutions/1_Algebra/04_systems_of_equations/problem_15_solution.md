### Exercise 15. Classifying Three Systems

#### Exercise Reminder

For each of the following systems, perform only as much elimination as necessary to recognize its type:

**System 1**

$$
\begin{cases}
x + y = 2, \\
x - y = 0,
\end{cases}
$$

**System 2**

$$
\begin{cases}
x + y = 2, \\
2x + 2y = 4,
\end{cases}
$$

**System 3**

$$
\begin{cases}
x + y = 2, \\
2x + 2y = 5.
\end{cases}
$$

For each, justify the classification: **one solution**, **infinitely many solutions**, or **no solution**.

---

#### Solution

**Result.**
- **System 1:** **One solution** (consistent with $2$ pivots among $2$ unknowns; specifically $(x, y) = (1, 1)$).
- **System 2:** **Infinitely many solutions** (consistent with $1$ pivot among $2$ unknowns, leaving $1$ free variable).
- **System 3:** **No solution** (inconsistent; elimination produces the contradictory row $0 = 1$).

<br>

**Main steps.**

1. **System 1 — Eliminate $x$ from row $2$ via $R_2 \leftarrow R_2 - R_1$:**

$$
\left(
\begin{array}{cc|c}
1 & 1 & 2 \\
1 & -1 & 0
\end{array}
\right)
\xrightarrow{R_2 \leftarrow R_2 - R_1}
\left(
\begin{array}{cc|c}
1 & 1 & 2 \\
0 & -2 & -2
\end{array}
\right).
$$

   - **Justification:** Elimination stops immediately at row echelon form because both columns $1$ and $2$ contain nonzero pivots ($1$ and $-2$). There is no contradictory row, and the number of pivots equals the number of unknowns ($r = n = 2$, leaving $0$ free variables), so the system has **exactly one solution** (specifically $y = 1$ and $x = 1$).

2. **System 2 — Eliminate $x$ from row $2$ via $R_2 \leftarrow R_2 - 2R_1$:**

$$
\left(
\begin{array}{cc|c}
1 & 1 & 2 \\
2 & 2 & 4
\end{array}
\right)
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\left(
\begin{array}{cc|c}
1 & 1 & 2 \\
0 & 0 & 0
\end{array}
\right).
$$

   - **Justification:** Row $2$ reduces completely to $(0 \quad 0 \mid 0)$, which is the valid identity $0 = 0$ (no contradiction). There is only $r = 1$ pivot (in column $1$) among $n = 2$ unknowns, leaving $n - r = 2 - 1 = 1$ free variable ($y = t \in \mathbb{R}$), so the system has **infinitely many solutions** ($(x, y) = (2 - t, t)$).

3. **System 3 — Eliminate $x$ from row $2$ via $R_2 \leftarrow R_2 - 2R_1$:**

$$
\left(
\begin{array}{cc|c}
1 & 1 & 2 \\
2 & 2 & 5
\end{array}
\right)
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\left(
\begin{array}{cc|c}
1 & 1 & 2 \\
0 & 0 & 1
\end{array}
\right).
$$

   - **Justification:** Row $2$ reduces to $(0 \quad 0 \mid 1)$, which translates to the impossible equation $0x + 0y = 1 \implies 0 = 1$. Because a row of zeros on the left is paired with a nonzero entry on the right, the system is inconsistent and has **no solution**.

<br>

**Property / method used.** *Trichotomy of linear systems in row echelon form:* reducing $[A \mid b]$ to echelon form immediately distinguishes all three cases via pivot structure—a row $(0 \ \dots \ 0 \mid c)$ with $c \neq 0$ implies **no solution**; otherwise, $r = n$ pivots implies **one solution**, and $r < n$ pivots implies **infinitely many solutions** ($n - r$ free parameters).

<br>

**Mathematical verification.** Checking each classification directly against the original equations confirms all three results:
- **System 1:** $(1, 1)$ satisfies $1 + 1 = 2$ and $1 - 1 = 0$, and $\det \begin{pmatrix} 1 & 1 \\ 1 & -1 \end{pmatrix} = -2 \neq 0$.
- **System 2:** Equation $2$ is $2(x + y) = 2(2)$, which is identical to Equation $1$.
- **System 3:** Equation $1$ implies $2(x + y) = 4$, which directly contradicts Equation $2$ ($2x + 2y = 5$).
```[cite: 10]
