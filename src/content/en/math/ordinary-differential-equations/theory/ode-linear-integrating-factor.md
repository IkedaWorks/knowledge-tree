---
id: "ode-linear-integrating-factor"
title: "First-Order Linear ODEs and Integrating Factor"
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
tags:
  - "differential-equations"
  - "linear-odes"
  - "integrating-factor"
  - "product-rule"
---

# First-Order Linear ODEs and Integrating Factor

## Standard Form and the Product Rule Challenge

A first-order ordinary differential equation is called **linear** if it can be written in the following standard form:

$$\frac{dy}{dx} + P(x)y = Q(x)$$

where $P(x)$ and $Q(x)$ are continuous functions on an open interval $I$.

Unlike separable equations, the additive term $P(x)y$ prevents direct isolation of variables $x$ and $y$. The solution method relies on multiplying the entire equation by an auxiliary function $\mu(x) > 0$, called the **integrating factor**, designed to transform the left-hand side into the exact derivative of a product.

---

## The Origin of the Integrating Factor (Derivation)

Multiplying the standard form by an unknown function $\mu(x)$:

$$\mu(x)\frac{dy}{dx} + \mu(x)P(x)y = \mu(x)Q(x)$$

By the product rule, the derivative of $\mu(x)y$ with respect to $x$ is:

$$\frac{d}{dx}\bigl[\mu(x)y\bigr] = \mu(x)\frac{dy}{dx} + \mu'(x)y$$

Equating coefficients of term $y$ so that the expression matches the left-hand side of the ODE:

$$\mu'(x) = \mu(x)P(x)$$

This is a separable ODE for $\mu(x)$:

$$\frac{d\mu}{\mu} = P(x)dx \implies \ln|\mu(x)| = \int P(x)dx + C_0$$

Exponentiating both sides:

$$\mu(x) = e^{\int P(x)dx + C_0} = e^{C_0} \cdot e^{\int P(x)dx} = K e^{\int P(x)dx} \quad (K > 0)$$

When substituting $\mu(x)$ into the original ODE and isolating $y(x)$, multiplicative constant $K$ appears in all terms and cancels out completely at the end. Thus, $K = 1$ ($C_0 = 0$) is chosen for convenience, fixing the standard integrating factor form:

$$\mu(x) = e^{\int P(x)dx}$$

With the integrating factor established, the linear ODE directly assumes the integrated form:

$$\frac{d}{dx}\bigl[\mu(x)y\bigr] = \mu(x)Q(x) \implies \mu(x)y = \int \mu(x)Q(x)dx + C$$

Isolating $y(x)$ yields the **explicit general solution**:

$$y(x) = \frac{1}{\mu(x)}\left[ \int \mu(x)Q(x)dx + C \right]$$

---

## Practical Solution Algorithm

In operational practice, replicating the term-by-term multiplication process from the derivation is unnecessary. Apply the integrating factor formula directly to the reduced equation:

1. **Normalization:** Write the ODE in standard form $\dfrac{dy}{dx} + P(x)y = Q(x)$.
2. **Integrating Factor Calculation:** Identify $P(x)$ and compute $\mu(x) = e^{\int P(x)dx}$ (omitting the integration constant at this step, as $C_0 = 0$).
3. **Direct Application of the Integrated Formula:** Write the fundamental equality obtained from the derivation:

   $$\mu(x)y = \int \mu(x)Q(x)dx + C$$

4. **Right-Hand Side Integration:** Evaluate the integral of product $\mu(x)Q(x)$ (frequently requiring integration by parts or substitution) and add arbitrary integration constant $C$.
5. **Isolation of $y(x)$:** Divide the result by $\mu(x)$ to obtain the explicit general solution.

---

## Worked Examples

### Example: General Solution with Exponential Factor

Find the general solution of the differential equation:

$$\frac{dy}{dx} + 2x y = 4x$$

**Resolution:**

**Term Identification:**
The equation is already in standard form, with $P(x) = 2x$ and $Q(x) = 4x$.

**Integrating Factor Calculation $\mu(x)$:**

$$\int P(x)dx = \int 2x dx = x^2 \implies \mu(x) = e^{x^2}$$

**Direct Application of the Method:**

$$\mu(x)y = \int \mu(x)Q(x)dx + C \implies e^{x^2}y = \int 4x e^{x^2} dx + C$$

**Solving the Integral:**
Applying substitution $u = x^2$, $du = 2x dx$:

$$e^{x^2}y = 2 e^{x^2} + C$$

**Isolating General Solution $y(x)$:**

$$y(x) = 2 + C e^{-x^2}$$

---

### Example: Initial Value Problem (IVP) with Integration by Parts

Solve the IVP:

$$\begin{cases} 
x\dfrac{dy}{dx} + y = x e^x, \quad x > 0 \\ 
y(1) = 3 
\end{cases}$$

**Resolution:**

**Normalization (dividing by $x$ for $x > 0$):**

$$\frac{dy}{dx} + \frac{1}{x}y = e^x$$

Where $P(x) = \dfrac{1}{x}$ and $Q(x) = e^x$.

**Integrating Factor Calculation:**

$$\int \frac{1}{x}dx = \ln|x| = \ln x \quad (x > 0) \implies \mu(x) = e^{\ln x} = x$$

**Direct Application of the Method:**

$$x y = \int x e^x dx + C$$

**Integration by Parts for $\int x e^x dx$:**
Choosing $u = x \implies du = dx$ and $dv = e^x dx \implies v = e^x$:

$$\int x e^x dx = x e^x - \int e^x dx = x e^x - e^x$$

Substituting back:

$$x y = x e^x - e^x + C$$

**General Solution:**

$$y(x) = e^x - \frac{e^x}{x} + \frac{C}{x}$$

**Applying Initial Condition $y(1) = 3$:**

$$3 = e^1 - \frac{e^1}{1} + \frac{C}{1} \implies 3 = e - e + C \implies C = 3$$

**Final Particular Solution:**

$$y(x) = e^x - \frac{e^x}{x} + \frac{3}{x}$$

---

## Practical Applications

### Series RL Electrical Circuits
Current $i(t)$ in a circuit with resistor $R$ and inductor $L$ driven by voltage source $V(t)$ obeys linear ODE $L\dfrac{di}{dt} + Ri = V(t)$, solved directly via integrating factor $\mu(t) = e^{\frac{R}{L}t}$.

### Mixing Processes (Storage Tanks)
Solute mass $y(t)$ in a tank maintained under constant inflow and outflow rates is described by a first-order linear ODE of the form $\dfrac{dy}{dt} + k y = r_{in}$.