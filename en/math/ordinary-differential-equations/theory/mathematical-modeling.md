---
id: mathematical-modeling
title: Mathematical Modeling with ODEs
domain: math
module: ordinary-differential-equations
type: concept
schema_version: "2.0"
language: en
level: advanced
prerequisites:
  - ode-concepts
  - single-variable-calculus
tags:
  - differential-equations
  - modeling
  - physics
  - engineering
---

# Mathematical Modeling with Ordinary Differential Equations

## Motivation and Context

Mathematical modeling is the art of translating real-world dynamic behaviors into the formal language of calculus. In physical, biological, and economic systems, it is rarely possible to measure or directly predict the state function $y(t)$ in an explicit manner. However, it is almost always possible to observe, measure, or deduce the **instantaneous rates of change** of this quantity based on conservation laws, mass balances, energy balances, or forces.

The core challenge of modeling lies not in solving the differential equation, but in its **initial formulation**. It involves answering the following question: how do we transform hypotheses and empirical observations regarding system variations into a rigorous mathematical equation?

Constructing a differential model requires abstracting secondary details, identifying relevant state variables, and expressing physical interactions purely through rates of change, yielding an Ordinary Differential Equation (ODE) that describes the deterministic behavior of the system.

## Theoretical Formulation

The formulation of a differential model follows a strict conceptual framework based on fundamental balance laws and constitutive equations.

### The Model Construction Protocol

To derive the differential equation for any continuous system, the following framework is applied:

- **Identification of Variables:** Define the independent variable (typically time $t$ or position $x$) and the dependent state variable $y(t)$ to be determined.
    
- **Rate Balance Principle:** Apply the universal conservation law where the net rate of change of the system is given by the difference between input and output rates:
    
    $$\frac{dy}{dt} = \text{Input Rate} - \text{Output Rate}$$
- **Application of Constitutive Laws:** Express rates using known physical relations (e.g., Hooke's Law, Newton's Laws, Kirchhoff's Laws, law of mass action).
    
- **Incorporation of Initial Conditions:** Define the physical boundaries of the system at the initial instant $y(t_0) = y_0$ to formulate the initial value problem (IVP).
    

### Typical Differential Structures by Phenomenon

#### Mass Balance and Tank Mixing

For the amount of solute $Q(t)$ in a reservoir with continuous flow:

$$\frac{dQ}{dt} = R_{\text{in}} - R_{\text{out}} = (C_{\text{in}} \cdot V_{\text{in}}) - (C_{\text{out}} \cdot V_{\text{out}})$$

Where $C$ represents concentration and $V$ represents volumetric flow rate.

#### Force Balance in Resistive Media

Applying Newton's Second Law ($\sum F = m \cdot a$) for velocity $v(t)$ under state-dependent forces:

$$m \frac{dv}{dt} = F_{\text{propulsion}}(t) - F_{\text{resistive}}(v)$$

## Examples and Solved Problems

### Formulation of Solute Dynamics in a Mixing Model

A reservoir initially contains $100\ \text{liters}$ of pure water. A saline solution containing $0.2\ \text{kg}$ of salt per liter is pumped into the tank at a constant rate of $3\ \text{liters per minute}$. The mixture is kept uniform by stirring and flows out of the tank at the same rate of $3\ \text{liters per minute}$. Formulate the differential equation governing the mass of salt $Q(t)$ in the tank at any time $t$.

#### Input Rate Formulation

The mass rate of salt entering the system is the product of the input concentration and the volumetric inflow rate:

$$R_{\text{in}} = \left(0.2\ \frac{\text{kg}}{\text{L}}\right) \cdot \left(3\ \frac{\text{L}}{\text{min}}\right) = 0.6\ \frac{\text{kg}}{\text{min}}$$

#### Output Rate Formulation

The instantaneous concentration of salt in the tank is given by the ratio of total salt mass $Q(t)$ to liquid volume $V(t) = 100\ \text{L}$ (which remains constant since the inflow rate equals the outflow rate):

$$C_{\text{out}}(t) = \frac{Q(t)}{100}\ \frac{\text{kg}}{\text{L}}$$

The rate at which salt leaves the tank is the product of this instantaneous concentration and the outflow rate:

$$R_{\text{out}} = \left(\frac{Q(t)}{100}\ \frac{\text{kg}}{\text{L}}\right) \cdot \left(3\ \frac{\text{L}}{\text{min}}\right) = \frac{3 Q(t)}{100}\ \frac{\text{kg}}{\text{min}}$$

#### System ODE Construction

Applying the rate balance principle $\frac{dQ}{dt} = R_{\text{in}} - R_{\text{out}}$:

$$\frac{dQ}{dt} = 0.6 - \frac{3}{100}Q(t)$$

Rearranging into canonical form as a first-order linear ODE with the initial condition of pure water $Q(0) = 0$:

$$\frac{dQ}{dt} + 0.03 Q(t) = 0.6, \quad Q(0) = 0$$

### Construction of a Damped Mass-Spring Mechanical Model

Consider a block of mass $m$ connected to a spring with stiffness constant $k$ and a viscous damper with friction coefficient $c$. The block moves along a horizontal surface. Derive the differential equation governing the displacement $x(t)$ of the block from its equilibrium position.

#### Identification of Acting Forces

By d'Alembert's principle and constitutive physical laws:

- **Spring Restoring Force:** By Hooke's Law, the spring opposes displacement: $F_{\text{spring}} = -k x(t)$.
    
- **Viscous Damping Force:** Damper resistance is proportional to instantaneous velocity and opposes motion: $F_{\text{damper}} = -c v(t) = -c \frac{dx}{dt}$.
    

#### Application of Newton's Second Law

The sum of all forces applied to the body must equal the product of its mass and acceleration $\frac{d^2x}{dt^2}$:

$$\sum F = m \frac{d^2x}{dt^2}$$$$-k x(t) - c \frac{dx}{dt} = m \frac{d^2x}{dt^2}$$

#### Construction of the Second-Order Model

Group all terms containing the state variable $x(t)$ on the left side of the equation:

$$m \frac{d^2x}{dt^2} + c \frac{dx}{dt} + k x(t) = 0$$

This homogeneous second-order linear ordinary differential equation is the rigorous formal model that completely describes the damped oscillatory dynamics of the mechanical system without requiring integration techniques during the modeling phase.

## Advanced Applications and Connections

The ability to isolate derivatives and construct governing equations connects physical intuition to advanced computational modeling:

- **Solver Abstraction:** In modern engineering, the formulated differential model is passed directly to numerical integration algorithms (such as Runge-Kutta). The engineer is responsible for correct ODE formulation, while computational algorithms perform the integration.
    
- **State-Space Modeling:** Higher-order differential models, such as the mass-spring-damper system ($m x'' + c x' + k x = 0$), can be converted into a system of first-order equations by defining auxiliary state variables ($y_1 = x$, $y_2 = x'$), enabling stability analysis via linear algebra.
    
- **Parameter Sensitivity:** Explicit ODE formulation enables qualitative analysis of how variations in constitutive system parameters (such as mass $m$, stiffness $k$, or viscosity $c$) alter model response prior to obtaining analytical solutions.