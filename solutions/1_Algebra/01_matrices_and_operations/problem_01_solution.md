### Exercise 1. Matrix Size and Entries

#### Exercise Reminder

Given

$$
A=
\begin{pmatrix}
2 & -1 & 3 \\
0 & 4 & 5 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
-2 & 3 \\
4 & 1 \\
\end{pmatrix},
$$

where $a_{ij}$ and $b_{ij}$ denote the entries in row $i$ and column $j$ of matrices $A$ and $B$, respectively:

1. State the sizes of matrices $A$ and $B$.
2. Read off the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.
3. Write the second row of $A$ and the first column of $B$ as vectors.

---

#### Solution

##### 1. Sizes of Matrices A and B

**Result.** Matrix $A$ has size $2\times 3$, and matrix $B$ has size $3\times 2$.

**Main steps.** Count the horizontal rows and vertical columns of each matrix. Matrix $A$ has $2$ horizontal rows and $3$ vertical columns, giving size $2\times 3$. Matrix $B$ has $3$ horizontal rows and $2$ vertical columns, giving size $3\times 2$.

**Property / method used.** *Matrix dimension convention:* a matrix with $m$ rows and $n$ columns has size $m\times n$, where the row count $m$ is always written first and the column count $n$ second.

**Mathematical verification.** Multiplying the dimensions gives the total number of entries: $A$ contains $2\cdot 3=6$ entries and $B$ contains $3\cdot 2=6$ entries, matching the $6$ numbers displayed in each matrix.

##### 2. Entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$

**Result.**

$$
a_{12}=-1,\qquad a_{23}=5,\qquad b_{21}=-2,\qquad b_{32}=1.
$$

**Main steps.**

1. Locate row $1$, column $2$ of $A$: $a_{12}=-1$.
2. Locate row $2$, column $3$ of $A$: $a_{23}=5$.
3. Locate row $2$, column $1$ of $B$: $b_{21}=-2$.
4. Locate row $3$, column $2$ of $B$: $b_{32}=1$.

**Property / method used.** *Double-subscript indexing:* in $x_{ij}$, the first subscript $i$ specifies the row index (top to bottom) and the second subscript $j$ specifies the column index (left to right).

**Mathematical verification.** Every index pair $(i,j)$ satisfies $1\le i\le m$ and $1\le j\le n$, and matching each entry position directly against the given matrices confirms all four values:

$$
A=
\begin{pmatrix}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
\end{pmatrix}=
\begin{pmatrix}
2 & -1 & 3 \\
0 & 4 & 5 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
b_{11} & b_{12} \\
b_{21} & b_{22} \\
b_{31} & b_{32} \\
\end{pmatrix}=
\begin{pmatrix}
1 & 0 \\
-2 & 3 \\
4 & 1 \\
\end{pmatrix}.
$$

##### 3. Second Row of A and First Column of B as Vectors

**Result.**

$$
r_2=
\begin{pmatrix}
0 & 4 & 5 \\
\end{pmatrix},\qquad c_1=
\begin{pmatrix}
1 \\
-2 \\
4 \\
\end{pmatrix}.
$$

**Main steps.** Extract all entries from the second row of $A$ from left to right ($a_{21}, a_{22}, a_{23}$) to form the row vector $r_2$, and extract all entries from the first column of $B$ from top to bottom ($b_{11}, b_{21}, b_{31}$) to form the column vector $c_1$.

**Property / method used.** *Row and column partitioning:* any row $i$ of an $m\times n$ matrix forms a $1\times n$ row vector, and any column $j$ forms an $m\times 1$ column vector.

**Mathematical verification.** Since $A$ has $3$ columns, $r_2$ has size $1\times 3$ ($3$ entries). Since $B$ has $3$ rows, $c_1$ has size $3\times 1$ ($3$ entries). Both vector dimensions match their parent matrices.
