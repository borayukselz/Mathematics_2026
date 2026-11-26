### Exercise 11. Decomposition into Parallel and Perpendicular Components

#### Exercise Reminder

Decompose $u = (3, 4)$ into components parallel and perpendicular to $v = (1, 2)$. Check

$$
u = u_\parallel + u_\perp, \qquad u_\perp \cdot v = 0.
$$

Explain why these are two independent checks of correctness.

---

#### Solution

**Result.**
- **Parallel component (orthogonal projection onto $v$):** $u_\parallel = \left(\frac{11}{5}, \frac{22}{5}\right)$
- **Perpendicular (orthogonal) component:** $u_\perp = \left(\frac{4}{5}, -\frac{2}{5}\right)$
- **Orthogonal decomposition:**

$$
u = u_\parallel + u_\perp = \left(\frac{11}{5}, \frac{22}{5}\right) + \left(\frac{4}{5}, -\frac{2}{5}\right) = (3, 4).
$$

<br>

**Main steps.**

1. **Compute the dot products $u \cdot v$ and $v \cdot v$ for $u = (3, 4)$ and $v = (1, 2)$:**

$$
u \cdot v = (3, 4) \cdot (1, 2) = (3)(1) + (4)(2) = 3 + 8 = 11,
$$

$$
v \cdot v = |v|^2 = (1, 2) \cdot (1, 2) = 1^2 + 2^2 = 5.
$$

2. **Compute the parallel component $u_\parallel = \mathrm{proj}_v u$:**

$$
u_\parallel = \frac{u \cdot v}{v \cdot v}v = \frac{11}{5}(1, 2) = \left(\frac{11}{5}, \frac{22}{5}\right).
$$

3. **Compute the perpendicular component $u_\perp = u - u_\parallel$:**

$$
u_\perp = u - u_\parallel = (3, 4) - \left(\frac{11}{5}, \frac{22}{5}\right) = \left(\frac{15}{5} - \frac{11}{5}, \ \frac{20}{5} - \frac{22}{5}\right) = \left(\frac{4}{5}, -\frac{2}{5}\right).
$$

4. **Check both conditions $u = u_\parallel + u_\perp$ and $u_\perp \cdot v = 0$:**
   - **Sum check:**

$$
u_\parallel + u_\perp = \left(\frac{11}{5}, \frac{22}{5}\right) + \left(\frac{4}{5}, -\frac{2}{5}\right) = \left(\frac{15}{5}, \frac{20}{5}\right) = (3, 4) = u.
$$

   - **Orthogonality check:**

$$
u_\perp \cdot v = \left(\frac{4}{5}, -\frac{2}{5}\right) \cdot (1, 2) = \left(\frac{4}{5}\right)(1) + \left(-\frac{2}{5}\right)(2) = \frac{4}{5} - \frac{4}{5} = 0.
$$

5. **Explain why these are two independent checks of correctness:**
   - **Neither condition implies the other:**
     - Infinitely many pairs $(w_1, w_2)$ satisfy $w_1 + w_2 = u$ (for example, $w_1 = (1, 2)$ and $w_2 = (2, 2)$ sum to $(3, 4)$, yet $w_2 \cdot v = 6 \neq 0$ because $w_2$ is not perpendicular to $v$). Thus, $u_\parallel + u_\perp = u$ verifies **completeness** (no part of $u$ was lost or mis-added) without testing direction.
     - Conversely, infinitely many vectors $w_2$ satisfy $w_2 \cdot v = 0$ (any scalar multiple of $(2, -1)$ is perpendicular to $v$, even if its scale is wrong so that $u - w_2$ does not reconstruct $u$). Thus, $u_\perp \cdot v = 0$ verifies **perpendicularity** without testing magnitude.
   - **Together they guarantee uniqueness:** Together with $u_\parallel \in \mathrm{span}(v)$, satisfying both $u = u_\parallel + u_\perp$ and $u_\perp \cdot v = 0$ pins down the **unique** orthogonal decomposition of $u$ along and perpendicular to $v$.

<br>

**Property / method used.** **Orthogonal projection and direct-sum decomposition in $\mathbb{R}^2$:** $\mathbb{R}^2 = \mathrm{span}(v) \oplus \mathrm{span}(v)^\perp$, so every vector $u \in \mathbb{R}^2$ splits uniquely into a parallel part $u_\parallel = \frac{u \cdot v}{|v|^2}v$ and an orthogonal part $u_\perp = u - u_\parallel$ satisfying $u_\perp \perp v$.

<br>

**Mathematical verification.** Checking the Pythagorean norm identity $|u|^2 = |u_\parallel|^2 + |u_\perp|^2$ confirms the right-triangle geometry of the two components:

$$
|u_\parallel|^2 + |u_\perp|^2 = \left(\left(\frac{11}{5}\right)^2 + \left(\frac{22}{5}\right)^2\right) + \left(\left(\frac{4}{5}\right)^2 + \left(-\frac{2}{5}\right)^2\right) = \frac{121 + 484}{25} + \frac{16 + 4}{25} = \frac{625}{25} = 25 = 3^2 + 4^2 = |u|^2.
$$
