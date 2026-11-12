### Exercise 3. Swapping Two Rows

#### Exercise Reminder

For

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 3 & 1 \\
2 & 1 & 1 \\
\end{pmatrix},
$$

1. Compute $\det A$.
2. Form a matrix $B$ by swapping the first and second rows of $A$. First predict $\det B$ using a determinant property, and then verify your prediction by calculation.

---

#### Solution

##### 1. Computing $\det A$

**Result.**

$$
\det A = 6.
$$

<br>

**Main steps.** Compute $\det A$ using cofactor expansion along the first row (taking advantage of the zero entry in position $(1,3)$):

$$
\begin{aligned}
\det A &= 1\cdot \det
\begin{pmatrix}
3 & 1 \\
1 & 1 \\
\end{pmatrix}- 2\cdot \det
\begin{pmatrix}
0 & 1 \\
2 & 1 \\
\end{pmatrix}+ 0\cdot \det
\begin{pmatrix}
0 & 3 \\
2 & 1 \\
\end{pmatrix} \\
&= 1(3\cdot 1 - 1\cdot 1) - 2(0\cdot 1 - 1\cdot 2) + 0 \\
&= 1(2) - 2(-2) \\
&= 2 + 4 = 6.
\end{aligned}
$$

<br>

**Property / method used.** *Cofactor expansion along a row:* for any $3\times 3$ matrix $A$, expanding along row $1$ gives $\det A = a_{11}C_{11} + a_{12}C_{12} + a_{13}C_{13}$, where $C_{ij} = (-1)^{i+j}M_{ij}$ is the $(i,j)$-cofactor.

<br>

**Mathematical verification.** Checking $\det A$ with Sarrus' rule confirms the result:

$$
\det A = (1\cdot 3\cdot 1 + 2\cdot 1\cdot 2 + 0\cdot 0\cdot 1) - (2\cdot 3\cdot 0 + 1\cdot 1\cdot 1 + 1\cdot 0\cdot 2) = (3 + 4 + 0) - (0 + 1 + 0) = 7 - 1 = 6.
$$

---

##### 2. Forming $B$, Predicting $\det B$, and Verifying by Calculation

**Result.** Swapping rows $1$ and $2$ of $A$ gives

$$
B=
\begin{pmatrix}
0 & 3 & 1 \\
1 & 2 & 0 \\
2 & 1 & 1 \\
\end{pmatrix}.
$$

- **Prediction:** $\det B = -6$.
- **Calculated value:** $\det B = -6$ (confirming the prediction).

<br>

**Main steps.**

1. **Form $B$ and predict $\det B$:** Interchange the first and second rows of $A$ ($R_1 \leftrightarrow R_2$) to obtain $B$:

$$
B=
\begin{pmatrix}
0 & 3 & 1 \\
1 & 2 & 0 \\
2 & 1 & 1 \\
\end{pmatrix}.
$$

Because $B$ is obtained from $A$ by a single row interchange, its determinant must have the opposite sign of $\det A$:

$$
\det B = -\det A = -6.
$$

2. **Verify by direct calculation:** Expand $\det B$ by cofactors along the first row of $B$:

$$
\begin{aligned}
\det B &= 0\cdot \det
\begin{pmatrix}
2 & 0 \\
1 & 1 \\
\end{pmatrix}- 3\cdot \det
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
\end{pmatrix}+ 1\cdot \det
\begin{pmatrix}
1 & 2 \\
2 & 1 \\
\end{pmatrix} \\
&= 0 - 3(1\cdot 1 - 0\cdot 2) + 1(1\cdot 1 - 2\cdot 2) \\
&= -3(1) + 1(-3) \\
&= -3 - 3 = -6.
\end{aligned}
$$

<br>

**Property / method used.** *Alternating (row-swap) property of determinants:* interchanging any two distinct rows of a square matrix reverses the sign of its determinant (multiplies the determinant by $-1$).

<br>

**Mathematical verification.** Checking $\det B$ via Sarrus' rule provides an independent verification of the sign reversal:

$$
\det B = (0\cdot 2\cdot 1 + 3\cdot 0\cdot 2 + 1\cdot 1\cdot 1) - (2\cdot 2\cdot 1 + 1\cdot 0\cdot 0 + 1\cdot 1\cdot 3) = (0 + 0 + 1) - (4 + 0 + 3) = 1 - 7 = -6.
$$
