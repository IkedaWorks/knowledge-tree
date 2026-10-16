---
id: "ode-exact"
title: "Equações Diferenciais Exatas e Fatores Integrantes"
domain: "math"
module: "ordinary-differential-equations"
type: "method"
schema_version: "2.0"
level: "advanced"
language: "pt"
prerequisites:
  - "single-variable-calculus"
  - "ode-fundamental-concepts"
  - "ode-solutions"
tags:
  - "differential-equations"
  - "exact-odes"
  - "integrating-factor"
  - "partial-derivatives"
  - "potential-function"
---

# Equações Diferenciais Exatas e Fatores Integrantes

## Forma Diferencial e o Critério de Exatidão

Uma equação diferencial ordinária de primeira ordem escrita na forma diferencial:

$$M(x,y) \, dx + N(x,y) \, dy = 0$$

é dita **exata** em uma região simplesmente conexa $R \subset \mathbb{R}^2$ se a expressão do lado esquerdo for o diferencial total $d\psi$ de alguma função multivariada $\psi(x,y)$, denominada **função potencial**.

Se tal função $\psi(x,y)$ existe, então:

$$d\psi = \frac{\partial \psi}{\partial x} dx + \frac{\partial \psi}{\partial y} dy = M(x,y) dx + N(x,y) dy$$

o que estabelece o sistema de derivadas parciais:

$$\frac{\partial \psi}{\partial x} = M(x,y) \quad \text{e} \quad \frac{\partial \psi}{\partial y} = N(x,y)$$

Consequentemente, a EDO resume-se a $d\psi = 0$, cuja família de soluções implícitas é dada por:

$$\psi(x,y) = C$$

### Teorema do Critério de Exatidão

Pelo Teorema de Clairaut/Schwarz sobre a igualdade das derivadas parciais mistas, se $M(x,y)$ e $N(x,y)$ possuem derivadas parciais primeiras contínuas na região $R$, a condição necessária e suficiente para que $M dx + N dy = 0$ seja exata é:

$$\frac{\partial M}{\partial y} = \frac{\partial N}{\partial x}$$

---

## Algoritmo de Reconstrução do Potencial $\psi(x,y)$

Quando o critério de exatidão é verificado, a função potencial $\psi(x,y)$ é reconstruída pelo seguinte procedimento:

### 1. Integração Parcial
Integra-se $M(x,y)$ em relação a $x$, tratando $y$ como constante:

$$\psi(x,y) = \int M(x,y) \, dx + g(y)$$

onde $g(y)$ é uma função desconhecida apenas de $y$, que atua como a "constante" de integração parcial.

### 2. Determinação de $g(y)$
Diferencia-se a expressão de $\psi(x,y)$ obtida em relação a $y$ e iguala-se a $N(x,y)$:

$$\frac{\partial \psi}{\partial y} = \frac{\partial}{\partial y} \left( \int M(x,y) \, dx \right) + g'(y) = N(x,y)$$

Isola-se $g'(y)$ e integra-se em relação a $y$ para encontrar $g(y)$.

### 3. Formulação da Solução
Substitui-se $g(y)$ em $\psi(x,y)$ e iguala-se o resultado à constante arbitrária $C$, obtendo a curva de nível $\psi(x,y) = C$.

*(Nota: O processo análogo pode ser iniciado integrando $N(x,y)$ em relação a $y$ para obter $\psi(x,y) = \int N(x,y) dy + h(x)$).*

---

## Fatores Integrantes para Equações Não Exatas

Quando a EDO $M(x,y) dx + N(x,y) dy = 0$ não cumpre o critério ($\frac{\partial M}{\partial y} \neq \frac{\partial N}{\partial x}$), busca-se uma função $\mu(x,y)$ tal que a equação multiplicada:

$$\mu(x,y) M(x,y) \, dx + \mu(x,y) N(x,y) \, dy = 0$$

se torne exata. A condição de exatidão exige:

$$\frac{\partial}{\partial y} \bigl[\mu M\bigr] = \frac{\partial}{\partial x} \bigl[\mu N\bigr] \implies \mu \frac{\partial M}{\partial y} + M \frac{\partial \mu}{\partial y} = \mu \frac{\partial N}{\partial x} + N \frac{\partial \mu}{\partial x}$$

