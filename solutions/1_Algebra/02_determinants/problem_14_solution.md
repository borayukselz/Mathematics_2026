### Exercise 14. A System of Equations and the Determinant

#### Exercise Reminder

Consider the linear system $Ax = b$, where

$$
A=
\begin{pmatrix}
1 & 2 \\
k & 4 \\
\end{pmatrix}.
$$

1. For which values of $k$ does the system have exactly one solution for every $b$?
2. For the remaining value, give an example of a right-hand side $b$ for which the system has infinitely many solutions, and an example for which it has no solution.

---

#### Solution

##### 1. Values of $k$ for Which $Ax = b$ Has a Unique Solution for Every $b$

**Result.** The system $Ax = b$ has a unique solution for every $b \in \mathbb{R}^2$ if and only if

$$
k \neq 2.
$$

<br>

**Main steps.** Compute the determinant of the $2\times 2$ coefficient matrix $A$:

$$
\det A = 1 \cdot 4 - 2 \cdot k = 4 - 2k.
$$

A square linear system $Ax = b$ admits a unique solution $x = A^{-1}b$ for every right-hand side $b$ if and only if $A$ is invertible, which occurs precisely when $\det A \neq 0$:

$$
\det A \neq 0 \iff 4 - 2k \neq 0 \iff 2k \neq 4 \iff k \neq 2.
$$

<br>

**Property / method used.** *Invertible Matrix Theorem (unique solvability criterion):* for an $n\times n$ matrix $A$, the linear system $Ax = b$ has a unique solution for every $b \in \mathbb{R}^n$ if and only if $\det A \neq 0$.

<br>

**Mathematical verification.** For any $k \neq 2$, $4 - 2k \neq 0$, so the explicit inverse matrix exists and produces the unique solution $x = A^{-1}b$:

$$
A^{-1} = \frac{1}{4 - 2k}
\begin{pmatrix}
4 & -2 \\
-k & 1 \\
\end{pmatrix}
\implies x = \frac{1}{4 - 2k}
\begin{pmatrix}
4b_1 - 2b_2 \\
-kb_1 + b_2 \\
\end{pmatrix}.
$$

---

##### 2. Examples for the Remaining Value $k = 2$

**Result.** For the remaining value $k = 2$:
- **Example with infinitely many solutions:**

$$
b=
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}.
$$

- **Example with no solution:**

$$
b=
\begin{pmatrix}
1 \\
3 \\
\end{pmatrix}.
$$

<br>

**Main steps.** When $k = 2$, the coefficient matrix becomes

$$
A=
\begin{pmatrix}
1 & 2 \\
2 & 4 \\
\end{pmatrix},
$$

and the system $Ax = b$ with $x = (x_1, x_2)^T$ and $b = (b_1, b_2)^T$ writes out as

$$
\begin{aligned}
x_1 + 2x_2 &= b_1, \\
2x_1 + 4x_2 &= b_2.
\end{aligned}
$$

Applying the row operation $R_2 \leftarrow R_2 - 2R_1$ to the augmented matrix gives

$$
\left(\begin{array}{cc|c}
1 & 2 & b_1 \\
2 & 4 & b_2
\end{array}\right)
\quad \longrightarrow \quad
\left(\begin{array}{cc|c}
1 & 2 & b_1 \\
0 & 0 & b_2 - 2b_1
\end{array}\right).
$$

1. **Case 1 — Infinitely many solutions ($b_2 - 2b_1 = 0$):** Choose $b_1 = 1$ and $b_2 = 2$, so $b = (1, 2)^T$. The second row reduces to $0x_1 + 0x_2 = 0$, leaving a single equation $x_1 + 2x_2 = 1$ in two unknowns. Setting $x_2 = t \in \mathbb{R}$ as a free parameter gives infinitely many solutions:

$$
x=
\begin{pmatrix}
1 - 2t \\
t \\
\end{pmatrix}, \qquad t \in \mathbb{R}.
$$

2. **Case 2 — No solution ($b_2 - 2b_1 \neq 0$):** Choose $b_1 = 1$ and $b_2 = 3$, so $b = (1, 3)^T$. The second row reduces to the impossible equation $0x_1 + 0x_2 = 1$. Because the system is inconsistent, it has no solution.

<br>

**Property / method used.** *Rouché–Capelli theorem (rank condition for consistency):* when $\det A = 0$ ($\mathrm{rank}(A) = 1 < 2$), $Ax = b$ has infinitely many solutions if $\mathrm{rank}(A \mid b) = 1$ (consistent with $2 - 1 = 1$ free variable), and has no solution if $\mathrm{rank}(A \mid b) = 2$ (inconsistent).

<br>

**Mathematical verification.**
- Substituting $x = (1 - 2t,\, t)^T$ into $Ax$ confirms $Ax = (1, 2)^T$ for every $t \in \mathbb{R}$:

$$
\begin{pmatrix}
1 & 2 \\
2 & 4 \\
\end{pmatrix}
\begin{pmatrix}
1 - 2t \\
t \\
\end{pmatrix}=
\begin{pmatrix}
(1 - 2t) + 2t \\
2(1 - 2t) + 4t \\
\end{pmatrix}=
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}.
$$

- For $b = (1, 3)^T$, any pair $(x_1, x_2)$ satisfying $x_1 + 2x_2 = 1$ must satisfy $2x_1 + 4x_2 = 2(x_1 + 2x_2) = 2 \neq 3$, confirming that no solution exists.
