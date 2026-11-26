### Exercise 1. From a System to a Matrix

#### Exercise Reminder

Write the system

$$
\begin{cases}
2x - y + z = 4, \\
x + 3y - 2z = 1, \\
3x + y + z = 7.
\end{cases}
$$

in the form $Ax = b$. Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.

---

#### Solution

**Result.** In matrix form $Ax = b$, the system is

$$
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1
\end{pmatrix}
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix} =
\begin{pmatrix}
4 \\
1 \\
7
\end{pmatrix},
$$

where:
- **Coefficient matrix:**

$$
A =
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1
\end{pmatrix}
$$

- **Vector of unknowns:**

$$
v =
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix}
$$

- **Right-hand side vector:**

$$
b =
\begin{pmatrix}
4 \\
1 \\
7
\end{pmatrix}
$$

(Note: denoting the vector of unknowns by $v$ above avoids reusing the scalar variable name $x$; in the compact matrix equation $Ax = b$, $x$ denotes this $3\times 1$ column vector of unknowns.)

<br>

**Main steps.**

1. **Extract the coefficients of each variable in order $(x, y, z)$:**
   - Equation 1 ($2x - y + z = 4$) has coefficients $(2, -1, 1)$ and constant term $4$.
   - Equation 2 ($x + 3y - 2z = 1$) has coefficients $(1, 3, -2)$ and constant term $1$.
   - Equation 3 ($3x + y + z = 7$) has coefficients $(3, 1, 1)$ and constant term $7$.

2. **Assemble $A$, the vector of unknowns, and $b$:** Place the coefficients of Equation $i$ into row $i$ of the $3\times 3$ matrix $A$, list the three unknowns in a $3\times 1$ column vector, and place the three constant terms into the $3\times 1$ column vector $b$:

$$
A =
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1
\end{pmatrix},\qquad x =
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix},\qquad b =
\begin{pmatrix}
4 \\
1 \\
7
\end{pmatrix}.
$$

3. **How each row of $A$ corresponds to one equation:** Under the row-by-column rule for matrix-vector multiplication, the $i$-th entry of the product $Ax$ is the dot product of the $i$-th row of $A$ with the column vector of unknowns:
   - **Row 1** $(2 \quad -1 \quad 1)$ dotted with $(x, y, z)^T$ gives $2x - y + z$, and equating it to the first entry of $b$ yields Equation 1: $2x - y + z = 4$.
   - **Row 2** $(1 \quad 3 \quad -2)$ dotted with $(x, y, z)^T$ gives $x + 3y - 2z$, and equating it to the second entry of $b$ yields Equation 2: $x + 3y - 2z = 1$.
   - **Row 3** $(3 \quad 1 \quad 1)$ dotted with $(x, y, z)^T$ gives $3x + y + z$, and equating it to the third entry of $b$ yields Equation 3: $3x + y + z = 7$.

<br>

**Property / method used.** *Matrix-vector representation of a linear system:* an $m\times n$ system of linear equations is equivalent to the single matrix equation $Ax = b$, where entry $a_{ij}$ is the coefficient of the $j$-th unknown in the $i$-th equation, and row $i$ of $Ax = b$ reproduces the $i$-th scalar equation.

<br>

**Mathematical verification.** Computing the matrix-vector product $Ax$ explicitly entry by entry recovers the exact original system of three equations:

$$
Ax =
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1
\end{pmatrix}
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix} =
\begin{pmatrix}
2x + (-1)y + 1z \\
1x + 3y + (-2)z \\
3x + 1y + 1z
\end{pmatrix} =
\begin{pmatrix}
2x - y + z \\
x + 3y - 2z \\
3x + y + z
\end{pmatrix} =
\begin{pmatrix}
4 \\
1 \\
7
\end{pmatrix} = b.
$$
