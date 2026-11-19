### Exercise 11. Parameter and Invertibility

#### Exercise Reminder

For

$$
A(t) =
\begin{pmatrix}
1 & t \\
t & 1
\end{pmatrix}
$$

find all $t$ for which the matrix is invertible, and then give a formula for $A(t)^{-1}$. Explain what happens to this formula at the excluded values.

---

#### Solution

**Result.** The matrix $A(t)$ is invertible for all $t \neq 1$ and $t \neq -1$ (that is, $t \in \mathbb{R} \setminus \{-1, 1\}$). For every such $t$, its inverse is

$$
A(t)^{-1} = \frac{1}{1 - t^2}
\begin{pmatrix}
1 & -t \\
-t & 1
\end{pmatrix} =
\begin{pmatrix}
\frac{1}{1 - t^2} & -\frac{t}{1 - t^2} \\
-\frac{t}{1 - t^2} & \frac{1}{1 - t^2}
\end{pmatrix}.
$$

At the excluded values $t = 1$ and $t = -1$, the denominator $1 - t^2$ becomes $0$, so the formula requires division by zero and is undefined.

<br>

**Main steps.**

1. **Find all $t$ for which $A(t)$ is invertible:** A $2\times 2$ matrix is invertible if and only if its determinant is nonzero:

$$
\det A(t) = (1)(1) - (t)(t) = 1 - t^2 = (1 - t)(1 + t).
$$

Setting $\det A(t) = 0$ gives $1 - t^2 = 0 \implies t^2 = 1 \implies t = 1$ or $t = -1$. Hence $A(t)$ is invertible if and only if $t \neq \pm 1$.

2. **Compute the formula for $A(t)^{-1}$:** For $t \neq \pm 1$, apply the $2\times 2$ inverse formula by swapping the diagonal entries, negating the off-diagonal entries, and dividing by $\det A(t) = 1 - t^2$:

$$
A(t)^{-1} = \frac{1}{\det A(t)}
\begin{pmatrix}
1 & -t \\
-t & 1
\end{pmatrix} = \frac{1}{1 - t^2}
\begin{pmatrix}
1 & -t \\
-t & 1
\end{pmatrix}.
$$

3. **Behavior at the excluded values $t = 1$ and $t = -1$:**
   - Algebraically, substituting $t = 1$ or $t = -1$ into $\frac{1}{1 - t^2}$ produces $\frac{1}{0}$, which is undefined (each entry diverges as $t \to \pm 1$).
   - Structurally, at $t = 1$ the matrix becomes

$$
A(1) =
\begin{pmatrix}
1 & 1 \\
1 & 1
\end{pmatrix},
$$

whose rows are identical ($R_1 = R_2$), and at $t = -1$ the matrix becomes

$$
A(-1) =
\begin{pmatrix}
1 & -1 \\
-1 & 1
\end{pmatrix},
$$

whose rows are negatives of each other ($R_1 = -R_2$). In both cases the rows are linearly dependent and $\mathrm{rank}(A(\pm 1)) = 1 < 2$, confirming that no inverse matrix exists.

<br>

**Property / method used.** *Determinant invertibility criterion and $2\times 2$ inverse formula:* a $2\times 2$ matrix $M$ is invertible if and only if $\det M \neq 0$, and the prefactor $\frac{1}{\det M}$ in the inverse formula blows up precisely when $\det M = 0$.

<br>

**Mathematical verification.** For any $t \neq \pm 1$, multiplying $A(t)$ by the formula for $A(t)^{-1}$ yields the $2\times 2$ identity matrix $I$:

$$
A(t)A(t)^{-1} =
\begin{pmatrix}
1 & t \\
t & 1
\end{pmatrix}
\cdot \frac{1}{1 - t^2}
\begin{pmatrix}
1 & -t \\
-t & 1
\end{pmatrix} = \frac{1}{1 - t^2}
\begin{pmatrix}
1 - t^2 & -t + t \\
t - t & -t^2 + 1
\end{pmatrix} = \frac{1}{1 - t^2}
\begin{pmatrix}
1 - t^2 & 0 \\
0 & 1 - t^2
\end{pmatrix} =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} = I.
$$
