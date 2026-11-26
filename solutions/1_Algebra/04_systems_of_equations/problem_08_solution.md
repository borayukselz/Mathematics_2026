### Exercise 8. Two Systems with the Same Coefficient Matrix

#### Exercise Reminder

Solve by elimination the two systems

$$
\begin{cases}
2x + y = 5, \\
x - y = 1,
\end{cases}
$$

$$
\begin{cases}
2x + y = 1, \\
x - y = 4.
\end{cases}
$$

Compare the successive elimination steps. Which part of the calculation is the same in both cases, and why?

---

#### Solution

**Result.**
- **System 1** has the unique solution $(x, y) = (2, 1)$.
- **System 2** has the unique solution $(x, y) = \left(\frac{5}{3}, -\frac{7}{3}\right)$.
- **Comparison:** The **choice and sequence of elementary row operations** ($R_1 \leftrightarrow R_2$, followed by $R_2 \leftarrow R_2 - 2R_1$) and the entire **left-hand coefficient block** in every step are identical in both cases because both systems share the exact same coefficient matrix $A$.

<br>

**Main steps.**

1. **Solve System 1 by elimination:** Form the augmented matrix $[A \mid b_1]$, swap rows $R_1 \leftrightarrow R_2$ to get a unit pivot in $(1,1)$, and eliminate $x$ from row $2$ via $R_2 \leftarrow R_2 - 2R_1$:

$$
[A \mid b_1] =
\left(
\begin{array}{cc|c}
2 & 1 & 5 \\
1 & -1 & 1
\end{array}
\right)
\xrightarrow{R_1 \leftrightarrow R_2}
\left(
\begin{array}{cc|c}
1 & -1 & 1 \\
2 & 1 & 5
\end{array}
\right)
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\left(
\begin{array}{cc|c}
1 & -1 & 1 \\
0 & 3 & 3
\end{array}
\right).
$$

   - **Back-substitution for System 1:**
     - From row $2$, $3y = 3 \implies y = 1$.
     - From row $1$, $x - y = 1 \implies x - 1 = 1 \implies x = 2$.
     - Thus $(x, y) = (2, 1)$.

2. **Solve System 2 by elimination:** Form the augmented matrix $[A \mid b_2]$ and apply the exact same sequence of row operations ($R_1 \leftrightarrow R_2$, then $R_2 \leftarrow R_2 - 2R_1$):

$$
[A \mid b_2] =
\left(
\begin{array}{cc|c}
2 & 1 & 1 \\
1 & -1 & 4
\end{array}
\right)
\xrightarrow{R_1 \leftrightarrow R_2}
\left(
\begin{array}{cc|c}
1 & -1 & 4 \\
2 & 1 & 1
\end{array}
\right)
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\left(
\begin{array}{cc|c}
1 & -1 & 4 \\
0 & 3 & -7
\end{array}
\right).
$$

   - **Back-substitution for System 2:**
     - From row $2$, $3y = -7 \implies y = -\frac{7}{3}$.
     - From row $1$, $x - y = 4 \implies x - \left(-\frac{7}{3}\right) = 4 \implies x = 4 - \frac{7}{3} = \frac{5}{3}$.
     - Thus $(x, y) = \left(\frac{5}{3}, -\frac{7}{3}\right)$.

3. **Compare the elimination steps and explain what stays the same:**
   - **What is identical:** In both reductions, the row operations ($R_1 \leftrightarrow R_2$ and $R_2 \leftarrow R_2 - 2R_1$), the pivot positions, and the left-hand side coefficient matrices at every stage are completely identical:

$$
\begin{pmatrix}
2 & 1 \\
1 & -1
\end{pmatrix}
\longrightarrow
\begin{pmatrix}
1 & -1 \\
2 & 1
\end{pmatrix}
\longrightarrow
\begin{pmatrix}
1 & -1 \\
0 & 3
\end{pmatrix}.
$$

     Only the right-hand augmented column changes.
   - **Why:** Elementary row operations are determined solely by the entries of the coefficient matrix $A$ (specifically, eliminating sub-pivot entries in $A$), independently of the right-hand side vector $b$. Consequently, both systems could even be reduced simultaneously in a single doubly augmented matrix $[A \mid b_1 \ \ b_2]$.

<br>

**Property / method used.** *Independence of forward elimination from the right-hand side:* elementary row operations act on a linear system via left-multiplication by an invertible elimination matrix $E$, transforming $[A \mid b]$ into $[EA \mid Eb]$; when two systems share $A$, the exact same elimination matrix $E$ reduces both coefficient blocks to the same echelon form $U = EA$.

<br>

**Mathematical verification.** Substituting each solution back into its original equations confirms consistency:
- **System 1** with $(x, y) = (2, 1)$: $2(2) + 1 = 5$ and $2 - 1 = 1$.
- **System 2** with $(x, y) = \left(\frac{5}{3}, -\frac{7}{3}\right)$: $2\left(\frac{5}{3}\right) + \left(-\frac{7}{3}\right) = \frac{10 - 7}{3} = 1$ and $\frac{5}{3} - \left(-\frac{7}{3}\right) = \frac{12}{3} = 4$.
