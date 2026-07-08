#  Physics I — Classical Mechanics

Welcome to the central hub for Physics I studies. This space is dedicated to the conceptual, mathematical, and intuitive exploration of **Classical Mechanics** — the analytical foundation describing the motion of matter on a macroscopic scale and the fundamental interactions governing engineering, from the equilibrium of rigid structures to the dynamics of rotating systems.

The goal of these notes is to build a deep understanding of how bodies and systems interact with forces, focusing on developing **geometric intuition** to set up and interpret equations of motion using calculus, rejecting the mere memorization of ready-made formulas ("black-box method").

##  Prerequisites and the Role of Calculus

Physics I uses Differential and Integral Calculus as its natural modeling language. We do not study motion merely through average changes ($\Delta$), but as instantaneous rates of change and continuous accumulations across time and space:

- **Differential and Integral Calculus I:** Deeply understand the concept of derivatives as instantaneous rates of change ($v = dx/dt$, $a = dv/dt$) and integrals as continuous accumulation of quantities (area under the curve and work calculations).
    
- **Vector Analysis and Analytic Geometry:** Vector decomposition in Cartesian components, dot product (fundamental for Work and Energy concepts), and **cross product** (essential for defining torque, axes of rotation, and angular momentum).
    
- **Coordinate Systems:** Intuition on using polar and cylindrical coordinates when dealing with problems exhibiting circular symmetry or rotational axes.
    

>  **Note on the University vs. High School Approach**
> 
> When we learn Mechanics in high school, equations look like a collection of isolated cases ($F = ma$, $v = v_0 + at$, $\tau = F \cdot d$). However, you fundamentally need **Calculus I and Vectors** at the university level to understand that all of classical mechanics unfolds organically from core principles of differentiation and geometry. Taking this module alongside Calculus transforms your perception of the subject entirely.

##  Learning Roadmap

The content advances linearly, starting from the pure geometry of trajectories to the laws governing forces and multi-dimensional rotational dynamics:

###  Block 1: Kinematics (The Geometry of Motion)

- **Fundamentals and Vector Tools:** The scope of mechanics, dimensional analysis, SI units, and core vector operations (decomposition, dot, and cross products).
    
- **Differential Kinematics (1D, 2D, and 3D):** Position, velocity, and acceleration treated strictly as derivatives and integrals over time. Projectile motion and trajectories under variable acceleration.
    
- **Angular Kinematics and Circular Motion:** The geometric definition of the radian ($\theta = s/r$), angular velocity ($\omega$), and the derivation of centripetal acceleration ($a_c$) via related rates of the velocity vector.
    
###  Block 2: Dynamics and Newton's Laws (The Causes of Motion)

- **Newton's Laws and Linear Momentum:** The modern concept of Force as the time rate of change of momentum ($\vec{F} = d\vec{p}/dt$). Applications involving friction, inclined planes, and drag forces.
    
- **Work, Energy, and Conservation:** Calculating work via the line integral of the dot product ($\int \vec{F} \cdot d\vec{r}$), the Work-Energy Theorem, and mechanical energy conservation in conservative systems.
    
- **Systems of Particles and Impulse:** Center of mass, conservation of linear momentum in collisions, and time-varying mass systems (variable mass systems).
    
### Block 3: Statics and Equilibrium (The Physics of Structures)

- **Equilibrium of a Particle:** The first condition of equilibrium ($\sum \vec{F} = 0$) and concurrent force analysis.
    
- **Rigid Body Equilibrium and Torque:** Introduction to Torque ($\vec{\tau} = \vec{r} \times \vec{F}$) as the rotational agent. The second condition of equilibrium ($\sum \vec{\tau} = 0$) applied to rigid structures, beams, and levers.
    

> **Highlight: Statics as a special case of Dynamics**
> 
> Statics is not an isolated subject, but rather Dynamics in a state where acceleration is strictly zero ($\vec{a} = 0$ and $\vec{\alpha} = 0$).

### Block 4: Advanced Rotations and Rigid Body Dynamics

- **Moment of Inertia and Rotational Second Law:** Scalar rotational inertia and the fundamental relationship between torque and angular acceleration ($\tau = I\alpha$).
    
- **Angular Momentum ($\vec{L}$) and Torque as a Derivative:** Translating linear motion into rotational space. Angular momentum defined via cross product ($\vec{L} = \vec{r} \times \vec{p}$) and torque proven to be its direct time derivative ($\vec{\tau} = d\vec{L}/dt$).
    
- **Conservation of Angular Momentum:** Phenomena where net external torque is zero ($\vec{\tau} = 0$), leading to the conservation of $\vec{L}$, precession, and gyroscopic behavior.
  
## Progression and Advancement Criteria

- **Prerequisite Validation:** The transition from kinematics to dynamics requires complete mastery of differential calculus. Entering rotational dynamics requires absolute mastery of cross products and moment of inertia.
    
- **Active Study Methodology:** Replacing "ready-to-use" formulas with derivations starting from fundamental principles. Solving literal problems before numerical substitution to validate dimensional logic.
    
- **Bibliography Integration:** Using Halliday for problem structure and basic rigor. Using Feynman Lectures for theoretical foundation and modern physics applied to mechanics.
    

> [!TIP]
> 
> **Engineer's Insight:** If you are an engineer, I also recommend Hibbeler; there you will find exercises that better reflect the reality of engineering practice.