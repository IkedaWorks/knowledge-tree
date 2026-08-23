---
id: one_sided_limits
title: One Sided Limits
---

# The Geometry of Unilateral Approximation

When examining the behavior of a real function $f(x)$ near a point $a$, the primary intuition of Calculus suggests observing the trend of the values of $f(x)$ as $x$ approaches $a$. However, the real line possesses a fundamental topological property: it is one-dimensional and orientable. This means that there are only two possible paths to approach a point $a$ along the real axis: walking from values strictly greater than $a$ (approaching from the right) or walking from values strictly less than $a$ (approaching from the left).

For a broad class of elementary functions—such as polynomials, exponential functions, and trigonometric functions within their domains of definition—the direction of approach does not alter the local behavior of the function. The curve is smooth and continuous, and the limit as $x$ approaches $a$ is identical regardless of the direction chosen. However, nature and the real world are filled with phenomena that exhibit abrupt changes. Consider the electrostatic force across the surface of a charged sphere, the density of a material at the interface between liquid and vapor during a phase transition, or the voltage change in a circuit when a switch is flipped.

In these scenarios, the function describing the system undergoes a rupture. If we attempt to analyze the global behavior around the transition point without discriminating the direction, the mathematical description collapses. It is here that the concept of a one-sided limit establishes itself not as a mere formal device, but as the natural tool for understanding the anatomy of discontinuities.

By investigating approximation from a single side, one realizes that for the same input $a$, the function can exhibit completely asymmetrical trends. If we take values $x > a$ and shrink them continuously toward $a$, the image $f(x)$ may stabilize at a value $L_1$. If we repeat the process taking values $x < a$, the image $f(x)$ may tend toward an entirely distinct value $L_2$. The study of one-sided limits is precisely the isolated investigation of these two directional trends.

# Conceptual Construction and Formal Definitions

To build an accurate intuitive picture of what occurs in a one-sided limit, consider the graph of a function $y = f(x)$ drawn in the Cartesian plane. Imagine tracking the trace of this curve with the tip of a pencil, moving along the graph from right to left toward the vertical line $x = a$. As your horizontal coordinate approaches $a$ (remaining strictly within the domain $x > a$), the tip of your pencil approaches a certain height on the vertical $y$-axis. This height of convergence is the right-hand limit.

If you repeat the experiment, but this time slide the tip of the pencil along the graph from left to right, approaching the same vertical line $x = a$ from values where $x < a$, the tip of the pencil may converge to a completely different height. This second height is the left-hand limit. When these two heights do not coincide at point $a$, the graph exhibits a break—a jump discontinuity—demonstrating that the behavior of the function depends critically on the direction of approach.

## Right-Hand Limit

We say that the limit of $f(x)$ as $x$ approaches $a$ from the right is equal to $L_1$, denoted by:

$$\lim_{x \to a^+} f(x) = L_1$$

If, for every $\epsilon > 0$, there exists a corresponding $\delta > 0$ such that $\vert{}f(x) - L_1\vert{} < \epsilon$ whenever $a < x < a + \delta$.

The notation $a^+$ specifies that the variable $x$ is restricted to the open interval $(a, a + \delta)$, ensuring that $x$ is strictly greater than $a$.

## Left-Hand Limit

We say that the limit of $f(x)$ as $x$ approaches $a$ from the left is equal to $L_2$, denoted by:

$$\lim_{x \to a^-} f(x) = L_2$$

If, for every $\epsilon > 0$, there exists a corresponding $\delta > 0$ such that $\vert{}f(x) - L_2\vert{} < \epsilon$ whenever $a - \delta < x < a$.

The notation $a^-$ restricts the variable $x$ to the open interval $(a - \delta, a)$, requiring that the approximation occurs exclusively through values strictly less than $a$.

> **Note on Notation:** It is fundamental to note that the superscripts $+$ and $-$ do not affect the algebraic sign of the number $a$. The expression $x \to -5^+$ means that $x$ approaches the negative number $-5$ from values to its right on the real line (such as $-4.99$), while $x \to 5^-$ indicates an approach toward the positive number $5$ from values to its left (such as $4.99$).

# The Fundamental Existence Theorem for Limits

The fundamental connection between one-sided limits and the ordinary (two-sided) limit is established by the following theorem:

