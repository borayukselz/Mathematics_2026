### Exercise 4. Dot Product and Perpendicularity

#### Exercise Reminder

For $u = (1, 2, -1)$ and $v = (2, -1, 3)$ compute $u \cdot v$ and determine whether the vectors are perpendicular. Then find $a$ so that $w = (2, -1, a)$ is perpendicular to $u$, and check the result.

---

#### Solution

**Result.**
- **Dot product $u \cdot v$:** $u \cdot v = -3$
- **Perpendicularity of $u$ and $v$:** **Not perpendicular** (since $u \cdot v = -3 \neq 0$; the angle between them is obtuse).
- **Parameter value for $w \perp u$:** $a = 0$, giving $w = (2, -1, 0)$.

<br>

**Main steps.**

1. **Compute the standard Euclidean dot product $u \cdot v$:**

$$
u \cdot v = (1, 2, -1) \cdot (2, -1, 3) = (1)(2) + (2)(-1) + (-1)(3) = 2 - 2 - 3 = -3.
$$

2. **Determine whether $u$ and $v$ are perpendicular:**
   - Two nonzero vectors in $\mathbb{R}^3$ are perpendicular (orthogonal) if and only if their dot product equals $0$.
   - Because $u \cdot v = -3 \neq 0$, the vectors $u$ and $v$ are **not perpendicular** (moreover, since $u \cdot v < 0$, the angle between them is strictly greater than $90^\circ$).

3. **Set up the orthogonality condition $u \cdot w = 0$ and solve for $a$:**
   - For $w = (2, -1, a)$ to be perpendicular to $u = (1, 2, -1)$, we require $u \cdot w = 0$:

$$
u \cdot w = (1)(2) + (2)(-1) + (-1)(a) = 0
$$

$$
2 - 2 - a = 0 \implies -a = 0 \implies a = 0.
$$

   - Hence $w = (2, -1, 0)$.

<br>

**Property / method used.** *Euclidean inner product orthogonality criterion in $\mathbb{R}^3$:* nonzero vectors $x, y \in \mathbb{R}^3$ satisfy $x \perp y \iff x \cdot y = x_1y_1 + x_2y_2 + x_3y_3 = 0$.

<br>

**Mathematical verification.** Substituting $a = 0$ into $w = (2, -1, a)$ and computing both $u \cdot w$ and the Pythagorean norm identity $|u + w|^2 = |u|^2 + |w|^2$ confirms orthogonality:

$$
u \cdot w = (1)(2) + (2)(-1) + (-1)(0) = 2 - 2 + 0 = 0,
$$

$$
|u + w|^2 = |(3, 1, -1)|^2 = 9 + 1 + 1 = 11, \qquad |u|^2 + |w|^2 = (1 + 4 + 1) + (4 + 1 + 0) = 6 + 5 = 11.
$$
```[cite: 12]
