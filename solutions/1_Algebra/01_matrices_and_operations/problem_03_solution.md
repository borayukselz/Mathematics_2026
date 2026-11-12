### Exercise 3. When Can Matrices Be Multiplied?

#### Exercise Reminder

Given four matrices with dimensions

$$
A_{2\times 3},\qquad B_{3\times 4},\qquad C_{4\times 2},\qquad D_{2\times 2},
$$

consider the eight matrix products

$$
AB,\ BA,\ BC,\ CB,\ AC,\ CA,\ AD,\ DA.
$$

1. Determine whether each product is defined.
2. If a product is defined, state the size of the resulting matrix.
3. Justify each decision using the dimension compatibility condition for matrix multiplication.

---

#### Solution

**Result.**

| Product | Factor Dimensions | Inner Dimensions | Status | Resulting Size |
| :--- | :---: | :---: | :---: | :---: |
| $AB$ | $(2\times 3)(3\times 4)$ | $3 = 3$ | Defined | $2\times 4$ |
| $BA$ | $(3\times 4)(2\times 3)$ | $4 \neq 2$ | Undefined | — |
| $BC$ | $(3\times 4)(4\times 2)$ | $4 = 4$ | Defined | $3\times 2$ |
| $CB$ | $(4\times 2)(3\times 4)$ | $2 \neq 3$ | Undefined | — |
| $AC$ | $(2\times 3)(4\times 2)$ | $3 \neq 4$ | Undefined | — |
| $CA$ | $(4\times 2)(2\times 3)$ | $2 = 2$ | Defined | $4\times 3$ |
| $AD$ | $(2\times 3)(2\times 2)$ | $3 \neq 2$ | Undefined | — |
| $DA$ | $(2\times 2)(2\times 3)$ | $2 = 2$ | Defined | $2\times 3$ |

**Main steps.** For each pair of matrices, compare the number of columns of the left matrix with the number of rows of the right matrix:

$$
\begin{aligned}
AB &: (2\times 3)(3\times 4) \implies 3 = 3 \quad \text{(defined; outer dimensions give size } 2\times 4\text{)}, \\
BA &: (3\times 4)(2\times 3) \implies 4 \neq 2 \quad \text{(undefined: columns of } B \neq \text{rows of } A\text{)}, \\
BC &: (3\times 4)(4\times 2) \implies 4 = 4 \quad \text{(defined; outer dimensions give size } 3\times 2\text{)}, \\
CB &: (4\times 2)(3\times 4) \implies 2 \neq 3 \quad \text{(undefined: columns of } C \neq \text{rows of } B\text{)}, \\
AC &: (2\times 3)(4\times 2) \implies 3 \neq 4 \quad \text{(undefined: columns of } A \neq \text{rows of } C\text{)}, \\
CA &: (4\times 2)(2\times 3) \implies 2 = 2 \quad \text{(defined; outer dimensions give size } 4\times 3\text{)}, \\
AD &: (2\times 3)(2\times 2) \implies 3 \neq 2 \quad \text{(undefined: columns of } A \neq \text{rows of } D\text{)}, \\
DA &: (2\times 2)(2\times 3) \implies 2 = 2 \quad \text{(defined; outer dimensions give size } 2\times 3\text{)}.
\end{aligned}
$$

**Property / method used.** *Dimension compatibility condition:* let $X$ be an $m\times n$ matrix and $Y$ be a $p\times q$ matrix. The product $XY$ is defined if and only if the inner dimensions match ($n = p$), in which case $XY$ has size $m\times q$ (determined by the outer dimensions):

$$
X_{m\times n}\,Y_{p\times q} \text{ is defined} \iff n = p, \qquad \text{resulting in } (XY)_{m\times q}.
$$

**Mathematical verification.** Each $(i,j)$ entry of a matrix product $XY$ is computed as the dot product of row $i$ of $X$ (a vector of length $n$) and column $j$ of $Y$ (a vector of length $p$).
- For $AB$, $BC$, $CA$, and $DA$, the row lengths of the left factor ($3, 4, 2, 2$) match the column lengths of the right factor ($3, 4, 2, 2$), allowing $2\cdot 4 = 8$, $3\cdot 2 = 6$, $4\cdot 3 = 12$, and $2\cdot 3 = 6$ valid dot products, respectively.
- Reversing the factor order ($BA$, $CB$, $AC$, $AD$) produces mismatched vector lengths in every case, confirming that dimension compatibility depends strictly on multiplication order.