$$\lim_{x \to a} f(x) = L \iff \lim_{x \to a^-} f(x) = L \quad \text{and} \quad \lim_{x \to a^+} f(x) = L$$

This result states that the two-sided limit of $f(x)$ as $x \to a$ exists and is equal to $L$ if, and only if, both one-sided limits exist and are both equal to $L$.

An immediate logical consequence of this theorem is that the two-sided limit $\lim_{x \to a} f(x)$ fails to exist if either of two conditions holds: either the one-sided limits exist but converge to different numerical values ($\lim_{x \to a^-} f(x) \neq \lim_{x \to a^+} f(x)$), or at least one of the one-sided limits does not exist due to infinite or oscillatory behavior.

# Practical Example: Analyzing One-Sided Limits in Practice

To illustrate this behavior numerically, consider the function $f(x)$ defined by:

$$f(x) = \frac{\vert{}x - 2\vert{}}{x - 2} + 3$$

Let us analyze the behavior of this function as we approach the point $a = 2$ from both sides.

### 1. Right-Hand Approach ($x \to 2^+$)

We select values of $x$ strictly greater than $2$ ($x > 2$). Since $(x - 2)$ results in a positive value, the absolute value does not alter the result ($\vert{}x - 2\vert{} = x - 2$):

- For $x = 2.1$:
    
    $$f(2.1) = \frac{\vert{}2.1 - 2\vert{}}{2.1 - 2} + 3 = \frac{0.1}{0.1} + 3 = 1 + 3 = 4$$
    
- For $x = 2.01$:
    
    $$f(2.01) = \frac{\vert{}2.01 - 2\vert{}}{2.01 - 2} + 3 = \frac{0.01}{0.01} + 3 = 1 + 3 = 4$$
    
- For $x = 2.001$:
    
    $$f(2.001) = \frac{\vert{}2.001 - 2\vert{}}{2.001 - 2} + 3 = \frac{0.001}{0.001} + 3 = 1 + 3 = 4$$
    

Approaching $2$ from the right, the $y$-values converge to a height of $4$:

$$\lim_{x \to 2^+} f(x) = 4$$

### 2. Left-Hand Approach ($x \to 2^-$)

Now, we select values of $x$ strictly less than $2$ ($x < 2$). Since $(x - 2)$ is a negative number, the absolute value inverts its sign ($\vert{}x - 2\vert{} = -(x - 2)$):

- For $x = 1.9$:
    
    $$f(1.9) = \frac{\vert{}1.9 - 2\vert{}}{1.9 - 2} + 3 = \frac{\vert{}-0.1\vert{}}{-0.1} + 3 = \frac{0.1}{-0.1} + 3 = -1 + 3 = 2$$
    
- For $x = 1.99$:
    
    $$f(1.99) = \frac{\vert{}1.99 - 2\vert{}}{1.99 - 2} + 3 = \frac{\vert{}-0.01\vert{}}{-0.01} + 3 = \frac{0.01}{-0.01} + 3 = -1 + 3 = 2$$
    
- For $x = 1.999$:
    
    $$f(1.999) = \frac{\vert{}1.999 - 2\vert{}}{1.999 - 2} + 3 = \frac{\vert{}-0.001\vert{}}{-0.001} + 3 = \frac{0.001}{-0.001} + 3 = -1 + 3 = 2$$
    

Approaching $2$ from the left, the $y$-values converge to a height of $2$:

$$\lim_{x \to 2^-} f(x) = 2$$

### Conclusion of the Example

Because the right-hand limit ($L_1 = 4$) and the left-hand limit ($L_2 = 2$) yield completely different values ($4 \neq 2$), the graph exhibits a jump at point $x = 2$, proving numerically that the overall limit $\lim_{x \to 2} f(x)$ does not exist.

# Operational Mechanics of One-Sided Notation

When performing algebraic manipulations to evaluate one-sided limits, the fundamental rules of algebra—such as factoring, canceling common factors, rationalizing, and simplifying rational expressions—remain strictly identical to those used in two-sided limits. The symbol $+$ or $-$ in the limit does not alter the structure of equivalent algebraic transformations.

The operational utility of one-sided notation becomes evident when determining the behavior of expressions whose sign or definition explicitly depends on the direction of approach. Three main scenarios demand special attention:

