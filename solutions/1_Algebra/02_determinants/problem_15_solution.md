### Exercise 15. Combining Determinant Properties

#### Exercise Reminder

Let $A$ and $B$ be invertible $2\times 2$ matrices with

$$
\det A = -2,\qquad \det B = 3.
$$

Without finding the entries of the matrices:

1. Compute $\det\left(B^{-1} A^T B\right)$ and state the determinant properties used in order.
2. Explain why the factors involving $B$ eventually cancel.

---

#### Solution

##### 1. Computing $\det\left(B^{-1} A^T B\right)$ and Properties Used in Order

**Result.**

$$
\det\left(B^{-1} A^T B\right) = -2.
$$

<br>

**Main steps.** Apply the determinant identities step by step without forming the entries of $A$ or $B$:

1. **Step 1 — Split the product of three matrices (Multiplicativity):**

$$
\det\left(B^{-1} A^T B\right) = \det\left(B^{-1}\right)\det\left(A^T\right)\det(B).
$$

2. **Step 2 — Evaluate $\det\left(B^{-1}\right)$ (Inverse property):** Because $B$ is invertible ($\det B = 3 \neq 0$),

$$
\det\left(B^{-1}\right) = \frac{1}{\det B} = \frac{1}{3}.
$$

3. **Step 3 — Evaluate $\det\left(A^T\right)$ (Transpose invariance):**

$$
\det\left(A^T\right) = \det A = -2.
$$

4. **Step 4 — Substitute the known values and simplify:**

$$
\det\left(B^{-1} A^T B\right) = \left(\frac{1}{\det B}\right)(\det A)(\det B) = \frac{1}{3} \cdot (-2) \cdot 3 = -2.
$$

<br>

**Property / method used.** *Determinant properties applied in order:*
1. **Multiplicativity of the determinant:** $\det(XYZ) = \det(X)\det(Y)\det(Z)$ for any square matrices $X, Y, Z$ of the same size.
2. **Determinant of an inverse:** $\det(B^{-1}) = (\det B)^{-1} = \dfrac{1}{\det B}$ for any invertible matrix $B$.
3. **Transpose invariance:** $\det(A^T) = \det A$ for any square matrix $A$.

<br>

**Mathematical verification.** Choose two concrete $2\times 2$ matrices satisfying $\det A = -2$ and $\det B = 3$, such as

$$
A=
\begin{pmatrix}
-2 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
3 & 1 \\
0 & 1 \\
\end{pmatrix}.
$$

Then

$$
A^T=
\begin{pmatrix}
-2 & 0 \\
1 & 1 \\
\end{pmatrix},\qquad B^{-1} = \frac{1}{3}
\begin{pmatrix}
1 & -1 \\
0 & 3 \\
\end{pmatrix}.
$$

Multiplying $B^{-1} A^T B$ explicitly gives

$$
B^{-1} A^T B = \frac{1}{3}
\begin{pmatrix}
1 & -1 \\
0 & 3 \\
\end{pmatrix}
\begin{pmatrix}
-2 & 0 \\
1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
3 & 1 \\
0 & 1 \\
\end{pmatrix}= \frac{1}{3}
\begin{pmatrix}
-3 & -1 \\
3 & 3 \\
\end{pmatrix}
\begin{pmatrix}
3 & 1 \\
0 & 1 \\
\end{pmatrix}= \frac{1}{3}
\begin{pmatrix}
-9 & -4 \\
9 & 6 \\
\end{pmatrix}=
\begin{pmatrix}
-3 & -\frac{4}{3} \\
3 & 2 \\
\end{pmatrix}.
$$

Computing the determinant of this resulting matrix directly yields

$$
\det\left(B^{-1} A^T B\right) = (-3)(2) - \left(-\frac{4}{3}\right)(3) = -6 - (-4) = -6 + 4 = -2,
$$

confirming the property-based calculation.

---

##### 2. Why the Factors Involving $B$ Cancel

**Result.** Although $B^{-1}$ and $B$ are not adjacent inside the matrix product $B^{-1} A^T B$ (and matrix multiplication is noncommutative), taking the determinant converts the matrix product into a product of ordinary nonzero real numbers, which commute and allow $\frac{1}{\det B}$ and $\det B$ to cancel to $1$.

<br>

**Main steps.**
1. **Noncommutativity vs. scalar commutativity:** Inside the matrix expression $B^{-1} A^T B$, $B^{-1}$ and $B$ are separated by $A^T$, so they cannot be canceled at the matrix level unless $A^T$ and $B$ happen to commute.
2. **Conversion to real numbers via $\det$:** Applying $\det$ turns matrix multiplication into multiplication of real scalars:

$$
\det\left(B^{-1} A^T B\right) = \det\left(B^{-1}\right)\det\left(A^T\right)\det(B).
$$

3. **Cancellation of reciprocal scalars:** Since $B$ is invertible, $\det B = 3 \neq 0$, and $\det\left(B^{-1}\right) = \frac{1}{\det B}$. Because multiplication of real numbers is commutative and associative, we can rearrange the scalar factors so that $\frac{1}{\det B}$ and $\det B$ pair together:

$$
\det\left(B^{-1}\right)\det\left(A^T\right)\det(B) = \left(\frac{1}{\det B} \cdot \det B\right)\det\left(A^T\right) = 1 \cdot \det\left(A^T\right) = \det A = -2.
$$

<br>

**Property / method used.** *Similarity invariance of the determinant:* for any square matrix $M$ and any invertible matrix $B$ of the same size, the conjugate (similar) matrix $B^{-1}MB$ represents the same linear operator in a different basis and always has the identical determinant:

$$
\det\left(B^{-1}MB\right) = \det M.
$$

<br>

**Mathematical verification.** Setting $M = A^T$ in the similarity invariance identity immediately gives

$$
\det\left(B^{-1} A^T B\right) = \det\left(A^T\right) = \det A = -2,
$$

showing that the result depends solely on $\det A$ and is completely independent of the choice of invertible matrix $B$.
