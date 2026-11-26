### Exercise 7. Linear Dependence Without Heavy Computation

#### Exercise Reminder

Given

$$
u = (1, 2, 3), \qquad v = (2, 4, 6), \qquad w = (0, 1, 1).
$$

Identify a specific relation between $u$ and $v$, decide whether the three vectors can be linearly independent, and explain why no long calculation is needed.

---

#### Solution

**Result.**
- **Specific relation between $u$ and $v$:** $v = 2u$ (or $2u - v = \mathbf{0}$), so $v$ is a scalar multiple of $u$ (collinear vectors).
- **Linear independence decision:** The three vectors $\{u, v, w\}$ are **linearly dependent** (they **cannot** be linearly independent).
- **Reason no long calculation is needed:** Because the subset $\{u, v\}$ is already linearly dependent ($2u - 1v + 0w = \mathbf{0}$ gives an immediate nontrivial linear combination equal to the zero vector), any superset $\{u, v, w\}$ containing it is automatically linearly dependent without setting up or row-reducing a $3\times 3$ system.

<br>

**Main steps.**

1. **Identify the scalar-multiple relation between $u = (1, 2, 3)$ and $v = (2, 4, 6)$:**
   - Comparing corresponding coordinates reveals that every component of $v$ is twice the corresponding component of $u$:

$$
2u = 2(1, 2, 3) = (2\cdot 1, \ 2\cdot 2, \ 2\cdot 3) = (2, 4, 6) = v.
$$

   - Rearranging gives $2u - v = \mathbf{0}$, showing that $u$ and $v$ are collinear (parallel) and form a linearly dependent pair.

2. **Decide whether $\{u, v, w\}$ can be linearly independent:**
   - By definition, $\{u, v, w\}$ is linearly independent if and only if the vector equation $c_1u + c_2v + c_3w = \mathbf{0}$ has only the trivial solution $c_1 = c_2 = c_3 = 0$.
   - Using $v = 2u$ and assigning coefficient $c_3 = 0$ to $w$, we immediately obtain a **nontrivial** solution $(c_1, c_2, c_3) = (2, -1, 0) \neq (0, 0, 0)$:

$$
2u - 1v + 0w = 2(1, 2, 3) - (2, 4, 6) + (0, 0, 0) = (0, 0, 0) = \mathbf{0}.
$$

   - Therefore, $\{u, v, w\}$ **cannot be linearly independent**; the three vectors are **linearly dependent**.

3. **Explain why no long calculation is needed:**
   - **Algebraic subset principle:** Whenever a subset of vectors is linearly dependent (here $\{u, v\}$), adding more vectors (here $w$) can never make the enlarged set linearly independent—one simply sets the coefficients of all newly added vectors to $0$ in the existing nontrivial zero-sum relation. Hence, solving a $3\times 3$ linear system or computing a $3\times 3$ determinant is completely unnecessary.
   - **Geometric intuition:** Because $v = 2u$ lies on the exact same line through the origin as $u$, the three vectors $\{u, v, w\}$ span at most the $2$-dimensional plane $\mathrm{span}\{u, w\}$ in $\mathbb{R}^3$ rather than a $3$-dimensional volume.

<br>

**Property / method used.** *Superset property of linear dependence:* if a subset $S_1 \subseteq S_2$ is linearly dependent, then $S_2$ is necessarily linearly dependent; in particular, if one vector in a set is a scalar multiple of another, the entire set is linearly dependent regardless of the remaining vectors.

<br>

**Mathematical verification.** Checking the linear combination $2u - v + 0w$ componentwise and evaluating the $3\times 3$ determinant confirm linear dependence:

$$
2(1, 2, 3) - (2, 4, 6) + 0(0, 1, 1) = (2 - 2 + 0, \ 4 - 4 + 0, \ 6 - 6 + 0) = (0, 0, 0),
$$

$$
\det
\begin{pmatrix}
1 & 2 & 0 \\
2 & 4 & 1 \\
3 & 6 & 1
\end{pmatrix} = 0 \quad (\text{since column } 2 = 2 \times \text{column } 1).
$$
