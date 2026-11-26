### Exercise 12. A Normal Vector to a Plane

#### Exercise Reminder

Given $A = (1, 0, 2)$, $B = (2, 1, 0)$, and $C = (0, 3, 1)$. Construct two vectors lying in the plane, find a vector perpendicular to both, and check the perpendicularity using dot products.

---

#### Solution

**Result.**
- **Two non-collinear vectors lying in the plane $(ABC)$:** $\overrightarrow{AB} = (1, 1, -2)$ and $\overrightarrow{AC} = (-1, 3, -1)$
- **Normal vector perpendicular to the plane:** $\mathbf{n} = \overrightarrow{AB} \times \overrightarrow{AC} = (5, 3, 4)$ (any nonzero scalar multiple $k(5, 3, 4)$ is also normal to the plane)
- **Perpendicularity check:** $\mathbf{n} \cdot \overrightarrow{AB} = 0$ and $\mathbf{n} \cdot \overrightarrow{AC} = 0$

<br>

**Main steps.**

1. **Construct two direction vectors $\overrightarrow{AB}$ and $\overrightarrow{AC}$ lying in the plane passing through $A$, $B$, and $C$:**

$$
\overrightarrow{AB} = B - A = (2, 1, 0) - (1, 0, 2) = (2 - 1, \ 1 - 0, \ 0 - 2) = (1, 1, -2),
$$

$$
\overrightarrow{AC} = C - A = (0, 3, 1) - (1, 0, 2) = (0 - 1, \ 3 - 0, \ 1 - 2) = (-1, 3, -1).
$$

   - Notice that $\overrightarrow{AB}$ and $\overrightarrow{AC}$ are not scalar multiples of one another, so the three points are non-collinear and uniquely span the plane.

2. **Find a vector $\mathbf{n}$ perpendicular to both $\overrightarrow{AB}$ and $\overrightarrow{AC}$ via their cross product:**

$$
\mathbf{n} = \overrightarrow{AB} \times \overrightarrow{AC} =
\det
\begin{pmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
1 & 1 & -2 \\
-1 & 3 & -1
\end{pmatrix} =
\begin{vmatrix}
1 & -2 \\
3 & -1
\end{vmatrix}\mathbf{i} -
\begin{vmatrix}
1 & -2 \\
-1 & -1
\end{vmatrix}\mathbf{j} +
\begin{vmatrix}
1 & 1 \\
-1 & 3
\end{vmatrix}\mathbf{k}
$$

$$
\mathbf{n} = ((1)(-1) - (-2)(3))\mathbf{i} - ((1)(-1) - (-2)(-1))\mathbf{j} + ((1)(3) - (1)(-1))\mathbf{k}
$$

$$
\mathbf{n} = (-1 + 6)\mathbf{i} - (-1 - 2)\mathbf{j} + (3 + 1)\mathbf{k} = 5\mathbf{i} + 3\mathbf{j} + 4\mathbf{k} = (5, 3, 4).
$$

3. **Check perpendicularity of $\mathbf{n} = (5, 3, 4)$ to both $\overrightarrow{AB}$ and $\overrightarrow{AC}$ using dot products:**

$$
\mathbf{n} \cdot \overrightarrow{AB} = (5, 3, 4) \cdot (1, 1, -2) = (5)(1) + (3)(1) + (4)(-2) = 5 + 3 - 8 = 0,
$$

$$
\mathbf{n} \cdot \overrightarrow{AC} = (5, 3, 4) \cdot (-1, 3, -1) = (5)(-1) + (3)(3) + (4)(-1) = -5 + 9 - 4 = 0.
$$

   - Since both dot products vanish and $\mathbf{n} \neq \mathbf{0}$, $\mathbf{n} = (5, 3, 4)$ is perpendicular to both spanning vectors and hence normal to the entire plane $(ABC)$.

<br>

**Property / method used.** **Normal vector construction via the cross product in $\mathbb{R}^3$:** for any two non-collinear direction vectors $\overrightarrow{AB}, \overrightarrow{AC}$ parallel to a plane, $\mathbf{n} = \overrightarrow{AB} \times \overrightarrow{AC}$ is nonzero and orthogonal to every linear combination $s\overrightarrow{AB} + t\overrightarrow{AC}$ in the plane.

<br>

**Mathematical verification.** Forming the third edge vector $\overrightarrow{BC} = C - B = (-2, 2, 1)$ in the plane and verifying $\mathbf{n} \cdot \overrightarrow{BC} = 0$ (as well as confirming that all three points satisfy the plane equation $5x + 3y + 4z = 13$) confirms the normal vector:

$$
\mathbf{n} \cdot \overrightarrow{BC} = (5, 3, 4) \cdot (-2, 2, 1) = -10 + 6 + 4 = 0,
$$

$$
5(1) + 3(0) + 4(2) = 13, \qquad 5(2) + 3(1) + 4(0) = 13, \qquad 5(0) + 3(3) + 4(1) = 13.
$$
```[cite: 9]
