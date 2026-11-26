### Exercise 9. Cross Product as a Perpendicular Direction

#### Exercise Reminder

For $u = (1, 2, 0)$ and $v = (0, 1, 3)$ compute $u \times v$. Use dot products to check perpendicularity to both vectors, compute $v \times u$, and compare the results.

---

#### Solution

**Result.**
- **Cross product $u \times v$:** $u \times v = (6, -3, 1)$
- **Reversed cross product $v \times u$:** $v \times u = (-6, 3, -1)$
- **Comparison:** $v \times u = -(u \times v)$ — both cross products have the exact same magnitude $\sqrt{46}$ and lie along the same line perpendicular to both $u$ and $v$, but point in **opposite orientations** (anti-commutativity).

<br>

**Main steps.**

1. **Compute $u \times v$ for $u = (1, 2, 0)$ and $v = (0, 1, 3)$ using the $3\times 3$ determinant expansion:**

$$
u \times v =
\det
\begin{pmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
1 & 2 & 0 \\
0 & 1 & 3
\end{pmatrix} =
\begin{vmatrix}
2 & 0 \\
1 & 3
\end{vmatrix}\mathbf{i} -
\begin{vmatrix}
1 & 0 \\
0 & 3
\end{vmatrix}\mathbf{j} +
\begin{vmatrix}
1 & 2 \\
0 & 1
\end{vmatrix}\mathbf{k}
$$

$$
u \times v = (2\cdot 3 - 0\cdot 1)\mathbf{i} - (1\cdot 3 - 0\cdot 0)\mathbf{j} + (1\cdot 1 - 2\cdot 0)\mathbf{k} = 6\mathbf{i} - 3\mathbf{j} + 1\mathbf{k} = (6, -3, 1).
$$

2. **Check perpendicularity of $u \times v$ to both $u$ and $v$ via dot products:**

$$
(u \times v) \cdot u = (6, -3, 1) \cdot (1, 2, 0) = (6)(1) + (-3)(2) + (1)(0) = 6 - 6 + 0 = 0,
$$

$$
(u \times v) \cdot v = (6, -3, 1) \cdot (0, 1, 3) = (6)(0) + (-3)(1) + (1)(3) = 0 - 3 + 3 = 0.
$$

   - Because both dot products equal $0$, $u \times v$ is simultaneously perpendicular to both $u$ and $v$ (and therefore normal to the plane spanned by $u$ and $v$).

3. **Compute $v \times u$ by swapping the two vector rows:**

$$
v \times u =
\det
\begin{pmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
0 & 1 & 3 \\
1 & 2 & 0
\end{pmatrix} =
\begin{vmatrix}
1 & 3 \\
2 & 0
\end{vmatrix}\mathbf{i} -
\begin{vmatrix}
0 & 3 \\
1 & 0
\end{vmatrix}\mathbf{j} +
\begin{vmatrix}
0 & 1 \\
1 & 2
\end{vmatrix}\mathbf{k}
$$

$$
v \times u = (1\cdot 0 - 3\cdot 2)\mathbf{i} - (0\cdot 0 - 3\cdot 1)\mathbf{j} + (0\cdot 2 - 1\cdot 1)\mathbf{k} = -6\mathbf{i} + 3\mathbf{j} - 1\mathbf{k} = (-6, 3, -1).
$$

4. **Compare $u \times v$ and $v \times u$:**
   - **Algebraically:** Every component of $v \times u = (-6, 3, -1)$ is the exact negative of the corresponding component of $u \times v = (6, -3, 1)$, confirming the anti-commutative law $v \times u = -(u \times v)$.
   - **Geometrically:** Both vectors share the same length $|u \times v| = |v \times u| = \sqrt{6^2 + (-3)^2 + 1^2} = \sqrt{46}$ (equal to the area of the parallelogram spanned by $u$ and $v$) and both are perpendicular to $\mathrm{span}(u, v)$, while their directions are reversed according to the **right-hand rule** when curling fingers from $v$ to $u$ instead of from $u$ to $v$.

<br>

**Property / method used.** *Cross product orthogonality and anti-commutativity in $\mathbb{R}^3$:* $(u \times v) \cdot u = 0$, $(u \times v) \cdot v = 0$, and swapping two rows in the determinant definition negates the result ($v \times u = -(u \times v)$).

<br>

**Mathematical verification.** Checking Lagrange's norm identity $|u \times v|^2 = |u|^2|v|^2 - (u \cdot v)^2$ confirms the magnitude and components of the cross product:

$$
|u|^2 = 1^2 + 2^2 + 0^2 = 5, \qquad |v|^2 = 0^2 + 1^2 + 3^2 = 10, \qquad u \cdot v = (1)(0) + (2)(1) + (0)(3) = 2,
$$

$$
|u|^2|v|^2 - (u \cdot v)^2 = (5)(10) - 2^2 = 50 - 4 = 46 = 6^2 + (-3)^2 + 1^2 = |u \times v|^2.
$$
