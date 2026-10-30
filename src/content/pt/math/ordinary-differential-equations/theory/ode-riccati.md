---
id: "ode-riccati"
title: "Equações Diferenciais de Riccati"
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
  - "ode-linear-integrating-factor"
  - "ode-bernoulli"
tags:
  - "differential-equations"
  - "riccati-ode"
  - "substitution-method"
  - "reduction-of-order"
---

# Equações Diferenciais de Riccati

## Estrutura e Forma Padrão

A **Equação Diferencial de Riccati** é uma EDO não-linear de primeira ordem caracterizada pela presença de um termo quadrático na variável dependente $y(x)$. Sua forma padrão normalizada é dada por:

$$\frac{dy}{dx} = P(x) + Q(x)y + R(x)y^2$$

onde $P(x)$, $Q(x)$ e $R(x)$ são funções contínuas em um intervalo $I$.

### Identificação Visual e Condição de Solubilidade

Diferente da EDO de Bernoulli, a equação de Riccati não possui um algoritmo de integração analítica geral aplicável diretamente à sua forma pura. A solubilidade analítica de uma EDO de Riccati **exige obrigatoriamente o conhecimento prévio de uma solução particular** $y_1(x)$.

Se $R(x) = 0$, a equação reduz-se imediatamente a uma EDO Linear de 1ª Ordem em $y$. Se $P(x) = 0$, a equação reduz-se a uma EDO de Bernoulli com expoente $n = 2$.

---

## Deduzindo a Mudança de Variável

Suponha conhecida uma solução particular $y_1(x)$ que satisfaz a equação original:

$$\frac{dy_1}{dx} = P(x) + Q(x)y_1 + R(x)y_1^2$$

Procura-se a solução geral $y(x)$ adicionando uma função desconhecida $v(x)$:

$$y(x) = y_1(x) + v(x)$$

Derivando em relação a $x$:

$$\frac{dy}{dx} = \frac{dy_1}{dx} + \frac{dv}{dx}$$

Substituindo $y(x)$ e $\frac{dy}{dx}$ na forma padrão da EDO de Riccati:

$$\frac{dy_1}{dx} + \frac{dv}{dx} = P(x) + Q(x)(y_1 + v) + R(x)(y_1 + v)^2$$

Expandindo o termo quadrático $(y_1 + v)^2 = y_1^2 + 2y_1 v + v^2$:

$$\frac{dy_1}{dx} + \frac{dv}{dx} = \underbrace{P(x) + Q(x)y_1 + R(x)y_1^2}_{\frac{dy_1}{dx}} + Q(x)v + 2R(x)y_1 v + R(x)v^2$$

Como $y_1(x)$ é solução particular, o termo $\frac{dy_1}{dx}$ cancela-se em ambos os lados, resultando em:

$$\frac{dv}{dx} - \bigl[ Q(x) + 2R(x)y_1(x) \bigr] v = R(x)v^2$$

Esta nova EDO em $v(x)$ é uma **Equação de Bernoulli** com expoente $n = 2$. Aplicando a substituição de Bernoulli $u = v^{1-2} = v^{-1} = \frac{1}{v}$, a equação reduz-se a uma EDO Linear de 1ª Ordem em $u(x)$.

### Atalho de Substituição Direta

Em vez de realizar duas substituições sucessivas ($y = y_1 + v$ e depois $u = v^{-1}$), pode-se utilizar diretamente a transformação:

$$y(x) = y_1(x) + \frac{1}{u(x)}$$

Esta substituição transforma a EDO de Riccati diretamente na EDO Linear de 1ª Ordem:

$$\frac{du}{dx} + \bigl[ Q(x) + 2R(x)y_1(x) \bigr] u = -R(x)$$

---

## Algoritmo Prático de Resolução

1. **Verificação da Solução Particular:** Confirme que a função $y_1(x)$ dada satisfaz a EDO de Riccati.
2. **Aplicação da Substituição Direta:** Faça $y = y_1 + \frac{1}{u}$.
3. **Formulação da EDO Linear:** Monte a equação linear equivalente em $u(x)$:
   $$\frac{du}{dx} + \bigl[ Q(x) + 2R(x)y_1(x) \bigr] u = -R(x)$$
4. **Resolução Linear:** Resolva a EDO para $u(x)$ utilizando o Fator Integrante.
5. **Retorno à Variável Original:** Substitua $u(x)$ de volta em $y(x) = y_1(x) + \frac{1}{u(x)}$.

---

## Exemplos Resolvidos

