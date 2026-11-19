### Exercise 5. A $3\times 3$ Matrix

#### Exercise Reminder

Use Gauss–Jordan elimination to find the inverse of

$$
A =
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1
\end{pmatrix}.
$$

Check the result by multiplication.

---

#### Solution

**Result.**

$$
A^{-1} =
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
-\frac{1}{2} & \frac{1}{2} & \frac{1}{2}
\end{pmatrix} = \frac{1}{2}
\begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1
\end{pmatrix}.
$$

<br>

**Main steps.** Form the $3\times 6$ augmented matrix $[A \mid I]$ by adjoining the $3\times 3$ identity matrix $I$ to the right of $A$, and apply elementary row operations to reduce the left block to $I$:

$$
[A \mid I] =
\left(
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
1 & 0 & 1 & 0 & 0 & 1
\end{array}
\right).
$$

1. **Step 1 — Eliminate the $(3,1)$ entry below the first pivot via $R_3 \leftarrow R_3 - R_1$:**

$$
\left(
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
1 & 0 & 1 & 0 & 0 & 1
\end{array}
\right)
\xrightarrow{R_3 \leftarrow R_3 - R_1}
\left(
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
0 & -1 & 1 & -1 & 0 & 1
\end{array}
\right).
$$

2. **Step 2 — Eliminate the $(3,2)$ entry below the second pivot via $R_3 \leftarrow R_3 + R_2$:**

$$
\left(
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
0 & -1 & 1 & -1 & 0 & 1
\end{array}
\right)
\xrightarrow{R_3 \leftarrow R_3 + R_2}
\left(
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
0 & 0 & 2 & -1 & 1 & 1
\end{array}
\right).
$$

3. **Step 3 — Scale row $3$ to create a leading $1$ in position $(3,3)$ via $R_3 \leftarrow \frac{1}{2}R_3$:**

$$
\left(
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
0 & 0 & 2 & -1 & 1 & 1
\end{array}
\right)
\xrightarrow{R_3 \leftarrow \frac{1}{2}R_3}
\left(
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2}
\end{array}
\right).
$$

4. **Step 4 — Eliminate the $(2,3)$ entry above the third pivot via $R_2 \leftarrow R_2 - R_3$:**

$$
\left(
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2}
\end{array}
\right)
\xrightarrow{R_2 \leftarrow R_2 - R_3}
\left(
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 0 & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2}
\end{array}
\right).
$$

5. **Step 5 — Eliminate the $(1,2)$ entry above the second pivot via $R_1 \leftarrow R_1 - R_2$:**

$$
\left(
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 0 & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2}
\end{array}
\right)
\xrightarrow{R_1 \leftarrow R_1 - R_2}
\left(
\begin{array}{ccc|ccc}
1 & 0 & 0 & \frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
0 & 1 & 0 & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2}
\end{array}
\right) = [I \mid A^{-1}].
$$

Reading off the $3\times 3$ block on the right yields $A^{-1}$.

<br>

**Property / method used.** *Gauss–Jordan elimination for matrix inversion:* reducing $[A \mid I]$ to reduced row echelon form $[I \mid B]$ multiplies both blocks on the left by the unique net row-operation matrix $E = A^{-1}$, producing $B = A^{-1}$.

<br>

**Mathematical verification.** Multiplying $A$ by the computed inverse $A^{-1}$ confirms that $A A^{-1} = I$:

$$
A A^{-1} =
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1
\end{pmatrix}
\cdot \frac{1}{2}
\begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1
\end{pmatrix} = \frac{1}{2}
\begin{pmatrix}
1 + 1 + 0 & -1 + 1 + 0 & 1 - 1 + 0 \\
0 + 1 - 1 & 0 + 1 + 1 & 0 - 1 + 1 \\
1 + 0 - 1 & -1 + 0 + 1 & 1 + 0 + 1
\end{pmatrix} = \frac{1}{2}
\begin{pmatrix}
2 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 2
\end{pmatrix} =
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix} = I.
$$
