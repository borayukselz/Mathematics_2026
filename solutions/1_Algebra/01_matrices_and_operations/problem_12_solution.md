### Exercise 12. Formula for a Matrix Power

#### Exercise Reminder

Let

$$A= \begin{pmatrix} 1 & 1 \\ 0 & 1 \\ \end{pmatrix}.$$

1. Compute $A^2$, $A^3$, and $A^4$, and use them to formulate a conjecture for $A^n$.
2. Assume the formula is true for $n$, multiply by $A$, and explain why you obtain exactly the formula for $n + 1$.

---

#### Solution

##### 1. Computing $A^2$, $A^3$, $A^4$ and Formulating a Conjecture for $A^n$

**Result.**

$$A^2= \begin{pmatrix} 1 & 2 \\ 0 & 1 \\ \end{pmatrix},\qquad A^3= \begin{pmatrix} 1 & 3 \\ 0 & 1 \\ \end{pmatrix},\qquad A^4= \begin{pmatrix} 1 & 4 \\ 0 & 1 \\ \end{pmatrix}.$$

Conjecture for any positive integer $n \ge 1$:

$$A^n= \begin{pmatrix} 1 & n \\ 0 & 1 \\ \end{pmatrix}.$$

<br>

**Main steps.** Compute each successive power using $A^k = A^{k-1}A$:

$$A^2 = A \cdot A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \\ \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \\ \end{pmatrix}= \begin{pmatrix} 1\cdot 1 + 1\cdot 0 & 1\cdot 1 + 1\cdot 1 \\ 0\cdot 1 + 1\cdot 0 & 0\cdot 1 + 1\cdot 1 \\ \end{pmatrix}= \begin{pmatrix} 1 & 2 \\ 0 & 1 \\ \end{pmatrix},$$

$$A^3 = A^2 \cdot A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \\ \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \\ \end{pmatrix}= \begin{pmatrix} 1\cdot 1 + 2\cdot 0 & 1\cdot 1 + 2\cdot 1 \\ 0\cdot 1 + 1\cdot 0 & 0\cdot 1 + 1\cdot 1 \\ \end{pmatrix}= \begin{pmatrix} 1 & 3 \\ 0 & 1 \\ \end{pmatrix},$$

$$A^4 = A^3 \cdot A = \begin{pmatrix} 1 & 3 \\ 0 & 1 \\ \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \\ \end{pmatrix}= \begin{pmatrix} 1\cdot 1 + 3\cdot 0 & 1\cdot 1 + 3\cdot 1 \\ 0\cdot 1 + 1\cdot 0 & 0\cdot 1 + 1\cdot 1 \\ \end{pmatrix}= \begin{pmatrix} 1 & 4 \\ 0 & 1 \\ \end{pmatrix}.$$

Comparing $A^1, A^2, A^3, A^4$ shows that the diagonal entries remain $1$, the bottom-left entry remains $0$, and the top-right entry equals the exponent $n$, leading to $A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}$.

<br>

**Property / method used.** *Recursive definition of matrix powers and pattern recognition:* positive integer powers of a square matrix satisfy $A^1 = A$ and $A^k = A^{k-1}A$ for $k \ge 2$.

<br>

**Mathematical verification.** Checking $A^4 = A^2 \cdot A^2$ via associativity confirms the fourth power independently:

$$A^2 \cdot A^2 = \begin{pmatrix} 1 & 2 \\ 0 & 1 \\ \end{pmatrix} \begin{pmatrix} 1 & 2 \\ 0 & 1 \\ \end{pmatrix}= \begin{pmatrix} 1\cdot 1 + 2\cdot 0 & 1\cdot 2 + 2\cdot 1 \\ 0\cdot 1 + 1\cdot 0 & 0\cdot 2 + 1\cdot 1 \\ \end{pmatrix}= \begin{pmatrix} 1 & 4 \\ 0 & 1 \\ \end{pmatrix}= A^4.$$

---

##### 2. Inductive Proof from $n$ to $n + 1$

**Result.** Assuming $A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}$ holds for an arbitrary integer $n \ge 1$, multiplying by $A$ produces

$$A^{n+1} = A^n A = \begin{pmatrix} 1 & n + 1 \\ 0 & 1 \\ \end{pmatrix},$$

which is the exact conjectured formula with $n$ replaced by $n + 1$.

<br>

**Main steps.** Start with the inductive hypothesis $A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}$ and multiply on the right by $A$:

$$A^{n+1} = A^n A = \begin{pmatrix} 1 & n \\ 0 & 1 \\ \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \\ \end{pmatrix}= \begin{pmatrix} 1\cdot 1 + n\cdot 0 & 1\cdot 1 + n\cdot 1 \\ 0\cdot 1 + 1\cdot 0 & 0\cdot 1 + 1\cdot 1 \\ \end{pmatrix}= \begin{pmatrix} 1 & n + 1 \\ 0 & 1 \\ \end{pmatrix}.$$

Entry by entry, multiplying by $A$ acts as follows:
- **Position $(1,1)$:** $1\cdot 1 + n\cdot 0 = 1$, leaving the upper-left diagonal entry equal to $1$.
- **Position $(1,2)$:** $1\cdot 1 + n\cdot 1 = n + 1$, adding $1$ to the existing upper-right entry $n$ to yield $n + 1$.
- **Position $(2,1)$:** $0\cdot 1 + 1\cdot 0 = 0$, preserving the zero below the diagonal.
- **Position $(2,2)$:** $0\cdot 1 + 1\cdot 1 = 1$, leaving the lower-right diagonal entry equal to $1$.

Because the base case $n = 1$ holds ($A^1 = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$) and validity for $n$ implies validity for $n + 1$, the formula holds for all positive integers $n \ge 1$.

<br>

**Property / method used.** *Principle of Mathematical Induction:* a statement $P(n)$ holds for all integers $n \ge 1$ when the base case $P(1)$ is true and the inductive step $P(n) \implies P(n + 1)$ holds for every $n \ge 1$.

<br>

**Mathematical verification.** Geometrically, $A$ represents a horizontal shear transformation $\begin{pmatrix} x \\ y \end{pmatrix} \mapsto \begin{pmatrix} x + y \\ y \end{pmatrix}$ that shifts the $x$-coordinate by $y$ while keeping $y$ fixed. Applying this shear $n$ times shifts $x$ by $y$ a total of $n$ times, mapping $\begin{pmatrix} x \\ y \end{pmatrix} \mapsto \begin{pmatrix} x + ny \\ y \end{pmatrix}$, which is represented precisely by $\begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}$. In addition, $\det(A^n) = 1\cdot 1 - n\cdot 0 = 1 = (\det A)^n$ for every $n \ge 1$.
