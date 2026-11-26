### Exercise 5. Angle Between Vectors

#### Exercise Reminder

Given $u = (1, 1, 0)$ and $v = (1, 0, 1)$:

1. Use the sign of $u \cdot v$ to predict the type of angle.
2. Compute the angle.
3. Compare the result with the prediction.

---

#### Solution

**Result.**
- **Dot product and prediction:** $u \cdot v = 1 > 0$, predicting an **acute angle** ($0^\circ \le \theta < 90^\circ$).
- **Exact angle between $u$ and $v$:** $\theta = \frac{\pi}{3}\text{ rad}$ (or $60^\circ$).
- **Comparison:** The computed angle $\theta = 60^\circ$ lies strictly between $0^\circ$ and $90^\circ$, matching the acute-angle prediction.

<br>

**Main steps.**

1. **Compute $u \cdot v$ and predict the angle type from its sign:**

$$
u \cdot v = (1, 1, 0) \cdot (1, 0, 1) = (1)(1) + (1)(0) + (0)(1) = 1 + 0 + 0 = 1.
$$

   - Because $u \cdot v = |u||v|\cos\theta$ and both norms $|u|, |v|$ are strictly positive, $\cos\theta$ shares the exact sign of $u \cdot v$.
   - Since $u \cdot v = 1 > 0$, we have $\cos\theta > 0$, which predicts that the angle $\theta \in [0, \pi]$ between $u$ and $v$ is **acute** ($0^\circ \le \theta < 90^\circ$).

2. **Compute the Euclidean norms $|u|$ and $|v|$, then solve for $\theta$ via the cosine formula:**

$$
|u| = \sqrt{1^2 + 1^2 + 0^2} = \sqrt{2}, \qquad |v| = \sqrt{1^2 + 0^2 + 1^2} = \sqrt{2}.
$$

   Substitute $u \cdot v = 1$, $|u| = \sqrt{2}$, and $|v| = \sqrt{2}$ into $\cos\theta = \frac{u \cdot v}{|u||v|}$:

$$
\cos\theta = \frac{1}{\sqrt{2} \cdot \sqrt{2}} = \frac{1}{2}.
$$

   Taking the inverse cosine on $[0, \pi]$ gives

$$
\theta = \arccos\left(\frac{1}{2}\right) = \frac{\pi}{3}\text{ rad} = 60^\circ.
$$

3. **Compare the computed result with the qualitative prediction:**
   - The qualitative sign test predicted an **acute** angle ($0^\circ \le \theta < 90^\circ$).
   - The exact computation gives $\theta = 60^\circ$ ($\frac{\pi}{3}\text{ rad}$), which satisfies $0^\circ < 60^\circ < 90^\circ$ and therefore confirms the prediction.

<br>

**Property / method used.** *Geometric dot product formula in $\mathbb{R}^3$:* $u \cdot v = |u||v|\cos\theta$ for $\theta \in [0, \pi]$, where $\mathrm{sgn}(u \cdot v) = \mathrm{sgn}(\cos\theta)$ classifies $\theta$ as acute ($u \cdot v > 0$), right ($u \cdot v = 0$), or obtuse ($u \cdot v < 0$) before computing $\theta = \arccos\left(\frac{u \cdot v}{|u||v|}\right)$.

<br>

**Mathematical verification.** Applying the law of cosines to the triangle formed by $u$, $v$, and $u - v = (0, 1, -1)$ confirms $\theta = 60^\circ$:

$$
|u - v|^2 = 0^2 + 1^2 + (-1)^2 = 2,
$$

$$
|u|^2 + |v|^2 - 2|u||v|\cos\left(\frac{\pi}{3}\right) = 2 + 2 - 2(\sqrt{2})(\sqrt{2})\left(\frac{1}{2}\right) = 4 - 2 = 2 = |u - v|^2.
$$
```[cite: 9]
