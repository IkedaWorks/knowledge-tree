---
id: calculo-uma-variavel
title: Cálculo de Uma Variável
domain: matematica
type: module
schema_version: "2.0"
language: pt
level: intermediate
tags:
  - calculo
  - limites
  - derivadas
  - integrais
  - series
prerequisites:
  - valor-absoluto
---
# Cálculo de Uma Variável

> "Se vi mais longe, foi por estar sobre os ombros de gigantes."  
> — **Isaac Newton**

O módulo de **Cálculo de Uma Variável** estuda as taxas de variação, o comportamento assintótico de funções e o acúmulo contínuo de quantidades reais. Ele fornece o alicerce matemático indispensável para as ciências exatas, engenharias e modelagem quantitativa.

Este módulo aborda de forma rigorosa a teoria de limites, o cálculo diferencial com suas técnicas e aplicações práticas, a teoria de integração com o Teorema Fundamental do Cálculo e as séries de potências.

## Conteúdo do Módulo

### Limites e Continuidade

| Tópico / Conceito                                                        | Descrição Sucinta                                                                     |
| :----------------------------------------------------------------------- | :------------------------------------------------------------------------------------ |
| [Conceito de Limite](./theory/limit-definition.md)                       | Definição intuitiva e formal de limites de funções reais.                             |
| [Propriedades dos Limites](./theory/limit-laws.md)                       | Leis algébricas e operatórias para o cálculo de limites.                              |
| [Demonstração das Propriedades de Limites](./theory/proof-limit-laws.md) | Provas formais das propriedades fundamentais de limites.                              |
| [Teorema do Confronto](./theory/squeeze-theorem.md)                      | Aplicação do Teorema do Squeeze para limites delimitados.                             |
| [Indeterminações em Limites](./theory/indeterminate-limits.md)           | Resolução de formas indeterminadas do tipo zero sobre zero e infinito sobre infinito. |
| [Limites Laterais](./theory/one-sided-limits.md)                         | Análise da existência de limites pela esquerda e pela direita.                        |
| [Limites Infinitos e no Infinito](./theory/infinite-limits.md)           | Comportamento assintótico de funções quando x cresce arbitrariamente.                 |
| [Limites Fundamentais](./theory/fundamental-limits.md)                   | Resolução de limites trigonométricos e exponenciais notáveis.                         |
| [Continuidade de Funções](./theory/continuity.md)                        | Condições para continuidade pontual e em intervalos.                                  |
| [Limite de Função Composta](./theory/composite-function-limit.md)        | Aplicação de limites em composições funcionais.                                       |
| [Assíntotas](./theory/asymptotes.md)                                     | Identificação geométrica de assíntotas no plano cartesiano.                           |
| [Teorema do Valor Intermediário](./theory/intermediate-value-theorem.md) | Propriedade de funções contínuas e localização de raízes.                             |
| [Revisão Geral de Limites](./theory/limits-review.md)                    | Síntese e consolidação dos conceitos de limites e continuidade.                       |

### Cálculo Diferencial: Conceitos e Regras

