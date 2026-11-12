### Exercise 13. A Recurrence Written in Matrix Form

#### Exercise Reminder

Let

$$
F=
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}.
$$

1. Compute $F^2$, $F^3$, $F^4$, and $F^5$. Compare the numbers obtained with the sequence $0, 1, 1, 2, 3, 5, 8, \dots$ and describe the relationship you observe.
2. Compute $F \begin{pmatrix} a \\ b \end{pmatrix}$ and explain how this multiplication performs one recurrence step: it creates the sum of two consecutive terms and keeps one of them for the next step.

---

#### Solution

##### 1. Computing Powers of $F$ and Relationship to the Fibonacci Sequence

**Result.**

$$
F^2=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix},\qquad F^3=
\begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix},\qquad F^4=
\begin{pmatrix}
5 & 3 \\
3 & 2 \\
\end{pmatrix},\qquad F^5=
\begin{pmatrix}
8 & 5 \\
5 & 3 \\
\end{pmatrix}.
$$

If the sequence $0, 1, 1, 2, 3, 5, 8, \dots$ is indexed by $f_0 = 0, f_1 = 1, f_2 = 1, f_3 = 2, f_4 = 3, f_5 = 5, f_6 = 8, \dots$ (the Fibonacci sequence), then for every integer $n \ge 1$, the matrix power $F^n$ is given by

$$
F^n=
\begin{pmatrix}
f_{n+1} & f_n \\
f_n & f_{n-1} \\
\end{pmatrix}.
$$

<br>

**Main steps.** Compute each successive power using $F^k = F^{k-1}F$:

$$
F^2 = F \cdot F =
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot 1 + 1\cdot 1 & 1\cdot 1 + 1\cdot 0 \\
1\cdot 1 + 0\cdot 1 & 1\cdot 1 + 0\cdot 0 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix},
$$

$$
F^3 = F^2 \cdot F =
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
2\cdot 1 + 1\cdot 1 & 2\cdot 1 + 1\cdot 0 \\
1\cdot 1 + 1\cdot 1 & 1\cdot 1 + 1\cdot 0 \\
\end{pmatrix}=
\begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix},
$$

$$
F^4 = F^3 \cdot F =
\begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
3\cdot 1 + 2\cdot 1 & 3\cdot 1 + 2\cdot 0 \\
2\cdot 1 + 1\cdot 1 & 2\cdot 1 + 1\cdot 0 \\
\end{pmatrix}=
\begin{pmatrix}
5 & 3 \\
3 & 2 \\
\end{pmatrix},
$$

$$
F^5 = F^4 \cdot F =
\begin{pmatrix}
5 & 3 \\
3 & 2 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
5\cdot 1 + 3\cdot 1 & 5\cdot 1 + 3\cdot 0 \\
3\cdot 1 + 2\cdot 1 & 3\cdot 1 + 2\cdot 0 \\
\end{pmatrix}=
\begin{pmatrix}
8 & 5 \\
5 & 3 \\
\end{pmatrix}.
$$

Comparing these entries with $f_0 = 0, f_1 = 1, f_2 = 1, f_3 = 2, f_4 = 3, f_5 = 5, f_6 = 8$:
- In $F^1 = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}$, the entries are $\begin{pmatrix} f_2 & f_1 \\ f_1 & f_0 \end{pmatrix}$.
- In $F^2 = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}$, the entries are $\begin{pmatrix} f_3 & f_2 \\ f_2 & f_1 \end{pmatrix}$.
- In $F^3 = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix}$, the entries are $\begin{pmatrix} f_4 & f_3 \\ f_3 & f_2 \end{pmatrix}$.
- In $F^4 = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix}$, the entries are $\begin{pmatrix} f_5 & f_4 \\ f_4 & f_3 \end{pmatrix}$.
- In $F^5 = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix}$, the entries are $\begin{pmatrix} f_6 & f_5 \\ f_5 & f_4 \end{pmatrix}$.

