### Exercise 10. Columns of a Matrix Product

#### Exercise Reminder

Given the matrices

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix},
$$

where $b_1$ and $b_2$ denote the columns of $B$:

1. Compute $Ab_1$ and $Ab_2$.
2. Compute the matrix $AB$.
3. Compare the results and explain why the columns of $AB$ are exactly the vectors $Ab_1$ and $Ab_2$.

---

#### Solution

##### 1. Computing $Ab_1$ and $Ab_2$

**Result.**

$$
Ab_1=
\begin{pmatrix}
-1 \\
2 \\
\end{pmatrix},\qquad Ab_2=
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}.
$$

<br>

**Main steps.** Extract the two $3\times 1$ column vectors from $B$:

$$
b_1=
\begin{pmatrix}
1 \\
-1 \\
3 \\
\end{pmatrix},\qquad b_2=
\begin{pmatrix}
2 \\
0 \\
1 \\
\end{pmatrix}.
$$

Since $A$ has size $2\times 3$ and each column $b_j$ has size $3\times 1$, each product $Ab_j$ is a $2\times 1$ column vector computed via row-by-column dot products:

$$
Ab_1=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
-1 \\
3 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot 1 + 2\cdot (-1) + 0\cdot 3 \\
0\cdot 1 + 1\cdot (-1) + 1\cdot 3 \\
\end{pmatrix}=
\begin{pmatrix}
1 - 2 + 0 \\
0 - 1 + 3 \\
\end{pmatrix}=
\begin{pmatrix}
-1 \\
2 \\
\end{pmatrix},
$$

$$
Ab_2=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 \\
0 \\
1 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot 2 + 2\cdot 0 + 0\cdot 1 \\
0\cdot 2 + 1\cdot 0 + 1\cdot 1 \\
\end{pmatrix}=
\begin{pmatrix}
2 + 0 + 0 \\
0 + 0 + 1 \\
\end{pmatrix}=
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}.
$$

<br>

**Property / method used.** *Matrix-vector multiplication:* for an $m\times n$ matrix $A$ and an $n\times 1$ vector $v$, the $i$-th entry of $Av$ is the dot product of row $i$ of $A$ with $v$.

<br>

**Mathematical verification.** Expressing $Ab_1$ and $Ab_2$ as linear combinations of the columns of $A$ confirms both vectors:

$$
Ab_1 = 1
\begin{pmatrix}
1 \\
0 \\
\end{pmatrix} - 1
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix} + 3
\begin{pmatrix}
0 \\
1 \\
\end{pmatrix}=
\begin{pmatrix}
1 - 2 + 0 \\
0 - 1 + 3 \\
\end{pmatrix}=
\begin{pmatrix}
-1 \\
2 \\
\end{pmatrix},
$$

$$
Ab_2 = 2
\begin{pmatrix}
1 \\
0 \\
\end{pmatrix} + 0
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix} + 1
\begin{pmatrix}
0 \\
1 \\
\end{pmatrix}=
\begin{pmatrix}
2 + 0 + 0 \\
0 + 0 + 1 \\
\end{pmatrix}=
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}.
$$

---

##### 2. Computing the Matrix $AB$

**Result.**

$$
AB=
\begin{pmatrix}
-1 & 2 \\
2 & 1 \\
\end{pmatrix}.
$$

<br>

**Main steps.** Matrix $A$ has size $2\times 3$ and matrix $B$ has size $3\times 2$, so their product $AB$ is defined and has size $2\times 2$. Compute each $(i,j)$ entry as the dot product of row $i$ of $A$ with column $j$ of $B$:

$$
AB=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot 1 + 2\cdot (-1) + 0\cdot 3 & 1\cdot 2 + 2\cdot 0 + 0\cdot 1 \\
0\cdot 1 + 1\cdot (-1) + 1\cdot 3 & 0\cdot 2 + 1\cdot 0 + 1\cdot 1 \\
\end{pmatrix}=
\begin{pmatrix}
-1 & 2 \\
2 & 1 \\
\end{pmatrix}.
$$

<br>

**Property / method used.** *Row-by-column matrix multiplication:* for compatible matrices $A$ ($m\times n$) and $B$ ($n\times p$), the product $AB$ is an $m\times p$ matrix whose $(i,j)$ entry is the dot product of row $i$ of $A$ with column $j$ of $B$.

<br>

**Mathematical verification.** Checking the transpose identity $(AB)^T = B^T A^T$ confirms all four entries of $AB$:

$$
B^T A^T=
\begin{pmatrix}
1 & -1 & 3 \\
2 & 0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1 - 2 + 0 & 0 - 1 + 3 \\
2 + 0 + 0 & 0 + 0 + 1 \\
\end{pmatrix}=
\begin{pmatrix}
-1 & 2 \\
2 & 1 \\
\end{pmatrix}=(AB)^T.
$$

---

##### 3. Comparison and Explanation of the Column Structure of $AB$

**Result.** The first column of $AB$ is identically equal to $Ab_1 = \begin{pmatrix} -1 \\ 2 \end{pmatrix}$ and the second column of $AB$ is identically equal to $Ab_2 = \begin{pmatrix} 2 \\ 1 \end{pmatrix}$, so

$$
AB =
\begin{pmatrix}
Ab_1 & Ab_2
\end{pmatrix}=
\begin{pmatrix}
-1 & 2 \\
2 & 1 \\
\end{pmatrix}.
$$

<br>

**Main steps.** By definition, the entries in column $j$ of $AB$ are computed exclusively by taking dot products of the rows of $A$ with column $j$ of $B$ (which is the vector $b_j$), without involving any other columns of $B$:

$$
(AB)_{ij} = \sum_{k=1}^{3} a_{ik} b_{kj} = (Ab_j)_i \qquad \text{for } i \in \{1, 2\} \text{ and } j \in \{1, 2\}.
$$

Because every coordinate $i$ of column $j$ of $AB$ matches coordinate $i$ of $Ab_j$, the entire $j$-th column of $AB$ equals $Ab_j$.

<br>

**Property / method used.** *Column-by-column definition of matrix multiplication:* if $B$ is partitioned into its columns $b_1, b_2, \dots, b_p$, then multiplying $A$ by $B$ acts independently on each column of $B$:

$$
AB = A
\begin{pmatrix}
b_1 & b_2 & \cdots & b_p
\end{pmatrix}=
\begin{pmatrix}
Ab_1 & Ab_2 & \cdots & Ab_p
\end{pmatrix}.
$$

<br>

**Mathematical verification.** Let $e_1 = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$ and $e_2 = \begin{pmatrix} 0 \\ 1 \end{pmatrix}$ be the standard basis vectors of $\mathbb{R}^2$. Multiplying $B$ on the right by $e_j$ isolates its $j$-th column, since $Be_1$ equals $b_1$ and $Be_2$ equals $b_2$. Applying associativity of matrix multiplication yields

$$
\text{Column } 1 \text{ of } AB = (AB)e_1 = A(Be_1) = Ab_1 =
\begin{pmatrix}
-1 \\
2 \\
\end{pmatrix},
$$

$$
\text{Column } 2 \text{ of } AB = (AB)e_2 = A(Be_2) = Ab_2 =
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix},
$$

which proves that the columns of $AB$ are $Ab_1$ and $Ab_2$.
