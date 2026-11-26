### Exercise 8. Linear Combination and Checking the Result

#### Exercise Reminder

Check whether $w = (5, 1)$ can be written as

$$
w = au + bv,
$$

where $u = (1, 1)$ and $v = (2, -1)$. If so, find $a, b$, reconstruct $w$ from them, and explain the geometric meaning of the existence of such coefficients.

---

#### Solution

**Result.** **Yes**, $w = (5, 1)$ can be written uniquely as a linear combination of $u = (1, 1)$ and $v = (2, -1)$ with coefficients

$$
a = \frac{7}{3}, \qquad b = \frac{4}{3},
$$

giving the explicit reconstruction

$$
w = \frac{7}{3}u + \frac{4}{3}v = \frac{7}{3}(1, 1) + \frac{4}{3}(2, -1) = (5, 1).
$$

<br>

**Main steps.**

1. **Set up the vector equation $au + bv = w$ as a $2\times 2$ linear system:**

$$
a(1, 1) + b(2, -1) = (5, 1) \implies (a + 2b, \ a - b) = (5, 1),
$$

   which yields the linear system

$$
\begin{cases}
a + 2b = 5, \\
a - b = 1.
\end{cases}
$$

2. **Solve the system for $a$ and $b$ by elimination:** Form the augmented matrix and eliminate $a$ from row $2$ via $R_2 \leftarrow R_2 - R_1$:

$$
\left(
\begin{array}{cc|c}
1 & 2 & 5 \\
1 & -1 & 1
\end{array}
\right)
\xrightarrow{R_2 \leftarrow R_2 - R_1}
\left(
\begin{array}{cc|c}
1 & 2 & 5 \\
0 & -3 & -4
\end{array}
\right).
$$

   - From row $2$: $-3b = -4 \implies b = \frac{4}{3}$.
   - From row $1$: $a + 2\left(\frac{4}{3}\right) = 5 \implies a = 5 - \frac{8}{3} = \frac{7}{3}$.
   - Since the system is consistent with a unique solution, $w$ can indeed be expressed as $au + bv$ with $a = \frac{7}{3}$ and $b = \frac{4}{3}$.

3. **Reconstruct $w$ from $a = \frac{7}{3}$ and $b = \frac{4}{3}$:**

$$
\frac{7}{3}u + \frac{4}{3}v = \frac{7}{3}(1, 1) + \frac{4}{3}(2, -1) = \left(\frac{7}{3}, \frac{7}{3}\right) + \left(\frac{8}{3}, -\frac{4}{3}\right) = \left(\frac{15}{3}, \frac{3}{3}\right) = (5, 1) = w.
$$

4. **Explain the geometric meaning of the existence of $a$ and $b$:**
   - **Reachability / spanning the plane:** The vectors $u = (1, 1)$ and $v = (2, -1)$ are non-collinear (not scalar multiples of one another), so they define two distinct, independent directions in $\mathbb{R}^2$ that span the entire $xy$-plane ($\mathrm{span}(u, v) = \mathbb{R}^2$).
   - **Parallelogram tip-to-tail path:** The existence of $a = \frac{7}{3}$ and $b = \frac{4}{3}$ means that starting from the origin $(0, 0)$, one can reach the target point $(5, 1)$ by moving $\frac{7}{3}$ units along the direction of $u$ and then $\frac{4}{3}$ units along the direction of $v$—equivalently, $w$ is the main diagonal of the parallelogram formed by the scaled vectors $\frac{7}{3}u$ and $\frac{4}{3}v$, and $(a, b) = \left(\frac{7}{3}, \frac{4}{3}\right)$ are the coordinates of $w$ in the skewed basis $(u, v)$.

<br>

**Property / method used.** *Linear combinations and basis coordinates in $\mathbb{R}^2$:* solving the matrix-vector equation

$$
\begin{pmatrix}
1 & 2 \\
1 & -1
\end{pmatrix}
\begin{pmatrix}
a \\
b
\end{pmatrix} =
\begin{pmatrix}
5 \\
1
\end{pmatrix}
$$

expresses $w$ in the coordinate system spanned by $(u, v)$; because its coefficient matrix determinant is nonzero,

$$
\det
\begin{pmatrix}
1 & 2 \\
1 & -1
\end{pmatrix} = -3 \neq 0,
$$

the pair $(u, v)$ forms a basis of $\mathbb{R}^2$, guaranteeing unique coordinates $(a, b)$ for every $w \in \mathbb{R}^2$.

<br>

**Mathematical verification.** Substituting $a = \frac{7}{3}$ and $b = \frac{4}{3}$ back into both component equations confirms exact equality:
- **First coordinate ($x$-component):** $\frac{7}{3}(1) + \frac{4}{3}(2) = \frac{7 + 8}{3} = \frac{15}{3} = 5$.
- **Second coordinate ($y$-component):** $\frac{7}{3}(1) + \frac{4}{3}(-1) = \frac{7 - 4}{3} = \frac{3}{3} = 1$.
