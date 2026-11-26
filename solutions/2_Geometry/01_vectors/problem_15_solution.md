### Exercise 15. Comparing Directions Using the Cosine of the Angle

#### Exercise Reminder

Given

$$
a = (1, 2, 1), \qquad b = (2, 4, 2), \qquad c = (2, 0, 3).
$$

For each pair, compute

$$
\frac{u \cdot v}{|u||v|}.
$$

Order the pairs by increasing angle between the vectors. Explain why for $a$ and $b$ the value is $1$ even though the vectors have different lengths.

---

#### Solution

**Result.**
- **Cosine values for each pair:**
  - **Pair $(a, b)$:** $\cos\theta_{ab} = \frac{a \cdot b}{|a||b|} = 1$ ($\theta_{ab} = 0^\circ$)
  - **Pair $(a, c)$:** $\cos\theta_{ac} = \frac{a \cdot c}{|a||c|} = \frac{5}{\sqrt{78}} \approx 0.5661$ ($\theta_{ac} \approx 55.52^\circ$)
  - **Pair $(b, c)$:** $\cos\theta_{bc} = \frac{b \cdot c}{|b||c|} = \frac{5}{\sqrt{78}} \approx 0.5661$ ($\theta_{bc} \approx 55.52^\circ$)
- **Order by increasing angle:**

$$
\theta_{ab} < \theta_{ac} = \theta_{bc} \qquad \text{or equivalently} \qquad \theta_{ab} < \theta_{bc} = \theta_{ac}.
$$

- **Why $\frac{a \cdot b}{|a||b|} = 1$ despite different lengths:** Dividing each vector by its norm normalizes both vectors to the exact same unit direction vector $\frac{a}{|a|} = \frac{b}{|b|} = \frac{1}{\sqrt{6}}(1, 2, 1)$, so the positive scaling factor $2$ in $b = 2a$ cancels completely between the numerator and denominator.

<br>

**Main steps.**

1. **Compute the Euclidean norms $|a|$, $|b|$, and $|c|$:**

$$
|a| = \sqrt{1^2 + 2^2 + 1^2} = \sqrt{1 + 4 + 1} = \sqrt{6},
$$

$$
|b| = \sqrt{2^2 + 4^2 + 2^2} = \sqrt{4 + 16 + 4} = \sqrt{24} = 2\sqrt{6},
$$

$$
|c| = \sqrt{2^2 + 0^2 + 3^2} = \sqrt{4 + 0 + 9} = \sqrt{13}.
$$

2. **Compute $\frac{u \cdot v}{|u||v|}$ for each of the three pairs:**
   - **Pair $(a, b)$:**

$$
a \cdot b = (1, 2, 1) \cdot (2, 4, 2) = (1)(2) + (2)(4) + (1)(2) = 2 + 8 + 2 = 12,
$$

$$
\cos\theta_{ab} = \frac{a \cdot b}{|a||b|} = \frac{12}{\sqrt{6} \cdot 2\sqrt{6}} = \frac{12}{2 \cdot 6} = \frac{12}{12} = 1.
$$

   - **Pair $(a, c)$:**

$$
a \cdot c = (1, 2, 1) \cdot (2, 0, 3) = (1)(2) + (2)(0) + (1)(3) = 2 + 0 + 3 = 5,
$$

$$
\cos\theta_{ac} = \frac{a \cdot c}{|a||c|} = \frac{5}{\sqrt{6}\sqrt{13}} = \frac{5}{\sqrt{78}} \approx 0.5661.
$$

   - **Pair $(b, c)$:**

$$
b \cdot c = (2, 4, 2) \cdot (2, 0, 3) = (2)(2) + (4)(0) + (2)(3) = 4 + 0 + 6 = 10,
$$

$$
\cos\theta_{bc} = \frac{b \cdot c}{|b||c|} = \frac{10}{2\sqrt{6}\sqrt{13}} = \frac{10}{2\sqrt{78}} = \frac{5}{\sqrt{78}} \approx 0.5661.
$$

3. **Order the pairs by increasing angle between the vectors:**
   - On the interval $\theta \in [0, \pi]$, the cosine function $\cos\theta$ is **strictly decreasing**, so a larger cosine corresponds to a smaller angle:

$$
\cos\theta_{ab} = 1 > \cos\theta_{ac} = \cos\theta_{bc} = \frac{5}{\sqrt{78}} \implies \theta_{ab} < \theta_{ac} = \theta_{bc}.
$$

   - Specifically, $\theta_{ab} = \arccos(1) = 0^\circ$ while $\theta_{ac} = \theta_{bc} = \arccos\left(\frac{5}{\sqrt{78}}\right) \approx 55.52^\circ$, so $(a, b)$ has the strictly smallest angle, followed by a tie between $(a, c)$ and $(b, c)$.

4. **Explain why $\frac{a \cdot b}{|a||b|} = 1$ even though $|a| \neq |b|$:**
   - The ratio $\frac{u \cdot v}{|u||v|} = \left(\frac{u}{|u|}\right) \cdot \left(\frac{v}{|v|}\right)$ depends **only on the unit direction vectors** of $u$ and $v$, not on their magnitudes.
   - Here $b = 2a$ is a **strictly positive scalar multiple** of $a$, meaning $b$ is twice as long as $a$ ($|b| = 2|a|$) while pointing in the exact same direction and orientation ($\theta_{ab} = 0^\circ$). Algebraically, the length factor $\lambda = 2 > 0$ factors out of both numerator and denominator and cancels:

$$
\frac{a \cdot (2a)}{|a||2a|} = \frac{2(a \cdot a)}{2|a|^2} = \frac{|a|^2}{|a|^2} = 1.
$$

<br>

**Property / method used.** **Scale-invariance of the cosine similarity formula in $\mathbb{R}^3$:** $\cos\theta = \frac{u \cdot v}{|u||v|} = \hat{u} \cdot \hat{v}$ is invariant under multiplication by positive scalars ($\lambda > 0$), so any two vectors pointing in the same direction satisfy $\cos\theta = 1$ regardless of their lengths.

<br>

**Mathematical verification.** Checking the Cauchy–Schwarz inequality $|u \cdot v| \le |u||v|$ (where equality holds if and only if $u$ and $v$ are linearly dependent) confirms all three ratios:
- For $(a, b)$, $b = 2a$ makes $\{a, b\}$ linearly dependent with positive proportionality constant, achieving the upper bound $\frac{a \cdot b}{|a||b|} = 1$.
- For $(a, c)$ and $(b, c)$, $5^2 = 25 < 78 = |a|^2|c|^2$, confirming strict inequality $0 < \frac{5}{\sqrt{78}} < 1$ and identical angles since $b = 2a$ shares the exact same ray as $a$.
