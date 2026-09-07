---
id: absolute-value-inequalities
title: Absolute Value Inequalities
---

# Absolute Value Inequalities

An absolute value inequality is any inequality ($\le, <, \ge, >$) where the variable is contained within at least one absolute value expression.

Just like with equations, the resolution logic relies on two approaches: the **Universal General Method** (domain partitioning derived directly from the piecewise definition) and **Algebraic Shortcuts** for specific structures.

---

## The Universal General Method: Domain Partition

The algorithm for inequalities follows the exact same partition procedure as equations:

* **Identify Critical Points:** Find the roots of all expressions inside absolute value bars (where $f(x) = 0$).
* **Partition the Domain:** Divide the real number line $\mathbb{R}$ into subintervals bounded by these critical points.
* **Remove Bars by Interval:** Replace each $|f(x)|$ with $f(x)$ (if $f(x) \ge 0$) or with $-f(x)$ (if $f(x) < 0$) within each specific interval.
* **Solve and Intersect:** Solve the resulting standard inequality for each interval and take the **intersection** of the solution set with that interval:
  $$S_i = S_{\text{inequality}} \cap I_i$$
* **Union of Solutions:** The final solution set is the union of all valid interval solutions:
  $$S = S_1 \cup S_2 \cup \dots \cup S_n$$

---

### Demonstrative Example

**Problem:** Solve $|x - 1| + |x - 3| < 4$.

#### Critical Points
* $x - 1 = 0 \implies x = 1$
* $x - 3 = 0 \implies x = 3$

The critical points divide the real line into three regions: $I_1 = (-\infty, 1)$, $I_2 = [1, 3]$, and $I_3 = (3, +\infty)$.

#### Solution by Interval

* **Interval I ($x < 1$):**  
  Both arguments are negative $\implies |x - 1| = -(x - 1)$ and $|x - 3| = -(x - 3)$.
  $$-(x - 1) - (x - 3) < 4 \implies -2x + 4 < 4 \implies -2x < 0 \implies x > 0$$
  **Intersection with $I_1$:** $(x > 0) \cap (x < 1) \implies \mathbf{S_1 = (0, 1)}$.

* **Interval II ($1 \le x \le 3$):**  
  First argument is non-negative, second is non-positive $\implies |x - 1| = x - 1$ and $|x - 3| = -(x - 3)$.
  $$(x - 1) - (x - 3) < 4 \implies x - 1 - x + 3 < 4 \implies 2 < 4 \quad \text{(Always True)}$$
  **Intersection with $I_2$:** Since the inequality holds for all elements in this range $\implies \mathbf{S_2 = [1, 3]}$.

* **Interval III ($x > 3$):**  
  Both arguments are positive $\implies |x - 1| = x - 1$ and $|x - 3| = x - 3$.
  $$(x - 1) + (x - 3) < 4 \implies 2x - 4 < 4 \implies 2x < 8 \implies x < 4$$
  **Intersection with $I_3$:** $(x < 4) \cap (x > 3) \implies \mathbf{S_3 = (3, 4)}$.

#### Union of Solutions
$$S = S_1 \cup S_2 \cup S_3 = (0, 1) \cup [1, 3] \cup (3, 4) \implies \mathbf{S = (0, 4)}$$

---

## Algebraic Shortcuts Based on Properties

For inequalities matching standard forms with a constant $k > 0$, properties proven in Module 02 significantly simplify the solution process.

### Case $|f(x)| < k$ (Compressing the Interval)
By the geometric interpretation of distance:

$$|f(x)| < k \iff -k < f(x) < k$$

*(Analogously holds for $\le$).*

---

### Case $|f(x)| > k$ (Expanding to the Tails)
Points whose distance from the origin is greater than $k$:

$$|f(x)| > k \iff f(x) > k \quad \text{or} \quad f(x) < -k$$

*(Analogously holds for $\ge$).*

---

### Case $|f(x)| < |g(x)|$ (Squaring Both Sides)
Since both sides are non-negative, we apply the Even Power property:

$$|f(x)|^2 < |g(x)|^2 \iff [f(x)]^2 - [g(x)]^2 < 0$$
$$[f(x) - g(x)][f(x) + g(x)] < 0$$

> **Advantage:** Avoids studying the signs of multiple absolute values individually.

---

### Triangle Inequality Form ($|a + b| \le |a| + |b|$)
Since the triangle inequality is **always true** for all real numbers:
* $|a + b| \le |a| + |b| \implies S = \mathbb{R}$ (within valid domains).
* $|a + b| > |a| + |b| \implies S = \emptyset$ (impossible by definition).

---

## Exotic Cases and Pitfalls

### Pitfall 1: Negative Constant ($|f(x)| \le k$ where $k < 0$)
**Problem:** Solve $|3x - 5| \le -2$.  
* **Shortcut Analysis:** By Non-negativity, $|3x - 5| \ge 0$ for all $x$. A non-negative number can never be $\le -2$.  
* **Solution:** $S = \emptyset$.

---

