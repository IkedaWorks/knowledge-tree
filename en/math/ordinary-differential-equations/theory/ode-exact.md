---
id: "ode-exact"
title: "Exact Differential Equations and Integrating Factors"
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
  - "exact-odes"
  - "integrating-factor"
  - "partial-derivatives"
  - "potential-function"
---

# Exact Differential Equations and Integrating Factors

## Differential Form and the Exactness Criterion

A first-order ordinary differential equation written in differential form:

$$M(x,y) \, dx + N(x,y) \, dy = 0$$

is called **exact** in a simply connected region $R \subset \mathbb{R}^2$ if the left-hand side expression corresponds to the total differential $d\psi$ of some multivariable function $\psi(x,y)$, termed the **potential function**.

If such function $\psi(x,y)$ exists, then:

$$d\psi = \frac{\partial \psi}{\partial x} dx + \frac{\partial \psi}{\partial y} dy = M(x,y) dx + N(x,y) dy$$

which establishes the system of partial derivatives:

$$\frac{\partial \psi}{\partial x} = M(x,y) \quad \text{and} \quad \frac{\partial \psi}{\partial y} = N(x,y)$$

Consequently, the ODE reduces to $d\psi = 0$, whose family of implicit solutions is given by:

$$\psi(x,y) = C$$

### Exactness Criterion Theorem

By Clairaut/Schwarz's theorem on mixed partial derivatives equality, if $M(x,y)$ and $N(x,y)$ possess continuous first partial derivatives in region $R$, the necessary and sufficient condition for $M dx + N dy = 0$ to be exact is:

$$\frac{\partial M}{\partial y} = \frac{\partial N}{\partial x}$$

---

## Potential Reconstruction Algorithm $\psi(x,y)$

When the exactness criterion is satisfied, the potential function $\psi(x,y)$ is reconstructed using the following procedure:

### 1. Partial Integration
Integrate $M(x,y)$ with respect to $x$, treating $y$ as a constant:

$$\psi(x,y) = \int M(x,y) \, dx + g(y)$$

where $g(y)$ is an unknown function solely of $y$, acting as the "constant" of partial integration.

### 2. Determination of $g(y)$
Differentiate the expression for $\psi(x,y)$ with respect to $y$ and set it equal to $N(x,y)$:

$$\frac{\partial \psi}{\partial y} = \frac{\partial}{\partial y} \left( \int M(x,y) \, dx \right) + g'(y) = N(x,y)$$

Isolate $g'(y)$ and integrate with respect to $y$ to determine $g(y)$.

### 3. Solution Formulation
Substitute $g(y)$ back into $\psi(x,y)$ and set the result equal to arbitrary constant $C$, yielding level curve $\psi(x,y) = C$.

*(Note: An analogous process can be initiated by integrating $N(x,y)$ with respect to $y$ to get $\psi(x,y) = \int N(x,y) dy + h(x)$).*

---

## Integrating Factors for Non-Exact Equations

When the ODE $M(x,y) dx + N(x,y) dy = 0$ fails the criterion ($\frac{\partial M}{\partial y} \neq \frac{\partial N}{\partial x}$), one seeks a function $\mu(x,y)$ such that the multiplied equation:

$$\mu(x,y) M(x,y) \, dx + \mu(x,y) N(x,y) \, dy = 0$$

becomes exact. The exactness condition demands:

$$\frac{\partial}{\partial y} \bigl[\mu M\bigr] = \frac{\partial}{\partial x} \bigl[\mu N\bigr] \implies \mu \frac{\partial M}{\partial y} + M \frac{\partial \mu}{\partial y} = \mu \frac{\partial N}{\partial x} + N \frac{\partial \mu}{\partial x}$$

Since finding general $\mu(x,y)$ requires solving a complex PDE, special cases depending on a single variable are evaluated:

### Case 1: Integrating Factor Depending Solely on $x$
If the ratio:

$$\frac{\dfrac{\partial M}{\partial y} - \dfrac{\partial N}{\partial x}}{N} = f(x)$$

is a function exclusively of $x$, then the integrating factor is:

$$\mu(x) = e^{\int f(x) \, dx}$$

### Case 2: Integrating Factor Depending Solely on $y$
If the ratio:

$$\frac{\dfrac{\partial N}{\partial x} - \dfrac{\partial M}{\partial y}}{M} = g(y)$$

is a function exclusively of $y$, then the integrating factor is:

$$\mu(y) = e^{\int g(y) \, dy}$$

---

## Worked Examples

### Example 1: Direct Exact ODE
Solve the differential equation:

$$(2x y + 3) \, dx + (x^2 - 1) \, dy = 0$$

**Resolution:**

**Checking exactness criterion:**
Here $M(x,y) = 2xy + 3$ and $N(x,y) = x^2 - 1$.

$$\frac{\partial M}{\partial y} = 2x, \quad \frac{\partial N}{\partial x} = 2x$$

Since $\dfrac{\partial M}{\partial y} = \dfrac{\partial N}{\partial x} = 2x$, the equation is exact.

**Reconstructing $\psi(x,y)$:**
Integrating $M$ with respect to $x$:

$$\psi(x,y) = \int (2xy + 3) \, dx + g(y) = x^2 y + 3x + g(y)$$

Differentiating with respect to $y$ and setting equal to $N(x,y)$:

$$\frac{\partial \psi}{\partial y} = x^2 + g'(y) = x^2 - 1 \implies g'(y) = -1 \implies g(y) = -y$$

**General Solution:**

$$\psi(x,y) = x^2 y + 3x - y = C$$

---

### Example 2: Using an Integrating Factor Depending on $x$
Find the general solution of:

$$(y^2 + 2xy) \, dx - x^2 \, dy = 0$$

**Resolution:**

**Checking exactness:**
$M(x,y) = y^2 + 2xy$ and $N(x,y) = -x^2$.

$$\frac{\partial M}{\partial y} = 2y + 2x, \quad \frac{\partial N}{\partial x} = -2x$$

Since $2y + 2x \neq -2x$, the ODE is not exact.

**Finding the Integrating Factor:**
Evaluating factor ratio with respect to $x$:

$$\mu(x) = e^{\int -\frac{2}{x} \, dx} = e^{-2 \ln x} = x^{-2} = \frac{1}{x^2}$$

Multiplying the ODE by $\mu(x) = \dfrac{1}{x^2}$:

$$\left(\frac{y^2}{x^2} + \frac{2y}{x}\right) dx - dy = 0$$

Testing exactness and integrating yields the implicit family of solutions:

$$\frac{y^2}{x} + 2y = C x$$

---

## Practical Applications

### Conservative Force Fields and Thermodynamics
In classical physics, if a force field $F = (M, N)$ is conservative, there exists a potential energy function $U(x,y) = -\psi(x,y)$ such that $F = -\nabla U$. In thermodynamics, inexact work or heat differentials transform into exact state functions via absolute temperature integrating factors (such as $1/T$).