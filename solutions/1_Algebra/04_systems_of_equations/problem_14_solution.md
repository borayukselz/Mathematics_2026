### Exercise 14. A Small Change in the Right-Hand Side

#### Exercise Reminder

Compare the systems

$$
\begin{cases}
x + y = 2, \\
2x - y = 1, \\
3x = 3
\end{cases}
$$

and

$$
\begin{cases}
x + y = 2, \\
2x - y = 1, \\
3x = 3.1.
\end{cases}
$$

Check the consistency of each system and explain why a small change in one number can change the type of the system.

---

#### Solution

**Result.**
- **System 1** (with $3x = 3$) is **consistent** and has the **unique solution** $(x, y) = (1, 1)$.
- **System 2** (with $3x = 3.1$) is **inconsistent** and has **no solution** (the solution set is $\emptyset$).
- **Why a small change changes the system type:** Both systems are **overdetermined** ($3$ equations in $2$ unknowns), where the third left-hand side is the exact sum of the first two left-hand sides ($3x = (x + y) + (2x - y)$). The first two equations already pin down a single intersection point $(x, y) = (1, 1)$, which forces $3x = 3$; perturbing the third constant from $3$ to $3.1$ breaks the linear compatibility condition $b_3 = b_1 + b_2$ and shifts the third line off the intersection point.

<br>

**Main steps.**

1. **Reduce System 1 via Gaussian elimination:** Form the augmented matrix $[A \mid b_1]$, eliminate $x$ from rows $2$ and $3$ via $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - 3R_1$, and then eliminate $y$ from row $3$ via $R_3 \leftarrow R_3 - R_2$:

$$
[A \mid b_1] =
\left(
\begin{array}{cc|c}
1 & 1 & 2 \\
2 & -1 & 1 \\
3 & 0 & 3
\end{array}
\right)
\xrightarrow{R_2 \leftarrow R_2 - 2R_1,\ R_3 \leftarrow R_3 - 3R_1}
\left(
\begin{array}{cc|c}
1 & 1 & 2 \\
0 & -3 & -3 \\
0 & -3 & -3
\end{array}
\right)
\xrightarrow{R_3 \leftarrow R_3 - R_2}
\left(
\begin{array}{cc|c}
1 & 1 & 2 \\
0 & -3 & -3 \\
0 & 0 & 0
\end{array}
\right).
$$

   - Row $3$ becomes $(0 \quad 0 \mid 0)$ ($0 = 0$), so System 1 is **consistent**.
   - Back-substitution gives $-3y = -3 \implies y = 1$ and $x + 1 = 2 \implies x = 1$, yielding the unique solution $(x, y) = (1, 1)$.

2. **Reduce System 2 via the exact same row operations:**

$$
[A \mid b_2] =
\left(
\begin{array}{cc|c}
1 & 1 & 2 \\
2 & -1 & 1 \\
3 & 0 & 3.1
\end{array}
\right)
\xrightarrow{R_2 \leftarrow R_2 - 2R_1,\ R_3 \leftarrow R_3 - 3R_1}
\left(
\begin{array}{cc|c}
1 & 1 & 2 \\
0 & -3 & -3 \\
0 & -3 & -2.9
\end{array}
\right)
\xrightarrow{R_3 \leftarrow R_3 - R_2}
\left(
\begin{array}{cc|c}
1 & 1 & 2 \\
0 & -3 & -3 \\
0 & 0 & 0.1
\end{array}
\right).
$$

   - Row $3$ becomes $(0 \quad 0 \mid 0.1)$, corresponding to the contradictory equation $0 = 0.1$. Thus System 2 is **inconsistent** and has **no solution**.

3. **Explain why an arbitrarily small change in $b_3$ changes the system type:**
   - **Algebraically (column space / compatibility condition):** In both systems, the coefficient matrix $A$ has $3$ rows and rank $2$, so its column space $\mathrm{Col}(A)$ is a $2$-dimensional plane inside $\mathbb{R}^3$ defined by the linear relation $b_3 = b_1 + b_2$ (since $\text{row}_3(A) = \text{row}_1(A) + \text{row}_2(A)$).
   - A vector $b = (b_1, b_2, b_3)^T \in \mathbb{R}^3$ lies in $\mathrm{Col}(A)$ if and only if $b_3 = b_1 + b_2$. For $b_1 = (2, 1, 3)^T$, we have $3 = 2 + 1$, so $b_1 \in \mathrm{Col}(A)$ and the system is consistent. Changing $b_3$ by even $\varepsilon = 0.1$ pushes $b_2 = (2, 1, 3.1)^T$ off that plane ($3.1 \neq 2 + 1$), immediately making $Ax = b_2$ inconsistent.
   - **Geometrically:** The first two lines $x + y = 2$ and $2x - y = 1$ intersect at the single point $(1, 1)$. In System 1, the third line $3x = 3$ ($x = 1$) passes directly through $(1, 1)$, so all three lines concur at one point. In System 2, changing $3$ to $3.1$ shifts the vertical line to $x = \frac{3.1}{3} = \frac{31}{30}$, which misses $(1, 1)$, leaving no point common to all three lines.

<br>

**Property / method used.** *Compatibility condition for overdetermined systems ($b \in \mathrm{Col}(A)$):* when the rows of $A$ satisfy a linear dependence ($\text{row}_3 = \text{row}_1 + \text{row}_2$), consistency requires the exact same dependence among the right-hand side entries ($b_3 = b_1 + b_2$), making consistency sensitive to any nonzero perturbation of $b_3$.

<br>

**Mathematical verification.** Adding the first two equations directly gives

$$
(x + y) + (2x - y) = 2 + 1 \implies 3x = 3.
$$

This matches the third equation $3x = 3$ of System 1 (confirming $(1, 1)$ satisfies all three equations), whereas in System 2 it yields $3 = 3.1$, confirming the contradiction $0 = 0.1$.