| Tópico / Conceito                                                                                                | Descrição Sucinta                                                         |
| :--------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------ |
| [Conceito de Derivada](./theory/derivative-definition.md)                                                        | Interpretação geométrica da reta tangente e taxa de variação instantânea. |
| [Regras Básicas de Derivação](./theory/derivative-rules.md)                                                      | Regra da potência, soma, produto e quociente.                             |
| [Demonstração das Regras de Derivação](./theory/proof-derivative-rules.md)                                       | Dedução formal das regras algébricas de derivação.                        |
| [Regra da Cadeia](./theory/chain-rule.md)                                                                        | Técnica de diferenciação de funções compostas.                            |
| [Demonstração da Regra da Cadeia](./theory/proof-chain-rule.md)                                                  | Prova matemática rigorosa da Regra da Cadeia.                             |
| [Derivada Exponencial e Logarítmica](./theory/exponential-logarithmic-derivatives.md)                            | Derivação de base e e bases arbitrárias.                                  |
| [Derivada da Função Inversa](./theory/inverse-function-derivative.md)                                            | Relação diferencial entre uma função bijetora e sua inversa.              |
| [Demonstração das Derivadas Logarítmicas e Exponenciais](./theory/proofs-exponential-logarithmic-derivatives.md) | Prova formal usando limites fundamentais.                                 |
| [Derivadas de Funções Trigonométricas](./theory/trigonometric-derivatives.md)                                    | Derivação de seno, cosseno, tangente e suas recíprocas.                   |
| [Demonstração das Derivadas do Seno e Cosseno](./theory/proofs-trigonometric-derivatives.md)                     | Prova usando identidades trigonométricas e limites centrais.              |
| [Demonstração da Derivada da Tangente](./theory/tangent-derivative-proof.md)                                     | Particularidades da aplicação da regra do quociente na tangente.          |
| [Derivadas de Trigonométricas Inversas](./theory/inverse-trigonometric-derivatives.md)                           | Diferenciação do arcseno, arccosseno e arctangente.                       |
| [Funções Hiperbólicas](./theory/hyperbolic-functions.md)                                                         | Definição e propriedades de seno e cosseno hiperbólicos.                  |
| [Derivadas de Funções Hiperbólicas](./theory/hyperbolic-derivatives.md)                                          | Diferenciação de funções hiperbólicas diretas e inversas.                 |
| [Derivadas de Ordem Superior](./theory/higher-order-derivatives.md)                                              | Derivadas segundas, terceiras e notação n-ésima.                          |
| [Derivação Implícita](./theory/implicit-differentiation.md)                                                      | Diferenciação de equações onde y não está isolado.                        |
| [Diferenciação Paramétrica](./theory/parametric-differentiation.md)                                              | Derivada de curvas definidas por equações paramétricas.                   |
| [Diferenciais e Aproximação Linear](./theory/differentials-linear-approximation.md)                              | Conceito de diferencial dy e estimativa de erros.                         |

### Aplicações da Derivada e Análise de Funções

