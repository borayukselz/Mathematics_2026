### Exercise 1. Vector Operations and Their Meaning

#### Exercise Reminder

For $u = (2, -1, 3)$ and $v = (-1, 4, 2)$ compute

$$
u + v, \qquad u - v, \qquad 3u - 2v.
$$

Then verify that $(u + v) - v = u$, and explain geometrically what adding two vectors means.

---

#### Solution

**Result.**
- $u + v = (1, 3, 5)$
- $u - v = (3, -5, 1)$
- $3u - 2v = (8, -11, 5)$

<br>

**Main steps.**

1. **Compute the vector sum $u + v$ componentwise:**

$$
u + v = (2, -1, 3) + (-1, 4, 2) = (2 + (-1), \ -1 + 4, \ 3 + 2) = (1, 3, 5).
$$

2. **Compute the vector difference $u - v$ componentwise:**

$$
u - v = (2, -1, 3) - (-1, 4, 2) = (2 - (-1), \ -1 - 4, \ 3 - 2) = (3, -5, 1).
$$

3. **Compute the linear combination $3u - 2v$ using scalar multiplication and componentwise subtraction:**

$$
3u = 3(2, -1, 3) = (6, -3, 9), \qquad 2v = 2(-1, 4, 2) = (-2, 8, 4),
$$

$$
3u - 2v = (6, -3, 9) - (-2, 8, 4) = (6 - (-2), \ -3 - 8, \ 9 - 4) = (8, -11, 5).
$$

4. **Geometric meaning of vector addition:**
   - **Tip-to-tail (triangle) rule:** Placing the initial point (tail) of $v$ at the terminal point (tip) of $u$ produces the resultant displacement vector $u + v$ starting at the tail of $u$ and ending at the tip of $v$; equivalently, $u + v$ represents the net displacement obtained by first moving along $u$ and then moving along $v$.
   - **Parallelogram rule:** When $u$ and $v$ are drawn starting from the same origin, $u + v$ is the main diagonal of the parallelogram spanned by $u$ and $v$.

<br>

**Property / method used.** *Vector space axioms in $\mathbb{R}^3$ (componentwise addition and scalar multiplication):* operations are performed coordinate by coordinate, satisfying associativity and additive inverse properties so that $(u + v) - v = u + (v - v) = u + \mathbf{0} = u$.

<br>

**Mathematical verification.** Subtracting $v = (-1, 4, 2)$ directly from the computed sum $u + v = (1, 3, 5)$ recovers $u$:

$$
(u + v) - v = (1, 3, 5) - (-1, 4, 2) = (1 - (-1), \ 3 - 4, \ 5 - 2) = (2, -1, 3) = u.
$$
```[cite: 11]