1. **Infinite Limits and Sign Analysis:** In the study of infinite limits where direct substitution produces a form of the class $k/0$ (with $k \neq 0$), one-sided notation defines the sign of the infinitesimal in the denominator. If $x \to a^+$, we analyze whether the denominator approaches zero through positive values ($0^+$) or negative values ($0^-$). A positive numerator divided by $0^+$ results in $+\infty$, whereas division by $0^-$ yields $-\infty$.
    
2. **Absolute Values:** In expressions containing absolute values, the definition $\vert{}u\vert{} = u$ for $u \ge 0$ and $\vert{}u\vert{} = -u$ for $u < 0$ requires knowing which side of $a$ the variable lies on. If we have the expression $\vert{}x - a\vert{}$ and the limit specifies $x \to a^+$, then $x - a > 0$, allowing us to directly replace $\vert{}x - a\vert{}$ with $(x - a)$. Conversely, if the limit specifies $x \to a^-$, then $x - a < 0$, and we must replace $\vert{}x - a\vert{}$ with $-(x - a)$.
    
3. **Even Radicals:** In handling even-indexed radicals, the fundamental algebraic identity $\sqrt{x^2} = \vert{}x\vert{}$ reveals the necessity of one-sided limits. Simplifying $\sqrt{x^2}/x$ as $x \to 0^-$ requires the left-hand approach, setting $\vert{}x\vert{} = -x$, leading to the ratio $-x/x = -1$. If the approach were from the right ($x \to 0^+$), we would have $\vert{}x\vert{} = x$, resulting in $x/x = 1$.
    

# Solved Examples: One-Sided Limits

## Pattern 1: Limit Analysis in Piecewise Functions

### Example 1

Consider the function $f(x)$ defined by:

$$f(x) = \begin{cases} x^2, & \text{if } x < 2 \\ x + 1, & \text{if } x = 2 \\ -x^2 + 2x + 4, & \text{if } x > 2 \end{cases}$$

Evaluate the following items:

1. $\lim_{x \to 2^-} f(x)$
    
2. $\lim_{x \to 2^+} f(x)$
    
3. $\lim_{x \to 2} f(x)$
    
4. $f(2)$
    

#### Solution:

1. **Calculating the left-hand limit ($\lim_{x \to 2^-} f(x)$):**
    
    For $x \to 2^-$, only values such that $x < 2$ are considered. The corresponding expression is $f(x) = x^2$.
    
    $$\lim_{x \to 2^-} f(x) = \lim_{x \to 2^-} x^2 = (2)^2 = 4$$
    
2. **Calculating the right-hand limit ($\lim_{x \to 2^+} f(x)$):**
    
    For $x \to 2^+$, only values such that $x > 2$ are considered. The corresponding expression is $f(x) = -x^2 + 2x + 4$.
    
    $$\lim_{x \to 2^+} f(x) = \lim_{x \to 2^+} (-x^2 + 2x + 4) = -(2)^2 + 2(2) + 4 = -4 + 4 + 4 = 4$$
    
3. **Analyzing the existence of the two-sided limit ($\lim_{x \to 2} f(x)$):**
    
    Since the left-hand and right-hand limits are equal ($\lim_{x \to 2^-} f(x) = 4$ and $\lim_{x \to 2^+} f(x) = 4$), it follows that the two-sided limit exists and equals $4$:
    
    $$\lim_{x \to 2} f(x) = 4$$
    
4. **Determining the value of the function at the point ($f(2)$):**
    
    By the definition of the function, for $x = 2$, the rule $x + 1$ is used:
    
    $$f(2) = 2 + 1 = 3$$
    

