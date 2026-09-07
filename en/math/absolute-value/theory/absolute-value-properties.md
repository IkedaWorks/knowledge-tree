---
id: absolute-value-properties
title: Absolute Value Properties
---
# Properties of Absolute Value

After defining absolute value as the geometric distance to the origin and formalizing it piecewise, we can derive its fundamental properties. None of these properties appear out of nowhere: all are direct consequences of the algebraic definition itself.

---

## Overview of Properties

For any real numbers $x, y \in \mathbb{R}$:

* **Non-negativity:** $|x| \ge 0$  
  Since absolute value represents physical distance, its value can never be negative.

* **Nullity:** $|x| = 0 \iff x = 0$  
  The only distance equal to zero occurs at the origin itself.

* **Symmetry:** $|-x| = |x|$ and $|a - b| = |b - a|$  
  The distance from a point to the origin (or between two points) does not depend on direction.

* **Multiplicativity:** $|x \cdot y| = |x| \cdot |y|$  
  The absolute value of a product is the product of the absolute values.

* **Divisibility:** $\left|\dfrac{x}{y}\right| = \dfrac{|x|}{|y|}$ (with $y \neq 0$)  
  The absolute value of a division is the division of the absolute values.

* **Identity with Even Power:** $\sqrt{x^2} = |x|$  
  The principal square root of a squared number always results in its absolute value.

* **Bounding Property:** $-|x| \le x \le |x|$  
  Any real number $x$ is bounded below by the negative of its absolute value and above by its absolute value.

* **Idempotence and Even Power:** $||x|| = |x|$ and $|x^2| = x^2 = |x|^2$  
  Applying absolute value multiple times is redundant, and squaring eliminates the need for absolute value bars.

* **Absolute Value Inequality Properties (for $k > 0$):**  
  * $|x| \le k \iff -k \le x \le k$ (defines a bounded interval around zero).  
  * $|x| \ge k \iff x \le -k \text{ or } x \ge k$ (defines the regions outside the interval).

* **Triangle Inequality:** $|x + y| \le |x| + |y|$  
  The sum of absolute values is always greater than or equal to the absolute value of the sum.

* **Reverse Triangle Inequality:** $||x| - |y|| \le |x - y|$  
  The difference between the absolute values of two numbers never exceeds the absolute value of their difference.

---

## Proofs Based on Definition

To prove any property without circular reasoning, we rely **solely** on the elementary definition:

$$|x| = \begin{cases} x, & \text{if } x \ge 0 \\ -x, & \text{if } x < 0 \end{cases}$$

---

### Symmetry ($|-x| = |x|$)

We want to prove that the absolute value of a number and the absolute value of its opposite yield the same result.

* **Case 1 ($x \ge 0$):**  
  By definition, $|x| = x$.  
  If $x \ge 0$, then its opposite $-x \le 0$.  
  * If $x = 0$, we have $|0| = 0$ and $|-0| = 0$, hence $|-x| = |x|$.  
  * If $x > 0$, then $-x < 0$. By definition, we invert the sign:  
    $$|-x| = -(-x) = x$$  
  Since $|x| = x$ and $|-x| = x$, we conclude that $|-x| = |x|$.

* **Case 2 ($x < 0$):**  
  By definition, $|x| = -x$.  
  If $x < 0$, multiplying by $-1$ shows its opposite is positive ($-x > 0$).  
  Applying the definition to the argument $(-x)$, since it is positive, the value remains unchanged:  
    $$|-x| = -x$$  
  Since $|x| = -x$ and $|-x| = -x$, we conclude that $|-x| = |x|$. $\blacksquare$

---

### Multiplicativity ($|x \cdot y| = |x| \cdot |y|$)

We split the analysis based on the sign of the product $x \cdot y$:

* **Case 1 ($x \cdot y \ge 0$):**  
  If the product is non-negative, by the definition of absolute value:
  $$|x \cdot y| = x \cdot y$$
  Analyzing individual factors:
  * If $x \ge 0$ and $y \ge 0$, we have $|x| = x$ and $|y| = y$. Thus, $|x| \cdot |y| = x \cdot y$.
  * If $x \le 0$ and $y \le 0$, we have $|x| = -x$ and $|y| = -y$. Thus, $|x| \cdot |y| = (-x)(-y) = x \cdot y$.  
  In both subcases, $|x \cdot y| = |x| \cdot |y|$.

* **Case 2 ($x \cdot y < 0$):**  
  If the product is negative, by definition we invert the sign:
  $$|x \cdot y| = -(x \cdot y)$$
  Since the product is negative, the factors have opposite signs. Without loss of generality, assume $x > 0$ and $y < 0$:
  * Since $x > 0$, by definition $|x| = x$.
  * Since $y < 0$, by definition $|y| = -y$.  
  Multiplying the absolute values:
  $$|x| \cdot |y| = x \cdot (-y) = -(x \cdot y)$$
  Since $|x \cdot y| = -(x \cdot y)$ and $|x| \cdot |y| = -(x \cdot y)$, we conclude that $|x \cdot y| = |x| \cdot |y|$. $\blacksquare$

