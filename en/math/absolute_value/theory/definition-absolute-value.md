---
id: definition_absolute_value
title: Definition of Absolute Value
---

## The Big Idea: Absolute Value as Distance

When you walk 5 meters forward, you have covered a distance of 5 meters. If you turn around and walk 5 meters backward, the distance traveled is still 5 meters. Physics and geometry do not recognize "negative distances" — the direction of motion may change, but the extent of the space covered is always a non-negative quantity.

The absolute value (or modulus) arises from this simple necessity: to extract the geometric magnitude of a number, regardless of which direction it points on the number line. It measures the physical distance between a point and the origin ($0$).

![Example of geometric definition](../../../../assets/diagrama-modulo-distancia.svg)

Visually, the concept is immediate:

* Point $4$ is $4$ units away from zero $\implies |4| = 4$
* Point $-4$ is also $4$ units away from zero $\implies |-4| = 4$
* The origin $0$ itself is at distance zero from itself $\implies |0| = 0$

When evaluating more complex expressions, the reasoning remains identical:

* $|7| = 7$, because the magnitude to the origin is $7$.
* $|-12| = 12$, because the absolute displacement is $12$ units.
* $|\pi - 3| = \pi - 3$, because since $\pi \approx 3.14$, the difference is already positive.
* $|3 - \pi| = \pi - 3$, because since $3 - \pi$ yields a negative value, reversing the order of subtraction guarantees the true positive distance.

### Measuring the Space Between Two Points

Since the absolute value measures the distance to the origin, we can expand this exact concept to calculate the space between any two points $a$ and $b$ on the real line:

$$d(a, b) = |a - b|$$

![Distance between two dots](../../../../assets/diagrama-distancia-dois-pontos.svg)

Notice how mathematics mirrors reality: the distance between two cities does not change whether you are going or returning. The order in which you subtract the points does not alter the extent of the path traveled:

* **From $-3$ to $5$:** we walk $3$ units to zero and another $5$ units forward, totaling $8$ units.
  $$|-3 - 5| = |-8| = 8$$

* **From $5$ to $-3$:**
  $$|5 - (-3)| = |5 + 3| = |8| = 8$$

The identity $|a - b| = |b - a|$ is the algebraic proof of this natural symmetry.

---

## Algebraic Definition

To solve equations and write code without relying on drawing number lines every time, we translate this geometric intuition into a piecewise function:

For any real number $x$:

$$|x| = \begin{cases} x, & \text{if } x \ge 0 \\ -x, & \text{if } x < 0 \end{cases}$$

### Untangling a Common Misconception: The Role of $-x$

When looking at the expression $-x$, our brains often associate the minus sign with a negative number. In algebra, however, the minus sign is an inversion operator — it means "the opposite of."

If the input is already positive or zero ($x = 5$), the function keeps the number unchanged: $|5| = 5$.

If the input is negative ($x = -5$), the function applies the inversion operator to neutralize the original sign:

$$|-5| = -(-5) = 5$$

The expression $-x$ does not make the output negative. On the contrary, it is the precise tool that cancels out the input's negative sign, ensuring the output always belongs to the set of non-negative real numbers ($\mathbb{R}_{\ge 0}$).

### Applying the Rule in Practice: Removing the Absolute Value Bars

The goal of the algebraic definition is to provide a rigorous mechanism to remove absolute value bars and operate within standard algebra. To do so, we analyze whether the internal expression is non-negative or negative.

#### Evaluating Constants and Order Relations

When values are explicitly known, deciding whether to keep the expression intact or invert its signs depends directly on which term is greater:

* **In $|\sqrt{2} - 1|$:** Since $\sqrt{2} \approx 1.414 > 1$, the internal term is positive ($\sqrt{2} - 1 > 0$). The rule keeps the expression as is:
  $$|\sqrt{2} - 1| = \sqrt{2} - 1$$

* **In $|1 - \sqrt{2}|$:** Since $1 < \sqrt{2}$, the internal term is negative ($1 - \sqrt{2} < 0$). The rule applies the inversion operator to the entire expression:
  $$|1 - \sqrt{2}| = -(1 - \sqrt{2}) = \sqrt{2} - 1$$

This exact mechanism algebraically guarantees that $|a - b| = |b - a|$ for all real numbers.

#### Algebraic Expressions and Sign Swapping

When dealing with variables in equations or algorithms, removing the absolute value bars requires analyzing the domain of the argument:

For the expression $|x - 3|$:

* **When $x \ge 3$:** The difference $x - 3$ produces a non-negative value. The absolute value bars are simply dropped:
  $$|x - 3| = x - 3$$

* **When $x < 3$:** The difference $x - 3$ yields a negative value. The absolute value bars are removed by applying sign inversion to the whole expression:
  $$|x - 3| = -(x - 3) = 3 - x$$

Solving any modular equation or inequality boils down to this single process: identifying the sign of the argument to replace the absolute value with its equivalent algebraic form.

> [!NOTE]
> Keep in mind that when solving equations involving absolute values, it is necessary to analyze the interval and evaluate the inner argument:
>
>- If $\text{argument} \ge 0$, the expression already represents a position in the non-negative region of the number line.
  >  
>- If $\text{argument} < 0$, it means that the inner value is negative; therefore, we multiply it by $-1$ (since physical distance is strictly non-negative), shifting it to the positive side.
  >  
>The algebraic definition exists precisely to guarantee that, regardless of knowing the explicit inner value beforehand, the final result after the absolute value operation is always a geometric magnitude (distance), which by nature is always non-negative.

---

## Why Does Mathematics Guarantee This Always Works?

The piecewise definition is not an arbitrary trick; it stems directly from the logical structure of real numbers $(\mathbb{R}, +, \cdot, \le)$. 

There is a fundamental property of real numbers known as the **Law of Trichotomy**. It dictates that any real number $x$ must satisfy exactly one of three mutually exclusive conditions:

$$x > 0 \quad \lor \quad x = 0 \quad \lor \quad x < 0$$

Because the real line is perfectly partitioned into these three non-overlapping groups, the absolute value rule never fails or creates ambiguity.

Furthermore, when $x < 0$, algebra proves why $-x$ becomes strictly positive: adding the additive inverse $-x$ to both sides of the inequality $x < 0$ yields:

$$x + (-x) < 0 + (-x) \implies 0 < -x \implies -x > 0$$

This provides a rigorous deductive proof that the opposite of any negative element is strictly positive.