_(Note: Observe that $\lim_{x \to 2} f(x) = 4 \neq f(2) = 3$, which exemplifies that the limit's value is independent of the value the function assumes at $x = 2$.)_

## Pattern 2: Denominator Sign Analysis ($0^+$ vs $0^-$)

### Example 2

Determine the one-sided limit $\lim_{x \to 3^+} \frac{5}{3 - x}$.

#### Solution:

Applying direct substitution shows that the numerator approaches $5$ and the denominator approaches $0$. To determine the limit's behavior, analyze the sign of the denominator as $x$ approaches $3$ from the right ($x > 3$).

Since $x \to 3^+$, assume $x > 3$ (e.g., $x = 3.1$). Thus:

$$3 - x < 0 \implies (3 - x) \to 0^-$$

Substituting this sign analysis into the limit:

$$\lim_{x \to 3^+} \frac{5}{3 - x} = \frac{5}{0^-} = -\infty$$

### Example 3

Determine the one-sided limit $\lim_{x \to 3^-} \frac{5}{3 - x}$.

#### Solution:

For $x \to 3^-$, consider values to the left of $3$, that is, $x < 3$ (e.g., $x = 2.9$). Thus:

$$3 - x > 0 \implies (3 - x) \to 0^+$$

Substituting this sign analysis into the limit:

$$\lim_{x \to 3^-} \frac{5}{3 - x} = \frac{5}{0^+} = +\infty$$

### Example 4

Determine the one-sided limit $\lim_{x \to 0^+} \frac{5}{x^2 - x}$.

#### Solution:

Factor the denominator to isolate the term associated with the indeterminate form:

$$x^2 - x = x(x - 1)$$

Rewriting the limit:

$$\lim_{x \to 0^+} \frac{5}{x(x - 1)}$$

Analyze the terms as $x \to 0^+$ ($x > 0$, very close to $0$, such as $x = 0.1$):

- The numerator remains $5$.
    
- The factor $x$ approaches $0^+$.
    
- The factor $(x - 1)$ approaches $(0 - 1) = -1$ (a negative value).
    

Combining the signs in the denominator gives:

$$x(x - 1) \to (0^+) \cdot (-1) = 0^-$$

Therefore:

$$\lim_{x \to 0^+} \frac{5}{x(x - 1)} = \frac{5}{0^-} = -\infty$$

### Example 5

Determine the one-sided limit $\lim_{x \to -1^+} \frac{3x^2 - 4}{1 - x^2}$.

#### Solution:

Evaluating the numerator as $x \to -1$:

$$3(-1)^2 - 4 = 3(1) - 4 = -1$$

Factoring the denominator as a difference of squares:

$$1 - x^2 = (1 - x)(1 + x)$$

When $x \to -1^+$ ($x > -1$, e.g., $x = -0.9$):

- The factor $(1 - x)$ approaches $1 - (-1) = 2 > 0$.
    
- The factor $(1 + x)$ approaches $1 + (-0.9) = 0.1 > 0 \implies (1 + x) \to 0^+$.
    

Thus, the denominator approaches:

$$(1 - x)(1 + x) \to (2) \cdot (0^+) = 0^+$$

Substituting these results back into the limit:

$$\lim_{x \to -1^+} \frac{3x^2 - 4}{1 - x^2} = \frac{-1}{0^+} = -\infty$$

## Pattern 3: Graphical Interpretation of One-Sided Limits

### Example 6

Consider a function $f(x)$ whose graph exhibits the following characteristics near $x = -2$:

- A curve coming from the left quadrant ending in an open dot at the coordinate $(-2, 2)$.
    
- A curve starting from the same height $y = 2$ at the open dot $(-2, 2)$ proceeding toward the origin $(0,0)$.
    
- A solid dot located on the x-axis at coordinate $(-2, 0)$.
    

Determine:

1. $\lim_{x \to -2^-} f(x)$
    
2. $\lim_{x \to -2^+} f(x)$
    
3. $\lim_{x \to -2} f(x)$
    
4. $f(-2)$
    

#### Solution:

1. **$\lim_{x \to -2^-} f(x)$:**
    
    Following the graph to the left of $x = -2$ ($x < -2$), the curve approaches height $y = 2$.
    
    $$\lim_{x \to -2^-} f(x) = 2$$
    
2. **$\lim_{x \to -2^+} f(x)$:**
    
    Following the graph to the right of $x = -2$ ($x > -2$), the curve also approaches height $y = 2$.
    
    $$\lim_{x \to -2^+} f(x) = 2$$
    
3. **$\lim_{x \to -2} f(x)$:**
    
    Since both one-sided limits converge to the same height ($\lim_{x \to -2^-} f(x) = \lim_{x \to -2^+} f(x) = 2$), the two-sided limit exists:
    
    $$\lim_{x \to -2} f(x) = 2$$
    
4. **$f(-2)$:**
    
    The function value is given by the position of the solid dot at $x = -2$, located at height $y = 0$.
    
    $$f(-2) = 0$$