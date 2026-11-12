### Exercise 2. Addition and Scalar Multiplication

#### Exercise Reminder

Given the $2\times 2$ matrices

$$
A=
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix},
$$

1. Compute $A+B$, $A-B$, and $3A-2B$.
2. Explain why matrix addition is possible only for matrices of the same size.

---

#### Solution

##### 1. Computing $A+B$, $A-B$, and $3A-2B$

**Result.**

$$
A+B=
\begin{pmatrix}
5 & 0 \\
-1 & 8 \\
\end{pmatrix},\qquad A-B=
\begin{pmatrix}
-3 & 4 \\
-1 & -2 \\
\end{pmatrix},\qquad 3A-2B=
\begin{pmatrix}
-5 & 10 \\
-3 & -1 \\
\end{pmatrix}.
$$

**Main steps.** Both $A$ and $B$ have size $2\times 2$, so all three operations are defined and produce $2\times 2$ matrices.

For $A+B$, add the entries in matching $(i,j)$ positions:

$$
A+B=
\begin{pmatrix}
1+4 & 2+(-2) \\
-1+0 & 3+5 \\
\end{pmatrix}=
\begin{pmatrix}
5 & 0 \\
-1 & 8 \\
\end{pmatrix}.
$$

For $A-B$, subtract each entry of $B$ from the corresponding entry of $A$:

$$
A-B=
\begin{pmatrix}
1-4 & 2-(-2) \\
-1-0 & 3-5 \\
\end{pmatrix}=
\begin{pmatrix}
-3 & 4 \\
-1 & -2 \\
\end{pmatrix}.
$$

For $3A-2B$, first multiply every entry of $A$ by $3$ and every entry of $B$ by $2$:

$$
3A=3
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix}=
\begin{pmatrix}
3 & 6 \\
-3 & 9 \\
\end{pmatrix},\qquad 2B=2
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix}=
\begin{pmatrix}
8 & -4 \\
0 & 10 \\
\end{pmatrix}.
$$

Then subtract $2B$ from $3A$ entry by entry:

$$
3A-2B=
\begin{pmatrix}
3-8 & 6-(-4) \\
-3-0 & 9-10 \\
\end{pmatrix}=
\begin{pmatrix}
-5 & 10 \\
-3 & -1 \\
\end{pmatrix}.
$$

**Property / method used.** *Entrywise matrix addition/subtraction and scalar multiplication:* for matrices of the same size $m\times n$ and any scalar $c$, operations are performed coordinate by coordinate via $(A\pm B)_{ij}=a_{ij}\pm b_{ij}$ and $(cA)_{ij}=c\,a_{ij}$.

**Mathematical verification.** Subtracting $B$ from $A+B$ and adding $B$ to $A-B$ both recover the original matrix $A$:

$$
(A+B)-B=
\begin{pmatrix}
5-4 & 0-(-2) \\
-1-0 & 8-5 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix}=A,
$$

$$
(A-B)+B=
\begin{pmatrix}
-3+4 & 4+(-2) \\
-1+0 & -2+5 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix}=A.
$$

Furthermore, rewriting $3A-2B$ using the distributive law as $2(A-B)+A$ yields the exact same result:

$$
2(A-B)+A=2
\begin{pmatrix}
-3 & 4 \\
-1 & -2 \\
\end{pmatrix}+
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix}=
\begin{pmatrix}
-6 & 8 \\
-2 & -4 \\
\end{pmatrix}+
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix}=
\begin{pmatrix}
-5 & 10 \\
-3 & -1 \\
\end{pmatrix}.
$$

##### 2. Why Matrix Addition Requires Matrices of the Same Size

**Result.** Matrix addition is defined only for matrices of the exact same dimensions ($m\times n$) because every entry $a_{ij}$ in the first matrix must pair with a corresponding entry $b_{ij}$ at the identical $(i,j)$ position in the second matrix.

**Main steps.** Let $A$ be an $m\times n$ matrix and $B$ be a $p\times q$ matrix. By definition, $(A+B)_{ij}=a_{ij}+b_{ij}$ must be evaluated across all valid row indices ($1\le i\le m$ and $1\le i\le p$) and column indices ($1\le j\le n$ and $1\le j\le q$). A complete one-to-one pairing of entries exists if and only if $m=p$ and $n=q$.

**Property / method used.** *Index-domain compatibility:* entrywise binary operations on matrices require identical index sets for both operands.

**Mathematical verification.** Consider a $2\times 2$ matrix $C$ and a $2\times 3$ matrix $D$:

$$
C=
\begin{pmatrix}
1 & 2 \\
3 & 4 \\
\end{pmatrix},\qquad D=
\begin{pmatrix}
5 & 6 & 7 \\
8 & 9 & 10 \\
\end{pmatrix}.
$$

Attempting to compute the $(1,3)$ entry $(C+D)_{13}=c_{13}+d_{13}$ fails because $C$ has only $2$ columns, so $c_{13}$ does not exist and $C+D$ is undefined.
