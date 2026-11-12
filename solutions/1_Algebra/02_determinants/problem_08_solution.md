### Exercise 8. Determinant of a Product

#### Exercise Reminder

Let $A, B$ be square matrices such that $\det A = 3$ and $\det B = -5$.

1. Compute $\det(AB)$, $\det(BA)$, and, if it exists, $\det(A^{-1}B)$.
2. Explain why the first two results are equal even though usually $AB \neq BA$.

---

#### Solution

##### 1. Computing $\det(AB)$, $\det(BA)$, and $\det(A^{-1}B)$

**Result.**

$$\det(AB) = -15,\qquad \det(BA) = -15,\qquad \det(A^{-1}B) = -\frac{5}{3}.$$

<br>

**Main steps.** Note that $AB$ and $BA$ are both defined, which implies $A$ and $B$ are square matrices of the same size $n\times n$.

1. **Computing $\det(AB)$:** Apply the multiplicative property $\det(XY) = \det(X)\det(Y)$:

$$\det(AB) = (\det A)(\det B) = 3 \cdot (-5) = -15.$$

2. **Computing $\det(BA)$:** Apply the multiplicative property in reversed matrix order:

$$\det(BA) = (\det B)(\det A) = (-5) \cdot 3 = -15.$$

3. **Existence and computation of $\det(A^{-1}B)$:** Because $\det A = 3 \neq 0$, the matrix $A$ is invertible, so $A^{-1}$ exists and has the same size $n\times n$ as $B$. Using $\det(A^{-1}) = (\det A)^{-1}$ together with multiplicativity gives

$$\det(A^{-1}B) = \det(A^{-1})\det(B) = \frac{1}{\det A}\,\det B = \frac{1}{3} \cdot (-5) = -\frac{5}{3}.$$

<br>

**Property / method used.** *Multiplicativity and inverse rule for determinants:* for any $n\times n$ matrices $A$ and $B$,

$$\det(AB) = \det(A)\det(B), \qquad \text{and when } \det A \neq 0, \qquad \det(A^{-1}) = \frac{1}{\det A}.$$

<br>

**Mathematical verification.** Choose two concrete $2\times 2$ matrices satisfying $\det A = 3$ and $\det B = -5$, such as

$$A= \begin{pmatrix} 3 & 1 \\ 0 & 1 \\ \end{pmatrix},\qquad B= \begin{pmatrix} 1 & 0 \\ 2 & -5 \\ \end{pmatrix}.$$

Computing the matrix products explicitly gives

$$AB= \begin{pmatrix} 5 & -5 \\ 2 & -5 \\ \end{pmatrix} \implies \det(AB) = 5(-5) - (-5)(2) = -25 + 10 = -15,$$

$$BA= \begin{pmatrix} 3 & 1 \\ 6 & -3 \\ \end{pmatrix} \implies \det(BA) = 3(-3) - 1(6) = -9 - 6 = -15,$$

$$A^{-1}B = \frac{1}{3} \begin{pmatrix} 1 & -1 \\ 0 & 3 \\ \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 2 & -5 \\ \end{pmatrix}= \frac{1}{3} \begin{pmatrix} -1 & 5 \\ 6 & -15 \\ \end{pmatrix} \implies \det(A^{-1}B) = \left(\frac{1}{3}\right)^2 (15 - 30) = -\frac{5}{3},$$

confirming all three results.

---

##### 2. Why $\det(AB) = \det(BA)$ Even Though Usually $AB \neq BA$

**Result.** Although $AB$ and $BA$ are generally different matrices, the determinant maps each matrix to a single real (or complex) number, and multiplication of numbers is commutative:

$$\det(AB) = (\det A)(\det B) = (\det B)(\det A) = \det(BA).$$

<br>

**Main steps.**
1. Matrix multiplication combines rows and columns in order-dependent dot products, so swapping the factors generally changes the entries of the resulting matrix ($AB \neq BA$, as seen in the verification matrices above where $AB$ and $BA$ have different entries).
2. However, the determinant satisfies $\det(XY) = \det(X)\det(Y)$, turning matrix multiplication into ordinary scalar multiplication.
3. Since real and complex numbers commute under multiplication ($xy = yx$), the scalar product $(\det A)(\det B)$ equals $(\det B)(\det A)$, forcing $\det(AB) = \det(BA)$ for all $n\times n$ matrices $A$ and $B$.

<br>

**Property / method used.** *Homomorphism property of the determinant:* the determinant $\det : M_n(\mathbb{R}) \to \mathbb{R}$ maps a noncommutative matrix ring into a commutative field, converting noncommutative matrix products into commutative scalar products.

<br>

**Mathematical verification.** Using the verification matrices from Part 1, notice that

$$AB = \begin{pmatrix} 5 & -5 \\ 2 & -5 \\ \end{pmatrix} \neq \begin{pmatrix} 3 & 1 \\ 6 & -3 \\ \end{pmatrix}= BA,$$

yet both matrices evaluate to the exact same determinant $-15$.
