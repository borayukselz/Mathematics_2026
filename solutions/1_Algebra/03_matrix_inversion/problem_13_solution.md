### Exercise 13. Undoing a Composite Transformation

#### Exercise Reminder

The matrices

$$
S =
\begin{pmatrix}
2 & 0 \\
0 & 1
\end{pmatrix},\qquad H =
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix}
$$

describe nonuniform scaling and shear. For $T = HS$, find $T^{-1}$ in two ways:
1. first compute $T$, then its inverse,
2. use $(HS)^{-1} = S^{-1}H^{-1}$.

Compare the results. Additionally compute $H^{-1}S^{-1}$ and verify that the incorrect order gives a different matrix. Explain the rule: "when undoing a composition of operations, we undo them from the end."

---

#### Solution

**Result.** Both valid methods give the exact same inverse transformation matrix:

$$
T^{-1} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & 1
\end{pmatrix}.
$$

Using the incorrect order yields a different matrix:

$$
H^{-1}S^{-1} =
\begin{pmatrix}
\frac{1}{2} & -1 \\
0 & 1
\end{pmatrix} \neq T^{-1}.
$$

<br>

**Main steps.**

1. **Method 1 — First compute $T = HS$, then find its inverse:** Multiply $H$ and $S$:

$$
T = HS =
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 1
\end{pmatrix} =
\begin{pmatrix}
1\cdot 2 + 1\cdot 0 & 1\cdot 0 + 1\cdot 1 \\
0\cdot 2 + 1\cdot 0 & 0\cdot 0 + 1\cdot 1
\end{pmatrix} =
\begin{pmatrix}
2 & 1 \\
0 & 1
\end{pmatrix}.
$$

Since $\det T = (2)(1) - (1)(0) = 2 \neq 0$, the $2\times 2$ inverse formula gives

$$
T^{-1} = \frac{1}{2}
\begin{pmatrix}
1 & -1 \\
0 & 2
\end{pmatrix} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & 1
\end{pmatrix}.
$$

2. **Method 2 — Use $(HS)^{-1} = S^{-1}H^{-1}$:** Compute the individual inverses of $S$ ($\det S = 2$) and $H$ ($\det H = 1$):

$$
S^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 1
\end{pmatrix},\qquad H^{-1} =
\begin{pmatrix}
1 & -1 \\
0 & 1
\end{pmatrix}.
$$

Multiply $S^{-1}$ and $H^{-1}$ in reversed order:

$$
S^{-1}H^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
0 & 1
\end{pmatrix} =
\begin{pmatrix}
\frac{1}{2}\cdot 1 + 0\cdot 0 & \frac{1}{2}\cdot (-1) + 0\cdot 1 \\
0\cdot 1 + 1\cdot 0 & 0\cdot (-1) + 1\cdot 1
\end{pmatrix} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & 1
\end{pmatrix}.
$$

3. **Compare the results and compute $H^{-1}S^{-1}$:** Both Method 1 and Method 2 produce the identical matrix $T^{-1}$. In contrast, multiplying the inverses in the unreversed (incorrect) order gives

$$
H^{-1}S^{-1} =
\begin{pmatrix}
1 & -1 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 1
\end{pmatrix} =
\begin{pmatrix}
1\cdot \frac{1}{2} + (-1)\cdot 0 & 1\cdot 0 + (-1)\cdot 1 \\
0\cdot \frac{1}{2} + 1\cdot 0 & 0\cdot 0 + 1\cdot 1
\end{pmatrix} =
\begin{pmatrix}
\frac{1}{2} & -1 \\
0 & 1
\end{pmatrix},
$$

which differs in the $(1,2)$ entry ($-1 \neq -\frac{1}{2}$).

4. **Explanation of the rule:** When $T = HS$ acts on a vector $x$, we evaluate $Tx = H(Sx)$ from right to left: first $S$ stretches the $x$-coordinate by $2$, and then $H$ shears the resulting vector horizontally by adding its $y$-coordinate to its $x$-coordinate. Because $H$ was the *last* operation applied (at the end of the pipeline), it must be the *first* operation undone: applying $H^{-1}$ removes the shear first, and applying $S^{-1}$ next shrinks the horizontal stretch back by $\frac{1}{2}$. Attempting $H^{-1}S^{-1}$ shrinks the $x$-coordinate before removing the shear, which scales the shear shift improperly.

<br>

**Property / method used.** *Inverse of a composite transformation:* for invertible matrices $H$ and $S$, $(HS)^{-1} = S^{-1}H^{-1}$ because $(S^{-1}H^{-1})(HS) = S^{-1}(H^{-1}H)S = S^{-1}IS = I$.

<br>

**Mathematical verification.** Testing $T$ followed by $T^{-1}$ on the vector

$$
v =
\begin{pmatrix}
1 \\
2
\end{pmatrix}
$$

confirms that $T^{-1}$ restores $v$, whereas $H^{-1}S^{-1}$ fails:

$$
Tv =
\begin{pmatrix}
2 & 1 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
1 \\
2
\end{pmatrix} =
\begin{pmatrix}
4 \\
2
\end{pmatrix} \implies T^{-1}(Tv) =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
4 \\
2
\end{pmatrix} =
\begin{pmatrix}
1 \\
2
\end{pmatrix} = v,
$$

while

$$
(H^{-1}S^{-1})(Tv) =
\begin{pmatrix}
\frac{1}{2} & -1 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
4 \\
2
\end{pmatrix} =
\begin{pmatrix}
0 \\
2
\end{pmatrix} \neq v.
$$
