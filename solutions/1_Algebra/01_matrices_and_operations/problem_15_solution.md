### Exercise 15. Associativity of Multiplication and Different Calculation Paths

#### Exercise Reminder

Given the matrices

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix},\qquad C=
\begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix},
$$

1. Compute $(AB)C$ and $A(BC)$.
2. Compare the results and the number of intermediate operations.
3. Explain what associativity of matrix multiplication means in this example.

---

#### Solution

##### 1. Computing $(AB)C$ and $A(BC)$

**Result.** Both calculation paths yield the exact same $2\times 2$ matrix:

$$
(AB)C = A(BC) =
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}.
$$

<br>

**Main steps.** Note the matrix dimensions: $A$ is $2\times 3$, $B$ is $3\times 2$, and $C$ is $2\times 2$.

**Path 1: Computing $(AB)C$**

First, multiply $A$ ($2\times 3$) and $B$ ($3\times 2$) to obtain the $2\times 2$ intermediate matrix $AB$:

$$
AB=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot 1 + 2\cdot 2 + 0\cdot (-1) & 1\cdot 0 + 2\cdot 1 + 0\cdot 3 \\
0\cdot 1 + 1\cdot 2 + 1\cdot (-1) & 0\cdot 0 + 1\cdot 1 + 1\cdot 3 \\
\end{pmatrix}=
\begin{pmatrix}
5 & 2 \\
1 & 4 \\
\end{pmatrix}.
$$

Second, multiply $AB$ ($2\times 2$) on the right by $C$ ($2\times 2$):

$$
(AB)C=
\begin{pmatrix}
5 & 2 \\
1 & 4 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix}=
\begin{pmatrix}
5\cdot 2 + 2\cdot 0 & 5\cdot 1 + 2\cdot (-1) \\
1\cdot 2 + 4\cdot 0 & 1\cdot 1 + 4\cdot (-1) \\
\end{pmatrix}=
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}.
$$

**Path 2: Computing $A(BC)$**

First, multiply $B$ ($3\times 2$) and $C$ ($2\times 2$) to obtain the $3\times 2$ intermediate matrix $BC$:

$$
BC=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot 2 + 0\cdot 0 & 1\cdot 1 + 0\cdot (-1) \\
2\cdot 2 + 1\cdot 0 & 2\cdot 1 + 1\cdot (-1) \\
(-1)\cdot 2 + 3\cdot 0 & (-1)\cdot 1 + 3\cdot (-1) \\
\end{pmatrix}=
\begin{pmatrix}
2 & 1 \\
4 & 1 \\
-2 & -4 \\
\end{pmatrix}.
$$

Second, multiply $A$ ($2\times 3$) on the right by $BC$ ($3\times 2$):

$$
A(BC)=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
4 & 1 \\
-2 & -4 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot 2 + 2\cdot 4 + 0\cdot (-2) & 1\cdot 1 + 2\cdot 1 + 0\cdot (-4) \\
0\cdot 2 + 1\cdot 4 + 1\cdot (-2) & 0\cdot 1 + 1\cdot 1 + 1\cdot (-4) \\
\end{pmatrix}=
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}.
$$

<br>

**Property / method used.** *Associative law of matrix multiplication:* for any compatible matrices $A$ ($m\times n$), $B$ ($n\times p$), and $C$ ($p\times q$), grouping adjacent factors in either order produces the exact same $m\times q$ product:

$$
(AB)C = A(BC).
$$

<br>

**Mathematical verification.** Taking the transpose of the product and checking $(ABC)^T = C^T B^T A^T$ confirms all four entries independently:

$$
C^T B^T A^T =
\begin{pmatrix}
2 & 0 \\
1 & -1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 4 & -2 \\
1 & 1 & -4 \\
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
10 & 2 \\
3 & -3 \\
\end{pmatrix}= \bigl((AB)C\bigr)^T.
$$

---

##### 2. Comparison of Results and Number of Intermediate Operations

**Result.** Although both paths yield the identical output matrix $\begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}$, **Path 1 $(AB)C$ requires fewer operations** ($32$ total scalar operations: $20$ multiplications and $12$ additions) than **Path 2 $A(BC)$** ($38$ total scalar operations: $24$ multiplications and $14$ additions).