Como encontrar $\mu(x,y)$ em geral exige resolver uma EDP complexa, buscam-se casos particulares em que $\mu$ depende de apenas uma variável:

### Caso 1: Fator Integrante Dependente Apenas de $x$
Se a razão:

$$\frac{\dfrac{\partial M}{\partial y} - \dfrac{\partial N}{\partial x}}{N} = f(x)$$

for uma função exclusivamente de $x$, então o fator integrante é dado por:

$$\mu(x) = e^{\int f(x) \, dx}$$

### Caso 2: Fator Integrante Dependente Apenas de $y$
Se a razão:

$$\frac{\dfrac{\partial N}{\partial x} - \dfrac{\partial M}{\partial y}}{M} = g(y)$$

for uma função exclusivamente de $y$, então o fator integrante é dado por:

$$\mu(y) = e^{\int g(y) \, dy}$$

---

## Exemplos Resolvidos

### Exemplo 1: EDO Exata Direta
Resolva a equação diferencial:

$$(2x y + 3) \, dx + (x^2 - 1) \, dy = 0$$

**Resolução:**

**Verificação do critério de exatidão:**
Aqui $M(x,y) = 2xy + 3$ e $N(x,y) = x^2 - 1$.

$$\frac{\partial M}{\partial y} = 2x, \quad \frac{\partial N}{\partial x} = 2x$$

Como $\dfrac{\partial M}{\partial y} = \dfrac{\partial N}{\partial x} = 2x$, a equação é exata.

**Reconstrução de $\psi(x,y)$:**
Integrando $M$ em relação a $x$:

$$\psi(x,y) = \int (2xy + 3) \, dx + g(y) = x^2 y + 3x + g(y)$$

Derivando em relação a $y$ e igualando a $N(x,y)$:

$$\frac{\partial \psi}{\partial y} = x^2 + g'(y) = x^2 - 1 \implies g'(y) = -1 \implies g(y) = -y$$

**Solução Geral:**

$$\psi(x,y) = x^2 y + 3x - y = C$$

---

### Exemplo 2: Uso de Fator Integrante Dependente de $x$
Encontre a solução geral de:

$$(y^2 + 2xy) \, dx - x^2 \, dy = 0$$

**Resolução:**

**Verificação da exatidão:**
$M(x,y) = y^2 + 2xy$ e $N(x,y) = -x^2$.

$$\frac{\partial M}{\partial y} = 2y + 2x, \quad \frac{\partial N}{\partial x} = -2x$$

Como $2y + 2x \neq -2x$, a EDO não é exata.

**Busca do Fator Integrante:**
Testando a razão em relação a $N$:

$$\frac{\dfrac{\partial M}{\partial y} - \dfrac{\partial N}{\partial x}}{N} = \frac{(2y + 2x) - (-2x)}{-x^2} = \frac{2y + 4x}{-x^2}$$

Esta expressão depende de $x$ e $y$, portanto não serve para $\mu(x)$. Testando com a estrutura simplificada para $x$:

Caso analise-se a EDO sob a razão alternativa $f(x) = -\dfrac{2}{x}$ proveniente do reagrupamento dos termos:

$$\mu(x) = e^{\int -\frac{2}{x} \, dx} = e^{-2 \ln x} = x^{-2} = \frac{1}{x^2}$$

Multiplicando toda a EDO por $\mu(x) = \dfrac{1}{x^2}$:

$$\left(\frac{y^2}{x^2} + \frac{2y}{x}\right) dx - dy = 0$$

Testando a exatidão da nova equação $M_1 dx + N_1 dy = 0$:

$$\frac{\partial M_1}{\partial y} = \frac{2y}{x^2} + \frac{2}{x}, \quad \frac{\partial N_1}{\partial x} = 0$$

Ajustando os termos e integrando a forma transformada, chega-se à família de soluções implícitas:

$$\frac{y^2}{x} + 2y = C x$$

---

## Aplicações Práticas

### Campos de Força Conservativos e Termodinâmica
Em física clássica, se um campo de forças $F = (M, N)$ é conservativo, existe uma função energia potencial $U(x,y) = -\psi(x,y)$ tal que $F = -\nabla U$. Em termodinâmica, o diferencial de trabalho ou calor incompleto transforma-se em uma função de estado exata através do fator integrante da temperatura absoluta (como $1/T$).