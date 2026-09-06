---
id: "computation"
title: "Computation"
type: "domain"
nodes:
  - "eletronica-digital"
---
# Computation Domain

The **Computation** domain covers theoretical foundations, processing architecture principles, and the discrete logic interface behind computing systems.

## Domain Structure

```mermaid
graph TD
    %% Base styling for High-Contrast Accessibility
    classDef domainFill fill:#1e1e2e,stroke:#cba6f7,stroke-width:2px,color:#cdd6f4;
    classDef moduleFill fill:#313244,stroke:#89b4fa,stroke-width:2px,color:#cdd6f4;

    Domain["Computation Domain"]:::domainFill
    ModEletr["Digital Electronics"]:::moduleFill

    Domain --> ModEletr
```
## Available Modules

| Module                                                 | Description                                                                           | Status |
| :----------------------------------------------------- | :------------------------------------------------------------------------------------ | :----- |
| [Digital Electronics](./digital-electronics/README.md) | Boolean logic, logic gates, combinational circuits, and digital hardware foundations. | Active |
