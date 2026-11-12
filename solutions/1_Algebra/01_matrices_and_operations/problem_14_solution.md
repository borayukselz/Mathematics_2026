### Exercise 14. Rotation Matrices

#### Exercise Reminder

The matrix for a rotation through an angle $\theta$ is

$$R(\theta)= \begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \\ \end{pmatrix}.$$

1. Compute $R(\alpha)R(\beta)$ and, using the angle-sum formulas for sine and cosine, show that $R(\alpha)R(\beta) = R(\alpha + \beta)$.
2. Explain the result geometrically.

---

#### Solution

##### 1. Computing $R(\alpha)R(\beta)$ and Verifying $R(\alpha)R(\beta) = R(\alpha + \beta)$

**Result.**

$$R(\alpha)R(\beta)= \begin{pmatrix} \cos(\alpha+\beta) & -\sin(\alpha+\beta) \\ \sin(\alpha+\beta) & \cos(\alpha+\beta) \\ \end{pmatrix}= R(\alpha+\beta).$$

<br>

**Main steps.** Multiply the two $2\times 2$ rotation matrices $R(\alpha)$ and $R(\beta)$ using row-by-column dot products:

$$\begin{aligned} R(\alpha)R(\beta) &= \begin{pmatrix} \cos\alpha & -\sin\alpha \\ \sin\alpha & \cos\alpha \\ \end{pmatrix} \begin{pmatrix} \cos\beta & -\sin\beta \\ \sin\beta & \cos\beta \\ \end{pmatrix} \\ &= \begin{pmatrix} \cos\alpha\cos\beta - \sin\alpha\sin\beta & -\cos\alpha\sin\beta - \sin\alpha\cos\beta \\ \sin\alpha\cos\beta + \cos\alpha\sin\beta & -\sin\alpha\sin\beta + \cos\alpha\cos\beta \\ \end{pmatrix} \\ &= \begin{pmatrix} \cos\alpha\cos\beta - \sin\alpha\sin\beta & -(\sin\alpha\cos\beta + \cos\alpha\sin\beta) \\ \sin\alpha\cos\beta + \cos\alpha\sin\beta & \cos\alpha\cos\beta - \sin\alpha\sin\beta \\ \end{pmatrix}. \end{aligned}$$

Apply the trigonometric angle-sum identities

$$\cos(\alpha+\beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta, \qquad \sin(\alpha+\beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta$$

to each of the four entries:

$$R(\alpha)R(\beta)= \begin{pmatrix} \cos(\alpha+\beta) & -\sin(\alpha+\beta) \\ \sin(\alpha+\beta) & \cos(\alpha+\beta) \\ \end{pmatrix}= R(\alpha+\beta).$$

<br>

**Property / method used.** *Matrix multiplication and trigonometric angle-sum identities:* the product of two $2\times 2$ rotation matrices reduces entrywise via the addition formulas for $\cos(\alpha+\beta)$ and $\sin(\alpha+\beta)$ to the rotation matrix of the summed angle.

<br>

**Mathematical verification.** Testing the identity at $\alpha = \frac{\pi}{2}$ ($90^\circ$) and $\beta = \frac{\pi}{2}$ ($90^\circ$) confirms the algebraic derivation:

$$R\left(\frac{\pi}{2}\right)R\left(\frac{\pi}{2}\right)= \begin{pmatrix} 0 & -1 \\ 1 & 0 \\ \end{pmatrix} \begin{pmatrix} 0 & -1 \\ 1 & 0 \\ \end{pmatrix}= \begin{pmatrix} -1 & 0 \\ 0 & -1 \\ \end{pmatrix}= \begin{pmatrix} \cos\pi & -\sin\pi \\ \sin\pi & \cos\pi \\ \end{pmatrix}= R(\pi).$$

Additionally, $\det(R(\theta)) = \cos^2\theta + \sin^2\theta = 1$ for every angle $\theta$, which agrees with $\det(R(\alpha)R(\beta)) = \det(R(\alpha))\det(R(\beta)) = 1\cdot 1 = 1 = \det(R(\alpha+\beta))$.

---

##### 2. Geometric Explanation

**Result.** Rotating a vector in the plane counterclockwise by an angle $\beta$ and subsequently rotating the result counterclockwise by an angle $\alpha$ produces the exact same final vector as performing a single counterclockwise rotation by the combined angle $\alpha + \beta$.

<br>

**Main steps.** For any vector $v \in \mathbb{R}^2$:
1. Multiplying $v$ on the left by $R(\beta)$ produces $R(\beta)v$, which rotates $v$ counterclockwise about the origin through angle $\beta$ without changing its length.
2. Multiplying that intermediate vector on the left by $R(\alpha)$ produces $R(\alpha)\bigl(R(\beta)v\bigr) = \bigl(R(\alpha)R(\beta)\bigr)v$, rotating it counterclockwise about the origin through an additional angle $\alpha$.
3. Because both rotations occur in the same two-dimensional plane around the same center (the origin), the two consecutive angular displacements add directly to a total counterclockwise rotation of $\alpha + \beta$, represented by $R(\alpha + \beta)v$.

<br>

**Property / method used.** *Composition of planar rotations (SO(2) group property):* planar rotations about the origin form a commutative group under composition, satisfying $R(\alpha)R(\beta) = R(\alpha + \beta) = R(\beta + \alpha) = R(\beta)R(\alpha)$.

<br>

**Mathematical verification.** Expressing an arbitrary nonzero vector in polar coordinates as $v = r \begin{pmatrix} \cos\phi \\ \sin\phi \end{pmatrix}$ shows explicitly how the angles add under successive multiplication:

$$R(\beta)v = r \begin{pmatrix} \cos(\phi + \beta) \\ \sin(\phi + \beta) \\ \end{pmatrix} \implies R(\alpha)\bigl(R(\beta)v\bigr) = r \begin{pmatrix} \cos(\phi + \beta + \alpha) \\ \sin(\phi + \beta + \alpha) \\ \end{pmatrix}= R(\alpha + \beta)v.$$
