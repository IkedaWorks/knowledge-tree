---
id: "computacao"
title: "Computação"
type: "domain"
language: "pt"
tags:
  - "computation"
  - "computer-science"
  - "digital-electronics"
modules:
  - "eletronica-digital"
---
# Domínio de Computação

O domínio de **Computação** abrange os fundamentos teóricos, princípios de arquitetura de processamento e a interface de lógica discreta que sustenta os sistemas computacionais.

## Estrutura do Domínio

```mermaid
graph TD
    %% Base styling for High-Contrast Accessibility
    classDef domainFill fill:#1e1e2e,stroke:#cba6f7,stroke-width:2px,color:#cdd6f4;
    classDef moduleFill fill:#313244,stroke:#89b4fa,stroke-width:2px,color:#cdd6f4;

    Domain["Domínio de Computação"]:::domainFill
    ModEletr["Eletrônica Digital"]:::moduleFill

    Domain --> ModEletr
```
## Módulos Disponíveis

| Módulo                                               | Descrição                                                                                    | Status |
| :--------------------------------------------------- | :------------------------------------------------------------------------------------------- | :----- |
| [Eletrônica Digital](./eletronica-digital/README.md) | Lógica booleana, portas lógicas, circuitos combinacionais e fundamentos de hardware digital. | Ativo  |
