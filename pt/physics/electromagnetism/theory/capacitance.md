---
id: "capacitance"
title: "Fundamentos de Capacitância e Separação de Cargas"
domain: "physics"
module: "electromagnetism"
type: "concept"
schema_version: "2.0"
level: "intermediate"
language: "pt"
prerequisites:
  - "electric-field"
  - "electric-potential"
  - "gauss-law"
tags:
  - "electrostatics"
  - "capacitance"
  - "charge-separation"
  - "electric-potential"
---


# Fundamentos de Capacitância e Separação de Cargas

## Motivação e Contexto

Macroscopicamente, um capacitor é um componente passivo de dois terminais projetado para armazenar energia potencial eletrostática no espaço por meio da separação de cargas.

Microscopicamente, ele consiste em dois condutores isolados (placas ou armaduras) separados por um meio isolante (vácuo ou dielétrico). Quando conectado a uma fonte ativa de tensão, o sistema atua como uma bomba de carga: remove elétrons de uma placa (deixando um déficit de elétrons, carga $+Q$) e os deposita na placa oposta (deixando um excesso de elétrons, carga $-Q$).

A carga líquida total de qualquer capacitor é estritamente zero:

$$(+Q) + (-Q) = 0$$

Portanto, quando a física define a "carga de um capacitor", refere-se exclusivamente à magnitude da carga $Q$ acumulada em um de seus condutores individuais.

![Separação eletrostática de cargas e confinamento do campo uniforme em um capacitor de placas paralelas](./../../../../assets/physics/electromagnetism/parallel-plate-capacitance.svg)

## Formulação Teórica

### A Equação Fundamental da Capacitância

A separação espacial de cargas opostas estabelece uma diferença de potencial (tensão) $V$ entre os condutores. Experimentalmente, a carga $Q$ acumulada nas placas é diretamente proporcional a essa diferença de potencial aplicada:

$$Q \propto V \implies Q = C \cdot V$$

Isolando a constante de proporcionalidade, obtém-se a definição de Capacitância ($C$):

$$C = \frac{Q}{V}$$

Onde:
- $Q$ é a magnitude da carga em um condutor em Coulombs ($\text{C}$).
- $V$ é a diferença de potencial entre os condutores em Volts ($\text{V}$).
- $C$ é a capacitância medida em Farads ($\text{F}$), onde $1\text{ F} = 1\text{ C/V}$.

### Independência Geométrica e Material

A capacitância é uma propriedade puramente geométrica e material da arrumação dos condutores. Ela quantifica quantos Coulombs de carga a geometria consegue isolar por Volt de pressão elétrica aplicada.

A capacitância **não** depende de $Q$ ou de $V$. Dobrar a tensão aplicada $V$ dobra proporcionalmente a carga armazenada $Q$, mantendo a razão $C = Q / V$ invariante.

### Cancelamento do Campo Elétrico e Efeitos de Borda

Em modelos ideais, o campo elétrico externo produzido por um capacitor é nulo. Um plano infinito isolado de carga gera um campo elétrico uniforme $E = \frac{\sigma}{2\varepsilon_0}$ independente da distância.

Fora da região entre duas placas paralelas carregadas com cargas opostas, o vetor campo elétrico emergente da placa positiva encontra o vetor campo elétrico convergente da placa negativa. Pelo Princípio da Sobreposição, esses vetores de mesma magnitude e direções opostas se anulam:

$$\mathbf{E}_{\text{externo}} = \mathbf{E}_{+} + \mathbf{E}_{-} = \frac{\sigma}{2\varepsilon_0}\hat{\mathbf{n}} - \frac{\sigma}{2\varepsilon_0}\hat{\mathbf{n}} = \mathbf{0}$$

#### Campos de Fuga em Sistemas Reais

Placas reais são finitas. Próximo às bordas físicas dos condutores, a simetria planar se quebra, fazendo com que as linhas de campo elétrico se curvem para o espaço circundante. Essas perturbações de borda são conhecidas como **campos de fuga** (*fringing fields*).

Em aplicações práticas de engenharia, quando a separação $d$ entre as placas é significativamente menor do que as dimensões lineares das placas ($d \ll \sqrt{A}$), os efeitos de borda são desprezíveis, e o modelo idealizado de plano infinito descreve com precisão mais de 99% da física do componente.