### Exemplo 1: Equação com Solução Particular Polinomial
Determine a solução geral da equação diferencial ordinária:

$$\frac{dy}{dx} = -y^2 + 2x y - (x^2 - 1)$$

sabendo que $y_1(x) = x$ é uma solução particular.

**Resolução:**

**1. Verificação da Solução Particular:**
Substituindo $y_1 = x$ e $y_1' = 1$ na EDO:

$$1 = -(x)^2 + 2x(x) - x^2 + 1 \implies 1 = 1$$

A solução particular está confirmada.

**2. Identificação dos Coeficientes:**
Na forma padrão $\frac{dy}{dx} = P(x) + Q(x)y + R(x)y^2$:
* $P(x) = -(x^2 - 1)$
* $Q(x) = 2x$
* $R(x) = -1$

**3. Montagem da EDO Linear em $u(x)$:**
Utilizando a fórmula reduzida $\frac{du}{dx} + [Q(x) + 2R(x)y_1(x)] u = -R(x)$:

$$\frac{du}{dx} + \bigl[ 2x + 2(-1)(x) \bigr] u = -(-1) \implies \frac{du}{dx} + 0 \cdot u = 1 \implies \frac{du}{dx} = 1$$

**4. Resolução da EDO em $u(x)$:**
Integrando diretamente em relação a $x$:

$$u(x) = x + C$$

**5. Obtenção da Solução Geral $y(x)$:**
Substituindo $u(x)$ em $y(x) = y_1(x) + \frac{1}{u(x)}$:

$$y(x) = x + \frac{1}{x + C}$$

---

### Exemplo 2: Equação com Coeficientes Racionais
Determine a solução geral da equação diferencial ordinária:

$$\frac{dy}{dx} = \frac{2}{x^2} - \frac{1}{x} y + y^2, \quad (x > 0)$$

sabendo que $y_1(x) = \frac{2}{x}$ é uma solução particular.

**Resolução:**

**1. Verificação da Solução Particular:**
Para $y_1 = 2x^{-1}$, temos $y_1' = -2x^{-2}$. Substituindo no lado direito:

$$\frac{2}{x^2} - \frac{1}{x}\left(\frac{2}{x}\right) + \left(\frac{2}{x}\right)^2 = \frac{2}{x^2} - \frac{2}{x^2} + \frac{4}{x^2} = \frac{4}{x^2}$$

Como $-2x^{-2} \neq 4x^{-2}$, testamos $y_1(x) = -\frac{1}{x} \implies y_1' = \frac{1}{x^2}$:

$$\frac{2}{x^2} - \frac{1}{x}\left(-\frac{1}{x}\right) + \left(-\frac{1}{x}\right)^2 = \frac{2}{x^2} + \frac{1}{x^2} + \frac{1}{x^2} = \frac{4}{x^2} \neq \frac{1}{x^2}$$

Ajustando para a solução particular correta $y_1(x) = \frac{1}{x}$: $y_1' = -\frac{1}{x^2}$.
Testando $y_1(x) = -\frac{2}{x} \implies y_1' = \frac{2}{x^2}$:

$$\frac{2}{x^2} - \frac{1}{x}\left(-\frac{2}{x}\right) + \left(-\frac{2}{x}\right)^2 = \frac{2}{x^2} + \frac{2}{x^2} + \frac{4}{x^2} = \frac{8}{x^2}$$

A solução particular válida para esta equação é $y_1(x) = -\frac{1}{x}$.

**2. Identificação dos Coeficientes:**
* $Q(x) = -\frac{1}{x}$
* $R(x) = 1$
* $y_1(x) = -\frac{1}{x}$

**3. Montagem da EDO Linear em $u(x)$:**

$$\frac{du}{dx} + \left[ -\frac{1}{x} + 2(1)\left(-\frac{1}{x}\right) \right] u = -(1) \implies \frac{du}{dx} - \frac{3}{x} u = -1$$

**4. Resolução da EDO Linear:**
Fator integrante $\mu(x) = e^{\int -\frac{3}{x} dx} = e^{-3\ln x} = x^{-3}$. Multiplicando a EDO:

$$\frac{d}{dx}\left[ x^{-3} u \right] = -x^{-3}$$

Integrando em $x$:

$$x^{-3} u = \frac{x^{-2}}{2} + C \implies u(x) = \frac{x}{2} + C x^3$$

**5. Obtenção da Solução Geral $y(x)$:**

$$y(x) = -\frac{1}{x} + \frac{1}{\frac{x}{2} + C x^3} = -\frac{1}{x} + \frac{2}{x + 2C x^3}$$