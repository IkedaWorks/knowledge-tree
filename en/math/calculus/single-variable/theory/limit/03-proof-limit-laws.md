---
id: property-proofs
title: Formal Proofs of Limit Properties
---
# Formal Proofs of Limit Properties

This document constitutes the rigorous module of mathematical proofs for the algebraic properties of limits. All proofs presented here strictly employ the **formal definition of a limit ($\epsilon-\delta$)** and real analysis theorems.

To make the construction of bounds ($\delta$) transparent and pedagogically accessible, the more complex proofs are accompanied by a **Backward Analysis (Preliminary Analysis)**. This step explicitly details the reverse deductive reasoning used to determine tolerances before writing the formal proof.

---

## Formal Hypotheses and Basic Definitions

For all subsequent proofs, we assume the formal definition of a limit:

$$\lim_{x \to a} f(x) = L \iff \forall \epsilon > 0, \exists \delta > 0 \text{ such that } 0 < |x - a| < \delta \implies |f(x) - L| < \epsilon$$

Whenever we state that $\lim_{x \to a} f(x) = L$ and $\lim_{x \to a} g(x) = M$, it is understood that for any $\epsilon_f, \epsilon_g > 0$, there exist corresponding $\delta_f, \delta_g > 0$.

---

## 1. Elementary Limits (Atomic Properties)

### Theorem 1.1: Limit of a Constant Function
If $f(x) = c$ for all $x \in \mathbb{R}$, then $\lim_{x \to a} c = c$.

* **Preliminary Analysis:**  
  We want $|c - c| < \epsilon$. Since $|c - c| = 0$, the inequality $0 < \epsilon$ holds identically for every $\epsilon > 0$. Thus, the choice of $\delta$ is independent and arbitrary.

* **Formal Proof:**  
  Given $\epsilon > 0$, choose $\delta = 1$ (or any $\delta > 0$). If $0 < |x - a| < \delta$, then $|c - c| = 0 < \epsilon$. $\blacksquare$

---

### Theorem 1.2: Limit of the Identity Function
If $f(x) = x$, then $\lim_{x \to a} x = a$.

* **Preliminary Analysis:**  
  We want $|x - a| < \epsilon$. Since the hypothesis condition is $0 < |x - a| < \delta$, the relationship between $\delta$ and $\epsilon$ is direct ($1:1$). It suffices to set $\delta = \epsilon$.

* **Formal Proof:**  
  Given $\epsilon > 0$, set $\delta = \epsilon$. If $0 < |x - a| < \delta$, the implication $0 < |x - a| < \epsilon$ is immediate. $\blacksquare$

---

## 2. Fundamental Arithmetic Properties

### Theorem 2.1: Proof of Sum and Difference
$$\lim_{x \to a} [f(x) \pm g(x)] = L \pm M$$

* **Backward Analysis:**
  1. **Goal:** Ensure that $|(f(x) \pm g(x)) - (L \pm M)| < \epsilon$.
  2. **Rearrangement:** By the Triangle Inequality, $|(f(x) - L) \pm (g(x) - M)| \le |f(x) - L| + |g(x) - M|$.
  3. **Error Partitioning:** For the sum to be strictly less than $\epsilon$, we assign the value $\frac{\epsilon}{2}$ to each error bound.
  4. **Compatibility:** Setting $\delta = \min(\delta_1, \delta_2)$ guarantees simultaneous validity for both functions in the same neighborhood.

* **Formal Proof:**  
  Given $\epsilon > 0$. By hypothesis, there exist $\delta_1, \delta_2 > 0$ such that:
  * $0 < |x - a| < \delta_1 \implies |f(x) - L| < \frac{\epsilon}{2}$
  * $0 < |x - a| < \delta_2 \implies |g(x) - M| < \frac{\epsilon}{2}$

  Let $\delta = \min(\delta_1, \delta_2)$. For $0 < |x - a| < \delta$:

  $$|(f(x) \pm g(x)) - (L \pm M)| \le |f(x) - L| + |g(x) - M| < \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon \quad \blacksquare$$

---

### Theorem 2.2: Proof of Constant Multiple
$$\lim_{x \to a} [k \cdot f(x)] = k \cdot L$$

* **Backward Analysis:**
  1. **Goal:** $|k \cdot f(x) - k \cdot L| < \epsilon \iff |k| \cdot |f(x) - L| < \epsilon$.
  2. **Isolation of Terms:** For $k \neq 0$, it is required that $|f(x) - L| < \frac{\epsilon}{|k|}$.
  3. **Conclusion:** The parameter $\epsilon_f$ of the function $f(x)$ must be adjusted proportionally to the scalar $|k|$.

* **Formal Proof:**  
  * **Case $k = 0$:** $|0 \cdot f(x) - 0 \cdot L| = 0 < \epsilon$, valid for all $\delta > 0$.
  * **Case $k \neq 0$:** Given $\epsilon > 0$, choose $\epsilon_f = \frac{\epsilon}{|k|} > 0$. By the definition of a limit, there exists $\delta > 0$ such that $0 < |x - a| < \delta \implies |f(x) - L| < \frac{\epsilon}{|k|}$.

  Multiplying the inequality by $|k|$:

  $$|k \cdot f(x) - k \cdot L| = |k| \cdot |f(x) - L| < |k| \cdot \frac{\epsilon}{|k|} = \epsilon \quad \blacksquare$$

