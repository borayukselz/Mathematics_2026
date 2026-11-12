### Exercise 9. Area and the Determinant

#### Exercise Reminder

The vectors

$$
u=
\begin{pmatrix}
3 \\
1 \\
\end{pmatrix},\qquad v=
\begin{pmatrix}
1 \\
4 \\
\end{pmatrix}
$$

span a parallelogram.

1. Compute its area using a determinant.
2. Reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.

---

#### Solution

##### 1. Computing the Area Using a Determinant

**Result.**

$$
\text{Area} = 11.
$$

<br>

**Main steps.** Form the $2\times 2$ matrix $M_1$ whose columns are $u$ and $v$ in the given order:

$$
M_1 =
\begin{pmatrix}
3 & 1 \\
1 & 4 \\
\end{pmatrix}.
$$

Compute the determinant of $M_1$:

$$
\det M_1 = 3 \cdot 4 - 1 \cdot 1 = 12 - 1 = 11.
$$

Take the absolute value of the determinant to obtain the area of the parallelogram spanned by $u$ and $v$:

$$
\text{Area} = |\det M_1| = |11| = 11.
$$

<br>

**Property / method used.** *Geometric area formula in $\mathbb{R}^2$:* the area of the parallelogram spanned by two vectors $u, v \in \mathbb{R}^2$ equals the absolute value of the determinant of the $2\times 2$ matrix formed by those vectors:

$$
\text{Area} = \bigl|\det
\begin{pmatrix}
u & v
\end{pmatrix}\bigr|.
$$

<br>

**Mathematical verification.** Using the Euclidean norms and dot product of $u$ and $v$, we have $\|u\|^2 = 3^2 + 1^2 = 10$, $\|v\|^2 = 1^2 + 4^2 = 17$, and $u \cdot v = 3(1) + 1(4) = 7$. The Lagrange identity gives

$$
\text{Area} = \sqrt{\|u\|^2 \|v\|^2 - (u \cdot v)^2} = \sqrt{10 \cdot 17 - 7^2} = \sqrt{170 - 49} = \sqrt{121} = 11,
$$

confirming the determinant calculation.

---

##### 2. Reversing the Order of the Vectors

**Result.** Reversing the order of $u$ and $v$ yields

$$
\det
\begin{pmatrix}
1 & 3 \\
4 & 1 \\
\end{pmatrix}= -11, \qquad \text{while} \qquad \text{Area} = |-11| = 11.
$$

- **What changes in the determinant:** Its **sign** flips from $+11$ to $-11$ (indicating opposite geometric orientation).
- **What does not change in the area:** The **area** remains unchanged at $11$.

<br>

**Main steps.** Place $v$ in the first column and $u$ in the second column to form $M_2$:

$$
M_2 =
\begin{pmatrix}
1 & 3 \\
4 & 1 \\
\end{pmatrix}.
$$

Compute $\det M_2$:

$$
\det M_2 = 1 \cdot 1 - 3 \cdot 4 = 1 - 12 = -11.
$$

1. **Change in the determinant:** Swapping the two columns reverses the sign of the determinant ($\det M_2 = -\det M_1 = -11$). Geometrically, the signed determinant measures *oriented* area: the ordered pair $(u, v)$ is oriented counterclockwise ($\det M_1 > 0$), whereas $(v, u)$ is oriented clockwise ($\det M_2 < 0$).
2. **Invariance of the area:** The geometric parallelogram spanned by $\{v, u\}$ is the exact same region in the plane as the parallelogram spanned by $\{u, v\}$, and taking the absolute value removes the sign:

$$
\text{Area} = |\det M_2| = |-11| = 11 = |\det M_1|.
$$

<br>

**Property / method used.** *Alternating (column-swap) property of determinants and nonnegativity of area:* interchanging two columns multiplies the determinant by $-1$, whereas geometric area equals $|\det M|$ and depends only on the spanning set of vectors, not their ordering.

<br>

**Mathematical verification.** Since $M_2$ is obtained from $M_1$ by a single column swap ($C_1 \leftrightarrow C_2$), the alternating property directly predicts $\det M_2 = -\det M_1 = -11$, and $|-11| = |11| = 11$ confirms that both orderings yield identical area.
