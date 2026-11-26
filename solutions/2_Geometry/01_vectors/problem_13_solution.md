### Exercise 13. Do Four Points Lie in One Plane?

#### Exercise Reminder

Given

$$
A = (0, 0, 0), \qquad B = (1, 2, 0), \qquad C = (0, 1, 1), \qquad D = (2, 5, 1).
$$

1. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$.
2. Find $\mathbf{n} = \overrightarrow{AB} \times \overrightarrow{AC}$.
3. Construct $\overrightarrow{AD}$ and check whether $\overrightarrow{AD} \cdot \mathbf{n} = 0$.
4. Based on this, decide whether $D$ lies in the plane determined by $A, B, C$, and justify the criterion.

---

#### Solution

**Result.**
- **Spanning vectors in plane $(ABC)$:** $\overrightarrow{AB} = (1, 2, 0)$ and $\overrightarrow{AC} = (0, 1, 1)$
- **Normal vector to plane $(ABC)$:** $\mathbf{n} = \overrightarrow{AB} \times \overrightarrow{AC} = (2, -1, 1)$
- **Displacement vector and orthogonality test:** $\overrightarrow{AD} = (2, 5, 1)$ and $\overrightarrow{AD} \cdot \mathbf{n} = 0$
- **Coplanarity conclusion:** **Yes**, point $D$ **does lie** in the plane determined by $A, B, C$ (the four points $A, B, C, D$ are coplanar)[cite: 9].

<br>

**Main steps.**

1. **Construct the two edge vectors $\overrightarrow{AB}$ and $\overrightarrow{AC}$ starting at $A = (0, 0, 0)$:**

$$
\overrightarrow{AB} = B - A = (1, 2, 0) - (0, 0, 0) = (1, 2, 0),
$$

$$
\overrightarrow{AC} = C - A = (0, 1, 1) - (0, 0, 0) = (0, 1, 1).
$$

   - Since $\overrightarrow{AB}$ and $\overrightarrow{AC}$ are not scalar multiples of each other, $A, B, C$ are non-collinear and uniquely determine a plane.

2. **Find the normal vector $\mathbf{n} = \overrightarrow{AB} \times \overrightarrow{AC}$:**

$$
\mathbf{n} = \overrightarrow{AB} \times \overrightarrow{AC} =
\det
\begin{pmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
1 & 2 & 0 \\
0 & 1 & 1
\end{pmatrix} =
\begin{vmatrix}
2 & 0 \\
1 & 1
\end{vmatrix}\mathbf{i} -
\begin{vmatrix}
1 & 0 \\
0 & 1
\end{vmatrix}\mathbf{j} +
\begin{vmatrix}
1 & 2 \\
0 & 1
\end{vmatrix}\mathbf{k}
$$

$$
\mathbf{n} = (2\cdot 1 - 0\cdot 1)\mathbf{i} - (1\cdot 1 - 0\cdot 0)\mathbf{j} + (1\cdot 1 - 2\cdot 0)\mathbf{k} = 2\mathbf{i} - 1\mathbf{j} + 1\mathbf{k} = (2, -1, 1).
$$

3. **Construct $\overrightarrow{AD}$ and check whether $\overrightarrow{AD} \cdot \mathbf{n} = 0$:**

$$
\overrightarrow{AD} = D - A = (2, 5, 1) - (0, 0, 0) = (2, 5, 1).
$$

   Compute the dot product $\overrightarrow{AD} \cdot \mathbf{n}$:

$$
\overrightarrow{AD} \cdot \mathbf{n} = (2, 5, 1) \cdot (2, -1, 1) = (2)(2) + (5)(-1) + (1)(1) = 4 - 5 + 1 = 0.
$$

   - Thus $\overrightarrow{AD} \cdot \mathbf{n} = 0$ holds[cite: 9].

4. **Decide whether $D$ lies in the plane $(ABC)$ and justify the criterion:**
   - **Decision:** **Yes**, $D$ lies in the plane determined by $A, B, C$.
   - **Justification:** Because $\mathbf{n} = \overrightarrow{AB} \times \overrightarrow{AC} = (2, -1, 1) \neq \mathbf{0}$ is perpendicular to both $\overrightarrow{AB}$ and $\overrightarrow{AC}$, the plane $(ABC)$ passing through $A$ consists of all points $P \in \mathbb{R}^3$ whose displacement vector $\overrightarrow{AP}$ is orthogonal to $\mathbf{n}$ (i.e., $\overrightarrow{AP} \cdot \mathbf{n} = 0$). Equivalently, the scalar triple product $\overrightarrow{AD} \cdot (\overrightarrow{AB} \times \overrightarrow{AC}) = 0$ represents the signed volume of the parallelepiped spanned by $\overrightarrow{AB}$, $\overrightarrow{AC}$, and $\overrightarrow{AD}$; zero volume means $\overrightarrow{AD}$ has zero height off the base plane and therefore lies in $\mathrm{span}(\overrightarrow{AB}, \overrightarrow{AC})$.

<br>

**Property / method used.** **Scalar triple product coplanarity criterion in $\mathbb{R}^3$:** four points $A, B, C, D$ (with $A, B, C$ non-collinear) lie in a single plane if and only if $\overrightarrow{AD} \cdot (\overrightarrow{AB} \times \overrightarrow{AC}) = 0$, equivalently $\overrightarrow{AD} \in \mathrm{span}(\overrightarrow{AB}, \overrightarrow{AC})$.

<br>

**Mathematical verification.** Expressing $\overrightarrow{AD}$ directly as a linear combination of $\overrightarrow{AB}$ and $\overrightarrow{AC}$ confirms that $D$ lies in the plane $(ABC)$:

$$
2\overrightarrow{AB} + 1\overrightarrow{AC} = 2(1, 2, 0) + 1(0, 1, 1) = (2, 4, 0) + (0, 1, 1) = (2, 5, 1) = \overrightarrow{AD}.
$$