---

### Theorem 2.3: Proof of General Product
$$\lim_{x \to a} [f(x) \cdot g(x)] = L \cdot M$$

* **Backward Analysis:**
  1. **Goal:** $|f(x)g(x) - LM| < \epsilon$.
  2. **Algebraic Identity:** Adding and subtracting $Lg(x)$, we obtain:
     $$f(x)g(x) - LM = g(x)(f(x) - L) + L(g(x) - M)$$
  3. **Bounding by the Triangle Inequality:**
     $$|f(x)g(x) - LM| \le |g(x)||f(x) - L| + |L||g(x) - M|$$
  4. **Bounding $g(x)$:** To avoid functional dependence in the bound, we restrict $g(x)$ in a bounded neighborhood: choosing $|g(x) - M| < 1$ guarantees $|g(x)| < |M| + 1$.
  5. **Error Distribution:** We require each of the two terms to be less than $\frac{\epsilon}{2}$:
     * $|f(x) - L| < \frac{\epsilon}{2(|M| + 1)}$
     * $|g(x) - M| < \frac{\epsilon}{2(|L| + 1)}$

* **Formal Proof:**  
  Given $\epsilon > 0$:
  1. There exists $\delta_1 > 0$ such that $0 < |x - a| < \delta_1 \implies |g(x) - M| < 1 \implies |g(x)| < |M| + 1$.
  2. There exists $\delta_2 > 0$ such that $0 < |x - a| < \delta_2 \implies |f(x) - L| < \frac{\epsilon}{2(|M| + 1)}$.
  3. There exists $\delta_3 > 0$ such that $0 < |x - a| < \delta_3 \implies |g(x) - M| < \frac{\epsilon}{2(|L| + 1)}$.

  Setting $\delta = \min(\delta_1, \delta_2, \delta_3)$, for $0 < |x - a| < \delta$:

  $$|f(x)g(x) - LM| \le |g(x)||f(x) - L| + |L||g(x) - M|$$
  $$< (|M| + 1) \frac{\epsilon}{2(|M| + 1)} + |L| \frac{\epsilon}{2(|L| + 1)} = \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon \quad \blacksquare$$

---

### Theorem 2.4: Proof of Quotient
$$\lim_{x \to a} \frac{f(x)}{g(x)} = \frac{L}{M} \quad (\text{with } M \neq 0)$$

* **Backward Analysis:**
  The problem reduces to finding the limit of the reciprocal $\lim \frac{1}{g(x)} = \frac{1}{M}$ and applying Theorem 2.3.
  1. **Reciprocal Goal:** $\left|\frac{1}{g(x)} - \frac{1}{M}\right| = \frac{|M - g(x)|}{|M||g(x)|} < \epsilon$.
  2. **Lower Bound for $|g(x)|$:** To prevent the denominator from approaching zero, we impose $|g(x) - M| < \frac{|M|}{2}$. This guarantees $|g(x)| > \frac{|M|}{2} \implies \frac{1}{|g(x)|} < \frac{2}{|M|}$.
  3. **Error Bound:**
     $$\frac{|M - g(x)|}{|M||g(x)|} < \frac{2 |g(x) - M|}{|M|^2}$$
  4. **Isolation of $\epsilon_g$:** To limit the expression by $\epsilon$, we impose $|g(x) - M| < \frac{|M|^2 \epsilon}{2}$.

* **Formal Proof:**  
  Given $\epsilon > 0$:
  1. There exists $\delta_1$ such that $0 < |x - a| < \delta_1 \implies |g(x) - M| < \frac{|M|}{2} \implies \frac{1}{|g(x)|} < \frac{2}{|M|}$.
  2. There exists $\delta_2$ such that $0 < |x - a| < \delta_2 \implies |g(x) - M| < \frac{|M|^2 \epsilon}{2}$.

  For $\delta = \min(\delta_1, \delta_2)$:

  $$\left| \frac{1}{g(x)} - \frac{1}{M} \right| = \frac{|M - g(x)|}{|M||g(x)|} < \frac{2}{|M|^2} \cdot \frac{|M|^2 \epsilon}{2} = \epsilon$$

  By direct application of Theorem 2.3 for the product of $f(x)$ and $\frac{1}{g(x)}$, we conclude that $\lim \frac{f(x)}{g(x)} = \frac{L}{M}$. $\blacksquare$

---

## 3. Direct Substitution in Polynomials

### Theorem 3.1: Integer Power ($x^n$)
$$\lim_{x \to a} x^n = a^n \quad (\forall n \in \mathbb{N})$$

