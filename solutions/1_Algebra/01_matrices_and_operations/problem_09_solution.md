### Exercise 9. Composing Transformations

#### Exercise Reminder

Let

$$S= \begin{pmatrix} 2 & 0 \\ 0 & 1 \\ \end{pmatrix},\qquad R= \begin{pmatrix} 0 & -1 \\ 1 & 0 \\ \end{pmatrix}.$$

The matrix $S$ describes nonuniform scaling, while $R$ describes a $90^\circ$ counterclockwise rotation. For

$$x= \begin{pmatrix} 1 \\ 2 \\ \end{pmatrix},$$

1. Compute $RSx$ and $SRx$.
2. Compare the results and explain geometrically why the order of these transformations matters.

---

#### Solution

##### 1. Computing $RSx$ and $SRx$

**Result.**

$$RSx= \begin{pmatrix} -2 \\ 2 \\ \end{pmatrix},\qquad SRx= \begin{pmatrix} -4 \\ 1 \\ \end{pmatrix}.$$

**Main steps.** In a composition of matrix transformations applied to a vector $x$, the matrix immediately to the left of $x$ acts first.

To compute $RSx = R(Sx)$, first apply the scaling matrix $S$ to $x$, and then apply the rotation matrix $R$ to the resulting vector:

$$Sx= \begin{pmatrix} 2 & 0 \\ 0 & 1 \\ \end{pmatrix} \begin{pmatrix} 1 \\ 2 \\ \end{pmatrix}= \begin{pmatrix} 2\cdot 1 + 0\cdot 2 \\ 0\cdot 1 + 1\cdot 2 \\ \end{pmatrix}= \begin{pmatrix} 2 \\ 2 \\ \end{pmatrix},$$

$$RSx = R(Sx) = \begin{pmatrix} 0 & -1 \\ 1 & 0 \\ \end{pmatrix} \begin{pmatrix} 2 \\ 2 \\ \end{pmatrix}= \begin{pmatrix} 0\cdot 2 + (-1)\cdot 2 \\ 1\cdot 2 + 0\cdot 2 \\ \end{pmatrix}= \begin{pmatrix} -2 \\ 2 \\ \end{pmatrix}.$$

To compute $SRx = S(Rx)$, first apply the rotation matrix $R$ to $x$, and then apply the scaling matrix $S$ to the resulting vector:

$$Rx= \begin{pmatrix} 0 & -1 \\ 1 & 0 \\ \end{pmatrix} \begin{pmatrix} 1 \\ 2 \\ \end{pmatrix}= \begin{pmatrix} 0\cdot 1 + (-1)\cdot 2 \\ 1\cdot 1 + 0\cdot 2 \\ \end{pmatrix}= \begin{pmatrix} -2 \\ 1 \\ \end{pmatrix},$$

$$SRx = S(Rx) = \begin{pmatrix} 2 & 0 \\ 0 & 1 \\ \end{pmatrix} \begin{pmatrix} -2 \\ 1 \\ \end{pmatrix}= \begin{pmatrix} 2\cdot (-2) + 0\cdot 1 \\ 0\cdot (-2) + 1\cdot 1 \\ \end{pmatrix}= \begin{pmatrix} -4 \\ 1 \\ \end{pmatrix}.$$

**Property / method used.** *Composition of linear transformations and associativity:* applying transformation $T_1$ (represented by matrix $B$) followed by transformation $T_2$ (represented by matrix $A$) maps $x$ to $A(Bx) = (AB)x$.

**Mathematical verification.** Computing the composite transformation matrices $RS$ and $SR$ first and then multiplying each by $x$ yields the exact same vectors:

$$RS= \begin{pmatrix} 0 & -1 \\ 1 & 0 \\ \end{pmatrix} \begin{pmatrix} 2 & 0 \\ 0 & 1 \\ \end{pmatrix}= \begin{pmatrix} 0 & -1 \\ 2 & 0 \\ \end{pmatrix} \implies (RS)x= \begin{pmatrix} 0 & -1 \\ 2 & 0 \\ \end{pmatrix} \begin{pmatrix} 1 \\ 2 \\ \end{pmatrix}= \begin{pmatrix} -2 \\ 2 \\ \end{pmatrix},$$

$$SR= \begin{pmatrix} 2 & 0 \\ 0 & 1 \\ \end{pmatrix} \begin{pmatrix} 0 & -1 \\ 1 & 0 \\ \end{pmatrix}= \begin{pmatrix} 0 & -2 \\ 1 & 0 \\ \end{pmatrix} \implies (SR)x= \begin{pmatrix} 0 & -2 \\ 1 & 0 \\ \end{pmatrix} \begin{pmatrix} 1 \\ 2 \\ \end{pmatrix}= \begin{pmatrix} -4 \\ 1 \\ \end{pmatrix}.$$

##### 2. Comparison and Geometric Explanation

**Result.** The two resulting vectors are different ($RSx \neq SRx$). Geometrically, the order matters because $S$ stretches space *nonuniformly* (only along the horizontal $x$-axis), so rotating a vector changes which coordinate lies along the stretched axis.

**Main steps.** Tracking the coordinates of $x = \begin{pmatrix} 1 \\ 2 \end{pmatrix}$ through both sequences shows the geometric difference:
- **In $RSx$ (scale first, then rotate):** $S$ doubles the horizontal coordinate from $1$ to $2$ while leaving the vertical coordinate at $2$, producing $\begin{pmatrix} 2 \\ 2 \end{pmatrix}$. Rotating by $90^\circ$ counterclockwise then maps $\begin{pmatrix} x_1 \\ x_2 \end{pmatrix} \mapsto \begin{pmatrix} -x_2 \\ x_1 \end{pmatrix}$, sending $\begin{pmatrix} 2 \\ 2 \end{pmatrix}$ to $\begin{pmatrix} -2 \\ 2 \end{pmatrix}$.
- **In $SRx$ (rotate first, then scale):** $R$ first rotates $\begin{pmatrix} 1 \\ 2 \end{pmatrix}$ by $90^\circ$ counterclockwise to $\begin{pmatrix} -2 \\ 1 \end{pmatrix}$, placing the original vertical coordinate ($2$) onto the horizontal axis. Applying $S$ afterward doubles this new horizontal coordinate from $-2$ to $-4$, yielding $\begin{pmatrix} -4 \\ 1 \end{pmatrix}$.

**Property / method used.** *Geometric noncommutativity of anisotropic scaling and rotation:* while uniform scaling ($cI$) commutes with rotations, nonuniform scaling along a fixed coordinate axis does not commute with a $90^\circ$ rotation because rotation swaps the horizontal and vertical directions.

**Mathematical verification.** A pure rotation $R$ is an isometry and preserves Euclidean vector length ($\Vert{}Rv\Vert{} = \Vert{}v\Vert{}$). In $RSx$, $Sx = \begin{pmatrix} 2 \\ 2 \end{pmatrix}$ has length $\sqrt{2^2 + 2^2} = \sqrt{8}$, so $\Vert{}RSx\Vert{} = \sqrt{(-2)^2 + 2^2} = \sqrt{8}$. In $SRx$, $Rx = \begin{pmatrix} -2 \\ 1 \end{pmatrix}$ has length $\sqrt{(-2)^2 + 1^2} = \sqrt{5}$, and stretching its horizontal component by $2$ changes the length to $\Vert{}SRx\Vert{} = \sqrt{(-4)^2 + 1^2} = \sqrt{17} \neq \sqrt{8}$, confirming geometrically why the two outcomes cannot coincide.
