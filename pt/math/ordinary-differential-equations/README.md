---
id: ordinary-differential-equations
title: Equações Diferenciais Ordinárias
domain: math
type: module
schema_version: "2.0"
language: pt
level: advanced
prerequisites:
  - single-variable-calculus
tags:
  - differential-equations
  - ordinary-differential-equations
  - differential-equation-order
  - linearity
  - initial-value-problem
---
# Equações Diferenciais Ordinárias

> "Deus é um matemático de altíssima ordem, e Ele usou matemática muito avançada na construção do universo."  
> — **Paul Dirac**

O módulo de **Equações Diferenciais Ordinárias (EDO)** abrange equações que relacionam uma função desconhecida de uma única variável às suas derivadas. Serve como a principal estrutura matemática para a modelagem de sistemas dinâmicos contínuos em engenharia, física e economia quantitativa.

Este módulo explora conceitos fundamentais de EDOs, classificações por ordem e linearidade, soluções gerais e particulares, e problemas de valor inicial (PVI).

## Conteúdo do Módulo

### Conceitos e Métodos de EDO

| Tópico / Conceito                                                          | Descrição Sucinta                                                                                                                                                |
| :------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Conceitos Fundamentais de EDO](theory/ode-fundamental-concepts.md)                  | Definição de EDOs, ordem, grau, linearidade, verificação de soluções e Problemas de Valor Inicial (PVI).                                                         |
| [Modelagem Matemática](./theory/mathematical-modeling.md)                  | Dedução de equações governantes baseadas em leis de conservação, taxas de variação e equações constitutivas.                                                     |
| [Natureza e Geometria das Soluções de uma EDO](./theory/ode-solutions.md)  | Análise geométrica de soluções explícitas/implícitas, campos de direções, soluções gerais, particulares e singulares.                                            |
| [Existência e Unicidade de Soluções](./theory/ode-existence-uniqueness.md) | Teoremas de Peano e Picard-Lindelöf, Retângulo de Picard, condição de Lipschitz e iteração de Picard.                                                            |
| [Metódo de Separação de Variáveis](./theory/ode-separable.md)              | Resolução de EDOs de 1ª ordem por separação e integração direta de variáveis $x$ e $y$, com análise de soluções de equilíbrio e singulares.                      |
| [Método do Fator Integrante](./theory/ode-linear-integrating-factor.md)    | Resolução de EDOs lineares de 1ª ordem via fator integrante $\mu(x) = e^{\int P(x)dx}$, com dedução pela regra do produto, aplicação direta e exemplos práticos. |
| [Método da Equação Exata](./theory/ode-exact.md)                           | Resolução de EDOs exatas via potencial $\psi(x,y) = C$, critério de Clairaut/Schwarz e dedução de fatores integrantes $\mu(x)$ e $\mu(y)$.                       |
| [EDOs de Bernoulli](./theory/ode-bernoulli.md)                             | Linearização de EDOs não-lineares da forma $y' + P(x)y = Q(x)y^n$ via substituição $u = y^{1-n}$.                                                                |

## Pré-requisitos

- **Cálculo de Uma Variável** (**single-variable-calculus**): Domínio de técnicas de diferenciação e integração contínua.

## Bibliografia e Referências

- BOYCE, William E.; DIPRIMA, Richard C. **Equações Diferenciais Elementares e Problemas de Valores de Contorno**. 10ª ed. Rio de Janeiro: LTC, 2015.
- ZILL, Dennis G. **Equações Diferenciais com Aplicações em Modelagem**. 10ª ed. São Paulo: Cengage Learning, 2016.