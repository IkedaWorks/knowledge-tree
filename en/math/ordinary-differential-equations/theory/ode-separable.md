---
id: "ode-separable"
title: "Separable Differential Equations"
domain: "math"
module: "ordinary-differential-equations"
type: "method"
schema_version: "2.0"
level: "advanced"
language: "en"
prerequisites:
  - "ode-fundamental-concepts"
  - "ode-solutions"
tags:
  - "differential-equations"
  - "separable-odes"
  - "integration"
  - "initial-value-problems"
---

# Separable Differential Equations

## Motivation and Definition

A first-order ordinary differential equation is called **separable** if the rate of change $\dfrac{dy}{dx}$ can be factored as the product of two distinct functions: one depending solely on the independent variable $x$, and the other depending solely on the dependent variable $y$.

General form:

$$\dfrac{dy}{dx} = g(x) \cdot h(y)$$

If $h(y) \neq 0$, we can isolate all instances of $y$ and $dy$ on the left side and all instances of $x$ and $dx$ on the right side. This algebraic manipulation reduces the differential equation to a direct two-variable integration problem.

---

## Theoretical Formulation and Method of Solution

### Separation of Variables

Dividing both sides by $h(y)$ and formally multiplying by the differential $dx$, we obtain:

$$\frac{1}{h(y)} \, dy = g(x) \, dx$$

Defining $p(y) = \dfrac{1}{h(y)}$, the equation assumes the classic separated form:

$$p(y) \, dy = g(x) \, dx$$

### Integrating Both Sides

Applying indefinite integration to both sides with respect to their respective variables:

$$\int p(y) \, dy = \int g(x) \, dx + C$$

where $C$ represents the arbitrary constant of integration combining constant terms from both integrals.

### Obtaining the Solution

Integration yields an implicit relation of the form $P(y) = G(x) + C$. Whenever possible, we isolate variable $y$ to obtain the **explicit solution** $y = \phi(x)$.

---

## Singular Solutions and Domain Restrictions

When dividing the differential equation by $h(y)$, we implicitly assume $h(y) \neq 0$. Constant roots of $h(y) = 0$ must be analyzed separately:

- If $y = y_c$ is a constant value such that $h(y_c) = 0$, then the constant function $y(x) = y_c$ is an **equilibrium solution** (or constant solution) of the ODE, since $\dfrac{dy}{dx} = 0$.
- If an equilibrium solution $y(x) = y_c$ cannot be obtained by assigning any numerical value to constant $C$ in the general family of solutions, it is called a **singular solution**.

---

## Worked Examples

### Example: Explicit General Solution

Solve the differential equation:

$$\dfrac{dy}{dx} = \frac{x^2}{y}$$

**Resolution:**

**Separating variables:**
Multiplying both sides by $y$ and $dx$:

$$y \, dy = x^2 \, dx$$

**Integrating both sides:**

$$\int y \, dy = \int x^2 \, dx$$

$$\frac{y^2}{2} = \frac{x^3}{3} + C_1$$

**Isolating variable $y$ (Explicit Solution):**
Multiplying through by 2:

$$y^2 = \frac{2}{3}x^3 + 2C_1$$

Renaming constant $2C_1$ as $C$:

$$y(x) = \pm \sqrt{\frac{2}{3}x^3 + C}$$

---

### Example: Initial Value Problem (IVP) with Singular Solution

Find the solution to the IVP:

$$\begin{cases} 
\dfrac{dy}{dx} = 3x^2 y^2 \\ 
y(0) = 1 
\end{cases}$$

**Resolution:**

**Analyzing constant solutions:**
We note $h(y) = y^2$. Setting $y = 0$ yields constant solution $y(x) = 0$.

**Separating variables for $y \neq 0$:**

$$\frac{1}{y^2} \, dy = 3x^2 \, dx \implies y^{-2} \, dy = 3x^2 \, dx$$

**Integrating both sides:**

$$\int y^{-2} \, dy = \int 3x^2 \, dx$$

$$-\frac{1}{y} = x^3 + C$$

**Isolating the general solution:**

$$y(x) = -\frac{1}{x^3 + C}$$

**Applying Initial Condition $y(0) = 1$:**

$$1 = -\frac{1}{0^3 + C} \implies 1 = -\frac{1}{C} \implies C = -1$$

**Final Particular Solution:**

$$y(x) = \frac{1}{1 - x^3}$$

---

## Practical Applications

### Exponential Growth and Decay
Unbounded population growth, radioactive decay, and Newton's law of cooling are described by separable ODEs of the form $\dfrac{dy}{dt} = k \cdot y$, whose general solution is exponential $y(t) = y_0 e^{kt}$.

### Fluid Dynamics (Torricelli's Law)
Draining water from a tank through a bottom orifice is governed by separable equation $\dfrac{dh}{dt} = -k \sqrt{h}$, where $h(t)$ denotes fluid height over time.