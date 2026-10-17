---
id: "ode-bernoulli"
title: "Equações Diferenciais de Bernoulli"
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
tags:
  - "differential-equations"
  - "bernoulli-ode"
  - "substitution-method"
  - "linearization"
---

# Equações Diferenciais de Bernoulli

## Estrutura e Forma Padrão

A **Equação Diferencial de Bernoulli** é uma EDO não-linear de primeira ordem cuja forma padrão normalizada é definida por:

$$\frac{dy}{dx} + P(x)y = Q(x)y^n$$

onde $P(x)$ e $Q(x)$ são funções contínuas em um intervalo $I$, e $n \in \mathbb{R}$ é um expoente real constante.

### Identificação Visual e Comparação com a EDO Linear

O lado esquerdo da EDO de Bernoulli ($\frac{dy}{dx} + P(x)y$) é idêntico à forma padrão de uma EDO Linear de 1ª Ordem. A única diferença, e o elemento que quebra a linearidade, é o fator $y^n$ multiplicando o termo independente $Q(x)$ no lado direito.

Em exercícios e exames, este termo muitas vezes aparece escondido por manipulações algébricas prévias (como $y' = x y^{-1} - P(x)y$ ou $x y' + y = x^2 y^2$). Garantir a normalização com o coeficiente de $\frac{dy}{dx}$ igual a 1 é o primeiro passo obrigatório para identificar corretamente $P(x)$, $Q(x)$ e $n$.

### Análise dos Casos Limite

- **Se $n = 0$:** A equação resume-se à forma linear padrão $\dfrac{dy}{dx} + P(x)y = Q(x)$, resolvida diretamente por Fator Integrante.
- **Se $n = 1$:** A equação torna-se separável: $\dfrac{dy}{dx} = [Q(x) - P(x)]y$.
- **Se $n \neq 0$ e $n \neq 1$:** A presença da potência $y^n$ introduz a não-linearidade. No entanto, a equação pode ser linearizada através da substituição $u = y^{1-n}$.

---

## Deduzindo a Mudança de Variável (Linearização)

Para eliminar a potência $y^n$ do lado direito, dividimos toda a equação por $y^n$ (assumindo $y \neq 0$):

$$y^{-n}\frac{dy}{dx} + P(x)y^{1-n} = Q(x)$$

Observando o termo dependente $y^{1-n}$ que acompanha $P(x)$, definimos a nova variável $u(x)$:

$$u = y^{1-n}$$

Derivando $u$ em relação a $x$ usando a Regra da Cadeia:

$$\frac{du}{dx} = (1-n) y^{-n} \frac{dy}{dx} \implies y^{-n} \frac{dy}{dx} = \frac{1}{1-n} \frac{du}{dx}$$

Substituindo essa relação e $u = y^{1-n}$ na EDO transformada:

$$\frac{1}{1-n} \frac{du}{dx} + P(x)u = Q(x)$$

Multiplicando toda a equação pelo fator $(1-n)$, obtemos a **EDO Linear de 1ª Ordem para $u(x)$**:

$$\frac{du}{dx} + (1-n)P(x)u = (1-n)Q(x)$$

Esta equação resultante é resolvida diretamente pelo método do fator integrante. Após determinar $u(x)$, isola-se a solução original $y(x)$:

$$y(x) = \bigl[ u(x) \bigr]^{\frac{1}{1-n}}$$

---

## Algoritmo Prático de Resolução

1. **Normalização Prévia:** Reescreva a EDO isolando $\dfrac{dy}{dx}$ com coeficiente $1$ para obter a forma $\dfrac{dy}{dx} + P(x)y = Q(x)y^n$ e identifique o valor do expoente $n$.
2. **Mudança de Variável:** Defina a substituição $u = y^{1-n}$.
3. **Formulação da EDO Linear:** Monte diretamente a EDO linear equivalente em $u$:
   $$\frac{du}{dx} + (1-n)P(x)u = (1-n)Q(x)$$
4. **Resolução Linear:** Encontre $u(x)$ utilizando o Fator Integrante $\mu(x) = e^{\int (1-n)P(x)dx}$.
5. **Retorno à Variável Original:** Substitua $u = y^{1-n}$ e isole $y(x)$.

---

## Exemplos Resolvidos

### Exemplo 1: Resolução Completa de Bernoulli
Determine a solução geral da equação diferencial:

$$x\frac{dy}{dx} + y = x^2 y^2$$

**Resolução:**

**1. Normalização:**
Dividindo por $x$ (para $x > 0$) para isolar $\dfrac{dy}{dx}$:

$$\frac{dy}{dx} + \frac{1}{x}y = x y^2$$

Identificamos $P(x) = \dfrac{1}{x}$, $Q(x) = x$ e o expoente não-linear $n = 2$.

**2. Substituição:**
Como $n = 2 \implies 1-n = -1$, definimos $u = y^{-1} = \dfrac{1}{y}$.

**3. Montagem da EDO Linear reduzida:**

$$\frac{du}{dx} + (-1)\left(\frac{1}{x}\right) u = (-1)(x) \implies \frac{du}{dx} - \frac{1}{x}u = -x$$

**4. Resolução da EDO Linear em $u(x)$:**
Calculando o fator integrante $\mu(x)$:

$$\mu(x) = e^{\int -\frac{1}{x} dx} = e^{-\ln x} = \frac{1}{x}$$

Multiplicando a EDO por $\mu(x)$:

$$\frac{d}{dx}\left[\frac{1}{x} u\right] = \frac{1}{x}(-x) = -1$$

Integrando ambos os lados:

$$\frac{1}{x} u = \int -1 dx + C = -x + C \implies u(x) = C x - x^2$$

**5. Retorno a $y(x)$:**
Como $u = \dfrac{1}{y}$, invertemos o resultado:

$$y(x) = \frac{1}{Cx - x^2}$$