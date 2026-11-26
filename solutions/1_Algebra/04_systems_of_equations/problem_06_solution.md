### Exercise 6. A System with a Parameter — Which Cases Actually Occur?

#### Exercise Reminder

Analyze, depending on the parameter $a$, the system

$$
\begin{cases}
x + y = 2, \\
ax + ay = 4.
\end{cases}
$$

Among the three possibilities — **exactly one solution**, **infinitely many solutions**, **no solution** — determine which actually occur and for which values of $a$. If one type cannot occur, explain why.

---

#### Solution

**Result.** Only **two** of the three possibilities actually occur:
- **Infinitely many solutions** occur when **$a = 2$** (specifically, $(x, y) = (2 - t, t)$ for any $t \in \mathbb{R}$).
- **No solution** (inconsistent system) occurs for **every $a \neq 2$**.
- **Exactly one solution never occurs** for any value of $a \in \mathbb{R}$, because the two left-hand sides are proportional for every $a$, so the coefficient matrix always has determinant $0$ (rank $1 < 2$).

<br>

**Main steps.**

1. **Set up the augmented matrix $[A \mid b]$ and eliminate $x$ from row $2$ via $R_2 \leftarrow R_2 - aR_1$:**

$$
[A \mid b] =
\left(
\begin{array}{cc|c}
1 & 1 & 2 \\
a & a & 4
\end{array}
\right)
\xrightarrow{R_2 \leftarrow R_2 - aR_1}
\left(
\begin{array}{cc|c}
1 & 1 & 2 \\
0 & 0 & 4 - 2a
\end{array}
\right).
$$

2. **Analyze the reduced second row $0x + 0y = 4 - 2a$ by cases:**
   - **Case 1: $4 - 2a = 0 \iff a = 2$.**
     The reduced matrix becomes

$$
\left(
\begin{array}{cc|c}
1 & 1 & 2 \\
0 & 0 & 0
\end{array}
\right).
$$

     There is no contradiction, and there is $r = 1$ pivot among $n = 2$ variables, leaving $2 - 1 = 1$ free variable ($y = t \in \mathbb{R}$). Thus, the system has **infinitely many solutions**:

$$
\begin{pmatrix}
x \\
y
\end{pmatrix} =
\begin{pmatrix}
2 - t \\
t
\end{pmatrix} =
\begin{pmatrix}
2 \\
0
\end{pmatrix} + t
\begin{pmatrix}
-1 \\
1
\end{pmatrix}, \qquad t \in \mathbb{R}.
$$

   - **Case 2: $4 - 2a \neq 0 \iff a \neq 2$.**
     Row $2$ reads $0 = 4 - 2a$ with $4 - 2a \neq 0$, which is an impossible algebraic contradiction. Hence, for all $a \neq 2$ (including $a = 0$, which gives $0 = 4$), the system is inconsistent and has **no solution**.

3. **Explain why "exactly one solution" cannot occur:**
   - In the coefficient matrix

$$
A =
\begin{pmatrix}
1 & 1 \\
a & a
\end{pmatrix},
$$

     row $2$ is always $a$ times row $1$, so $\det A = 1 \cdot a - 1 \cdot a = 0$ and $\mathrm{rank}(A) = 1 < 2$ for every $a \in \mathbb{R}$.
   - A $2\times 2$ linear system has a unique solution if and only if $\det A \neq 0$ (equivalently, $\mathrm{rank}(A) = 2$, meaning the two lines intersect at a single point). Because the left-hand side of equation $2$ is $a(x + y)$, any point satisfying $x + y = 2$ forces $ax + ay = 2a$; thus, the two equations either describe the exact same line (when $2a = 4 \iff a = 2$) or parallel/degenerate inconsistent conditions (when $a \neq 2$), never two intersecting lines.

<br>

**Property / method used.** *Parametric row reduction and determinant rank condition:* eliminating the parameter from the coefficient block exposes the consistency condition $4 - 2a = 0$, while $\det A = 0$ rules out a unique solution for all $a$.

<br>

**Mathematical verification.** Substituting $x + y = 2$ directly into the left-hand side of the second equation gives

$$
ax + ay = a(x + y) = a(2) = 2a.
$$

Comparing $2a$ with the right-hand side $4$ confirms immediately that the system is satisfied (by all points on $x + y = 2$) if and only if $2a = 4 \iff a = 2$, and has no solutions whenever $a \neq 2$.
