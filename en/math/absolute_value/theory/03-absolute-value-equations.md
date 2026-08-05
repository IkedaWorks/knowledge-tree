---
id: absolute_value_equations
title: Absolute Value Equations
---

# Absolute Value Equations

An absolute value equation is any equation where the unknown variable is contained within at least one absolute value expression.

In this module, we will explore the **Universal General Method** — a domain partition technique derived directly from the piecewise definition of absolute value —, followed by **Algebraic Shortcuts** utilizing the properties proven in the previous module, and concluding with a set of **Exotic Cases and Pitfalls**.

---

## The Universal General Method: Domain Partition

The general method is not an arbitrary rule: **it is the direct application of the piecewise definition of absolute value to the real number line**. 

Recall the fundamental definition:

$$|f(x)| = \begin{cases} f(x), & \text{if } f(x) \ge 0 \\ -f(x), & \text{if } f(x) < 0 \end{cases}$$

When an equation contains multiple absolute values, the behavior of each expression depends on the sign of its argument. By finding where each expression equals zero (the critical points), we partition the real number line $\mathbb{R}$ into subintervals where the signs of all arguments remain constant, allowing us to remove the absolute value bars unambiguously.

---

### The Resolution Algorithm

* **Identify Critical Points:** Find the roots of all expressions inside absolute value bars (where $f(x) = 0$).
* **Partition the Domain:** Divide the real line $\mathbb{R}$ into subintervals bounded by these critical points.
* **Evaluate and Remove Bars by Interval:** Replace each $|f(x)|$ with $f(x)$ (if $f(x) \ge 0$) or with $-f(x)$ (if $f(x) < 0$) within each specific interval.
* **Solve and Validate:** Solve the resulting standard algebraic equation for each interval and take the **intersection** of the solution with that interval ($S_i = S_{\text{equation}} \cap I_i$).
* **Union of Solutions:** The final solution set is the union of all valid solutions:
  $$S = S_1 \cup S_2 \cup \dots \cup S_n$$

---

### Demonstrative Example

**Problem:** Solve $|x - 2| + |2x + 4| = 6 - x$.

#### Critical Points
* $x - 2 = 0 \implies x = 2$
* $2x + 4 = 0 \implies x = -2$

#### Domain Partition
The critical points $-2$ and $2$ divide the real line into three regions:
* **Interval I:** $x < -2$
* **Interval II:** $-2 \le x < 2$
* **Interval III:** $x \ge 2$

---

#### Solution by Interval

* **Interval I ($x < -2$):**  
  For $x < -2$, we have $(x - 2) < 0 \implies |x - 2| = -(x - 2)$  
  For $x < -2$, we have $(2x + 4) < 0 \implies |2x + 4| = -(2x + 4)$  
  
  Substituting into the equation:
  $$-(x - 2) - (2x + 4) = 6 - x$$
  $$-3x - 2 = 6 - x \implies -2x = 8 \implies x = -4$$
  
  **Validation:** Does $x = -4$ belong to Interval I ($x < -2$)? **Yes.**  
  $\implies S_1 = \{-4\}$

* **Interval II ($-2 \le x < 2$):**  
  For $x < 2$, we have $(x - 2) < 0 \implies |x - 2| = -(x - 2)$  
  For $x \ge -2$, we have $(2x + 4) \ge 0 \implies |2x + 4| = 2x + 4$  
  
  Substituting into the equation:
  $$-(x - 2) + (2x + 4) = 6 - x$$
  $$x + 6 = 6 - x \implies 2x = 0 \implies x = 0$$
  
  **Validation:** Does $x = 0$ belong to Interval II ($-2 \le x < 2$)? **Yes.**  
  $\implies S_2 = \{0\}$

* **Interval III ($x \ge 2$):**  
  For $x \ge 2$, we have $(x - 2) \ge 0 \implies |x - 2| = x - 2$  
  For $x \ge 2$, we have $(2x + 4) \ge 0 \implies |2x + 4| = 2x + 4$  
  
  Substituting into the equation:
  $$(x - 2) + (2x + 4) = 6 - x$$
  $$3x + 2 = 6 - x \implies 4x = 4 \implies x = 1$$
  
  **Validation:** Does $x = 1$ belong to Interval III ($x \ge 2$)? **No** ($1 < 2$).  
  $\implies S_3 = \emptyset$

---

#### Union of Solutions
$$S = S_1 \cup S_2 \cup S_3 = \{-4\} \cup \{0\} \cup \emptyset \implies S = \{-4, 0\}$$

---

## Algebraic Shortcuts Based on Properties

When an equation matches specific structural patterns, we can leverage proven properties to bypass domain partitioning.

