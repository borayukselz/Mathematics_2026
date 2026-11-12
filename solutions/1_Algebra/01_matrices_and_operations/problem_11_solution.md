### Exercise 11. When Do Matrices Commute?

#### Exercise Reminder

Given the $2\times 2$ matrices

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix},
$$

1. Find the conditions on $a, b, c, d$ under which $AB = BA$.
2. Describe the general form of all such matrices $B$.

---

#### Solution

##### 1. Conditions on $a, b, c, d$ for $AB = BA$

**Result.** The matrices $A$ and $B$ commute ($AB = BA$) if and only if

$$
c = 0 \qquad \text{and} \qquad a = d,
$$

while $b$ can be any arbitrary scalar.

<br>

**Main steps.** Compute both products $AB$ and $BA$ in terms of $a, b, c, d$:

$$
AB=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot a + 1\cdot c & 1\cdot b + 1\cdot d \\
0\cdot a + 1\cdot c & 0\cdot b + 1\cdot d \\
\end{pmatrix}=
\begin{pmatrix}
a + c & b + d \\
c & d \\
\end{pmatrix},
$$

$$
BA=
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
a\cdot 1 + b\cdot 0 & a\cdot 1 + b\cdot 1 \\
c\cdot 1 + d\cdot 0 & c\cdot 1 + d\cdot 1 \\
\end{pmatrix}=
\begin{pmatrix}
a & a + b \\
c & c + d \\
\end{pmatrix}.
$$

Set $AB = BA$:

$$
\begin{pmatrix}
a + c & b + d \\
c & d \\
\end{pmatrix}=
\begin{pmatrix}
a & a + b \\
c & c + d \\
\end{pmatrix}.
$$

Equating corresponding entries in all four positions yields the system of equations:

$$
\begin{aligned}
\text{Position } (1,1): &\quad a + c = a \implies c = 0, \\
\text{Position } (1,2): &\quad b + d = a + b \implies d = a, \\
\text{Position } (2,1): &\quad c = c \quad \text{(always satisfied)}, \\
\text{Position } (2,2): &\quad d = c + d \implies c = 0.
\end{aligned}
$$

Hence, $AB = BA$ holds if and only if $c = 0$ and $a = d$, with no restriction on $b$.

<br>

**Property / method used.** *Definition of matrix equality:* two matrices of the same size are equal if and only if their entries are equal in every $(i,j)$ coordinate position.

<br>

**Mathematical verification.** Substituting $c = 0$ and $d = a$ directly into $AB$ and $BA$ confirms that both products simplify to the exact same matrix:

$$
AB=
\begin{pmatrix}
a + 0 & b + a \\
0 & a \\
\end{pmatrix}=
\begin{pmatrix}
a & a + b \\
0 & a \\
\end{pmatrix},\qquad BA=
\begin{pmatrix}
a & a + b \\
0 & 0 + a \\
\end{pmatrix}=
\begin{pmatrix}
a & a + b \\
0 & a \\
\end{pmatrix}.
$$

---

##### 2. General Form of All Matrices $B$ That Commute with $A$

**Result.** Every matrix $B$ that commutes with $A$ is an upper triangular matrix with equal diagonal entries, having the general form

$$
B=
\begin{pmatrix}
a & b \\
0 & a \\
\end{pmatrix}= aI + bN,
$$

where $a, b \in \mathbb{R}$ are arbitrary scalars, $I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$ is the $2\times 2$ identity matrix, and $N = \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix}$.

<br>

**Main steps.** Replace $c$ by $0$ and $d$ by $a$ in the general $2\times 2$ matrix $B$, then decompose it into a linear combination of $I$ and $N$:

$$
B=
\begin{pmatrix}
a & b \\
0 & a \\
\end{pmatrix}=
\begin{pmatrix}
a & 0 \\
0 & a \\
\end{pmatrix}+
\begin{pmatrix}
0 & b \\
0 & 0 \\
\end{pmatrix}= a
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}+ b
\begin{pmatrix}
0 & 1 \\
0 & 0 \\
\end{pmatrix}= aI + bN.
$$

<br>

**Property / method used.** *Centralizer / polynomial algebra of a matrix:* notice that $A = I + N$, so every commuting matrix $B = aI + bN$ is simply a linear combination of $I$ and $A$ itself (specifically, $B = (a - b)I + bA$).

<br>

**Mathematical verification.** Writing $B = (a - b)I + bA$ and using linearity of matrix multiplication shows immediately why $A$ and $B$ commute for all choices of $a$ and $b$:

$$
AB = A\bigl((a - b)I + bA\bigr) = (a - b)AI + bA^2 = (a - b)IA + bA^2 = \bigl((a - b)I + bA\bigr)A = BA.
$$
