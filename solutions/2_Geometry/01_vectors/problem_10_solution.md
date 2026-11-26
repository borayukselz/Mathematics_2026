### Exercise 10. Triangle Area from Vectors

#### Exercise Reminder

The points $A = (0, 0, 0)$, $B = (2, 1, 0)$, and $C = (1, 3, 2)$ form a triangle. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$, compute the area of the parallelogram using the cross product, and then find the area of the triangle. Explain the factor $\frac{1}{2}$.

---

#### Solution

**Result.**
- **Edge vectors from $A$:** $\overrightarrow{AB} = (2, 1, 0)$ and $\overrightarrow{AC} = (1, 3, 2)$
- **Area of the parallelogram spanned by $\overrightarrow{AB}$ and $\overrightarrow{AC}$:** $A_{\text{parallelogram}} = |\overrightarrow{AB} \times \overrightarrow{AC}| = \sqrt{45} = 3\sqrt{5}$
- **Area of triangle $\triangle ABC$:** $A_{\triangle ABC} = \frac{1}{2}|\overrightarrow{AB} \times \overrightarrow{AC}| = \frac{3\sqrt{5}}{2}$

<br>

**Main steps.**

1. **Construct the two adjacent edge vectors $\overrightarrow{AB}$ and $\overrightarrow{AC}$ originating at $A = (0, 0, 0)$:**

$$
\overrightarrow{AB} = B - A = (2, 1, 0) - (0, 0, 0) = (2, 1, 0),
$$

$$
\overrightarrow{AC} = C - A = (1, 3, 2) - (0, 0, 0) = (1, 3, 2).
$$

2. **Compute the cross product $\overrightarrow{AB} \times \overrightarrow{AC}$:**

$$
\overrightarrow{AB} \times \overrightarrow{AC} =
\det
\begin{pmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
2 & 1 & 0 \\
1 & 3 & 2
\end{pmatrix} =
\begin{vmatrix}
1 & 0 \\
3 & 2
\end{vmatrix}\mathbf{i} -
\begin{vmatrix}
2 & 0 \\
1 & 2
\end{vmatrix}\mathbf{j} +
\begin{vmatrix}
2 & 1 \\
1 & 3
\end{vmatrix}\mathbf{k}
$$

$$
\overrightarrow{AB} \times \overrightarrow{AC} = (1\cdot 2 - 0\cdot 3)\mathbf{i} - (2\cdot 2 - 0\cdot 1)\mathbf{j} + (2\cdot 3 - 1\cdot 1)\mathbf{k} = 2\mathbf{i} - 4\mathbf{j} + 5\mathbf{k} = (2, -4, 5).
$$

3. **Compute the area of the parallelogram spanned by $\overrightarrow{AB}$ and $\overrightarrow{AC}$:**
   - The magnitude of the cross product equals the area of the parallelogram with adjacent sides $\overrightarrow{AB}$ and $\overrightarrow{AC}$:

$$
A_{\text{parallelogram}} = |\overrightarrow{AB} \times \overrightarrow{AC}| = \sqrt{2^2 + (-4)^2 + 5^2} = \sqrt{4 + 16 + 25} = \sqrt{45} = 3\sqrt{5}.
$$

4. **Compute the area of triangle $\triangle ABC$ and explain the factor $\frac{1}{2}$:**
   - Multiplying the parallelogram area by $\frac{1}{2}$ gives the area of $\triangle ABC$:

$$
A_{\triangle ABC} = \frac{1}{2}|\overrightarrow{AB} \times \overrightarrow{AC}| = \frac{1}{2}\sqrt{45} = \frac{3\sqrt{5}}{2}.
$$

   - **Geometric explanation of the factor $\frac{1}{2}$:** The segment $BC$ is a diagonal of the parallelogram spanned by $\overrightarrow{AB}$ and $\overrightarrow{AC}$, with fourth vertex $D = B + C = (3, 4, 2)$. Because a diagonal divides any parallelogram into two congruent triangles of equal base $|\overrightarrow{AB}|$ and equal altitude $h = |\overrightarrow{AC}|\sin\theta$, triangle $\triangle ABC$ occupies **exactly half** of the parallelogram's area:

$$
A_{\triangle ABC} = \frac{1}{2}\left(\text{base} \times \text{height}\right) = \frac{1}{2}|\overrightarrow{AB}||\overrightarrow{AC}|\sin\theta = \frac{1}{2}|\overrightarrow{AB} \times \overrightarrow{AC}|.
$$

<br>

**Property / method used.** **Geometric magnitude of the cross product in $\mathbb{R}^3$:** $|\mathbf{u} \times \mathbf{v}| = |\mathbf{u}||\mathbf{v}|\sin\theta$ gives the area of the parallelogram spanned by $\mathbf{u}$ and $\mathbf{v}$, and halving it yields the area of the triangle formed by their endpoints.

<br>

**Mathematical verification.** Computing the triangle area independently via the dot-product area formula

$$
A_{\triangle ABC} = \frac{1}{2}\sqrt{|\overrightarrow{AB}|^2|\overrightarrow{AC}|^2 - (\overrightarrow{AB} \cdot \overrightarrow{AC})^2}
$$

confirms the result:

$$
|\overrightarrow{AB}|^2 = 2^2 + 1^2 + 0^2 = 5, \qquad |\overrightarrow{AC}|^2 = 1^2 + 3^2 + 2^2 = 14, \qquad \overrightarrow{AB} \cdot \overrightarrow{AC} = (2)(1) + (1)(3) + (0)(2) = 5,
$$

$$
A_{\triangle ABC} = \frac{1}{2}\sqrt{(5)(14) - 5^2} = \frac{1}{2}\sqrt{70 - 25} = \frac{1}{2}\sqrt{45} = \frac{3\sqrt{5}}{2}.
$$
