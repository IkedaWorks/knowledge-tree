---
id: "capacitance-derivations"
title: "Dedução Analítica da Capacitância em Geometrias Canônicas"
domain: "physics"
module: "electromagnetism"
type: "method"
schema_version: "2.0"
level: "intermediate"
language: "pt"
prerequisites:
  - "capacitance"
  - "gauss-law"
  - "electric-potential"
tags:
  - "electrostatics"
  - "capacitance"
  - "gauss-law"
  - "analytical-methods"
---
# Dedução Analítica da Capacitância em Geometrias Canônicas

## Declaração do Problema e Condições

O cálculo da capacitância $C$ de um sistema arbitrário de dois condutores exige a determinação do campo elétrico $\mathbf{E}$ gerado por cargas separadas $+Q$ e $-Q$, a integração deste campo para encontrar a diferença de potencial $V$, e a avaliação da razão geométrica $C = Q / V$.

Este protocolo se aplica a geometrias de alta simetria onde a Lei de Gauss fornece facilmente o campo $\mathbf{E}$. As condições de contorno assumem condutores ideais no vácuo ($\varepsilon_0$) com cargas distribuídas uniformemente em suas superfícies.

## Procedimento Algorítmico Passo a Passo

Para deduzir a capacitância de qualquer geometria simétrica de dois condutores, execute o protocolo em três etapas:

1. **Calcular o Campo Elétrico ($\mathbf{E}$):** Defina uma superfície gaussiana adequada passando pela região entre os condutores e aplique a Lei de Gauss:
    
    $$\oint_S \mathbf{E} \cdot d\mathbf{A} = \frac{Q_{\text{envol}}}{\varepsilon_0}$$
    
2. **Calcular a Diferença de Potencial ($V$):** Integre o campo elétrico ao longo de um caminho do condutor positivo ao condutor negativo:
    
    $$V = -\int_{\text{negativo}}^{\text{positivo}} \mathbf{E} \cdot d\mathbf{r} = \int_{a}^{b} E \, dr$$
    
3. **Determinar a Capacitância ($C$):** Substitua o potencial $V$ obtido na relação fundamental:
    
    $$C = \frac{Q}{V}$$
    

## Aplicação Completa Resolvida

### 1. Geometria de Placas Paralelas

Considere duas placas condutoras planas de área $A$ separadas por uma pequena distância $d$, transportando cargas $+Q$ e $-Q$.

![Superfície gaussiana cilíndrica interceptando um condutor de placas paralelas para avaliar o fluxo elétrico.](./../../../../gaussian-surface-parallel.svg)

_Figura 1: Representação em corte transversal de um capacitor de placas paralelas mostrando a superfície gaussiana cilíndrica usada para deduzir o campo elétrico interno uniforme._

#### Execução:

1. **Campo Elétrico via Gauss:** Construa uma superfície gaussiana cilíndrica que intercepta a placa positiva. O fluxo elétrico passa exclusivamente pela face interna de área $A$:
    
    $$E \cdot A = \frac{Q}{\varepsilon_0} \implies E = \frac{Q}{\varepsilon_0 A}$$
    
2. **Diferença de Potencial:** Integre $E$ ao longo do espaçamento uniforme $d$:
    
    $$V = \int_{0}^{d} E \, dx = \left(\frac{Q}{\varepsilon_0 A}\right) d$$
    
3. **Capacitância:**
    
    $$C = \frac{Q}{\left(\frac{Q d}{\varepsilon_0 A}\right)} \implies C = \varepsilon_0 \frac{A}{d}$$
    

### 2. Geometria Cilíndrica (Cabo Coaxial)

Considere um condutor cilíndrico interno de raio $a$ e uma casca cilíndrica condutora externa concêntrica de raio $b$, ambos de comprimento $L$ ($L \gg b$), transportando cargas $+Q$ e $-Q$.

![Modelo 3D isométrico de um capacitor cilíndrico coaxial de comprimento L](./../../../../capacitance-cylindrical-3d.svg)