In every power $F^n$, the $(1,1)$ entry is $f_{n+1}$, both the $(1,2)$ and $(2,1)$ entries equal $f_n$, and the $(2,2)$ entry is $f_{n-1}$.

<br>

**Property / method used.** *Fibonacci Q-matrix representation:* the linear recurrence $f_{n+1} = f_n + f_{n-1}$ with $f_0 = 0, f_1 = 1$ is encoded by the $2\times 2$ symmetric matrix $F = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}$, whose powers advance the sequence indices by $1$ at each step.

<br>

**Mathematical verification.** Since $\det(F) = 1\cdot 0 - 1\cdot 1 = -1$, the determinant property $\det(F^n) = (\det F)^n = (-1)^n$ yields Cassini's identity $f_{n+1}f_{n-1} - f_n^2 = (-1)^n$. Checking $F^4$ and $F^5$ confirms the computed entries:

$$
\det(F^4) = 5\cdot 2 - 3\cdot 3 = 10 - 9 = 1 = (-1)^4, \qquad \det(F^5) = 8\cdot 3 - 5\cdot 5 = 24 - 25 = -1 = (-1)^5.
$$

---

##### 2. Computing $F \begin{pmatrix} a \\ b \end{pmatrix}$ and Explaining One Recurrence Step

**Result.**

$$
F
\begin{pmatrix}
a \\
b \\
\end{pmatrix}=
\begin{pmatrix}
a + b \\
a \\
\end{pmatrix}.
$$

<br>

**Main steps.** Multiply the $2\times 2$ matrix $F$ by the $2\times 1$ column vector $\begin{pmatrix} a \\ b \end{pmatrix}$:

$$
F
\begin{pmatrix}
a \\
b \\
\end{pmatrix}=
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
a \\
b \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot a + 1\cdot b \\
1\cdot a + 0\cdot b \\
\end{pmatrix}=
\begin{pmatrix}
a + b \\
a \\
\end{pmatrix}.
$$

Suppose the state vector $\begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} f_n \\ f_{n-1} \end{pmatrix}$ stores two consecutive terms of the recurrence, with the newer term $a = f_n$ in the top position and the older term $b = f_{n-1}$ in the bottom position:
1. **Top entry (creates the next term):** The first row $\begin{pmatrix} 1 & 1 \end{pmatrix}$ adds the two entries to produce $a + b = f_n + f_{n-1} = f_{n+1}$, placing the newly computed term at the top of the output vector.
2. **Bottom entry (keeps one term for the next step):** The second row $\begin{pmatrix} 1 & 0 \end{pmatrix}$ selects $a = f_n$ and discards $b = f_{n-1}$, shifting the current term $f_n$ down into the bottom position so that $\begin{pmatrix} f_{n+1} \\ f_n \end{pmatrix}$ holds the updated pair of consecutive terms for the next step.

<br>

**Property / method used.** *State-space (companion matrix) formulation of a second-order linear recurrence:* a two-term recurrence $x_{n+1} = x_n + x_{n-1}$ is converted into a first-order vector update $v_{n+1} = F v_n$ by stacking two consecutive terms into a state vector $v_n = \begin{pmatrix} x_n \\ x_{n-1} \end{pmatrix}$.

<br>

**Mathematical verification.** Starting from the initial state vector $v_1 = \begin{pmatrix} f_1 \\ f_0 \end{pmatrix} = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$ and applying $F$ five times reproduces the sequence step by step and matches the first column of each matrix power $F^n$ from Part 1:

$$
v_2 = Fv_1 =
\begin{pmatrix}
1 \\
1 \\
\end{pmatrix},\quad v_3 = Fv_2 =
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix},\quad v_4 = Fv_3 =
\begin{pmatrix}
3 \\
2 \\
\end{pmatrix},\quad v_5 = Fv_4 =
\begin{pmatrix}
5 \\
3 \\
\end{pmatrix},\quad v_6 = Fv_5 =
\begin{pmatrix}
8 \\
5 \\
\end{pmatrix}.
$$
