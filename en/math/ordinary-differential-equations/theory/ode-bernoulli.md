---
id: "ode-bernoulli"
title: "Bernoulli Differential Equations"
domain: "math"
module: "ordinary-differential-equations"
type: "method"
schema_version: "2.0"
level: "advanced"
language: "en"
prerequisites:
  - "single-variable-calculus"
  - "ode-fundamental-concepts"
  - "ode-solutions"
  - "ode-linear-integrating-factor"
tags:
  - "differential-equations"
  - "bernoulli-ode"
  - "substitution-method"
  - "linearization"
---

# Bernoulli Differential Equations

## Structure and Standard Form

A **Bernoulli Differential Equation** is a first-order non-linear ODE whose normalized standard form is defined by:

$$\frac{dy}{dx} + P(x)y = Q(x)y^n$$

where $P(x)$ and $Q(x)$ are continuous functions on an interval $I$, and $n \in \mathbb{R}$ is a real constant exponent.

### Visual Identification and Comparison with Linear ODEs

The left-hand side of Bernoulli's ODE ($\frac{dy}{dx} + P(x)y$) is identical to the standard form of a First-Order Linear ODE. The sole difference, and the element breaking linearity, is the $y^n$ factor multiplying independent term $Q(x)$ on the right-hand side.

In practice and exams, this term is frequently disguised through prior algebraic manipulation (e.g., $y' = x y^{-1} - P(x)y$ or $x y' + y = x^2 y^2$). Ensuring full normalization with derivative coefficient equal to 1 is the mandatory first step to correctly identify $P(x)$, $Q(x)$, and $n$.

### Analysis of Limiting Cases

- **If $n = 0$:** The equation reduces to standard linear form $\dfrac{dy}{dx} + P(x)y = Q(x)$, solved directly via Integrating Factors.
- **If $n = 1$:** The equation becomes separable: $\dfrac{dy}{dx} = [Q(x) - P(x)]y$.
- **If $n \neq 0$ and $n \neq 1$:** The power $y^n$ introduces non-linearity. However, the equation can be linearized using substitution $u = y^{1-n}$.

---

## Deriving the Variable Transformation (Linearization)

To eliminate power $y^n$ on the right side, divide the entire equation by $y^n$ (assuming $y \neq 0$):

$$y^{-n}\frac{dy}{dx} + P(x)y^{1-n} = Q(x)$$

Observing dependent term $y^{1-n}$ attached to $P(x)$, define new variable $u(x)$:

$$u = y^{1-n}$$

Differentiating $u$ with respect to $x$ via the Chain Rule:

$$\frac{du}{dx} = (1-n) y^{-n} \frac{dy}{dx} \implies y^{-n} \frac{dy}{dx} = \frac{1}{1-n} \frac{du}{dx}$$

Substituting this relation and $u = y^{1-n}$ into the transformed ODE:

$$\frac{1}{1-n} \frac{du}{dx} + P(x)u = Q(x)$$

Multiplying the entire equation by $(1-n)$ yields the **First-Order Linear ODE for $u(x)$**:

$$\frac{du}{dx} + (1-n)P(x)u = (1-n)Q(x)$$

This resulting equation is solved directly using the integrating factor method. After determining $u(x)$, isolate the original solution $y(x)$:

$$y(x) = \bigl[ u(x) \bigr]^{\frac{1}{1-n}}$$

---

## Practical Solution Algorithm

1. **Prior Normalization:** Rewrite the ODE isolating $\dfrac{dy}{dx}$ with coefficient $1$ to achieve form $\dfrac{dy}{dx} + P(x)y = Q(x)y^n$ and identify exponent $n$.
2. **Variable Transformation:** Set substitution $u = y^{1-n}$.
3. **Formulate Linear ODE:** Construct the equivalent linear ODE directly in terms of $u$:
   $$\frac{du}{dx} + (1-n)P(x)u = (1-n)Q(x)$$
4. **Linear Resolution:** Solve for $u(x)$ using Integrating Factor $\mu(x) = e^{\int (1-n)P(x)dx}$.
5. **Return to Original Variable:** Substitute $u = y^{1-n}$ and isolate $y(x)$.

---

## Worked Examples

### Example 1: Full Bernoulli Resolution
Find the general solution of the differential equation:

$$x\frac{dy}{dx} + y = x^2 y^2$$

**Resolution:**

**1. Normalization:**
Dividing by $x$ (for $x > 0$) to isolate $\dfrac{dy}{dx}$:

$$\frac{dy}{dx} + \frac{1}{x}y = x y^2$$

Identify $P(x) = \dfrac{1}{x}$, $Q(x) = x$, and non-linear exponent $n = 2$.

**2. Substitution:**
Since $n = 2 \implies 1-n = -1$, set $u = y^{-1} = \dfrac{1}{y}$.

**3. Construct Reduced Linear ODE:**

$$\frac{du}{dx} + (-1)\left(\frac{1}{x}\right) u = (-1)(x) \implies \frac{du}{dx} - \frac{1}{x}u = -x$$

**4. Solving Linear ODE for $u(x)$:**
Calculating integrating factor $\mu(x)$:

$$\mu(x) = e^{\int -\frac{1}{x} dx} = e^{-\ln x} = \frac{1}{x}$$

Multiplying ODE by $\mu(x)$:

$$\frac{d}{dx}\left[\frac{1}{x} u\right] = \frac{1}{x}(-x) = -1$$

Integrating both sides:

$$\frac{1}{x} u = \int -1 dx + C = -x + C \implies u(x) = C x - x^2$$

**5. Return to $y(x)$:**
Since $u = \dfrac{1}{y}$, invert the result:

$$y(x) = \frac{1}{Cx - x^2}$$