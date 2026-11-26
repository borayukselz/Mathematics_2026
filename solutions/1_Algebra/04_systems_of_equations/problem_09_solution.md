### Exercise 9. A System from a Sum Condition

#### Exercise Reminder

Find numbers $x, y$ satisfying

$$
x + y = 10, \qquad 2x + 5y = 32.
$$

Solve the system and explain geometrically why the solution is unique.

---

#### Solution

**Result.** The unique pair of numbers satisfying both conditions is

$$
(x, y) = (6, 4).
$$

Geometrically, the two equations represent two non-parallel lines in the $xy$-plane with different slopes ($-1$ and $-\frac{2}{5}$), which therefore intersect at a single unique point $(6, 4)$.

<br>

**Main steps.**

1. **Form the augmented matrix $[A \mid b]$ and eliminate $x$ from row $2$ via $R_2 \leftarrow R_2 - 2R_1$:**

$$
[A \mid b] =
\left(
\begin{array}{cc|c}
1 & 1 & 10 \\
2 & 5 & 32
\end{array}
\right)
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\left(
\begin{array}{cc|c}
1 & 1 & 10 \\
0 & 3 & 12
\end{array}
\right).
$$

2. **Solve by back-substitution:**
   - From row $2$, $3y = 12 \implies y = 4$.
   - Substitute $y = 4$ into row $1$, $x + y = 10$:

$$
x + 4 = 10 \implies x = 6.
$$

   - Hence $(x, y) = (6, 4)$.

3. **Geometric explanation of uniqueness:**
   - Rewriting each linear equation in slope-intercept form ($y = mx + c$) gives two lines in $\mathbb{R}^2$:

$$
L_1 : y = -x + 10 \quad (\text{slope } m_1 = -1), \qquad L_2 : y = -\frac{2}{5}x + \frac{32}{5} \quad (\text{slope } m_2 = -\frac{2}{5}).
$$

   - Because $m_1 = -1 \neq -\frac{2}{5} = m_2$, the two lines have distinct slopes and are neither parallel nor coincident. In the Euclidean plane $\mathbb{R}^2$, two non-parallel lines intersect in **exactly one point**, which is $(6, 4)$. (Algebraically, the normal vectors $(1, 1)$ and $(2, 5)$ are linearly independent, so $\det A = 1\cdot 5 - 1\cdot 2 = 3 \neq 0$.)

<br>

**Property / method used.** *Gaussian elimination and geometric intersection of lines in $\mathbb{R}^2$:* a $2\times 2$ linear system has a unique solution if and only if the two lines have distinct slopes (equivalently, $\det A \neq 0$).

<br>

**Mathematical verification.** Substituting $x = 6$ and $y = 4$ into both original equations confirms both conditions:
- **First condition:** $6 + 4 = 10$.
- **Second condition:** $2(6) + 5(4) = 12 + 20 = 32$.
