### Exercise 10. Inverse of a Diagonal Matrix

#### Exercise Reminder

Given

$$
D =
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5
\end{pmatrix},\qquad E =
\begin{pmatrix}
2 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 5
\end{pmatrix}.
$$

Without using Gauss–Jordan elimination, decide which matrix is invertible. For the invertible matrix, give the inverse and check the result by multiplication.

---

#### Solution

**Result.** The matrix **$D$ is invertible**, whereas **$E$ is not invertible** (singular). The inverse of $D$ is

$$
D^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 & 0 \\
0 & -\frac{1}{3} & 0 \\
0 & 0 & \frac{1}{5}
\end{pmatrix}.
$$

<br>

**Main steps.**

1. **Decide which matrix is invertible:** A diagonal matrix is invertible if and only if every entry on its main diagonal is nonzero (equivalently, its determinant, which is the product of the diagonal entries, is nonzero):
   - For $D$, all three diagonal entries are nonzero ($2 \neq 0$, $-3 \neq 0$, and $5 \neq 0$), and $\det D = 2 \cdot (-3) \cdot 5 = -30 \neq 0$. Therefore, $D$ is invertible.
   - For $E$, the $(2,2)$ diagonal entry is $0$ (producing an entire row and column of zeros), and $\det E = 2 \cdot 0 \cdot 5 = 0$. Therefore, $E$ is not invertible.

2. **Write down $D^{-1}$ directly:** The inverse of an invertible diagonal matrix is obtained by replacing each diagonal entry $d_{ii}$ with its reciprocal $d_{ii}^{-1}$ while keeping all off-diagonal entries $0$:

$$
D^{-1} =
\begin{pmatrix}
2^{-1} & 0 & 0 \\
0 & (-3)^{-1} & 0 \\
0 & 0 & 5^{-1}
\end{pmatrix} =
\begin{pmatrix}
\frac{1}{2} & 0 & 0 \\
0 & -\frac{1}{3} & 0 \\
0 & 0 & \frac{1}{5}
\end{pmatrix}.
$$

<br>

**Property / method used.** *Invertibility and inverse of a diagonal matrix:* a diagonal matrix $D = \mathrm{diag}(d_1, d_2, \dots, d_n)$ is invertible if and only if $d_i \neq 0$ for every $i = 1, \dots, n$, in which case

$$
D^{-1} = \mathrm{diag}(d_1^{-1}, d_2^{-1}, \dots, d_n^{-1}).
$$

<br>

**Mathematical verification.** Multiplying $D$ by $D^{-1}$ confirms that their product is the $3\times 3$ identity matrix $I$:

$$
D D^{-1} =
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & 0 & 0 \\
0 & -\frac{1}{3} & 0 \\
0 & 0 & \frac{1}{5}
\end{pmatrix} =
\begin{pmatrix}
2 \cdot \frac{1}{2} & 0 & 0 \\
0 & (-3) \cdot \left(-\frac{1}{3}\right) & 0 \\
0 & 0 & 5 \cdot \frac{1}{5}
\end{pmatrix} =
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix} = I.
$$