---

### Divisibility ($\left|\dfrac{x}{y}\right| = \dfrac{|x|}{|y|}$)

For $y \neq 0$, we first prove that $\left|\dfrac{1}{y}\right| = \dfrac{1}{|y|}$:

By the multiplicativity property:
$$|y| \cdot \left|\frac{1}{y}\right| = \left|y \cdot \frac{1}{y}\right| = |1| = 1$$

Isolating $\left|\dfrac{1}{y}\right|$:
$$\left|\frac{1}{y}\right| = \frac{1}{|y|}$$

Now, rewriting the fraction $\dfrac{x}{y}$ as a product $x \cdot \dfrac{1}{y}$:
$$\left|\frac{x}{y}\right| = \left|x \cdot \frac{1}{y}\right| = |x| \cdot \left|\frac{1}{y}\right| = |x| \cdot \frac{1}{|y|} = \frac{|x|}{|y|} \quad \blacksquare$$

---

### Identity $\sqrt{x^2} = |x|$

> [!WARNING]
> **Common Error**  
> The expression $\sqrt{x^2}$ is **not** simply $x$. The radical $\sqrt{\quad}$ denotes by convention the **non-negative** square root.

Analyzing the operation $\sqrt{x^2}$:

* **If $x \ge 0$:** The value $x^2$ is non-negative and its positive root is $x$ itself. Since $|x| = x$, we have $\sqrt{x^2} = |x|$.
* **If $x < 0$:** The value $x^2$ remains positive, but its positive root will be the opposite of $x$ (that is, $-x$). Since for $x < 0$ the definition yields $|x| = -x$, we again have $\sqrt{x^2} = |x|$.

---

### Absolute Value Inequality Properties ($|x| \le k$)

For a real constant $k > 0$:

$$|x| \le k \iff -k \le x \le k$$

* **From left to right ($\implies$):**  
  If $|x| \le k$, then:
  * If $x \ge 0$, we have $|x| = x \le k$. Since $k > 0$, $-k < 0 \le x$ also holds, so $-k \le x \le k$.
  * If $x < 0$, we have $|x| = -x \le k$. Multiplying by $-1$ flips the inequality: $x \ge -k$. Since $x < 0 < k$, combining both yields $-k \le x \le k$.

* **From right to left ($\impliedby$):**  
  If $-k \le x \le k$, we have two simultaneous conditions: $x \le k$ and $x \ge -k \implies -x \le k$.  
  By definition of $|x|$, since $|x|$ equals either $x$ or $-x$, and both are $\le k$, it follows that $|x| \le k$. $\blacksquare$

---

### Triangle Inequality ($|x + y| \le |x| + |y|$)

Applying the bounding property to $x$ and $y$:

$$-|x| \le x \le |x|$$
$$-|y| \le y \le |y|$$

Adding both inequalities term by term:

$$-(|x| + |y|) \le x + y \le (|x| + |y|)$$

Since $x + y$ is bounded between $-k$ and $+k$ (where $k = |x| + |y|$), by the inequality property proved above, this is equivalent to:

$$|x + y| \le |x| + |y| \quad \blacksquare$$

---

### Equality Condition for Triangle Inequality ($|a + b| = |a| + |b| \iff a \cdot b \ge 0$)

Squaring both sides:

$$|a + b|^2 = (|a| + |b|)^2$$

Using $|x|^2 = x^2$ and expanding the algebraic identity:

$$(a + b)^2 = |a|^2 + 2|a||b| + |b|^2$$
$$a^2 + 2ab + b^2 = a^2 + 2|a \cdot b| + b^2$$

Subtracting $a^2 + b^2$ from both sides:

$$2ab = 2|a \cdot b| \implies ab = |a \cdot b|$$

By definition, $x = |x|$ holds if and only if $x \ge 0$.  
Thus, $ab = |ab|$ holds if and only if:

$$a \cdot b \ge 0 \quad \blacksquare$$

---

### Idempotence ($||x|| = |x|$)

Let $y = |x|$.  
By non-negativity, $y \ge 0$.  
Applying the definition for a non-negative argument:

$$|y| = y \implies ||x|| = |x| \quad \blacksquare$$

---

### Even Power ($|x^2| = x^2 = |x|^2$)

1. **Proving $|x^2| = x^2$:**  
   Since $x^2 \ge 0$ for all $x \in \mathbb{R}$, by definition of non-negative arguments, $|x^2| = x^2$.

2. **Proving $|x|^2 = x^2$:**  
   * If $x \ge 0$: $|x| = x \implies |x|^2 = x^2$.
   * If $x < 0$: $|x| = -x \implies |x|^2 = (-x)^2 = x^2$.

Conclusion: $|x^2| = x^2 = |x|^2$. $\blacksquare$