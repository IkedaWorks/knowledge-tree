---
id: "ode-separable"
title: "Equações Diferenciais Separáveis"
domain: "math"
module: "ordinary-differential-equations"
type: "method"
schema_version: "2.0"
level: "advanced"
language: "pt"
prerequisites:
  - "ode-fundamental-concepts"
  - "ode-solutions"
tags:
  - "differential-equations"
  - "separable-odes"
  - "integration"
  - "initial-value-problems"
---

# Equações Diferenciais Separáveis

## Motivação e Definição

Uma equação diferencial ordinária de primeira ordem é chamada de **separável** se a taxa de variação $\dfrac{dy}{dx}$ puder ser fatorada como o produto de duas funções distintas: uma que depende exclusivamente da variável independente $x$ e outra que depende exclusivamente da variável dependente $y$.

Forma geral:

$$\dfrac{dy}{dx} = g(x) \cdot h(y)$$

Se $h(y) \neq 0$, podemos isolar todas as instâncias de $y$ e $dy$ do lado esquerdo e todas as instâncias de $x$ e $dx$ do lado direito. Esta manipulação algébrica transforma a equação diferencial em um problema de integração direta de duas variáveis independentes.

---

## Formulação Teórica e Método de Resolução

### Separação de Variáveis

Dividindo ambos os lados por $h(y)$ e multiplicando formalmente pelo diferencial $dx$, obtemos:

$$\frac{1}{h(y)} \, dy = g(x) \, dx$$

Definindo $p(y) = \dfrac{1}{h(y)}$, a equação assume a forma separada clássica:

$$p(y) \, dy = g(x) \, dx$$

### Integração de Ambos os Lados

Aplicando a integração indefinida em ambos os lados em relação às suas respectivas variáveis:

$$\int p(y) \, dy = \int g(x) \, dx + C$$

onde $C$ representa a constante arbitrária de integração que agrupa as constantes de ambas as integrais.

### Obtenção da Solução

A integração resulta em uma relação implícita do tipo $P(y) = G(x) + C$. Quando possível, isolamos a variável $y$ para obter a **solução explícita** $y = \phi(x)$.

---

## Soluções Singulares e Restrições de Domínio

Ao dividir a equação diferencial por $h(y)$, assumimos implicitamente que $h(y) \neq 0$. As raízes constantes da equação $h(y) = 0$ devem ser analisadas separadamente:

- Se $y = y_c$ é um valor constante tal que $h(y_c) = 0$, então a função constante $y(x) = y_c$ é uma **solução de equilíbrio** (ou solução constante) da EDO, pois $\dfrac{dy}{dx} = 0$.
- Se a solução de equilíbrio $y(x) = y_c$ não puder ser obtida atribuindo nenhum valor numérico à constante $C$ na família geral de soluções, ela é chamada de **solução singular**.

---

## Exemplos Resolvidos

### Exemplo: Solução Geral Explícita

Resolva a equação diferencial:

$$\dfrac{dy}{dx} = \frac{x^2}{y}$$

**Resolução:**

**Separação das variáveis:**
Multiplicando ambos os lados por $y$ e por $dx$:

$$y \, dy = x^2 \, dx$$

**Integração de ambos os lados:**

$$\int y \, dy = \int x^2 \, dx$$

$$\frac{y^2}{2} = \frac{x^3}{3} + C_1$$

**Isolamento da variável $y$ (Solução Explícita):**
Multiplicando toda a equação por 2:

$$y^2 = \frac{2}{3}x^3 + 2C_1$$

Renomeando a constante $2C_1$ como $C$:

$$y(x) = \pm \sqrt{\frac{2}{3}x^3 + C}$$

---

### Exemplo: Problema de Valor Inicial (PVI) com Solução Singular
Encontre a solução do PVI:

$$\begin{cases} 
\dfrac{dy}{dx} = 3x^2 y^2 \\ 
y(0) = 1 
\end{cases}$$

**Resolução:**

**Análise de soluções constantes:**
Notamos que $h(y) = y^2$. Se $y = 0$, temos uma solução constante $y(x) = 0$.

**Separação de variáveis para $y \neq 0$:**

$$\frac{1}{y^2} \, dy = 3x^2 \, dx \implies y^{-2} \, dy = 3x^2 \, dx$$

**Integração de ambos os lados:**

$$\int y^{-2} \, dy = \int 3x^2 \, dx$$

$$-\frac{1}{y} = x^3 + C$$

**Isolamento da solução geral:**

$$y(x) = -\frac{1}{x^3 + C}$$

**Aplicação da Condição Inicial $y(0) = 1$:**

$$1 = -\frac{1}{0^3 + C} \implies 1 = -\frac{1}{C} \implies C = -1$$

**Solução Particular Final:**

$$y(x) = \frac{1}{1 - x^3}$$

---

## Aplicações Práticas

### Crescimento e Decaimento Exponencial
Modelos de população não limitada, decaimento radioativo e resfriamento de Newton são descritos por EDOs separáveis da forma $\dfrac{dy}{dt} = k \cdot y$, cuja solução geral é a função exponencial $y(t) = y_0 e^{kt}$.

### Dinâmica de Fluidos (Lei de Torricelli)
O esvaziamento de um reservatório de água por um orifício no fundo é governado pela equação separável $\dfrac{dh}{dt} = -k \sqrt{h}$, onde $h(t)$ representa o nível do fluido em função do tempo.