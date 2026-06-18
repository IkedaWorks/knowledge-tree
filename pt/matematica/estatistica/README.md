# Estatística, Metrologia e Modelagem Estocástica

Este módulo reúne o arcabouço matemático e computacional necessário para quantificar a incerteza, analisar a dispersão de dados experimentais e modelar fenômenos probabilísticos. Em vez de uma abordagem puramente teórica, os tópicos são dissecados a partir da anatomia de suas equações, conectando o formalismo estatístico à realidade prática da engenharia e do desenvolvimento de algoritmos.

## 📌 Pré-requisitos

* **Matemática Discreta e Álgebra:** Manipulação de somatórios ($\sum$), teoria de conjuntos e álgebra elementar.
* **Cálculo Vetorial e Diferencial:** Derivadas parciais, diferenciais totais (essenciais para propagação de erros) e integrais definidas (para distribuições contínuas).

## 🗺️ Roteiro de Aprendizado e Estrutura de Notas

O módulo é estruturado de forma cronológica e incremental, dividindo-se nas seguintes frentes analíticas:

### 01. Medidas de Centralidade e Comportamento Amostral
* **Foco:** Determinação do centro de gravidade dos dados brutos.
* **Conceitos:** Média aritmética, mediana e moda. Análise de simetria e o impacto de valores discrepantes (*outliers*) sobre as métricas de tendência central.

### 02. Dispersão de Dados e a Anatomia do RMS
* **Foco:** Quantificação da variabilidade e do ruído inerentes a qualquer processo de medição.
* **Conceitos:** Variância, Desvio Padrão Amostral ($N-1$) vs. Populacional ($\sigma$). O formalismo da Correção de Bessel (graus de liberdade) e a ponte matemática com o valor eficaz estatístico (Root Mean Square - RMS).

### 03. Metrologia Teórica e Incerteza de Medição
* **Foco:** Cálculo do parâmetro de confiabilidade e da margem de dúvida geométrica de um resultado experimental.
* **Conceitos:** Incerteza Tipo A (flutuação estatística amortecida por $\sqrt{n}$), Incerteza Tipo B (limites do hardware normalizados por $\sqrt{3}$) e a Incerteza Combinada Quadrática ($u_c$). Formalismo de expansão ($U = k \cdot u_c$) e as equações diferenciais para Propagação de Incertezas em medições indiretas.

### 04. Análise Multivariada e Sincronia de Dados
* **Foco:** Mapeamento do comportamento conjunto entre duas ou mais variáveis independentes.
* **Conceitos:** Geometria da Covariância Amostral, o Coeficiente de Correlação de Pearson ($r$) como métrica de normalização vetorial e introdução aos modelos de regressão linear.

### 05. Teoria Probabilística e Modelos Estocásticos
* **Foco:** Transição da análise de dados estáticos para a modelagem preditiva de eventos aleatórios.
* **Conceitos:** Espaço amostral, axiomas da probabilidade, variáveis aleatórias discretas (Binomial, Poisson) e contínuas (Distribuição Normal / Gaussiana).