### Pitfall 2: Negative Constant ($|f(x)| > k$ where $k < 0$)
**Problem:** Solve $|x^2 + 1| > -5$.  
* **Shortcut Analysis:** An absolute value is always $\ge 0$, making it strictly greater than any negative number for all $x \in \mathbb{R}$.  
* **Solution:** $S = \mathbb{R}$.

---

### Pitfall 3: Rational Inequalities with Absolute Value in Denominator
**Problem:** Solve $\dfrac{2}{|x - 1|} \ge 1$.  

* **Domain Restriction (Existence Condition):** Denominator cannot be zero $\implies x \neq 1$.
* Since $|x - 1| > 0$ for all $x \neq 1$, we can multiply both sides by $|x - 1|$ **without reversing the inequality sign**:
  $$2 \ge |x - 1| \iff |x - 1| \le 2$$
* Applying shortcut $|u| \le k$:
  $$-2 \le x - 1 \le 2 \implies -1 \le x \le 3$$
* **Applying Domain Restriction ($x \neq 1$):**
  $$S = [-1, 3] \setminus \{1\} \quad \text{or} \quad S = [-1, 1) \cup (1, 3]$$

---

## Conclusion: The General Method vs. Exotic Cases

To demonstrate the universality of the **General Method (Domain Partition)**, we will solve all three exotic cases above using **only the piecewise definition**, proving it handles every edge case without relying on shortcut rules.

---

### Pitfall 1 via General Method: $|3x - 5| \le -2$

Critical point: $3x - 5 = 0 \implies x = \frac{5}{3}$.

* **Interval I ($x < \frac{5}{3}$):**  
  Argument is negative $\implies |3x - 5| = -(3x - 5)$.
  $$-(3x - 5) \le -2 \implies -3x + 5 \le -2 \implies -3x \le -7 \implies x \ge \frac{7}{3}$$
  **Intersection:** $(x \ge \frac{7}{3}) \cap (x < \frac{5}{3})$.  
  Since $\frac{7}{3} \approx 2.33 > 1.66 \approx \frac{5}{3}$, there is no overlap $\implies S_1 = \emptyset$.

* **Interval II ($x \ge \frac{5}{3}$):**  
  Argument is non-negative $\implies |3x - 5| = 3x - 5$.
  $$3x - 5 \le -2 \implies 3x \le 3 \implies x \le 1$$
  **Intersection:** $(x \le 1) \cap (x \ge \frac{5}{3})$.  
  Since $1 < \frac{5}{3}$, there is no overlap $\implies S_2 = \emptyset$.

**Conclusion:** $S = S_1 \cup S_2 = \emptyset$.

---

### Pitfall 2 via General Method: $|x^2 + 1| > -5$

Critical point: $x^2 + 1 = 0 \implies x^2 = -1$ (no real roots).  
Since $x^2 + 1 > 0$ for all $x \in \mathbb{R}$, there are no critical points splitting the real line. The sign is strictly positive everywhere.

* **Single Interval ($x \in \mathbb{R}$):**  
  Because the argument is always positive, $|x^2 + 1| = x^2 + 1$.
  $$x^2 + 1 > -5 \implies x^2 > -6$$
  Since the square of any real number is always non-negative ($x^2 \ge 0$), $x^2 > -6$ holds for **all** real numbers.

**Conclusion:** $S = \mathbb{R}$.

---

### Pitfall 3 via General Method: $\dfrac{2}{|x - 1|} \ge 1$

Domain Restriction: $x \neq 1$.  
Critical point for $|x - 1|$: $x = 1$.

* **Interval I ($x < 1$):**  
  Here, $|x - 1| = -(x - 1) = 1 - x$.
  $$\frac{2}{1 - x} \ge 1 \implies \frac{2}{1 - x} - 1 \ge 0 \implies \frac{2 - (1 - x)}{1 - x} \ge 0 \implies \frac{x + 1}{1 - x} \ge 0$$
  Analyzing signs of numerator $(x + 1)$ and denominator $(1 - x)$:
  * Roots at $x = -1$ and $x = 1$.
  * Fraction is positive for $-1 \le x < 1$.  
  **Intersection with $I_1$ ($x < 1$):** $\mathbf{S_1 = [-1, 1)}$.

* **Interval II ($x > 1$):**  
  Here, $|x - 1| = x - 1$.
  $$\frac{2}{x - 1} \ge 1 \implies \frac{2}{x - 1} - 1 \ge 0 \implies \frac{2 - (x - 1)}{x - 1} \ge 0 \implies \frac{3 - x}{x - 1} \ge 0$$
  Analyzing signs of numerator $(3 - x)$ and denominator $(x - 1)$:
  * Roots at $x = 1$ and $x = 3$.
  * Fraction is positive for $1 < x \le 3$.  
  **Intersection with $I_2$ ($x > 1$):** $\mathbf{S_2 = (1, 3]}$.

**Conclusion:** $S = S_1 \cup S_2 = [-1, 1) \cup (1, 3] = [-1, 3] \setminus \{1\}$.
