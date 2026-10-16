---
id: ordinary-differential-equations
title: Ordinary Differential Equations
domain: math
type: module
schema_version: "2.0"
language: en
level: advanced
tags:
  - differential-equations
  - ordinary-differential-equations
  - differential-equation-order
  - linearity
  - initial-value-problem
prerequisites:
  - single-variable-calculus
---
# Ordinary Differential Equations

> "God is a mathematician of a very high order, and He used very advanced mathematics in constructing the universe."  
> — **Paul Dirac**

The **Ordinary Differential Equations (ODE)** module covers equations relating an unknown function of a single variable to its derivatives. It serves as the primary mathematical framework for modeling continuous dynamical systems across engineering, physics, and quantitative economics.

This module explores core ODE concepts, classifications by order and linearity, general versus particular solutions, and initial value problems (IVPs).

## Module Content

### ODE Concepts and Methods

| Topic / Concept                                                               | Brief Description                                                                                                                                               |
| :---------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [ODE Fundamental Concepts](./theory/ode-concepts.md)                          | Definition of ODEs, order, degree, linearity, solution verification, and Initial Value Problems (IVP).                                                          |
| [Mathematical Modeling](./theory/mathematical-modeling.md)                    | Derivation of governing equations based on conservation laws, rates of change, and constitutive equations.                                                      |
| [Nature and Geometry of EDO Solutions](./theory/ode-solutions.md)             | Geometric analysis of explicit/implicit solutions, direction fields, general, particular, and singular solutions.                                               |
| [Existence and Uniqueness of Solutions](./theory/ode-existence-uniqueness.md) | Peano and Picard-Lindelöf theorems, Picard Rectangle, Lipschitz condition, and Picard iteration.                                                                |
| [Method of Separation of Variables](./theory/ode-separable.md)                | Solving 1st-order ODEs via separation and direct integration of $x$ and $y$ variables, including equilibrium and singular solution analysis.                    |
| [Integrating Factor Method](./theory/ode-linear-integrating-factor.md)        | Solving 1st-order linear ODEs via integrating factor $\mu(x) = e^{\int P(x)dx}$, including product-rule derivation, direct application, and practical examples. |
| [Exact Equation Method](./theory/ode-exact.md)                                | Solving exact ODEs via potential function $\psi(x,y) = C$, Clairaut/Schwarz criterion, and derivation of integrating factors $\mu(x)$ and $\mu(y)$.             |

## Prerequisites

- **Single-Variable Calculus** (**single-variable-calculus**): Mastery of differentiation and continuous integration techniques.

## Bibliography and References

- BOYCE, William E.; DIPRIMA, Richard C. **Elementary Differential Equations and Boundary Value Problems**. 11th ed. Wiley, 2017.
- ZILL, Dennis G. **A First Course in Differential Equations with Modeling Applications**. 11th ed. Cengage Learning, 2018.