| Tópico / Conceito                                                              | Descrição Sucinta                                                            |
| :----------------------------------------------------------------------------- | :--------------------------------------------------------------------------- |
| [Regra de L'Hôpital](./theory/lhopital-rule.md)                                | Resolução de indeterminações por diferenciação de numerador e denominador.   |
| [Taxas Relacionadas](./theory/related-rates.md)                                | Modelagem de variáveis interdependentes em variação temporal.                |
| [Lógica das Taxas Relacionadas](./theory/related-rates-logic.md)               | Estruturação lógica e física de problemas de taxas encadeadas.               |
| [Resolução de Taxas Relacionadas](./theory/related-rates-problem-solving.md)   | Exercícios práticos e estratégias de resolução.                              |
| [Análise Marginal](./theory/marginal-analysis.md)                              | Aplicação das derivadas no estudo de custo, receita e lucro marginal.        |
| [Máximos e Mínimos](./theory/extrema-maxima-minima.md)                         | Identificação de pontos críticos, valores extremos locais e globais.         |
| [Teorema do Valor Médio](./theory/mean-value-theorem.md)                       | Enunciado e interpretação geométrica do Teorema de Rolle e do TVM.           |
| [Demonstração do Teorema do Valor Médio](./theory/proof-mean-value-theorem.md) | Prova matemática formal do Teorema do Valor Médio.                           |
| [Testes das Derivadas](./theory/derivative-tests.md)                           | Testes da primeira e segunda derivada para concavidade e pontos de inflexão. |
| [Construção de Gráficos de Funções](./theory/curve-sketching.md)               | Esboço completo de curvas analisando domínio, assíntotas e extremos.         |

### Cálculo Integral: Fundamentos e Sequência Didática

| Tópico / Conceito                                                                    | Descrição Sucinta                                             |
| :----------------------------------------------------------------------------------- | :------------------------------------------------------------ |
| [Conceito de Integral](./theory/integral-concept.md)                                 | Abertura do problema da área e operador anti-derivada.        |
| [Integral Indefinida](./theory/indefinite-integrals.md)                              | Definição de primitiva e constante de integração.             |
| [Integrais Imediatas](./theory/immediate-integrals.md)                               | Tabela fundamental de primitivas diretas.                     |
| [Soma de Riemann](./theory/riemann-sums.md)                                          | Construção rigorosa da integral definida via limite de somas. |
| [Integral Definida](./theory/definite-integrals.md)                                  | Definição e interpretação geométrica da área sob a curva.     |
| [Propriedades das Integrais Definidas](./theory/definite-integral-properties.md)     | Operações lineares, aditividade de intervalo e desigualdades. |
| [Teorema Fundamental do Cálculo](./theory/fundamental-theorem-calculus.md)           | Conexão entre o cálculo diferencial e o cálculo integral.     |
| [Demonstração do TFC](./theory/proof-fundamental-theorem-calculus.md)                | Prova formal da primeira e segunda parte do TFC.              |
| [Cálculo de Áreas com Integral](./theory/area-calculation-integrals.md)              | Determinação de áreas entre curvas no plano.                  |
| [Integral de Função Contínua por Partes](./theory/piecewise-continuous-integrals.md) | Integração de funções definidas com múltiplas sentenças.      |

### Técnicas Avançadas de Integração

| Tópico / Conceito                                                              | Descrição Sucinta                                                          |
| :----------------------------------------------------------------------------- | :------------------------------------------------------------------------- |
| [Método da Substituição](./theory/integration-substitution-method.md)          | Mudança de variável para simplificação de integrandos.                     |
| [Substituição com Mudança de Limites](./theory/substitution-limits-change.md)  | Aplicação do método da substituição diretamente em integrais definidas.    |
| [Substituição Trigonométrica](./theory/trigonometric-substitution.md)          | Eliminação de radicais através de identidades trigonométricas.             |
| [Integração por Partes](./theory/integration-by-parts.md)                      | Técnica baseada na derivada do produto de funções.                         |
| [Divisão de Polinômios](./theory/polynomial-division.md)                       | Método de redução de frações racionais impróprias.                         |
| [Método de Briot-Ruffini](./theory/briot-ruffini-method.md)                    | Algoritmo rápido para divisão de polinômios.                               |
| [Decomposição em Frações Parciais](./theory/partial-fraction-decomposition.md) | Integração de funções racionais por fatores lineares e quadráticos.        |
| [Demonstração das Frações Parciais](./theory/proof-partial-fractions.md)       | Fundamentação algébrica da decomposição em frações simples.                |
| [Integrais Impróprias](./theory/improper-integrals.md)                         | Integração com limites infinitos ou integrandos desatendidos/descontínuos. |
| [Integrais Trigonométricas](./theory/trigonometric-integrals.md)               | Métodos de integração para potências de seno, cosseno, secante e tangente. |

### Aproximações Polinomiais e Séries

| Tópico / Conceito                                                   | Descrição Sucinta                                                         |
| :------------------------------------------------------------------ | :------------------------------------------------------------------------ |
| [Séries de Taylor e Maclaurin](./theory/taylor-maclaurin-series.md) | Representação e aproximação de funções por séries de potências infinitas. |

## Pré-requisitos

- **Valor Absoluto** (**valor-absoluto**): Domínio de propriedades de módulo, inequações modulares e manipulação algébrica fundamental.
    
- **Fundamentos de Matemática (Geral)**: Conhecimento prático em álgebra elementar, equações polinomiais, funções trigonométricas e geometria analítica.
## Bibliografia e Referências

* STEWART, James. **Cálculo, Volume 1**. 8ª ed. São Paulo: Cengage Learning, 2016.
* GUIDORIZZI, Hamilton Luiz. **Um Curso de Cálculo, Volume 1**. 5ª ed. Rio de Janeiro: LTC, 2001.
* THOMAS, George B. **Cálculo, Volume 1**. 12ª ed. São Paulo: Pearson, 2012.