* **Proof (By Mathematical Induction on $n$):**
  * **Base Case ($n=1$):** $\lim_{x \to a} x = a^1 = a$ (Proved in Theorem 1.2).
  * **Inductive Step:** Assume validity for $n = k$, that is, $\lim_{x \to a} x^k = a^k$. For $n = k+1$:
    $$\lim_{x \to a} x^{k+1} = \lim_{x \to a} (x^k \cdot x) = \left(\lim_{x \to a} x^k\right) \cdot \left(\lim_{x \to a} x\right) = a^k \cdot a = a^{k+1}$$
    (by the product property — Theorem 2.3). By mathematical induction, the equality holds for all $n \in \mathbb{N}$. $\blacksquare$

---

### Theorem 3.2: General Polynomial Substitution
If $P(x) = c_n x^n + c_{n-1} x^{n-1} + \dots + c_0$, then $\lim_{x \to a} P(x) = P(a)$.

* **Proof:**  
  By finite chaining of the algebraic properties of sum (Theorem 2.1), constant multiple (Theorem 2.2), and integer power (Theorem 3.1):

  $$\lim_{x \to a} P(x) = \lim_{x \to a} \left( \sum_{i=0}^n c_i x^i \right) = \sum_{i=0}^n c_i \left( \lim_{x \to a} x^i \right) = \sum_{i=0}^n c_i a^i = P(a) \quad \blacksquare$$

---

## 4. General Power and Radication

### Theorem 4.1: Proof of Square Root ($\sqrt{f(x)}$)
$$\lim_{x \to a} \sqrt{f(x)} = \sqrt{L} \quad (\text{for } L > 0 \text{ and } f(x) \ge 0)$$

* **Backward Analysis:**
  1. **Goal:** $|\sqrt{f(x)} - \sqrt{L}| < \epsilon$.
  2. **Rationalizing the Expression:**
     $$|\sqrt{f(x)} - \sqrt{L}| \cdot \frac{\sqrt{f(x)} + \sqrt{L}}{\sqrt{f(x)} + \sqrt{L}} = \frac{|f(x) - L|}{\sqrt{f(x)} + \sqrt{L}}$$
  3. **Conservative Upper Bound:** Since $f(x) \ge 0$, we have $\sqrt{f(x)} \ge 0$. Thus, $\sqrt{f(x)} + \sqrt{L} \ge \sqrt{L}$. Replacing the denominator with a strictly smaller value bounds the fraction from above:
     $$\frac{|f(x) - L|}{\sqrt{f(x)} + \sqrt{L}} \le \frac{|f(x) - L|}{\sqrt{L}}$$
  4. **Condition on $f(x)$:** For $\frac{|f(x) - L|}{\sqrt{L}} < \epsilon$, we require $|f(x) - L| < \epsilon \sqrt{L}$.

* **Formal Proof:**  
  Given $\epsilon > 0$, set the inner function's error bound as $\epsilon_f = \epsilon \sqrt{L} > 0$.  
  Since $\lim_{x \to a} f(x) = L$, there exists $\delta > 0$ such that $0 < |x - a| < \delta \implies |f(x) - L| < \epsilon \sqrt{L}$.

  Applying the upper bound estimate:

  $$|\sqrt{f(x)} - \sqrt{L}| \le \frac{|f(x) - L|}{\sqrt{L}} < \frac{\epsilon \sqrt{L}}{\sqrt{L}} = \epsilon \quad \blacksquare$$

---

## 5. Transcendental and Composite Functions

### Theorem 5.1: Limit of Composite Function
If $\lim_{x \to a} g(x) = L$ and $f$ is **continuous at $L$** ($\lim_{y \to L} f(y) = f(L)$), then:

$$\lim_{x \to a} f(g(x)) = f\left(\lim_{x \to a} g(x)\right) = f(L)$$

* **Backward Analysis:**
  The continuity of $f$ at $L$ guarantees that output variation $|f(y) - f(L)|$ is arbitrarily small as long as input variation $|y - L|$ is controlled. The inner function $g(x)$ acts as the generator for argument $y$, needing its image contained within $f$'s tolerance radius.

* **Formal Proof:**  
  1. By continuity of $f$ at $L$, given $\epsilon > 0$, there exists $\eta > 0$ such that:
     $$|y - L| < \eta \implies |f(y) - f(L)| < \epsilon$$
  2. Since $\lim_{x \to a} g(x) = L$, taking $\eta > 0$ as the error bound for $g(x)$, there exists $\delta > 0$ such that:
     $$0 < |x - a| < \delta \implies |g(x) - L| < \eta$$
  3. Substituting $y = g(x)$, the implications chain together:  
     $$0 < |x - a| < \delta \implies |g(x) - L| < \eta \implies |f(g(x)) - f(L)| < \epsilon \quad \blacksquare$$

---

### Corollary 5.2: Application to Transcendental Functions
If $h(y)$ represents an elementary transcendental function ($\sin(y)$, $\cos(y)$, $\ln(y)$, $e^y$) continuous at point $L$:

$$\lim_{x \to a} h(f(x)) = h\left(\lim_{x \to a} f(x)\right) = h(L)$$

* **Proof:**  
  Direct consequence of Theorem 5.1, considering the continuity of function $h$ within its respective real domain. $\blacksquare$