---
id: definicao-edo
title: Definition of Ordinary Differential Equation
---
# Definition of Ordinary Differential Equation

## Context and Origin

Traditional calculus teaches us to map reality in a static manner, revealing the slope of a curve at a specific point or the instantaneous velocity of an object from a known position law. However, when investigating natural phenomena, we realize that fundamental laws rarely hand us a ready-made photograph of a system's behavior. What empirical observation grants us are the rules of change, such as the rate at which a microbial population expands, the way heat migrates through a metallic rod, or the mode in which gravity alters the momentum of a body in free fall. In these scenarios, the available knowledge is not the function describing the state, but rather an intrinsic relationship between that state and its rates of change. Thus, the fundamental inverse problem arises: how do we recover the complete trajectory of a phenomenon when we possess only the law governing its pace of transformation.

## Intuition and Mental Model

To gauge the nature of this quest, it is useful to contrast this new object with the safe terrain of elementary algebra. In a traditional algebraic equation, such as $x^2 - 4 = 0$, the sought-after unknown is a number or a discrete set of numerical values satisfying the equality, meaning that the universe of solutions is static. In the territory of differential equations, however, the unknown ceases to be a mere number and becomes an entire function. The equation does not ask which value satisfies an arithmetic operation, but rather which curve, amid an infinite continuum of possibilities, possesses a rate of variation that strictly obeys an imposed condition. The conceptual distance becomes even clearer when we compare differential equations among themselves. If the unknown function depends on multiple independent variables, such as the temperature at a point on a metal plate varying across both space and time, the rates of change manifest through partial derivatives, giving rise to partial differential equations. Conversely, when the phenomenon under scrutiny depends on a single independent variable, typically time or a one-dimensional spatial coordinate, the derivatives involved are total. It is precisely this restricted dependence on a single variable that earns the object the term ordinary. To visualize the geometric meaning of this structure, imagine that each point of a Cartesian plane carries a small directional indicator pointing out the slope a curve must possess when passing through it. This mesh of slopes forms a directional field, and solving the equation amounts to finding a continuous curve winding through this field while perfectly respecting, at each point of its path, the orientation imposed by the mesh.
## Formal Definition

Formally, an Ordinary Differential Equation of order $n$ is a mathematical relation involving an unknown function $y = f(x)$, its independent variable $x$, and the successive derivatives of this function up to order $n$, expressed in the general implicit form by:

$$F\left(x, y, y', y'', \dots, y^{(n)}\right) = 0$$

The order of an ODE is determined by the highest-degree derivative present in the equation. The algebraic degree of the equation, in turn, refers to the power to which this highest-order derivative is raised. Since the differentiation process erases information about constant values, solving an ODE naturally produces an entire family of curves parameterized by integration constants, reflecting the inherent loss of information during the process. To pin down a unique trajectory in practice, establishing initial conditions becomes essential, anchoring the system's behavior at a known starting point and guaranteeing the uniqueness of the mathematical model applicable to the real world.

## Conceptual Examples

To illustrate the mechanism in practice, consider the law of radioactive decay, modeled by the expression:

$$\frac{dy}{dt} = -k y$$

In this structure, $y(t)$ represents the remaining radioactive mass as a function of time $t$, and $k$ is a positive disintegration constant. The equation states that the rate of decay of the substance at any instant is directly proportional to the amount of material present at that exact moment. The order of this equation is determined by the highest-degree derivative present, which in this case is the first derivative, classifying it as a first-order ODE of degree one. Another classic example occurs in classical mechanics when analyzing the oscillation of a simple pendulum under small amplitudes, whose modeling results in the expression:

$$\frac{d^2\theta}{dt^2} + \frac{g}{L}\theta = 0$$

In this case, the unknown function is the angle $\theta$ as a function of time $t$, and the presence of the second derivative raises the equation's order to two. In both examples, the analytical goal does not consist of isolating a fixed number, but of decoding the rule governing the continuous evolution of the system.