_Figura 2A: Perspectiva isométrica 3D de um capacitor cilíndrico coaxial destacando as linhas de campo radial e os eixos de simetria._

![Vista em corte transversal de condutores cilíndricos concêntricos com uma superfície gaussiana radial](./../../../../capacitance-cylindrical-crosssection.svg)

_Figura 2B: Corte transversal 2D mostrando a superfície gaussiana de raio $r$ situada estritamente entre o raio interno $a$ e o raio externo $b$._

#### Execução:

1. **Campo Elétrico via Gauss:** Escolha uma superfície gaussiana cilíndrica coaxial de raio $r$ ($a < r < b$) e comprimento $L$:
    
    $$\oint_S \mathbf{E} \cdot d\mathbf{A} = E \cdot (2\pi r L) = \frac{Q}{\varepsilon_0} \implies E = \frac{Q}{2\pi \varepsilon_0 L r}$$
    
2. **Diferença de Potencial:** Integre radialmente de $a$ até $b$:
    
    $$V = \int_{a}^{b} \frac{Q}{2\pi \varepsilon_0 L r} \, dr = \frac{Q}{2\pi \varepsilon_0 L} \ln\left(\frac{b}{a}\right)$$
    
3. **Capacitância:**
    
    $$C = \frac{Q}{\frac{Q}{2\pi \varepsilon_0 L} \ln\left(\frac{b}{a}\right)} \implies C = \frac{2\pi \varepsilon_0 L}{\ln(b/a)}$$
    

### 3. Geometria Esférica

Considere uma esfera condutora maciça interna de raio $a$ cercada por uma casca condutora esférica concêntrica de raio interno $b$, transportando cargas $+Q$ e $-Q$.

![Corte transversal de um capacitor esférico concêntrico ilustrando os raios a e b e o raio gaussiano r.](./../../../../capacitance-spherical-derivation.svg)

_Figura 3: Configuração geométrica de um capacitor esférico exibindo a esfera interna de raio $a$, a casca externa de raio $b$ e a superfície gaussiana concêntrica em $r$._

#### Execução:

1. **Campo Elétrico via Gauss:** Escolha uma superfície gaussiana esférica concêntrica de raio $r$ ($a < r < b$):
    
    $$\oint_S \mathbf{E} \cdot d\mathbf{A} = E \cdot (4\pi r^2) = \frac{Q}{\varepsilon_0} \implies E = \frac{Q}{4\pi \varepsilon_0 r^2}$$
    
2. **Diferença de Potencial:** Integre radialmente de $a$ até $b$:
    
    $$V = \int_{a}^{b} \frac{Q}{4\pi \varepsilon_0 r^2} \, dr = \frac{Q}{4\pi \varepsilon_0} \left( \frac{1}{a} - \frac{1}{b} \right) = \frac{Q}{4\pi \varepsilon_0} \left( \frac{b - a}{a b} \right)$$
    
3. **Capacitância:**
    
    $$C = \frac{Q}{\frac{Q}{4\pi \varepsilon_0} \left( \frac{b - a}{a b} \right)} \implies C = 4\pi \varepsilon_0 \left( \frac{a b}{b - a} \right)$$
    

## Armadilhas Comuns e Casos de Borda

- **Sinais na Integração do Caminho:** Inverter os limites de integração pode introduzir um sinal negativo sem sentido físico para $V$. A capacitância $C$ é estritamente uma grandeza escalar positiva; sempre avalie $V$ como um módulo positivo ($V = \vert{}\Delta V\vert{}$).
    
- **Falha da Aproximação Infinita:** A fórmula de placas paralelas $C = \varepsilon_0 A / d$ assume $d \ll \sqrt{A}$. Quando $d \approx \sqrt{A}$, os efeitos de borda passam a dominar e a capacitância real supera o valor geométrico calculado.
    
- **Condutor Único Isolado:** Para um condutor isolado (ex.: uma esfera isolada de raio $R$), assume-se que o condutor externo reside no infinito ($b \to \infty$). Aplicando este limite ao modelo esférico, obtém-se $C = 4\pi \varepsilon_0 R$.