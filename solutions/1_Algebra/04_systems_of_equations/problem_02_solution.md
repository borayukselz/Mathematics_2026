### Exercise 2. Gaussian Elimination — One Solution

#### Exercise Reminder

Solve using Gaussian elimination:

$$
\begin{cases}
x + y + z = 6, \\
2x - y + z = 3, \\
x + 2y - z = 2.
\end{cases}
$$

After solving, substitute the result into all equations and check consistency.

---

#### Solution

**Result.** The system has a unique solution $(x, y, z) = (1, 2, 3)$, or in column vector form:

$$
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix} =
\begin{pmatrix}
1 \\
2 \\
3
\end{pmatrix}.
$$

<br>

**Main steps.** Write the $3\times 4$ augmented matrix $[A \mid b]$ and reduce it to row echelon form using elementary row operations:

$$
[A \mid b] =
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
2 & -1 & 1 & 3 \\
1 & 2 & -1 & 2
\end{array}
\right).
$$

1. **Step 1 — Eliminate $x$ from rows $2$ and $3$ using the pivot in $(1,1)$ via $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - R_1$:**

$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
2 & -1 & 1 & 3 \\
1 & 2 & -1 & 2
\end{array}
\right)
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & -3 & -1 & -9 \\
1 & 2 & -1 & 2
\end{array}
\right)
\xrightarrow{R_3 \leftarrow R_3 - R_1}
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & -3 & -1 & -9 \\
0 & 1 & -2 & -4
\end{array}
\right).
$$

2. **Step 2 — Swap rows $2$ and $3$ ($R_2 \leftrightarrow R_3$) to place a unit pivot in position $(2,2)$:**

$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & -3 & -1 & -9 \\
0 & 1 & -2 & -4
\end{array}
\right)
\xrightarrow{R_2 \leftrightarrow R_3}
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & 1 & -2 & -4 \\
0 & -3 & -1 & -9
\end{array}
\right).
$$

3. **Step 3 — Eliminate $y$ from row $3$ via $R_3 \leftarrow R_3 + 3R_2$:**

$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & 1 & -2 & -4 \\
0 & -3 & -1 & -9
\end{array}
\right)
\xrightarrow{R_3 \leftarrow R_3 + 3R_2}
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & 1 & -2 & -4 \\
0 & 0 & -7 & -21
\end{array}
\right).
$$

4. **Step 4 — Back-substitution:** From the triangular system

$$
\begin{cases}
x + y + z = 6, \\
y - 2z = -4, \\
-7z = -21,
\end{cases}
$$

solve from the bottom equation upward:
- From $-7z = -21$, divide by $-7$ to get $z = 3$.
- Substitute $z = 3$ into $y - 2z = -4$:

$$
y - 2(3) = -4 \implies y - 6 = -4 \implies y = 2.
$$

- Substitute $y = 2$ and $z = 3$ into $x + y + z = 6$:

$$
x + 2 + 3 = 6 \implies x + 5 = 6 \implies x = 1.
$$

<br>

**Property / method used.** *Gaussian elimination with back-substitution:* elementary row operations (row replacement and row swapping) transform the augmented matrix $[A \mid b]$ into an equivalent upper triangular system with three nonzero pivots, guaranteeing a unique solution.

<br>

**Mathematical verification.** Substitute $(x, y, z) = (1, 2, 3)$ into all three original equations to verify consistency:
- **Equation 1:** $1 + 2 + 3 = 6$ (matches $6$).
- **Equation 2:** $2(1) - 2 + 3 = 2 - 2 + 3 = 3$ (matches $3$).
- **Equation 3:** $1 + 2(2) - 3 = 1 + 4 - 3 = 2$ (matches $2$).

All three equations hold identically.
