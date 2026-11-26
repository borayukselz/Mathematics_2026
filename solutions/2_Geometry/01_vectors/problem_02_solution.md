### Exercise 2. Distance as the Length of a Vector

#### Exercise Reminder

The points are $A = (1, 2, 3)$ and $B = (4, -2, 6)$.

1. Construct $\overrightarrow{AB}$.
2. Compute its length.
3. Compute the distance between the points using the coordinate formula.
4. Explain why both calculations give the same result.

---

#### Solution

**Result.**
- **Displacement vector:** $\overrightarrow{AB} = (3, -4, 3)$
- **Length / Euclidean distance:** $|\overrightarrow{AB}| = d(A, B) = \sqrt{34}$

<br>

**Main steps.**

1. **Construct the displacement vector $\overrightarrow{AB}$ (terminal point minus initial point):**

$$
\overrightarrow{AB} = B - A = (4, -2, 6) - (1, 2, 3) = (4 - 1, \ -2 - 2, \ 6 - 3) = (3, -4, 3).
$$

2. **Compute the Euclidean length (norm) $|\overrightarrow{AB}|$ of the vector $\overrightarrow{AB} = (3, -4, 3)$:**

$$
|\overrightarrow{AB}| = \sqrt{3^2 + (-4)^2 + 3^2} = \sqrt{9 + 16 + 9} = \sqrt{34}.
$$

3. **Compute the distance $d(A, B)$ directly using the $3\text{D}$ coordinate distance formula:**

$$
d(A, B) = \sqrt{(x_B - x_A)^2 + (y_B - y_A)^2 + (z_B - z_A)^2}
$$

$$
d(A, B) = \sqrt{(4 - 1)^2 + (-2 - 2)^2 + (6 - 3)^2} = \sqrt{3^2 + (-4)^2 + 3^2} = \sqrt{9 + 16 + 9} = \sqrt{34}.
$$

4. **Explain why both calculations give the exact same result:**
   - The components of $\overrightarrow{AB} = (x_B - x_A, \, y_B - y_A, \, z_B - z_A)$ represent the signed coordinate displacements along the $x$-, $y$-, and $z$-axes needed to travel from $A$ to $B$.
   - The Euclidean norm $|v| = \sqrt{v_1^2 + v_2^2 + v_3^2}$ applies the $3\text{D}$ Pythagorean theorem to those three orthogonal displacement components, which is algebraically identical to the coordinate distance formula $d(A, B) = \sqrt{(x_B - x_A)^2 + (y_B - y_A)^2 + (z_B - z_A)^2}$ — in fact, Euclidean distance between two points in $\mathbb{R}^3$ is defined as the length of the vector connecting them ($d(A, B) = |\overrightarrow{AB}|$).

<br>

**Property / method used.** *Euclidean norm of a displacement vector in $\mathbb{R}^3$:* the distance metric $d(A, B)$ induced by the standard inner product on $\mathbb{R}^3$ equals the norm $|\overrightarrow{AB}| = \sqrt{\overrightarrow{AB} \cdot \overrightarrow{AB}}$ of the difference vector $B - A$.

<br>

**Mathematical verification.** Reversing the orientation to construct $\overrightarrow{BA} = A - B = (-3, 4, -3)$ and computing its length confirms invariance under direction reversal:

$$
|\overrightarrow{BA}| = \sqrt{(-3)^2 + 4^2 + (-3)^2} = \sqrt{9 + 16 + 9} = \sqrt{34} = |\overrightarrow{AB}|.
$$
