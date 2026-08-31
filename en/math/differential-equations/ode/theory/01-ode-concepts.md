---
id: "01-ode-concepts"
title: "Concept and Classification of Ordinary Differential Equations"
domain: "mathematics"
type: "concept"
language: "en"
tags:
  - "calculus"
  - "differential-equations"
  - "ode"
prerequisites:
  - "differential-integral-calculus"
  - "elementary-functions"
---
# Concept and Classification of Ordinary Differential Equations

## From the Problem to the Definition

When solving traditional mathematical problems and working with introductory models, we usually deal with ideal and static scenarios. For instance, when solving an algebraic equation like $x^2 - 9 = 0$ or applying Calculus to find the rate of change of a known function $y = f(x)$, the main goal is to find specific numerical values or analyze behaviors where the function's rule is already given.

The real world rarely offers such convenience. In nature and engineering systems, physical quantities change in an interdependent way. For example, the speed at which an infection spreads depends on how many people are currently infected. Similarly, how fast a body cools down depends on the continuous difference between its current temperature and the ambient temperature. Likewise, a rocket's acceleration changes dynamically as it burns fuel and loses mass.

In these real dynamic scenarios, we do not know the function $y(x)$ beforehand. We only know the relationship between this unknown function, its rates of change (derivatives), and the system variables. The instantaneous rate of change of a quantity becomes directly linked to the current state of that same quantity.

To describe this continuous transformation in mathematical language, the unknown object to be determined is no longer a static value, but the evolving function itself.

When we express this relationship between an unknown function $y(x)$, the independent variable $x$, and its derivatives, we obtain a **Differential Equation**.

An equation is classified as an **Ordinary Differential Equation (ODE)** when the unknown function depends exclusively on a single independent variable.

When the unknown function depends on two or more independent variables, the derivatives involved are partial derivatives, forming a Partial Differential Equation (PDE), which belongs to a distinct domain of mathematical analysis.

---

## Origin and Need for the Model

To understand the transition from an algebraic model to a differential model, consider the variation of a population $N(t)$ over time $t$.

The basic physical hypothesis states that the rate of population growth is proportional to the number of individuals present at any given instant.

Translating this relationship into calculus language:

$$\frac{dN}{dt} = k \cdot N(t)$$

In this structure:
* $t$ represents the independent variable (time).
* $N(t)$ represents the dependent and unknown variable.
* $k$ represents the proportionality constant.
* $\frac{dN}{dt}$ represents the instantaneous rate of change of $N$ with respect to $t$.

The solution to this equation is not an isolated number, but a family of functions $N(t) = C \cdot e^{kt}$ describing the continuous evolution of the quantity over time.

---

## Classification and Behavior

Analyzing an ODE requires identifying three fundamental attributes that determine the model's complexity and the choice of study strategy.

### Order
The order of an ODE is strictly determined by the highest derivative present in the equation.

* **First Order:** Involves only the first derivative of the unknown function.
  $$\frac{dy}{dx} + 5y = 0$$

* **Second Order:** Involves the second derivative, commonly used to describe acceleration and mechanical or electrical oscillatory systems.
  $$\frac{d^2y}{dx^2} + 9y = 0$$

### Degree
The degree of an ODE is the algebraic power to which the highest-order derivative is raised, after the equation has been rationalized to remove fractional exponents or radicals involving the derivatives.

$$\left(\frac{d^2y}{dx^2}\right)^3 + 4\left(\frac{dy}{dx}\right)^4 + y = 0$$

In the equation above, the highest derivative is the second derivative ($\frac{d^2y}{dx^2}$), which is raised to the third power. This makes it a **second-order, third-degree ODE**.

### Linearity
An ODE is considered **Linear** if the dependent variable and its derivatives appear in a purely linear form throughout the equation. This requires meeting three conditions simultaneously:

1. The dependent variable $y$ and all its derivatives are raised exclusively to the first power.
2. There are no products between the dependent variable and its derivatives, nor products between different derivatives.
3. There are no non-linear functions applied to the dependent variable or its derivatives, such as $\sin(y)$, $e^y$, $\ln(y)$, or $\sqrt{y'}$.

The general form of an $n$-th order linear ODE is expressed as:

$$a_n(x) \frac{d^n y}{dx^n} + a_{n-1}(x) \frac{d^{n-1} y}{dx^{n-1}} + \dots + a_1(x) \frac{dy}{dx} + a_0(x)y = g(x)$$

---

## Comparative Structural Table

| Differential Equation | Order | Degree | Classification | Cause of Non-Linearity |
| :--- | :--- | :--- | :--- | :--- |
| $\frac{dy}{dx} + 3y = e^x$ | $1^{\text{st}}$ | $1^{\text{st}}$ | **Linear** | None. All linearity criteria are met. |
| $\frac{d^2y}{dx^2} + y^2 = 0$ | $2^{\text{nd}}$ | $1^{\text{st}}$ | **Non-Linear** | The term $y$ is raised to the second power ($y^2$). |
| $y \cdot \frac{dy}{dx} + x = 0$ | $1^{\text{st}}$ | $1^{\text{st}}$ | **Non-Linear** | Product between the dependent variable $y$ and its derivative $\frac{dy}{dx}$. |
| $\frac{d^2y}{dx^2} + \cos(y) = 0$ | $2^{\text{nd}}$ | $1^{\text{st}}$ | **Non-Linear** | Application of the trigonometric function $\cos(y)$ to the dependent variable. |
| $\left(\frac{dy}{dx}\right)^2 + y = x$ | $1^{\text{st}}$ | $2^{\text{nd}}$ | **Non-Linear** | The highest-order derivative is raised to the second power. |

---

## Model Construction / Deductive Reasoning

To solidify the concept of an ODE without diving into algebraic resolution methods, consider building the formal model for electric charge $q(t)$ in a simple $RC$ circuit composed of a resistor $R$ and a capacitor $C$.

### Physical Laws of the System
1. The voltage drop across the resistor is proportional to the electric current $i(t)$: 
   $$V_R = R \cdot i(t)$$
2. The voltage drop across the capacitor is proportional to the stored charge $q(t)$: 
   $$V_C = \frac{q(t)}{C}$$
3. Electric current is the rate of change of charge over time: 
   $$i(t) = \frac{dq}{dt}$$

### Applying Kirchhoff's Voltage Law
The sum of the voltage drops in a closed loop must equal the applied source voltage $E(t)$:

$$V_R + V_C = E(t)$$

### Substitution and Formulation of the ODE
Substituting $V_R$, $V_C$, and the relationship $i(t) = \frac{dq}{dt}$ into the circuit equation:

$$R \frac{dq}{dt} + \frac{1}{C} q(t) = E(t)$$

This final expression is a **1st-order linear Ordinary Differential Equation**, where the unknown function to be determined is the electric charge distribution $q(t)$ over time.

---

## Practical Application and Demonstrative Example

### Structural Identification Problem
Consider the differential equation given by:

$$x^2 \frac{d^3 y}{dx^3} + x \frac{dy}{dx} + \left(x^2 - n^2\right)y = 0$$

Analyze the equation and determine its order, degree, and linearity classification.

#### Resolution

**Order Analysis:**
The highest derivative present in the equation is $\frac{d^3 y}{dx^3}$ (the third derivative of $y$ with respect to $x$). Therefore, it is a **third-order equation**.

**Degree Analysis:**
The highest-order derivative ($\frac{d^3 y}{dx^3}$) is implicitly raised to the power of $1$. Therefore, it is a **first-degree equation**.

**Linearity Analysis:**
1. The dependent variable $y$ and its derivatives ($\frac{d^3 y}{dx^3}$ and $\frac{dy}{dx}$) are all raised to the first power.
2. There are no products such as $y \cdot \frac{dy}{dx}$ or $\frac{dy}{dx} \cdot \frac{d^3 y}{dx^3}$.
3. The coefficients $a_3(x) = x^2$, $a_1(x) = x$, and $a_0(x) = (x^2 - n^2)$ depend exclusively on the independent variable $x$.

The equation satisfies all criteria and is classified as a **3rd-Order Linear ODE**.

---

## High-Level Bridge

> [!TIP]
> Correctly identifying the order and linearity of an ODE defines the simulation architecture in computing. In programming languages and modeling tools, non-linear or higher-order equations must be converted into a system of first-order ODEs so that classical integration algorithms, such as the Runge-Kutta method, can compute system trajectories stably.