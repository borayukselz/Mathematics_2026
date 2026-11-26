### Exercise 7. Choosing a Method Deliberately

#### Exercise Reminder

Do not solve all of the following systems completely. For each situation, choose the method that best uses its structure and justify your choice:

1. one system with a triangular coefficient matrix

$$
\begin{cases}
2x - y = 3, \\
4y = 8;
\end{cases}
$$

2. three systems $Ax = b_i$ with the same invertible matrix $A$, when $A^{-1}$ is already known;
3. one $3\times 3$ system for which the inverse matrix is not given and the goal is only to find one solution vector.

For case 1, carry out the chosen method completely. For cases 2 and 3, describe the plan and indicate which part of the computation would be reusable or unnecessary. Do not judge a method by its name alone — refer to the number of right-hand sides and the structure of the matrix.

---

#### Solution

**Result.**
- **Case 1:** Use **direct back-substitution** (no row reduction or matrix inversion needed); the unique solution is $(x, y) = \left(\frac{5}{2}, 2\right)$.
- **Case 2:** Use **direct matrix-vector multiplication $x_i = A^{-1}b_i$** for each $i = 1, 2, 3$ (reusing the precomputed matrix $A^{-1}$ three times; computing $A^{-1}$ or running Gaussian elimination from scratch is unnecessary).
- **Case 3:** Use **Gaussian elimination with back-substitution** on the single augmented matrix $[A \mid b]$ (computing the full inverse $A^{-1}$ is unnecessary for a single right-hand side vector $b$).

<br>

**Main steps.**

1. **Case 1 — Triangular coefficient matrix (chosen method: direct back-substitution):**
   - **Justification (structure and right-hand sides):** The coefficient matrix

$$
A =
\begin{pmatrix}
2 & -1 \\
0 & 4
\end{pmatrix}
$$

     is already in upper triangular form (its lower-left entry is $0$), and there is only a single right-hand side vector $b = (3, 8)^T$. Forward elimination is already complete, and forming $A^{-1}$ would add unnecessary work.
   - **Complete execution of back-substitution:**
     - Solve the bottom equation $4y = 8$ directly for $y$:

$$
4y = 8 \implies y = 2.
$$

     - Substitute $y = 2$ into the top equation $2x - y = 3$ and solve for $x$:

$$
2x - 2 = 3 \implies 2x = 5 \implies x = \frac{5}{2}.
$$

   - Hence the unique solution is $(x, y) = \left(\frac{5}{2}, 2\right)$.

2. **Case 2 — Three systems $Ax = b_i$ with the same invertible $A$ and known $A^{-1}$ (chosen method: direct multiplication $x_i = A^{-1}b_i$):**
   - **Justification (structure and right-hand sides):** There are multiple right-hand side vectors ($b_1, b_2, b_3$) sharing the exact same coefficient matrix $A$, and $A^{-1}$ is already available.
   - **Execution plan:** Compute each solution vector directly via $x_1 = A^{-1}b_1$, $x_2 = A^{-1}b_2$, and $x_3 = A^{-1}b_3$ (or simultaneously as a single matrix product $X = A^{-1}B$ where $B = [b_1 \ \ b_2 \ \ b_3]$).
   - **Reusable vs. unnecessary work:** The given inverse matrix $A^{-1}$ is the **reusable** component across all three right-hand sides; repeating row reduction on $[A \mid b_i]$ three separate times or recomputing $\det A$ and $A^{-1}$ is completely **unnecessary**.

3. **Case 3 — One $3\times 3$ system with unknown $A^{-1}$ and a single target vector $x$ (chosen method: Gaussian elimination with back-substitution):**
   - **Justification (structure and right-hand sides):** The coefficient matrix $A$ is general (not pre-triangularized) and there is only **one** right-hand side vector $b$, with no $A^{-1}$ provided.
   - **Execution plan:** Form the $3\times 4$ augmented matrix $[A \mid b]$, use elementary row operations to reduce $A$ to upper triangular (row echelon) form while applying the same operations to the single column $b$, and then solve for $(x_1, x_2, x_3)^T$ via back-substitution.
   - **Reusable vs. unnecessary work:** Because there is only one right-hand side, there are no subsequent systems to reuse $A^{-1}$ on; therefore, augmenting $A$ with the full $3\times 3$ identity matrix $[A \mid I]$ to compute all three columns of $A^{-1}$ (or computing determinants/cofactors) is **unnecessary** extra computation.

<br>

**Property / method used.** *Structure-aware linear solver selection:* computational cost depends on both matrix structure (triangular vs. general) and the number of right-hand sides $k$ (single $b$ favors Gaussian elimination; multiple $b_i$ or precomputed $A^{-1}$ favors reusing $A^{-1}b_i$).

<br>

**Mathematical verification.** Substituting $(x, y) = \left(\frac{5}{2}, 2\right)$ into both equations of Case 1 confirms consistency:

$$
2\left(\frac{5}{2}\right) - 2 = 5 - 2 = 3, \qquad 4(2) = 8.
$$
