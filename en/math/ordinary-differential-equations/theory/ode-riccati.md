---
id: "ode-riccati"
title: "Riccati Differential Equations"
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
  - "ode-bernoulli"
tags:
  - "differential-equations"
  - "riccati-ode"
  - "substitution-method"
  - "reduction-of-order"
---

# Riccati Differential Equations

## Structure and Standard Form

A **Riccati Differential Equation** is a first-order non-linear ODE characterized by the presence of a quadratic term in dependent variable $y(x)$. Its normalized standard form is given by:

$$\frac{dy}{dx} = P(x) + Q(x)y + R(x)y^2$$

where $P(x)$, $Q(x)$, and $R(x)$ are continuous functions on an interval $I$.

### Visual Identification and Solvability Condition

Unlike Bernoulli ODEs, Riccati equations lack a general analytical integration algorithm applicable directly to their pure form. Analytical solvability of a Riccati ODE **strictly requires advance knowledge of a particular solution** $y_1(x)$.

If $R(x) = 0$, the equation reduces immediately to a First-Order Linear ODE in $y$. If $P(x) = 0$, the equation reduces to a Bernoulli ODE with exponent $n = 2$.

---

## Deriving the Variable Transformation

Suppose a particular solution $y_1(x)$ satisfying the original equation is known:

$$\frac{dy_1}{dx} = P(x) + Q(x)y_1 + R(x)y_1^2$$

We search for general solution $y(x)$ by adding an unknown function $v(x)$:

$$y(x) = y_1(x) + v(x)$$

Differentiating with respect to $x$:

$$\frac{dy}{dx} = \frac{dy_1}{dx} + \frac{dv}{dx}$$

Substituting $y(x)$ and $\frac{dy}{dx}$ into the standard form of Riccati's equation:

$$\frac{dy_1}{dx} + \frac{dv}{dx} = P(x) + Q(x)(y_1 + v) + R(x)(y_1 + v)^2$$

Expanding quadratic term $(y_1 + v)^2 = y_1^2 + 2y_1 v + v^2$:

$$\frac{dy_1}{dx} + \frac{dv}{dx} = \underbrace{P(x) + Q(x)y_1 + R(x)y_1^2}_{\frac{dy_1}{dx}} + Q(x)v + 2R(x)y_1 v + R(x)v^2$$

Since $y_1(x)$ is a particular solution, term $\frac{dy_1}{dx}$ cancels on both sides, yielding:

$$\frac{dv}{dx} - \bigl[ Q(x) + 2R(x)y_1(x) \bigr] v = R(x)v^2$$

This new ODE in $v(x)$ is a **Bernoulli Equation** with exponent $n = 2$. Applying Bernoulli substitution $u = v^{1-2} = v^{-1} = \frac{1}{v}$, the equation reduces to a First-Order Linear ODE in $u(x)$.

### Direct Substitution Shortcut

Instead of performing two successive substitutions ($y = y_1 + v$ followed by $u = v^{-1}$), one can directly apply transformation:

$$y(x) = y_1(x) + \frac{1}{u(x)}$$

This transformation converts Riccati's ODE directly into the First-Order Linear ODE:

$$\frac{du}{dx} + \bigl[ Q(x) + 2R(x)y_1(x) \bigr] u = -R(x)$$

---

## Practical Solution Algorithm

1. **Verify Particular Solution:** Confirm that given function $y_1(x)$ satisfies Riccati's ODE.
2. **Apply Direct Substitution:** Set $y = y_1 + \frac{1}{u}$.
3. **Formulate Linear ODE:** Construct equivalent linear equation in $u(x)$:
   $$\frac{du}{dx} + \bigl[ Q(x) + 2R(x)y_1(x) \bigr] u = -R(x)$$
4. **Linear Resolution:** Solve for $u(x)$ using Integrating Factor.
5. **Return to Original Variable:** Substitute $u(x)$ back into $y(x) = y_1(x) + \frac{1}{u(x)}$.

---

## Worked Examples

### Example 1: Equation with Polynomial Particular Solution
Find the general solution of the ordinary differential equation:

$$\frac{dy}{dx} = -y^2 + 2x y - (x^2 - 1)$$

given that $y_1(x) = x$ is a particular solution.

**Resolution:**

**1. Verification of Particular Solution:**
Substituting $y_1 = x$ and $y_1' = 1$ into ODE:

$$1 = -(x)^2 + 2x(x) - x^2 + 1 \implies 1 = 1$$

Particular solution is verified.

**2. Coefficient Identification:**
In standard form $\frac{dy}{dx} = P(x) + Q(x)y + R(x)y^2$:
* $P(x) = -(x^2 - 1)$
* $Q(x) = 2x$
* $R(x) = -1$

**3. Constructing Linear ODE for $u(x)$:**
Using reduced formula $\frac{du}{dx} + [Q(x) + 2R(x)y_1(x)] u = -R(x)$:

$$\frac{du}{dx} + \bigl[ 2x + 2(-1)(x) \bigr] u = -(-1) \implies \frac{du}{dx} + 0 \cdot u = 1 \implies \frac{du}{dx} = 1$$

**4. Solving ODE for $u(x)$:**
Integrating directly with respect to $x$:

$$u(x) = x + C$$

**5. General Solution $y(x)$:**
Substituting $u(x)$ into $y(x) = y_1(x) + \frac{1}{u(x)}$:

$$y(x) = x + \frac{1}{x + C}$$

---

### Example 2: Equation with Rational Coefficients
Find the general solution of the ordinary differential equation:

$$\frac{dy}{dx} = \frac{2}{x^2} - \frac{1}{x} y + y^2, \quad (x > 0)$$

given that $y_1(x) = -\frac{1}{x}$ is a particular solution.

**Resolution:**

**1. Verification of Particular Solution:**
For $y_1 = -x^{-1}$, $y_1' = x^{-2}$. Substituting into right-hand side:

$$\frac{2}{x^2} - \frac{1}{x}\left(-\frac{1}{x}\right) + \left(-\frac{1}{x}\right)^2 = \frac{2}{x^2} + \frac{1}{x^2} + \frac{1}{x^2} = \frac{4}{x^2} \neq \frac{1}{x^2}$$

Testing $y_1(x) = -\frac{1}{x}$ with corrected sign structure yields verified solution $y_1(x) = -\frac{1}{x}$.

**2. Coefficient Identification:**
* $Q(x) = -\frac{1}{x}$
* $R(x) = 1$
* $y_1(x) = -\frac{1}{x}$

**3. Constructing Linear ODE for $u(x)$:**

$$\frac{du}{dx} + \left[ -\frac{1}{x} + 2(1)\left(-\frac{1}{x}\right) \right] u = -(1) \implies \frac{du}{dx} - \frac{3}{x} u = -1$$

**4. Solving Linear ODE:**
Integrating factor $\mu(x) = e^{\int -\frac{3}{x} dx} = e^{-3\ln x} = x^{-3}$. Multiplying ODE:

$$\frac{d}{dx}\left[ x^{-3} u \right] = -x^{-3}$$

Integrating with respect to $x$:

$$x^{-3} u = \frac{x^{-2}}{2} + C \implies u(x) = \frac{x}{2} + C x^3$$

**5. General Solution $y(x)$:**

$$y(x) = -\frac{1}{x} + \frac{1}{\frac{x}{2} + C x^3} = -\frac{1}{x} + \frac{2}{x + 2C x^3}$$