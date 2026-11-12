### Exercise 1. Determinant of a $2\times 2$ Matrix

#### Exercise Reminder

Compute

$$
\det
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix},\qquad \det
\begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix}.
$$

Which matrix is invertible? Justify your answer.

---

#### Solution

##### 1. Computing Both $2\times 2$ Determinants

**Result.**

$$
\det
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix}= 22,\qquad \det
\begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix}= 0.
$$

<br>

**Main steps.** Let

$$
A=
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix}.
$$

Apply the $2\times 2$ determinant formula $\det\begin{pmatrix} a & b \\ c & d \end{pmatrix} = ad - bc$ to each matrix:

$$
\det(A) = 3\cdot 4 - (-2)\cdot 5 = 12 - (-10) = 12 + 10 = 22,
$$

$$
\det(B) = 1\cdot 14 - 7\cdot 2 = 14 - 14 = 0.
$$

<br>

**Property / method used.** *Closed-form $2\times 2$ determinant formula:* for any $2\times 2$ matrix, the determinant equals the product of the main diagonal entries minus the product of the off-diagonal entries:

$$
\det
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}= ad - bc.
$$

<br>

**Mathematical verification.** Using the transpose invariance property $\det(M^T) = \det(M)$ confirms both calculations:

$$
\det(A^T) = \det
\begin{pmatrix}
3 & 5 \\
-2 & 4 \\
\end{pmatrix}= 3\cdot 4 - 5\cdot (-2) = 12 + 10 = 22 = \det(A),
$$

$$
\det(B^T) = \det
\begin{pmatrix}
1 & 2 \\
7 & 14 \\
\end{pmatrix}= 1\cdot 14 - 2\cdot 7 = 14 - 14 = 0 = \det(B).
$$

---

##### 2. Invertibility Check and Justification

**Result.** Only the first matrix,

$$
A=
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix},
$$

is invertible. The second matrix $B$ is singular (not invertible).

<br>

**Main steps.**
1. For matrix $A$, $\det(A) = 22 \neq 0$, so $A$ has a nonzero determinant and therefore possesses a unique inverse $A^{-1}$.
2. For matrix $B$, $\det(B) = 0$. Notice that the second row of $B$ is an exact scalar multiple of the first row ($R_2$ equals $2R_1$, since $\begin{pmatrix} 2 & 14 \end{pmatrix} = 2\begin{pmatrix} 1 & 7 \end{pmatrix}$), making the rows linearly dependent and preventing $B$ from having an inverse.

<br>

**Property / method used.** *Determinant criterion for invertibility:* an $n\times n$ square matrix $M$ is invertible if and only if its determinant is nonzero ($\det(M) \neq 0$).

<br>

**Mathematical verification.** Constructing the explicit inverse of $A$ using the $2\times 2$ inverse formula confirms that $A A^{-1} = I$:

$$
A^{-1} = \frac{1}{\det(A)}
\begin{pmatrix}
4 & 2 \\
-5 & 3 \\
\end{pmatrix}= \frac{1}{22}
\begin{pmatrix}
4 & 2 \\
-5 & 3 \\
\end{pmatrix},
$$

$$
A A^{-1} = \frac{1}{22}
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix}
\begin{pmatrix}
4 & 2 \\
-5 & 3 \\
\end{pmatrix}= \frac{1}{22}
\begin{pmatrix}
12 + 10 & 6 - 6 \\
20 - 20 & 10 + 12 \\
\end{pmatrix}= \frac{1}{22}
\begin{pmatrix}
22 & 0 \\
0 & 22 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}= I.
$$
