### Exercise 3. Inconsistent System

#### Exercise Reminder

Solve or show that the system is inconsistent:

$$
\begin{cases}
x + 2y = 3, \\
2x + 4y = 7.
\end{cases}
$$

Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.

---

#### Solution

**Result.** The system is **inconsistent** and has **no solution** (the solution set is $\emptyset$).

<br>

**Main steps.**

1. **Form the augmented matrix $[A \mid b]$:**

$$
[A \mid b] =
\left(
\begin{array}{cc|c}
1 & 2 & 3 \\
2 & 4 & 7
\end{array}
\right).
$$

2. **Perform Gaussian elimination to eliminate $x$ from row $2$ via $R_2 \leftarrow R_2 - 2R_1$:**

$$
\left(
\begin{array}{cc|c}
1 & 2 & 3 \\
2 & 4 & 7
\end{array}
\right)
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\left(
\begin{array}{cc|c}
1 & 2 & 3 \\
0 & 0 & 1
\end{array}
\right).
$$

3. **Identify the contradiction in the matrix and interpret it in terms of equations:**
   - **In the matrix:** Row $2$ of the reduced augmented matrix has all zeros on the left of the vertical bar and a nonzero constant $1$ on the right, showing that the coefficient matrix has rank $1$ while the augmented matrix has rank $2$.
   - **In terms of equations:** Translating row $2$ back into an algebraic equation gives

$$
0x + 0y = 1 \implies 0 = 1,
$$

which is an impossible contradiction satisfied by no pair $(x, y) \in \mathbb{R}^2$. Equivalently, multiplying the first equation $x + 2y = 3$ by $2$ requires $2x + 4y = 6$, which directly contradicts the second equation $2x + 4y = 7$ (geometrically, the two equations represent distinct parallel lines with slope $-\frac{1}{2}$ that never intersect).

<br>

**Property / method used.** *Rouché–Capelli inconsistency criterion via row reduction:* a linear system $Ax = b$ is inconsistent if and only if row reduction of $[A \mid b]$ produces a row with all zero coefficients on the left and a nonzero constant $c \neq 0$ on the right, corresponding to the contradictory equation $0 = c$.

<br>

**Mathematical verification.** Subtracting twice the first equation from the second equation directly confirms the algebraic contradiction:

$$
(2x + 4y) - 2(x + 2y) = 7 - 2(3) \implies (2x - 2x) + (4y - 4y) = 7 - 6 \implies 0 = 1.
$$