<br>

**Main steps.** Multiplying an $m\times n$ matrix by an $n\times p$ matrix produces $mp$ entries, where each entry requires $n$ scalar multiplications and $n - 1$ scalar additions. Counting the exact operations for each path gives:

| Calculation Path | Step 1 Product & Size | Step 1 Operations | Step 2 Product & Size | Step 2 Operations | Total Operations |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Path 1: $(AB)C$** | $AB$ ($2\times 2$) | $4\times 3 = 12$ mult.<br>$4\times 2 = 8$ add. | $(AB)C$ ($2\times 2$) | $4\times 2 = 8$ mult.<br>$4\times 1 = 4$ add. | **$20$ mult. + $12$ add. = $32$** |
| **Path 2: $A(BC)$** | $BC$ ($3\times 2$) | $6\times 2 = 12$ mult.<br>$6\times 1 = 6$ add. | $A(BC)$ ($2\times 2$) | $4\times 3 = 12$ mult.<br>$4\times 2 = 8$ add. | **$24$ mult. + $14$ add. = $38$** |

Path 1 saves $4$ multiplications and $2$ additions ($6$ operations total) because $AB$ immediately contracts the shared dimension $3$ down to a compact $2\times 2$ matrix, whereas $BC$ builds a larger $3\times 2$ intermediate matrix.

<br>

**Property / method used.** *Computational complexity of matrix chain multiplication:* multiplying $X_{m\times n}$ and $Y_{n\times p}$ costs $mnp$ scalar multiplications and $m(n-1)p$ scalar additions; minimizing the dimensions of intermediate products reduces total arithmetic cost.

<br>

**Mathematical verification.** Applying the general cost formulas $mnp$ (multiplications) and $m(n-1)p$ (additions) to both steps confirms the table totals:
- **Path 1:** Multiplications $= (2\cdot 3\cdot 2) + (2\cdot 2\cdot 2) = 12 + 8 = 20$; Additions $= 2(3-1)2 + 2(2-1)2 = 8 + 4 = 12$.
- **Path 2:** Multiplications $= (3\cdot 2\cdot 2) + (2\cdot 3\cdot 2) = 12 + 12 = 24$; Additions $= 3(2-1)2 + 2(3-1)2 = 6 + 8 = 14$.

---

##### 3. Meaning of Associativity in This Example

**Result.** Associativity means that while the *left-to-right order* of the matrices $A$, $B$, and $C$ cannot be swapped (since matrix multiplication is noncommutative), the *grouping* (parenthesization) of adjacent multiplications does not change the final product, allowing us to choose the most computationally efficient grouping.

<br>

**Main steps.**
1. **Invariance of the mathematical result:** Whether we first combine $A$ and $B$ into $AB$ and then apply $C$, or first combine $B$ and $C$ into $BC$ and then apply $A$, the resulting linear transformation from $\mathbb{R}^2$ to $\mathbb{R}^2$ is identical: $(AB)C = A(BC)$.
2. **Practical freedom in computation:** Because both groupings are mathematically guaranteed to agree, we are free to select the parenthesization $(AB)C$ that minimizes intermediate matrix sizes and arithmetic operations without sacrificing accuracy.

<br>

**Property / method used.** *Associativity of linear map composition:* if $T_C: \mathbb{R}^2 \to \mathbb{R}^2$, $T_B: \mathbb{R}^2 \to \mathbb{R}^3$, and $T_A: \mathbb{R}^3 \to \mathbb{R}^2$ are linear transformations represented by $C$, $B$, and $A$, then function composition is associative: $(T_A \circ T_B) \circ T_C = T_A \circ (T_B \circ T_C)$.

<br>

**Mathematical verification.** Evaluating both grouped matrices on the standard basis vectors $e_1 = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$ and $e_2 = \begin{pmatrix} 0 \\ 1 \end{pmatrix}$ confirms that they map every input vector identically:

$$
\bigl((AB)C\bigr)e_1 =
\begin{pmatrix}
10 \\
2 \\
\end{pmatrix}= \bigl(A(BC)\bigr)e_1, \qquad \bigl((AB)C\bigr)e_2 =
\begin{pmatrix}
3 \\
-3 \\
\end{pmatrix}= \bigl(A(BC)\bigr)e_2.
$$