### Case $|f(x)| = k$ (where $k \in \mathbb{R}$)
By Non-negativity and Nullity properties:
* If $k < 0 \implies S = \emptyset$
* If $k = 0 \implies f(x) = 0$
* If $k > 0 \implies f(x) = k \quad \text{or} \quad f(x) = -k$

---

### Case $|f(x)| = g(x)$
Since $|f(x)| \ge 0$, the right side must also be non-negative.
1. **Existence Condition (EC):** $g(x) \ge 0$
2. **Resolution:** $f(x) = g(x) \quad \text{or} \quad f(x) = -g(x)$
3. **Filter:** Keep only candidate roots satisfying the EC.

---

### Equality Between Absolute Values ($|f(x)| = |g(x)|$)
By the Even Power property ($|a|^2 = a^2$), squaring both sides yields:

$$|f(x)|^2 = |g(x)|^2 \implies [f(x)]^2 - [g(x)]^2 = 0$$
$$[f(x) - g(x)][f(x) + g(x)] = 0 \iff f(x) = g(x) \quad \text{or} \quad f(x) = -g(x)$$

> **Advantage:** No Existence Condition required, as both sides are naturally non-negative.

---

### Form of the Triangle Equality ($|a + b| = |a| + |b|$)
By the Triangle Equality Condition property:

$$|a + b| = |a| + |b| \iff a \cdot b \ge 0$$

---

## Exotic Cases and Pitfalls

### Pitfall 1: Extraneous Solutions and Existence Conditions

**Problem:** Solve $|2x - 3| = x - 3$.

**Resolution:**  
Splitting the equation without checking the right-hand side yields:
1. $2x - 3 = x - 3 \implies x = 0$
2. $2x - 3 = -(x - 3) \implies 3x = 6 \implies x = 2$

Applying the **Existence Condition (EC)** for $|f(x)| = g(x)$:
$$\text{EC: } g(x) \ge 0 \implies x - 3 \ge 0 \implies x \ge 3$$

**Evaluating Candidates:**
* $x = 0$: $0 \ge 3$ is **false**.
* $x = 2$: $2 \ge 3$ is **false**.

**Conclusion:** Neither candidate is valid.  
$$S = \emptyset$$

---

### Pitfall 2: Nested Absolute Values

**Problem:** Solve $||x - 3| - 4| = 2$.

**Resolution:**  
Instead of partitioning immediately, apply $|u| = k \implies u = k \text{ or } u = -k$ to the outer absolute value:

Let $u = |x - 3| - 4$. Since $k = 2 > 0$:

* **Branch A:**
  $$|x - 3| - 4 = 2 \implies |x - 3| = 6$$
  $$x - 3 = 6 \implies x = 9 \quad \text{or} \quad x - 3 = -6 \implies x = -3$$

* **Branch B:**
  $$|x - 3| - 4 = -2 \implies |x - 3| = 2$$
  $$x - 3 = 2 \implies x = 5 \quad \text{or} \quad x - 3 = -2 \implies x = 1$$

**Solution Set:**
$$S = \{-3, 1, 5, 9\}$$

---

### Pitfall 3: Equations with Infinite Solutions (Continuous Sets)

**Problem:** Solve $|x - 1| + |x - 5| = 4$.

**Resolution via Triangle Equality:**  
Notice that the constant on the right ($4$) is equal to $(x - 1) - (x - 5)$.  
Using symmetry $|a| = |-a|$, rewrite $|x - 5|$ as $|5 - x|$:

$$|x - 1| + |5 - x| = 4$$

Since $(x - 1) + (5 - x) = 4$, the equation matches the form $|a| + |b| = a + b$.  
The necessary and sufficient condition is $a \cdot b \ge 0$:

$$(x - 1)(5 - x) \ge 0 \iff (x - 1)(x - 5) \le 0$$

Solving the quadratic inequality yields:
$$1 \le x \le 5$$

**Solution Set:**
$$S = [1, 5]$$

---

### Pitfall 4: The Square Root of a Square Trap

**Problem:** Solve $\sqrt{x^2 - 6x + 9} + |x - 3| = 8$.

**Resolution:**  
Simplifying $\sqrt{(x-3)^2}$ directly to $(x - 3)$ is incorrect.  
Using the identity $\sqrt{u^2} = |u|$:

$$\sqrt{x^2 - 6x + 9} = \sqrt{(x - 3)^2} = |x - 3|$$

Substituting back:
$$|x - 3| + |x - 3| = 8 \implies 2|x - 3| = 8 \implies |x - 3| = 4$$

Unfolding the absolute value:
* $x - 3 = 4 \implies x = 7$
* $x - 3 = -4 \implies x = -1$

**Solution Set:**
$$S = \{-1, 7\}$$