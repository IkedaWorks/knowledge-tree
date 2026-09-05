---
id: chemistry
title: Domínio de Química
type: domain
language: pt
tags:
  - chemistry
  - natural-sciences
  - matter
modules:
  - basic-chemistry
---
# Domínio de Química Geral

> "Nada na vida deve ser temido, apenas compreendido. Agora é a hora de compreender mais, para que possamos temer menos." — Marie Curie

## Visão Geral

Este domínio serve como o ponto de entrada principal para o estudo da ciência química. Ele organiza os princípios químicos fundamentais em módulos de aprendizagem estruturados, cobrindo desde a estrutura atômica básica até disciplinas avançadas e especializadas.

## Roteiro do Domínio


```mermaid
flowchart LR
    %% Módulo Principal
    subgraph L1 [Nível 1 · Núcleo]
        BC([Química Básica])
    end

    %% Módulos Fundamentais
    subgraph L2 [Nível 2 · Fundamentos]
        IC[Química Inorgânica]
        OC[Química Orgânica]
        PC[Físico-Química]
        AC[Química Analítica]
    end

    %% Especializações
    subgraph L3 [Nível 3 · Especializações]
        BIO[Bioquímica]
    end

    %% Conexões
    BC ==> IC
    BC ==> OC
    BC ==> PC
    BC ==> AC

    OC --> BIO

    %% Estilização Místico-Minimalista de Alto Contraste
    style BC fill:#18181b,stroke:#d4d4d4,stroke-width:2px,color:#ffffff
    style IC fill:#0f172a,stroke:#475569,stroke-width:1px,color:#f8fafc
    style OC fill:#0f172a,stroke:#475569,stroke-width:1px,color:#f8fafc
    style PC fill:#0f172a,stroke:#475569,stroke-width:1px,color:#f8fafc
    style AC fill:#0f172a,stroke:#475569,stroke-width:1px,color:#f8fafc
    style BIO fill:#0f172a,stroke:#475569,stroke-width:1px,color:#f8fafc
```

## Módulos

| Módulo                                     | Descrição                                                                      | Nível         | Status         |
| :----------------------------------------- | :----------------------------------------------------------------------------- | :------------ | :------------- |
| [Química Básica](quimica-basica/README.md) | Princípios fundamentais, teoria atômica, estados da matéria e estequiometria.  | Iniciante     | **Disponível** |
| Química Inorgânica                         | Estudo de compostos inorgânicos, metais de transição e química de coordenação. | Intermediário | *Planejado*    |
| Química Orgânica                           | Química baseada em carbono, grupos funcionais, mecanismos de reação e síntese. | Intermediário | *Planejado*    |
| Físico-Química                             | Termodinâmica química, cinética, mecânica quântica e eletroquímica.            | Avançado      | *Planejado*    |
| Química Analítica                          | Métodos de análise qualitativa e quantitativa, titulometria e espectrometria.  | Avançado      | *Planejado*    |
| Bioquímica                                 | Processos químicos dentro e relacionados a organismos vivos.                   | Avançado      | *Planejado*    |

## Pré-requisitos

* **Matemática**: Álgebra elementar, logaritmos básicos e cálculo introdutório.
* **Física**: Fundamentos de energia, trabalho e eletrostática.