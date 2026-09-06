---
id: "physics"
title: "Physics"
type: "domain"
language: "en"
tags:
  - "physics"
  - "mechanics"
  - "electromagnetism"
  - "circuits"
modules:
  - "classical-mechanics"
  - "electromagnetism"
  - "electric-circuits"
---
# Physics Domain

> "If I have seen further it is by standing on the shoulders of Giants."
> — Isaac Newton

The **Physics** domain encompasses the fundamental principles governing the natural universe, ranging from the mechanical laws of motion and energy conservation to the dynamics of electromagnetic fields and circuit theory.

This structure establishes the conceptual and mathematical foundation required for advanced studies in engineering, computer science, and natural sciences, enabling the modeling and resolution of real-world physical problems.

## Domain Roadmap

```mermaid
flowchart LR
    %% High-Contrast Minimalist Palette
    style ROOT fill:#18181b,stroke:#d4d4d4,stroke-width:2px,color:#ffffff
    style L1 fill:#0f172a,stroke:#475569,stroke-width:1px,color:#f8fafc
    style L2_1 fill:#0f172a,stroke:#475569,stroke-width:1px,color:#f8fafc
    style L2_2 fill:#0f172a,stroke:#475569,stroke-width:1px,color:#f8fafc

    subgraph Core [Fundamental Core]
        ROOT["Physics Domain"]
    end

    subgraph Level1 [Foundations]
        L1["Classical Mechanics"]
    end

    subgraph Level2 [Applications & Fields]
        L2_1["Electromagnetism"]
        L2_2["Electric Circuits"]
    end

    ROOT --> L1
    L1 --> L2_1
    L1 --> L2_2
````

## Available Modules

| **Module**                                             | **Description**                                                                      | **Level**    | **Status** |
| ------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------ | ---------- |
| [Classical Mechanics](./classical-mechanics/README.md) | Kinematics, Newton's laws, work, energy, momentum, and rotational mechanics.         | Beginner     | Active     |
| [Electromagnetism](./electromagnetism/README.md)       | Electric charge, electric field, Gauss's law, potential, capacitance, and magnetism. | Intermediate | Active     |
| [Electric Circuits](./electric-circuits/README.md)     | Kirchhoff's laws, nodal/mesh analysis methods, network theorems, and DC analysis.    | Intermediate | Active     |

## General Prerequisites

- **Differential and Integral Calculus:** Limits, derivatives, definite/indefinite integrals, and basic differential equations.
    
- **Vector Algebra:** Vector operations, dot product, cross product, and coordinate system decomposition.