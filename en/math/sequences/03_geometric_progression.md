
# Geometric Progression

## Intuition and Definition

In Arithmetic Progression, we explored systems that evolve through addition — steps of strictly constant size. However, many natural, financial, and physical phenomena do not grow by adding a fixed amount, but rather by **multiplying** by a scaling factor at each stage.

When you observe a biological population doubling every hour, compound interest accumulating on an investment, or a bouncing ball reaching a fraction of its previous height with each rebound, you are looking at a **Geometric Progression (GP)**.

A Geometric Progression is any numerical sequence in which the ratio between two consecutive terms is constant across the entire domain of the sequence. We call this constant multiplier the **common ratio** ($q$, from *quotient*).

Formally, we say that a sequence $(a_n)$ of non-zero terms is a Geometric Progression if, and only if, there exists a real number $q$ such that:

$$\frac{a_n}{a_{n-1}} = q \quad \text{for all } n \ge 2$$

Or equivalently:

$$a_n = a_{n-1} \cdot q \quad \text{for all } n \ge 2$$

> [!NOTE]
> **Important Restrictions:**
> * **$a_1 \neq 0$:** The initial term can never be zero. Otherwise, all subsequent terms would be zero ($0, 0, 0 \dots$), making it impossible to calculate the ratio ($\frac{0}{0}$).
> * **$q \neq 0$:** The common ratio can never be zero, as it would generate a sequence that loses reversibility and destroys exponential behavior.

---

## Examples and Classification

Unlike Arithmetic Progressions, where the sign of the common difference alone determines whether the sequence increases or decreases, the behavior of a Geometric Progression depends on **both the common ratio ($q$) and the sign of the initial term ($a_1$)**.

### Increasing GP

Each term is strictly greater than the previous one ($a_n > a_{n-1}$). This occurs in two scenarios:
* Positive terms ($a_1 > 0$) with a common ratio greater than 1 ($q > 1$):  
  $2, 4, 8, 16, 32 \dots$ ($a_1 = 2, q = 2$)
* Negative terms ($a_1 < 0$) with a common ratio between 0 and 1 ($0 < q < 1$):  
  $-100, -50, -25, -12.5 \dots$ ($a_1 = -100, q = 0.5$)

### Decreasing GP

Each term is strictly smaller than the previous one ($a_n < a_{n-1}$). This occurs in two scenarios:
* Positive terms ($a_1 > 0$) with a common ratio between 0 and 1 ($0 < q < 1$):  
  $81, 27, 9, 3, 1 \dots$ ($a_1 = 81, q = \frac{1}{3}$)
* Negative terms ($a_1 < 0$) with a common ratio greater than 1 ($q > 1$):  
  $-2, -4, -8, -16 \dots$ ($a_1 = -2, q = 2$)

### Constant GP

All terms remain identical throughout the sequence ($a_n = a_{n-1}$). This occurs when the common ratio equals 1 ($q = 1$):  
* $7, 7, 7, 7 \dots$ ($a_1 = 7, q = 1$)

### Alternating (Oscillating) GP

The sign of the terms alternates between positive and negative at each step. This behavior is unique to Geometric Progressions and occurs **whenever the common ratio is negative ($q < 0$)**:
* $3, -6, 12, -24, 48 \dots$ ($a_1 = 3, q = -2$)

---

## The General Term of a GP

Just like in an AP, calculating a distant element of this sequence by multiplying repeatedly is inefficient. To find any term in constant time, we build the general term equation by observing the multiplicative steps from the starting point ($a_1$).

### The Intuitive Construction

* To reach the 2nd term: $a_2 = a_1 \cdot q$
* To reach the 3rd term: $a_3 = a_2 \cdot q = (a_1 \cdot q) \cdot q = a_1 \cdot q^2$
* To reach the 4th term: $a_4 = a_3 \cdot q = (a_1 \cdot q^2) \cdot q = a_1 \cdot q^3$

Notice the pattern? Instead of multiplying the common ratio by $(n-1)$ as we did in addition, we raise the common ratio to the power of $(n-1)$.

Therefore, to reach position $n$, you must scale the initial element $a_1$ by the factor $q$ exactly $(n - 1)$ times.

> [!TIP]
> **Key Insight:** Compare the two fundamental mechanics:
> * **AP (Linear):** $a_n = a_1 + (n - 1)r \implies$ Repeated addition becomes **multiplication**.
> * **GP (Exponential):** $a_n = a_1 \cdot q^{n-1} \implies$ Repeated multiplication becomes **exponentiation**.

### The Equation

$$a_n = a_1 \cdot q^{n-1}$$

Where:
* $a_n$: value of the term at position $n$.
* $a_1$: first term of the sequence ($a_1 \neq 0$).
* $n$: position index ($n \in \mathbb{N}^*$).
* $q$: common ratio ($q \neq 0$).

---

## The Fundamental Property: Link to the Geometric Mean

In any finite Geometric Progression with positive terms, **any intermediate term is the geometric mean of its immediate predecessor and successor**.

Taking three consecutive terms $(a_{k-1}, a_k, a_{k+1})$, we know by definition that:

