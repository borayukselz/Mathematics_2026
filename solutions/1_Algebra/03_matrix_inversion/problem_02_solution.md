### Exercise 2. Formula for a $2\times 2$ Matrix

#### Exercise Reminder

Find the inverse of

$$
A =
\begin{pmatrix}
3 & 2 \\
5 & 4
\end{pmatrix}
$$

using the formula for a $2\times 2$ matrix. At the end, check the result by computing one product with $A$.

---

#### Solution

**Result.**

$$
A^{-1} =
\begin{pmatrix}
2 & -1 \\
-\frac{5}{2} & \frac{3}{2}
\end{pmatrix}.
$$

<br>

**Main steps.** Identify the four entries of $A$:

$$
a = 3,\qquad b = 2,\qquad c = 5,\qquad d = 4.
$$

1. **Compute the determinant $\det A$:**

$$
\det A = ad - bc = (3)(4) - (2)(5) = 12 - 10 = 2.
$$

Since $\det A = 2 \neq 0$, the inverse matrix $A^{-1}$ exists.

2. **Apply the $2\times 2$ inverse formula:** Swap the main diagonal entries ($a$ and $d$), negate the off-diagonal entries ($b$ and $c$), and divide by $\det A$:

$$
A^{-1} = \frac{1}{\det A}
\begin{pmatrix}
d & -b \\
-c & a
\end{pmatrix} = \frac{1}{2}
\begin{pmatrix}
4 & -2 \\
-5 & 3
\end{pmatrix} =
\begin{pmatrix}
2 & -1 \\
-\frac{5}{2} & \frac{3}{2}
\end{pmatrix}.
$$

<br>

**Property / method used.** *Closed-form inverse of a $2\times 2$ matrix:* for any $2\times 2$ matrix

$$
M =
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
$$

with $\det M = ad - bc \neq 0$, its inverse is given by

$$
M^{-1} = \frac{1}{ad - bc}
\begin{pmatrix}
d & -b \\
-c & a
\end{pmatrix}.
$$

<br>

**Mathematical verification.** Checking the product $A A^{-1}$ confirms that it equals the $2\times 2$ identity matrix $I$:

$$
A A^{-1} =
\begin{pmatrix}
3 & 2 \\
5 & 4
\end{pmatrix}
\begin{pmatrix}
2 & -1 \\
-\frac{5}{2} & \frac{3}{2}
\end{pmatrix} =
\begin{pmatrix}
3\cdot 2 + 2\cdot \left(-\frac{5}{2}\right) & 3\cdot (-1) + 2\cdot \frac{3}{2} \\
5\cdot 2 + 4\cdot \left(-\frac{5}{2}\right) & 5\cdot (-1) + 4\cdot \frac{3}{2}
\end{pmatrix} =
\begin{pmatrix}
6 - 5 & -3 + 3 \\
10 - 10 & -5 + 6
\end{pmatrix} =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} = I.
$$
