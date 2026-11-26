### Exercise 6. Projection and Perpendicular Component

#### Exercise Reminder

Find the projection of $u = (4, 2)$ onto the direction $v = (1, 1)$. Then compute

$$
r = u - \mathrm{proj}_v u
$$

and verify that $r \cdot v = 0$. Explain this result geometrically.

---

#### Solution

**Result.**
- **Orthogonal projection of $u$ onto $v$:** $\mathrm{proj}_v u = (3, 3)$
- **Perpendicular (residual) component:** $r = u - \mathrm{proj}_v u = (1, -1)$
- **Orthogonality check:** $r \cdot v = 0$

<br>

**Main steps.**

1. **Compute the dot products $u \cdot v$ and $v \cdot v$ needed for the projection formula:**

$$
u \cdot v = (4, 2) \cdot (1, 1) = (4)(1) + (2)(1) = 4 + 2 = 6,
$$

$$
v \cdot v = |v|^2 = (1, 1) \cdot (1, 1) = 1^2 + 1^2 = 2.
$$

2. **Find the orthogonal projection $\mathrm{proj}_v u$ of $u = (4, 2)$ onto $v = (1, 1)$:**

$$
\mathrm{proj}_v u = \frac{u \cdot v}{v \cdot v}v = \frac{6}{2}(1, 1) = 3(1, 1) = (3, 3).
$$

3. **Compute the perpendicular component $r = u - \mathrm{proj}_v u$:**

$$
r = u - \mathrm{proj}_v u = (4, 2) - (3, 3) = (4 - 3, \ 2 - 3) = (1, -1).
$$

4. **Verify that $r \cdot v = 0$:**

$$
r \cdot v = (1, -1) \cdot (1, 1) = (1)(1) + (-1)(1) = 1 - 1 = 0.
$$

5. **Explain the result geometrically:**
   - The vector $\mathrm{proj}_v u = (3, 3)$ is the **orthogonal shadow** cast by $u = (4, 2)$ onto the line $L = \mathrm{span}\{v\}$ ($y = x$) when dropping a perpendicular line from the tip of $u$ to $L$.
   - The residual vector $r = u - \mathrm{proj}_v u = (1, -1)$ is the **shortest displacement vector** connecting the line $\mathrm{span}\{v\}$ to the tip of $u$; in Euclidean geometry, the shortest segment from a point to a line meets that line at a **right angle ($90^\circ$)**, which is why $r \perp v$ ($r \cdot v = 0$).
   - Consequently, $u$ decomposes uniquely into two mutually perpendicular vectors $u = \mathrm{proj}_v u + r = (3, 3) + (1, -1)$ forming a right triangle with hypotenuse $u$.

<br>

**Property / method used.** *Orthogonal decomposition in $\mathbb{R}^2$:* every vector $u \in \mathbb{R}^2$ splits uniquely as $u = u_\parallel + u_\perp$, where $u_\parallel = \mathrm{proj}_v u = \frac{u \cdot v}{|v|^2}v \in \mathrm{span}\{v\}$ is parallel to $v$ and $u_\perp = r = u - \mathrm{proj}_v u$ satisfies $u_\perp \cdot v = 0$.

<br>

**Mathematical verification.** Checking both the vector sum reconstruction $u = \mathrm{proj}_v u + r$ and the Pythagorean norm identity $|u|^2 = |\mathrm{proj}_v u|^2 + |r|^2$ confirms the decomposition:

$$
\mathrm{proj}_v u + r = (3, 3) + (1, -1) = (4, 2) = u,
$$

$$
|\mathrm{proj}_v u|^2 + |r|^2 = (3^2 + 3^2) + (1^2 + (-1)^2) = 18 + 2 = 20 = 4^2 + 2^2 = |u|^2.
$$
```[cite: 9]
