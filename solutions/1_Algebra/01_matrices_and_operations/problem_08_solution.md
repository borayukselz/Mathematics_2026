### Exercise 8. Row Operations and Their Reversibility

#### Exercise Reminder

Given the $3\times 3$ matrix

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix},
$$

1. Perform the following elementary row operations in order and write the matrix after each step:
   - Step 1: $R_2 \leftarrow R_2 - 2R_1$,
   - Step 2: $R_3 \leftarrow R_3 + R_1$,
   - Step 3: interchange $R_2$ and $R_3$ ($R_2 \leftrightarrow R_3$).
2. For each of the three operations, state an operation that reverses it.

---

#### Solution

##### 1. Performing the Sequence of Row Operations

**Result.**

- After Step 1 ($R_2 \leftarrow R_2 - 2R_1$):

$$
A_1=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3 \\
\end{pmatrix}.
$$

- After Step 2 ($R_3 \leftarrow R_3 + R_1$):

$$
A_2=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2 \\
\end{pmatrix}.
$$

- After Step 3 ($R_2 \leftrightarrow R_3$):

$$
A_3=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3 \\
\end{pmatrix}.
$$

**Main steps.** Start with the initial matrix $A$ and apply each operation sequentially to the result of the previous step:

1. **Step 1 ($R_2 \leftarrow R_2 - 2R_1$):** Subtract $2$ times row $1$ from row $2$, leaving rows $1$ and $3$ unchanged:

$$
R_2^{\text{new}} =
\begin{pmatrix}
2 & 4 & 1
\end{pmatrix} - 2
\begin{pmatrix}
1 & 2 & -1
\end{pmatrix} =
\begin{pmatrix}
2 - 2 & 4 - 4 & 1 - (-2)
\end{pmatrix} =
\begin{pmatrix}
0 & 0 & 3
\end{pmatrix},
$$

$$
A_1=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3 \\
\end{pmatrix}.
$$

2. **Step 2 ($R_3 \leftarrow R_3 + R_1$):** Add row $1$ of $A_1$ to row $3$ of $A_1$, leaving rows $1$ and $2$ unchanged:

$$
R_3^{\text{new}} =
\begin{pmatrix}
-1 & 1 & 3
\end{pmatrix} +
\begin{pmatrix}
1 & 2 & -1
\end{pmatrix} =
\begin{pmatrix}
-1 + 1 & 1 + 2 & 3 + (-1)
\end{pmatrix} =
\begin{pmatrix}
0 & 3 & 2
\end{pmatrix},
$$

$$
A_2=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2 \\
\end{pmatrix}.
$$

3. **Step 3 ($R_2 \leftrightarrow R_3$):** Swap row $2$ and row $3$ of $A_2$ to place the nonzero pivot $3$ into the $(2,2)$ position:

$$
A_3=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3 \\
\end{pmatrix}.
$$

**Property / method used.** *Elementary row operations (Gaussian elimination):*
- *Row replacement* ($R_i \leftarrow R_i + cR_j$ for $i \neq j$) eliminates target entries below a pivot without altering the solution set of an associated linear system.
- *Row interchange* ($R_i \leftrightarrow R_j$) reorders rows so that a nonzero pivot sits on the main diagonal.

**Mathematical verification.** Row replacement operations do not change the determinant of a matrix, whereas a single row swap multiplies the determinant by $-1$. Computing $\det(A)$ by cofactor expansion along the first column gives

$$
\det(A) = 1(4\cdot 3 - 1\cdot 1) - 2(2\cdot 3 - (-1)\cdot 1) + (-1)(2\cdot 1 - (-1)\cdot 4) = 11 - 14 - 6 = -9.
$$

Because $A_3$ is upper triangular, its determinant is the product of its main diagonal entries:

$$
\det(A_3) = 1 \cdot 3 \cdot 3 = 9 = -\det(A),
$$

which confirms that the two row replacements preserved the magnitude of the determinant while the single row swap reversed its sign.

##### 2. Operations That Reverse Each Step

**Result.**
1. Operation 1 ($R_2 \leftarrow R_2 - 2R_1$) is reversed by **$R_2 \leftarrow R_2 + 2R_1$**.
2. Operation 2 ($R_3 \leftarrow R_3 + R_1$) is reversed by **$R_3 \leftarrow R_3 - R_1$**.
3. Operation 3 ($R_2 \leftrightarrow R_3$) is reversed by **$R_2 \leftrightarrow R_3$** (interchanging $R_2$ and $R_3$ again).

**Main steps.**
1. Since Step 1 subtracted $2R_1$ from $R_2$ while keeping $R_1$ fixed, adding $2R_1$ back to the new $R_2$ cancels $-2R_1$ and restores the original second row.
2. Since Step 2 added $R_1$ to $R_3$ while keeping $R_1$ fixed, subtracting $R_1$ from the new $R_3$ cancels $+R_1$ and restores the original third row.
3. Since Step 3 swapped rows $2$ and $3$, swapping rows $2$ and $3$ a second time returns each row to its previous position.

**Property / method used.** *Invertibility of elementary row operations:* every elementary row operation is invertible, and its inverse is an elementary row operation of the exact same type:
- The inverse of $R_i \leftarrow R_i + cR_j$ ($i \neq j$) is $R_i \leftarrow R_i - cR_j$.
- The inverse of $R_i \leftrightarrow R_j$ is $R_i \leftrightarrow R_j$ itself (it is self-inverse).

**Mathematical verification.** Applying the three inverse operations to $A_3$ in reverse order (Step 3 inverse, then Step 2 inverse, then Step 1 inverse) recovers the original matrix $A$:

$$
A_3=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3 \\
\end{pmatrix}
\xrightarrow{R_2 \leftrightarrow R_3}
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2 \\
\end{pmatrix}
\xrightarrow{R_3 \leftarrow R_3 - R_1}
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3 \\
\end{pmatrix}
\xrightarrow{R_2 \leftarrow R_2 + 2R_1}
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}=A.
$$
