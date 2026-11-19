### Exercise 8. Inverse of a Transformation

#### Exercise Reminder

The matrix

$$
S =
\begin{pmatrix}
2 & 0 \\
0 & \frac{1}{2}
\end{pmatrix}
$$

describes a scaling of the plane. Find $S^{-1}$ and explain geometrically what the inverse transformation does. Check the action of the pair $S, S^{-1}$ on one simple vector.

---

#### Solution

**Result.**

$$
S^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2
\end{pmatrix}.
$$

Geometrically, $S^{-1}$ reverses the nonuniform scaling of $S$: it **compresses the plane horizontally by a factor of $2$** (multiplying the $x$-coordinate by $\frac{1}{2}$) and **stretches the plane vertically by a factor of $2$** (multiplying the $y$-coordinate by $2$).

<br>

**Main steps.**

1. **Compute $S^{-1}$:** Compute the determinant of the diagonal matrix $S$:

$$
\det S = (2)\left(\frac{1}{2}\right) - (0)(0) = 1.
$$

Since $\det S = 1 \neq 0$, the inverse exists. Applying the $2\times 2$ inverse formula (or inverting each nonzero diagonal entry directly) gives

$$
S^{-1} = \frac{1}{1}
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2
\end{pmatrix} =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2
\end{pmatrix}.
$$

2. **Geometric interpretation of $S$ and $S^{-1}$:** For any vector

$$
v =
\begin{pmatrix}
x \\
y
\end{pmatrix}
$$

in $\mathbb{R}^2$, the transformation $S$ acts by

$$
Sv =
\begin{pmatrix}
2 & 0 \\
0 & \frac{1}{2}
\end{pmatrix}
\begin{pmatrix}
x \\
y
\end{pmatrix} =
\begin{pmatrix}
2x \\
\frac{1}{2}y
\end{pmatrix},
$$

which stretches the horizontal coordinate by $2$ and shrinks the vertical coordinate by $\frac{1}{2}$. To restore the original vector, $S^{-1}$ performs the opposite scaling along each axis:

$$
S^{-1}v =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2
\end{pmatrix}
\begin{pmatrix}
x \\
y
\end{pmatrix} =
\begin{pmatrix}
\frac{1}{2}x \\
2y
\end{pmatrix}.
$$

3. **Check the action of $S$ and $S^{-1}$ on a simple vector:** Choose the simple test vector

$$
v =
\begin{pmatrix}
1 \\
2
\end{pmatrix}.
$$

First apply $S$ to $v$:

$$
Sv =
\begin{pmatrix}
2 & 0 \\
0 & \frac{1}{2}
\end{pmatrix}
\begin{pmatrix}
1 \\
2
\end{pmatrix} =
\begin{pmatrix}
2\cdot 1 \\
\frac{1}{2}\cdot 2
\end{pmatrix} =
\begin{pmatrix}
2 \\
1
\end{pmatrix}.
$$

Now apply $S^{-1}$ to the transformed vector $Sv$:

$$
S^{-1}(Sv) =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2
\end{pmatrix}
\begin{pmatrix}
2 \\
1
\end{pmatrix} =
\begin{pmatrix}
\frac{1}{2}\cdot 2 \\
2\cdot 1
\end{pmatrix} =
\begin{pmatrix}
1 \\
2
\end{pmatrix} = v.
$$

<br>

**Property / method used.** *Inverse of a diagonal scaling matrix:* a diagonal matrix $\mathrm{diag}(d_1, d_2, \dots, d_n)$ with nonzero diagonal entries is invertible, and its inverse is $\mathrm{diag}(d_1^{-1}, d_2^{-1}, \dots, d_n^{-1})$, which undoes each coordinate-wise scaling factor.

<br>

**Mathematical verification.** Multiplying $S$ and $S^{-1}$ in both orders confirms that $S S^{-1} = S^{-1} S = I$:

$$
S S^{-1} =
\begin{pmatrix}
2 & 0 \\
0 & \frac{1}{2}
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2
\end{pmatrix} =
\begin{pmatrix}
2\cdot \frac{1}{2} & 0 \\
0 & \frac{1}{2}\cdot 2
\end{pmatrix} =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} = I,
$$

and notice also that $\det(S)\det(S^{-1}) = 1 \cdot 1 = 1$, confirming that $S^{-1}$ preserves area just as $S$ does.
