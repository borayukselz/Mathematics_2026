### Exercise 7. Identity Matrix, Zero Matrix, and Powers

#### Exercise Reminder

Given the $2\times 2$ matrix

$$
A=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix},
$$

1. Compute $AI$, $IA$, $A+0$, $A^2$, and $A^3$.
2. Explain the roles of the matrices $I$ and $0$, and describe the pattern you observe in successive powers of $A$.

---

#### Solution

##### 1. Computing $AI$, $IA$, $A+0$, $A^2$, and $A^3$

**Result.**

$$
AI = IA = A + 0 =
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix},\qquad A^2 =
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix},\qquad A^3 =
\begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}.
$$

**Main steps.** Since $A$ has size $2\times 2$, the compatible identity matrix $I$ and zero matrix $0$ also have size $2\times 2$:

$$
I=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad 0=
\begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix}.
$$

First, compute $AI$, $IA$, and $A+0$:

$$
AI=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
2\cdot 1 + 1\cdot 0 & 2\cdot 0 + 1\cdot 1 \\
0\cdot 1 + 2\cdot 0 & 0\cdot 0 + 2\cdot 1 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix},
$$

$$
IA=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot 2 + 0\cdot 0 & 1\cdot 1 + 0\cdot 2 \\
0\cdot 2 + 1\cdot 0 & 0\cdot 1 + 1\cdot 2 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix},
$$

$$
A+0=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}+
\begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
2+0 & 1+0 \\
0+0 & 2+0 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}.
$$

Next, compute $A^2 = AA$ and $A^3 = A^2 A$:

$$
A^2=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}=
\begin{pmatrix}
2\cdot 2 + 1\cdot 0 & 2\cdot 1 + 1\cdot 2 \\
0\cdot 2 + 2\cdot 0 & 0\cdot 1 + 2\cdot 2 \\
\end{pmatrix}=
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix},
$$

$$
A^3 = A^2 A =
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}=
\begin{pmatrix}
4\cdot 2 + 4\cdot 0 & 4\cdot 1 + 4\cdot 2 \\
0\cdot 2 + 4\cdot 0 & 0\cdot 1 + 4\cdot 2 \\
\end{pmatrix}=
\begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}.
$$

**Property / method used.** *Identity and zero matrix axioms and recursive matrix powers:* for any square matrix $A$, $AI = IA = A$ and $A + 0 = A$, while positive integer powers are defined recursively by $A^1 = A$ and $A^k = A^{k-1}A$ for $k \ge 2$.

**Mathematical verification.** Because matrix multiplication is associative, computing $A^3$ as $A(A^2)$ instead of $(A^2)A$ must yield the exact same matrix:

$$
A(A^2)=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}=
\begin{pmatrix}
2\cdot 4 + 1\cdot 0 & 2\cdot 4 + 1\cdot 4 \\
0\cdot 4 + 2\cdot 0 & 0\cdot 4 + 2\cdot 4 \\
\end{pmatrix}=
\begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}.
$$

In addition, determinants satisfy $\det(A^k) = (\det(A))^k$: since $\det(A) = 2\cdot 2 - 1\cdot 0 = 4$, we get $\det(A^2) = 4\cdot 4 = 16 = 4^2$ and $\det(A^3) = 8\cdot 8 = 64 = 4^3$.

##### 2. Roles of $I$ and $0$, and Pattern in Successive Powers of $A$

**Result.**
- **Role of $I$:** The identity matrix $I$ is the *multiplicative identity* (neutral element for matrix multiplication), leaving any compatible matrix unchanged ($AI = IA = A$).
- **Role of $0$:** The zero matrix $0$ is the *additive identity* (neutral element for matrix addition), leaving any matrix of the same size unchanged ($A + 0 = 0 + A = A$).
- **Pattern in powers of $A$:** For every integer $n \ge 1$, the $n$-th power of $A$ has the closed form

$$
A^n=
\begin{pmatrix}
2^n & n\cdot 2^{n-1} \\
0 & 2^n \\
\end{pmatrix}.
$$

**Main steps.** Comparing $A^1$, $A^2$, and $A^3$ reveals a clear structure in each entry:
- **Main diagonal entries:** $(A^1)_{11} = (A^1)_{22} = 2^1 = 2$, $(A^2)_{11} = (A^2)_{22} = 2^2 = 4$, and $(A^3)_{11} = (A^3)_{22} = 2^3 = 8$, following $2^n$.
- **Lower-left entry:** $(A^n)_{21} = 0$ remains $0$ for all $n \ge 1$ because $A$ is upper triangular.
- **Upper-right entry:** $(A^1)_{12} = 1 = 1\cdot 2^0$, $(A^2)_{12} = 4 = 2\cdot 2^1$, and $(A^3)_{12} = 12 = 3\cdot 2^2$, following $n\cdot 2^{n-1}$.

**Property / method used.** *Jordan-block / nilpotent decomposition:* writing $A = 2I + N$, where $N = \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix}$ satisfies $N^2 = 0$ and commutes with $2I$, allows applying the binomial theorem to $(2I + N)^n$.

**Mathematical verification.** Since $(2I)N = N(2I)$ and $N^k = 0$ for all $k \ge 2$, all higher-order terms in the binomial expansion vanish:

$$
A^n = (2I + N)^n = (2I)^n + n(2I)^{n-1}N = 2^n
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix} + n\cdot 2^{n-1}
\begin{pmatrix}
0 & 1 \\
0 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
2^n & n\cdot 2^{n-1} \\
0 & 2^n \\
\end{pmatrix}.
$$

Substituting $n = 1, 2, 3$ reproduces $A$, $A^2$, and $A^3$ exactly.