$$\frac{a_k}{a_{k-1}} = q \quad \text{and} \quad \frac{a_{k+1}}{a_k} = q$$

Equating both expressions for $q$:

$$\frac{a_k}{a_{k-1}} = \frac{a_{k+1}}{a_k}$$

Cross-multiplying:

$$a_k^2 = a_{k-1} \cdot a_{k+1} \implies a_k = \sqrt{a_{k-1} \cdot a_{k+1}}$$

Just as in an AP, this property extends to any pair of terms equidistant from the central element $a_k$.

---

## Sum of the First $n$ Terms (Finite GP)

To calculate the accumulated sum $S_n = a_1 + a_2 + \dots + a_n$ without adding each term individually, we use an algebraic elimination trick.

Write out the expanded sum:

$$S_n = a_1 + a_1 q + a_1 q^2 + \dots + a_1 q^{n-1}$$

Now, multiply the entire equation by the common ratio $q$:

$$q \cdot S_n = a_1 q + a_1 q^2 + a_1 q^3 + \dots + a_1 q^n$$

Subtract the first equation from the second ($q \cdot S_n - S_n$). Notice how all intermediate terms cancel out:

$$q \cdot S_n - S_n = a_1 q^n - a_1$$

Factoring out $S_n$ on the left and $a_1$ on the right:

$$S_n(q - 1) = a_1(q^n - 1)$$

Isolating $S_n$ (for $q \neq 1$):

$$S_n = \frac{a_1(q^n - 1)}{q - 1} \quad \text{or} \quad S_n = \frac{a_1(1 - q^n)}{1 - q}$$

> [!NOTE]
> Notice that we arrived at two versions of the same equation. They are equivalent — you can test this on a small GP to confirm. This happens because, depending on which equation you chose to subtract from the other, you arrive at one of these two forms.

---

## Sum of an Infinite GP (Geometric Series)

Is it possible to add infinitely many numbers and arrive at a finite result?

To understand this behavior, the common ratio must lie strictly within the interval between $-1$ and $1$, excluding zero: **$|q| < 1$ and $q \neq 0$** (that is, $q \in ]-1, 1[ \setminus \{0\}$).

Under these conditions, the behavior of the sum depends on where the ratio lies:

### Positive Ratio ($0 < q < 1$): Continuous Shrinking

Consider a bounce sequence where a ball drops from 1 meter, bounces to $\frac{1}{2}$ meter, then $\frac{1}{4}$, then $\frac{1}{8}$, and so on. All terms are positive, but they continuously shrink:

$$S_\infty = 1 + \frac{1}{2} + \frac{1}{4} + \frac{1}{8} + \dots$$

### Negative Ratio ($-1 < q < 0$): Convergent Oscillation

Now consider an alternating GP with $a_1 = 1$ and $q = -0.5$:

$$1, \, -0.5, \, 0.25, \, -0.125, \, 0.0625 \dots$$

At first glance, adding terms that alternate between positive and negative might seem strange. However, if we observe the partial sums step by step:

* $S_1 = 1$
* $S_2 = 1 - 0.5 = \mathbf{0.5}$
* $S_3 = 0.5 + 0.25 = \mathbf{0.75}$
* $S_4 = 0.75 - 0.125 = \mathbf{0.625}$
* $S_5 = 0.625 + 0.0625 = \mathbf{0.6875}$

The cumulative sum bounces back and forth ($1 \to 0.5 \to 0.75 \to 0.625 \to 0.6875$), but with each step the "leap" gets smaller, and the sum is squeezed around a central value.

### Derivation and Formula

In both scenarios (positive or negative ratio), as the number of terms grows toward infinity ($n \to \infty$), the term $q^n$ shrinks toward zero ($q^n \to 0$).

Applying this limit to our finite sum formula gives us the **infinite sum formula** for convergent series ($|q| < 1$ and $q \neq 0$):

$$S_\infty = \lim_{n \to \infty} \frac{a_1(1 - q^n)}{1 - q} = \frac{a_1(1 - 0)}{1 - q} \implies S_\infty = \frac{a_1}{1 - q}$$

Applying it to our two examples:

* **For the bounce example ($a_1 = 1, q = 0.5$):**
  $$S_\infty = \frac{1}{1 - 0.5} = \frac{1}{0.5} = 2$$
  Infinitely many bounces add up to a finite total distance of exactly **2 meters**.

* **For the alternating example ($a_1 = 1, q = -0.5$):**
  $$S_\infty = \frac{1}{1 - (-0.5)} = \frac{1}{1.5} = \frac{2}{3} \approx 0.6666\dots$$
  The oscillation squeezes precisely around **$\frac{2}{3}$**.

---

> [!TIP]
> **Bridge to Advanced Calculus:**
> The sum of an infinite GP is the discrete equivalent of an **Improper Integral** ($\int_a^\infty f(x) \, dx$). 
> 
> While the integral calculates the continuous area under a curve extending to infinity, the infinite GP adds individual discrete steps of shrinking size. Both prove the same fascinating fact: **it is possible to add infinitely many pieces and arrive at a perfectly finite, bounded result** (convergence).