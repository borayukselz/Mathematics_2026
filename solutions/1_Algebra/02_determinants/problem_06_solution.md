### Exercise 6. Parameter and Invertibility

#### Exercise Reminder

For

$$A(t)= \begin{pmatrix} t & 1 \\ 2 & t \\ \end{pmatrix},$$

1. Find all values of $t$ for which the matrix is not invertible.
2. Explain how your answer is related to the determinant being zero.

---

#### Solution

##### 1. Values of $t$ for Which $A(t)$ Is Not Invertible

**Result.** The matrix $A(t)$ is not invertible for

$$t = \sqrt{2} \qquad \text{and} \qquad t = -\sqrt{2} \qquad (\text{i.e., } t = \pm\sqrt{2}).$$

<br>

**Main steps.** Compute the determinant of the $2\times 2$ matrix $A(t)$ as a function of the parameter $t$:

$$\det A(t) = t \cdot t - 1 \cdot 2 = t^2 - 2.$$

Set $\det A(t) = 0$ and solve for $t$:

$$t^2 - 2 = 0 \implies t^2 = 2 \implies t = \pm\sqrt{2}.$$

Thus, $A(t)$ fails to be invertible exclusively when $t = \sqrt{2}$ or $t = -\sqrt{2}$.

<br>

**Property / method used.** *Determinant singularity criterion:* a square matrix $A(t)$ is singular (not invertible) if and only if $\det A(t) = 0$.

<br>

**Mathematical verification.** For any $t \neq \pm\sqrt{2}$, the explicit inverse of $A(t)$ is

$$A(t)^{-1} = \frac{1}{t^2 - 2} \begin{pmatrix} t & -1 \\ -2 & t \\ \end{pmatrix},$$

which involves division by $t^2 - 2$ and therefore exists if and only if $t^2 - 2 \neq 0$, confirming that $t = \pm\sqrt{2}$ are the exact values where $A(t)^{-1}$ fails to exist.

---

##### 2. Relation to the Determinant Being Zero

**Result.** By the Invertible Matrix Theorem, an $n\times n$ matrix is invertible if and only if its determinant is nonzero; therefore, the values $t = \pm\sqrt{2}$ where $A(t)$ loses invertibility are precisely the roots of the equation $\det A(t) = 0$, at which the rows (and columns) of $A(t)$ become linearly dependent.

<br>

**Main steps.**
1. **Algebraic connection:** A square matrix $M$ has a multiplicative inverse $M^{-1}$ satisfying $MM^{-1} = I$ if and only if $\det M \neq 0$. Setting $\det A(t) = t^2 - 2 = 0$ directly characterizes the singular cases in the parameter family $A(t)$.
2. **Row-dependence interpretation:** When $\det A(t) = 0$, the two rows of $A(t)$ become scalar multiples of one another:
   - At $t = \sqrt{2}$, $A(\sqrt{2}) = \begin{pmatrix} \sqrt{2} & 1 \\ 2 & \sqrt{2} \end{pmatrix}$ satisfies $R_2 = \sqrt{2}R_1$.
   - At $t = -\sqrt{2}$, $A(-\sqrt{2}) = \begin{pmatrix} -\sqrt{2} & 1 \\ 2 & -\sqrt{2} \end{pmatrix}$ satisfies $R_2 = -\sqrt{2}R_1$.
3. Because the rows collapse onto a single line (rank $1 < 2$), $A(t)$ maps nonzero vectors to the zero vector and cannot be inverted.

<br>

**Property / method used.** *Invertible Matrix Theorem (determinant and linear dependence equivalence):* for a $2\times 2$ matrix $M$, $\det M = 0 \iff M \text{ is not invertible} \iff \text{the rows/columns of } M \text{ are linearly dependent}$.

<br>

**Mathematical verification.** Substituting $t = \sqrt{2}$ and $t = -\sqrt{2}$ directly into $\det A(t)$ confirms that both yield a zero determinant:

$$\det A(\sqrt{2}) = \det \begin{pmatrix} \sqrt{2} & 1 \\ 2 & \sqrt{2} \\ \end{pmatrix}= (\sqrt{2})(\sqrt{2}) - (1)(2) = 2 - 2 = 0,$$

$$\det A(-\sqrt{2}) = \det \begin{pmatrix} -\sqrt{2} & 1 \\ 2 & -\sqrt{2} \\ \end{pmatrix}= (-\sqrt{2})(-\sqrt{2}) - (1)(2) = 2 - 2 = 0.$$
