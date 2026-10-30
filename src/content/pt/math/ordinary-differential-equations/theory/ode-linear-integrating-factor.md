---
id: "ode-linear-integrating-factor"
title: "EDOs Lineares de Primeira Ordem e Fator Integrante"
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
  - "linear-odes"
  - "integrating-factor"
  - "product-rule"
---
# EDOs Lineares de Primeira Ordem e Fator Integrante

## Forma Canônica e o Problema da Regra do Produto

Uma equação diferencial ordinária de primeira ordem é dita **linear** se puder ser escrita na seguinte forma canônica:

$$\frac{dy}{dx} + P(x)y = Q(x)$$

onde $P(x)$ e $Q(x)$ são funções contínuas em um intervalo aberto $I$.

Diferente das equações separáveis, o termo aditivo $P(x)y$ impede o isolamento direto das variáveis $x$ e $y$. A resolução fundamenta-se em multiplicar toda a equação por uma função auxiliar $\mu(x) > 0$, denominada **fator integrante**, projetada para transformar o lado esquerdo na derivada exata de um produto.

---

## A Origem do Fator Integrante (Dedução)

Multiplicando a forma canônica por uma função desconhecida $\mu(x)$:

$$\mu(x)\frac{dy}{dx} + \mu(x)P(x)y = \mu(x)Q(x)$$

Pela regra do produto, a derivada de $\mu(x)y$ em relação a $x$ é dada por:

$$\frac{d}{dx}\bigl[\mu(x)y\bigr] = \mu(x)\frac{dy}{dx} + \mu'(x)y$$

Igualando os coeficientes do termo $y$ para que a expressão coincida com o lado esquerdo da EDO:

$$\mu'(x) = \mu(x)P(x)$$

Trata-se de uma EDO separável para $\mu(x)$:

$$\frac{d\mu}{\mu} = P(x)dx \implies \ln|\mu(x)| = \int P(x)dx + C_0$$

Tomando o exponencial em ambos os lados:

$$\mu(x) = e^{\int P(x)dx + C_0} = e^{C_0} \cdot e^{\int P(x)dx} = K e^{\int P(x)dx} \quad (K > 0)$$

Ao substituir $\mu(x)$ na EDO original e isolar $y(x)$, a constante multiplicativa $K$ aparece em todos os termos e se cancela integralmente ao final do processo. Dessa forma, assume-se por conveniência $K = 1$ ($C_0 = 0$), fixando a forma padrão do fator integrante:

$$\mu(x) = e^{\int P(x)dx}$$

Com o fator integrante estabelecido, a EDO linear assume diretamente a forma integrada:

$$\frac{d}{dx}\bigl[\mu(x)y\bigr] = \mu(x)Q(x) \implies \mu(x)y = \int \mu(x)Q(x)dx + C$$

Isolando $y(x)$, obtém-se a **solução geral explícita**:

$$y(x) = \frac{1}{\mu(x)}\left[ \int \mu(x)Q(x)dx + C \right]$$

---

## Algoritmo Prático de Resolução

Na prática operacional, não é necessário replicar o processo de multiplicação termo a termo da dedução. Basta aplicar diretamente a fórmula do fator integrante na equação reduzida:

1. **Normalização:** Escreva a EDO na forma canônica $\dfrac{dy}{dx} + P(x)y = Q(x)$.
2. **Cálculo do Fator Integrante:** Identifique $P(x)$ e calcule $\mu(x) = e^{\int P(x)dx}$ (omitindo a constante de integração nesta etapa, pois $C_0 = 0$).
3. **Aplicação Direta da Fórmula Integrada:** Escreva a igualdade fundamental obtida na dedução:

   $$\mu(x)y = \int \mu(x)Q(x)dx + C$$

4. **Integração do Lado Direito:** Calcule a integral do produto $\mu(x)Q(x)$ (frequentemente requer técnica de integração por partes ou por substituição) e adicione a constante arbitrária de integração $C$.
5. **Isolamento de $y(x)$:** Divida o resultado por $\mu(x)$ para obter a solução geral explícita.

---

## Exemplos Resolvidos

### Exemplo: Solução Geral com Fator Exponencial

Encontre a solução geral da equação diferencial:

$$\frac{dy}{dx} + 2x y = 4x$$

**Resolução:**

**Identificação dos termos:**
A equação já se encontra na forma canônica, com $P(x) = 2x$ e $Q(x) = 4x$.

**Cálculo do fator integrante $\mu(x)$:**

$$\int P(x)dx = \int 2x dx = x^2 \implies \mu(x) = e^{x^2}$$

**Aplicação direta do método:**

$$\mu(x)y = \int \mu(x)Q(x)dx + C \implies e^{x^2}y = \int 4x e^{x^2} dx + C$$

**Resolução da integral:**
Aplicando a substituição $u = x^2$, $du = 2x dx$:

$$e^{x^2}y = 2 e^{x^2} + C$$

**Isolamento da solução geral $y(x)$:**

$$y(x) = 2 + C e^{-x^2}$$

---

### Exemplo: Problema de Valor Inicial (PVI) com Integração por Partes

Resolva o PVI:

$$\begin{cases} 
x\dfrac{dy}{dx} + y = x e^x, \quad x > 0 \\ 
y(1) = 3 
\end{cases}$$

**Resolução:**

**Normalização (divisão por $x$ para $x > 0$):**

$$\frac{dy}{dx} + \frac{1}{x}y = e^x$$

Onde $P(x) = \dfrac{1}{x}$ e $Q(x) = e^x$.

**Cálculo do fator integrante:**

$$\int \frac{1}{x}dx = \ln|x| = \ln x \quad (x > 0) \implies \mu(x) = e^{\ln x} = x$$

**Aplicação direta do método:**

$$x y = \int x e^x dx + C$$

**Integração por partes para $\int x e^x dx$:**
Escolhendo $u = x \implies du = dx$ e $dv = e^x dx \implies v = e^x$:

$$\int x e^x dx = x e^x - \int e^x dx = x e^x - e^x$$

Substituindo de volta:

$$x y = x e^x - e^x + C$$

**Solução geral:**

$$y(x) = e^x - \frac{e^x}{x} + \frac{C}{x}$$

**Aplicação da condição inicial $y(1) = 3$:**

$$3 = e^1 - \frac{e^1}{1} + \frac{C}{1} \implies 3 = e - e + C \implies C = 3$$

**Solução particular final:**

$$y(x) = e^x - \frac{e^x}{x} + \frac{3}{x}$$

---

## Aplicações Práticas

### Circuitos elétricos RL em série
A corrente $i(t)$ em um circuito com resistor $R$ e indutor $L$ alimentado por uma fonte de tensão $V(t)$ obedece à EDO linear $L\dfrac{di}{dt} + Ri = V(t)$, resolvida diretamente pelo fator integrante $\mu(t) = e^{\frac{R}{L}t}$.

### Processos de Mistura (Tanques de Armazenamento)
A quantidade de massa de soluto $y(t)$ em um tanque submetido a fluxos contínuos de entrada e saída é descrita por uma EDO linear de primeira ordem da forma $\dfrac{dy}{dt} + k y = r_{in}$.