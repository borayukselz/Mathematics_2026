### Exercise 3. Vector Normalization

#### Exercise Reminder

For $v = (3, 4)$ find a unit vector $e$ with the same direction and orientation. Check that $|e| = 1$, reconstruct $v$ in the form $v = |v|e$, and explain what changes during normalization and what remains unchanged.

---

#### Solution

**Result.**
- **Norm of $v$:** $|v| = 5$
- **Unit vector in the same direction and orientation:** $e = \left(\frac{3}{5}, \frac{4}{5}\right)$ (or $(0.6, 0.8)$)
- **Polar / magnitude-direction decomposition:** $v = 5\left(\frac{3}{5}, \frac{4}{5}\right)$

<br>

**Main steps.**

1. **Compute the Euclidean length (norm) $|v|$ of $v = (3, 4)$:**

$$
|v| = \sqrt{3^2 + 4^2} = \sqrt{9 + 16} = \sqrt{25} = 5.
$$

2. **Divide $v$ by its positive length $|v| = 5$ to obtain the unit vector $e$:**

$$
e = \frac{1}{|v|}v = \frac{1}{5}(3, 4) = \left(\frac{3}{5}, \frac{4}{5}\right).
$$

3. **Check that $|e| = 1$:**

$$
|e| = \sqrt{\left(\frac{3}{5}\right)^2 + \left(\frac{4}{5}\right)^2} = \sqrt{\frac{9}{25} + \frac{16}{25}} = \sqrt{\frac{25}{25}} = \sqrt{1} = 1.
$$

4. **Reconstruct $v$ in the form $v = |v|e$:**

$$
|v|e = 5\left(\frac{3}{5}, \frac{4}{5}\right) = \left(5 \cdot \frac{3}{5}, \ 5 \cdot \frac{4}{5}\right) = (3, 4) = v.
$$

5. **Explain what changes during normalization and what remains unchanged:**
   - **What changes:** The **magnitude (length)** of the vector changes from its original length $|v| = 5$ to $|e| = 1$ (scaling each coordinate by the positive factor $\frac{1}{5}$), placing the terminal point of $e$ on the unit circle centered at the origin.
   - **What remains unchanged:** Because normalization multiplies $v$ by a **strictly positive scalar** $\lambda = \frac{1}{|v|} = \frac{1}{5} > 0$, both the **line of action (direction)**—the angle $\theta = \arctan\left(\frac{4}{3}\right)$ with the positive $x$-axis—and the **orientation (sense)** along that line remain completely unchanged.

<br>

**Property / method used.** *Positive scalar homogeneity of the Euclidean norm:* for any nonzero vector $v \in \mathbb{R}^n$ and positive scalar $c = \frac{1}{|v|} > 0$, $|cv| = c|v| = 1$, decoupling a vector into its scalar magnitude $|v|$ and pure directional unit vector $e = \frac{v}{|v|}$.

<br>

**Mathematical verification.** Computing the dot product $v \cdot e$ confirms that $e$ points in the exact same direction as $v$ ($\cos\theta = 1$, i.e., $\theta = 0^\circ$):

$$
v \cdot e = 3\left(\frac{3}{5}\right) + 4\left(\frac{4}{5}\right) = \frac{9 + 16}{5} = \frac{25}{5} = 5 = |v||e|.
$$
