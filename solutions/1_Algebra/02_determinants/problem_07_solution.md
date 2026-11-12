### Exercise 7. Using Properties Instead of Recomputing

#### Exercise Reminder

Suppose that for a $3\times 3$ matrix $A$, $\det A = -4$. Compute

$$
\det(2A),\qquad \det(A^T),\qquad \det(A^2),\qquad \det(-A).
$$

Justify each answer using the appropriate property.

---

#### Solution

**Result.**

$$
\det(2A) = -32,\qquad \det(A^T) = -4,\qquad \det(A^2) = 16,\qquad \det(-A) = 4.
$$

<br>

**Main steps.** Here the matrix dimension is $n = 3$ and $\det A = -4$. Apply the corresponding determinant identity to each expression:

- **Computing $\det(2A)$:** Multiplying a $3\times 3$ matrix by the scalar $c = 2$ multiplies each of its $3$ rows by $2$, scaling the determinant by $2^3$:

$$
\det(2A) = 2^3 \det A = 8 \cdot (-4) = -32.
$$

- **Computing $\det(A^T)$:** Transposing a square matrix leaves its determinant unchanged:

$$
\det(A^T) = \det A = -4.
$$

- **Computing $\det(A^2)$:** Using the multiplicative property $\det(AB) = \det(A)\det(B)$ with $B = A$:

$$
\det(A^2) = \det(A \cdot A) = (\det A)^2 = (-4)^2 = 16.
$$

- **Computing $\det(-A)$:** Since $-A = (-1)A$ and $A$ has size $3\times 3$, apply the scalar-multiple rule with $c = -1$ and $n = 3$:

$$
\det(-A) = \det\bigl((-1)A\bigr) = (-1)^3 \det A = (-1) \cdot (-4) = 4.
$$

<br>

**Property / method used.** *Algebraic properties of determinants for an $n\times n$ matrix $A$:*
- **Scalar multiplication:** $\det(cA) = c^n \det A$ for any scalar $c$.
- **Transpose invariance:** $\det(A^T) = \det A$.
- **Multiplicativity (powers):** $\det(AB) = \det(A)\det(B)$, so $\det(A^k) = (\det A)^k$ for any integer $k \ge 1$.
- **Negation:** $\det(-A) = (-1)^n \det A$ (which reverses the sign of $\det A$ when $n$ is odd).

<br>

**Mathematical verification.** Choosing a concrete $3\times 3$ diagonal matrix with $\det A = -4$, such as

$$
A=
\begin{pmatrix}
-4 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix},
$$

and evaluating each matrix explicitly confirms all four results:

$$
2A=
\begin{pmatrix}
-8 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 2 \\
\end{pmatrix}
\implies \det(2A) = (-8)\cdot 2\cdot 2 = -32,
$$

$$
A^T=
\begin{pmatrix}
-4 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}
\implies \det(A^T) = (-4)\cdot 1\cdot 1 = -4,
$$

$$
A^2=
\begin{pmatrix}
16 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}
\implies \det(A^2) = 16\cdot 1\cdot 1 = 16,
$$

$$
-A=
\begin{pmatrix}
4 & 0 & 0 \\
0 & -1 & 0 \\
0 & 0 & -1 \\
\end{pmatrix}
\implies \det(-A) = 4\cdot (-1)\cdot (-1) = 4.
$$
