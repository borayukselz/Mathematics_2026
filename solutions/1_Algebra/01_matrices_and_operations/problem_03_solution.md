### Exercise 3. When Can Matrices Be Multiplied?

#### Exercise Reminder

The matrix sizes are

$$
A_{2\times 3},\qquad B_{3\times 4},\qquad C_{4\times 2},\qquad D_{2\times 2}.
$$

For the products

$$
AB,\; BA,\; BC,\; CB,\; AC,\; CA,\; AD,\; DA,
$$

1. Determine whether each product is defined.
2. If so, state the size of the result.
3. Justify each decision using the dimension compatibility condition.

---

#### Solution

**Result.**

- **$AB$:** Defined, size **$2\times 4$**
- **$BA$:** Undefined
- **$BC$:** Defined, size **$3\times 2$**
- **$CB$:** Undefined
- **$AC$:** Undefined
- **$CA$:** Defined, size **$4\times 3$**
- **$AD$:** Undefined
- **$DA$:** Defined, size **$2\times 3$**

<br>

**Main steps.** For two matrices $X$ of size $m\times n$ and $Y$ of size $p\times q$, the matrix product $XY$ is defined if and only if the inner dimensions match ($n = p$), in which case the resulting matrix $XY$ has outer dimensions $m\times q$. Checking each of the eight products gives:

| Product | Factor Sizes | Inner Dimensions Match? | Status | Result Size | Justification |
| :---: | :---: | :---: | :---: | :---: | :--- |
| **$AB$** | $(2\times 3)(3\times 4)$ | $3 = 3$ (Yes) | **Defined** | **$2\times 4$** | Columns of $A$ ($3$) equal rows of $B$ ($3$); outer dimensions give $2\times 4$. |
| **$BA$** | $(3\times 4)(2\times 3)$ | $4 \neq 2$ (No) | **Undefined** | — | Columns of $B$ ($4$) do not equal rows of $A$ ($2$). |
| **$BC$** | $(3\times 4)(4\times 2)$ | $4 = 4$ (Yes) | **Defined** | **$3\times 2$** | Columns of $B$ ($4$) equal rows of $C$ ($4$); outer dimensions give $3\times 2$. |
| **$CB$** | $(4\times 2)(3\times 4)$ | $2 \neq 3$ (No) | **Undefined** | — | Columns of $C$ ($2$) do not equal rows of $B$ ($3$). |
| **$AC$** | $(2\times 3)(4\times 2)$ | $3 \neq 4$ (No) | **Undefined** | — | Columns of $A$ ($3$) do not equal rows of $C$ ($4$). |
| **$CA$** | $(4\times 2)(2\times 3)$ | $2 = 2$ (Yes) | **Defined** | **$4\times 3$** | Columns of $C$ ($2$) equal rows of $A$ ($2$); outer dimensions give $4\times 3$. |
| **$AD$** | $(2\times 3)(2\times 2)$ | $3 \neq 2$ (No) | **Undefined** | — | Columns of $A$ ($3$) do not equal rows of $D$ ($2$). |
| **$DA$** | $(2\times 2)(2\times 3)$ | $2 = 2$ (Yes) | **Defined** | **$2\times 3$** | Columns of $D$ ($2$) equal rows of $A$ ($2$); outer dimensions give $2\times 3$. |

<br>

**Property / method used.** *Dimension compatibility condition for matrix multiplication:* the product $X_{m\times n} Y_{p\times q}$ exists if and only if $n = p$, and when it exists, its dimensions are $m\times q$.

<br>

**Mathematical verification.** The compatibility condition requires the $(i,j)$ entry of $XY$ to be the dot product of row $i$ of $X$ (which has length $n$) and column $j$ of $Y$ (which has length $p$). Those dot products are well-defined precisely when $n = p$:
- In $AB$, $BC$, $CA$, and $DA$, the row lengths of the left factor ($3, 4, 2, 2$) match the column heights of the right factor ($3, 4, 2, 2$), producing $2\times 4$, $3\times 2$, $4\times 3$, and $2\times 3$ matrices respectively.
- In $BA$, $CB$, $AC$, and $AD$, the mismatched inner pairs $(4,2)$, $(2,3)$, $(3,4)$, and $(3,2)$ prevent forming valid dot products, confirming that those four products do not exist.
