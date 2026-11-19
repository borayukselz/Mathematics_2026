### Exercise 14. A Matrix That Is Its Own Inverse

#### Exercise Reminder

Assume that a square matrix $A$ satisfies

$$
A^2 = I.
$$

Show that

$$
A^{-1} = A.
$$

Then give an example of a $2\times 2$ matrix different from $I$ and $-I$ that satisfies this condition, and verify it by multiplication.

---

#### Solution

**Result.** Any square matrix $A$ satisfying $A^2 = I$ is invertible with $A^{-1} = A$. A concrete $2\times 2$ example different from $I$ and $-I$ is the reflection matrix across the $x$-axis:

$$
A =
\begin{pmatrix}
1 & 0 \\
0 & -1
\end{pmatrix}.
$$

<br>

**Main steps.**

1. **Proof that $A^2 = I \implies A^{-1} = A$:** Rewrite the hypothesis $A^2 = I$ using the definition of the matrix square $A^2 = A \cdot A$:

$$
A \cdot A = I.
$$

By the definition of the matrix inverse, an $n\times n$ matrix $A$ is invertible with inverse $B$ if and only if $AB = I$ and $BA = I$. Setting $B = A$, both conditions hold simultaneously because $A \cdot A = I$. Therefore, $A$ is invertible and

$$
A^{-1} = A.
$$

(Alternatively, taking determinants of both sides of $A^2 = I$ gives $(\det A)^2 = \det(A^2) = \det I = 1 \neq 0$, so $\det A \neq 0$ and $A^{-1}$ exists; multiplying $A^2 = I$ on the left by $A^{-1}$ then yields $A^{-1}A^2 = A^{-1}I \implies (A^{-1}A)A = A^{-1} \implies IA = A^{-1} \implies A = A^{-1}$.)

2. **Constructing a nontrivial $2\times 2$ example:** Choose the diagonal reflection matrix

$$
A =
\begin{pmatrix}
1 & 0 \\
0 & -1
\end{pmatrix}.
$$

Clearly $A \neq I$ (since the $(2,2)$ entry is $-1 \neq 1$) and $A \neq -I$ (since the $(1,1)$ entry is $1 \neq -1$). Geometrically, $A$ reflects vectors across the horizontal axis, and reflecting twice restores every vector to its original position.

<br>

**Property / method used.** *Involutory matrices and the definition of the inverse:* a square matrix satisfying $A^2 = I$ is called an *involution*; because $A$ acts as both its own left and right inverse ($AA = I$), uniqueness of the inverse guarantees $A^{-1} = A$.

<br>

**Mathematical verification.** Multiplying the example matrix $A$ by itself directly confirms that $A^2 = I$:

$$
A^2 = A \cdot A =
\begin{pmatrix}
1 & 0 \\
0 & -1
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
0 & -1
\end{pmatrix} =
\begin{pmatrix}
1\cdot 1 + 0\cdot 0 & 1\cdot 0 + 0\cdot (-1) \\
0\cdot 1 + (-1)\cdot 0 & 0\cdot 0 + (-1)\cdot (-1)
\end{pmatrix} =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} = I.
$$
