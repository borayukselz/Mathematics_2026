### Exercise 14. Closest Point on a Line

#### Exercise Reminder

Given a point $P = (4, 1)$ and a line through the origin with direction $v = (1, 2)$. Using projection, find the closest point on the line, the distance from $P$ to the line, and verify that the appropriate vector is perpendicular to the direction of the line.

---

#### Solution

**Result.**
- **Closest point on the line $L = \mathrm{span}(v)$:** $Q = \left(\frac{6}{5}, \frac{12}{5}\right)$
- **Minimum distance from $P$ to the line:** $d(P, L) = |\overrightarrow{QP}| = \frac{7}{\sqrt{5}} = \frac{7\sqrt{5}}{5}$
- **Perpendicularity check:** $\overrightarrow{QP} \cdot v = 0$, where $\overrightarrow{QP} = P - Q = \left(\frac{14}{5}, -\frac{7}{5}\right)$

<br>

**Main steps.**

1. **Represent $P = (4, 1)$ as the position vector $p = \overrightarrow{OP} = (4, 1)$ and compute the dot products $p \cdot v$ and $v \cdot v$:**

$$
p \cdot v = (4, 1) \cdot (1, 2) = (4)(1) + (1)(2) = 4 + 2 = 6,
$$

$$
v \cdot v = |v|^2 = (1, 2) \cdot (1, 2) = 1^2 + 2^2 = 5.
$$

2. **Find the closest point $Q$ on the line through the origin by projecting $p$ onto $v$:**
   - Because the line $L = \{tv : t \in \mathbb{R}\}$ passes through the origin, the position vector $q = \overrightarrow{OQ}$ of the point $Q \in L$ closest to $P$ is the orthogonal projection $\mathrm{proj}_v p$:

$$
q = \mathrm{proj}_v p = \frac{p \cdot v}{v \cdot v}v = \frac{6}{5}(1, 2) = \left(\frac{6}{5}, \frac{12}{5}\right).
$$

   - Hence the closest point on the line is $Q = \left(\frac{6}{5}, \frac{12}{5}\right)$.

3. **Compute the error (residual) vector $\overrightarrow{QP} = p - q$ and find the distance from $P$ to the line:**

$$
\overrightarrow{QP} = p - q = (4, 1) - \left(\frac{6}{5}, \frac{12}{5}\right) = \left(\frac{20}{5} - \frac{6}{5}, \ \frac{5}{5} - \frac{12}{5}\right) = \left(\frac{14}{5}, -\frac{7}{5}\right).
$$

   - The Euclidean distance from $P$ to the line $L$ is the length of the perpendicular segment $\overrightarrow{QP}$:

$$
d(P, L) = |\overrightarrow{QP}| = \sqrt{\left(\frac{14}{5}\right)^2 + \left(-\frac{7}{5}\right)^2} = \sqrt{\frac{196 + 49}{25}} = \sqrt{\frac{245}{25}} = \sqrt{\frac{49}{5}} = \frac{7}{\sqrt{5}} = \frac{7\sqrt{5}}{5}.
$$

4. **Verify that the residual vector $\overrightarrow{QP}$ is perpendicular to the line's direction $v = (1, 2)$:**

$$
\overrightarrow{QP} \cdot v = \left(\frac{14}{5}, -\frac{7}{5}\right) \cdot (1, 2) = \left(\frac{14}{5}\right)(1) + \left(-\frac{7}{5}\right)(2) = \frac{14}{5} - \frac{14}{5} = 0.
$$

<br>

**Property / method used.** **Best-approximation theorem for orthogonal projection in $\mathbb{R}^2$:** for a line $L = \mathrm{span}(v)$ through the origin and any point $P$ with position vector $p$, $q = \mathrm{proj}_v p = \frac{p \cdot v}{|v|^2}v$ is the unique point on $L$ minimizing $|p - x|$ over all $x \in L$, characterized by $(p - q) \perp v$.

<br>

**Mathematical verification.** Checking both that $Q = \left(\frac{6}{5}, \frac{12}{5}\right)$ lies on the line $y = 2x$ (i.e., $Q = \frac{6}{5}v$) and that the $2\text{D}$ point-to-line distance formula for $2x - y = 0$ gives the same distance confirms the result:

$$
\frac{12}{5} = 2\left(\frac{6}{5}\right) \implies Q \in L,
$$

$$
d(P, L) = \frac{|2(4) - 1(1)|}{\sqrt{2^2 + (-1)^2}} = \frac{|8 - 1|}{\sqrt{5}} = \frac{7}{\sqrt{5}} = \frac{7\sqrt{5}}{5}.
$$
