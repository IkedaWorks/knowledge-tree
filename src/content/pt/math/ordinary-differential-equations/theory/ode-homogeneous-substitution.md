---
id: ode-homogeneous-substitution
title: Equações Diferenciais Homogêneas por Substituição
domain: math
module: ordinary-differential-equations
type: method
schema_version: "2.0"
level: advanced
language: pt
prerequisites:
  - ode-separable
tags:
  - differential-equations
  - homogeneous-substitution
  - separation-of-variables
  - scale-invariance
---

# Equações Diferenciais Homogêneas por Substituição

## O Conceito Rigoroso de Homogeneidade (Simetria de Escala)

Em equações diferenciais, o termo "homogênea" possui significados distintos dependendo do contexto. Enquanto em EDOs lineares de ordem superior o termo se refere à ausência de um termo independente ($L[y] = 0$), no contexto das EDOs de primeira ordem tratadas neste módulo, **homogeneidade é uma propriedade algébrico-geométrica de simetria de escala dos coeficientes**.

### Definição Formal de Função Homogênea

Uma função multivariada $f(x,y)$ é dita **homogênea de grau $k$** se, ao reescalarmos simultaneamente todos os seus argumentos por um fator escalar real $\lambda \neq 0$, a função resultante for multiplicada pelo fator de escala $\lambda^k$:

$$f(\lambda x, \lambda y) = \lambda^k f(x,y)$$

#### O Teste Formal da Constante

Para verificar se uma função é homogênea de grau $k$, aplica-se a substituição $x \to \lambda x$ e $y \to \lambda y$:

* Se for possível isolar $\lambda^k$ como um fator comum global e restaurar a expressão original $f(x,y)$, a função é homogênea de grau $k$.
* Se o termo $\lambda$ permanecer preso dentro de funções transcendentais (como $\sin(\lambda x)$, $e^{\lambda y}$ ou $\ln(\lambda x)$) sem a possibilidade de fatoração, a função **não** é homogênea.

### A EDO na Forma Homogênea

Uma equação diferencial ordinária na forma diferencial:

$$M(x,y) \, dx + N(x,y) \, dy = 0$$

é dita **homogênea** se ambos os coeficientes $M(x,y)$ e $N(x,y)$ forem funções homogêneas de **mesmo grau $k$**.

Alternativamente, ao isolar a derivada $y' = \frac{dy}{dx} = -\frac{M(x,y)}{N(x,y)}$, o quociente de duas funções homogêneas de mesmo grau gera uma função de grau zero ($k - k = 0$). Isso significa que a taxa de variação depende exclusivamente da **razão adimensional** das variáveis:

$$y' = F\left(\frac{y}{x}\right)$$

---

## Comparativo Estrutural: EDO Homogênea vs. EDO Exata

Embora ambas sejam escritas na forma universal $M(x,y) \, dx + N(x,y) \, dy = 0$, as propriedades testadas e as naturezas geométricas são completamente distintas:

* **EDO Exata:** Avalia se $M\,dx + N\,dy$ é o diferencial total $dF$ de uma superfície potencial $z = F(x,y)$. O teste de validação é a simetria de Schwarz ($\frac{\partial M}{\partial y} = \frac{\partial N}{\partial x}$).
* **EDO Homogênea:** Avalia se o campo de direções é invariante por dilatação radial. O teste de validação é a igualdade dos graus de escala de $M$ e $N$ ($M(\lambda x, \lambda y) = \lambda^k M$ e $N(\lambda x, \lambda y) = \lambda^k N$).

---

## Fundamentação Geométrica: Invariância por Dilatação Radial

A fundamentação geométrica das EDOs Homogêneas por Substituição baseia-se na **invariância por escala (simetria de dilatação radial)**.

### Famílias de Soluções e Retas Radiais

Quando $M(x,y)$ e $N(x,y)$ compartilham o mesmo grau de homogeneidade $k$, a inclinação do campo de direções depende exclusivamente da razão das variáveis, e não da distância à origem:

$$y' = -\frac{M(x,y)}{N(x,y)} = F\left(\frac{y}{x}\right)$$

Geometricamente, essa propriedade implica que:

* **Inclinação constante sobre raios:** Ao longo de qualquer reta radial $y = c \cdot x$ que passa pela origem, a razão $y/x = c$ é constante. Assim, todas as curvas integrais que cruzam essa reta possuem exatamente a mesma inclinação naquele ponto de intersecção.
* **Simetria por dilatação:** Se $y = \phi(x)$ é uma curva solução da EDO, qualquer versão reescalada $y = \frac{1}{\lambda} \phi(\lambda x)$ também é uma solução válida. 

A mudança de variável $u = y/x$ desfaz o acoplamento entre $x$ e $y$ justamente porque substitui a coordenada cartesiana $y$ por uma variável $u$ que representa a inclinação do raio polar, transformando a simetria radial em uma equação de variáveis separáveis.

---

## O Algoritmo de Substituição e Redução de Ordem

A estratégia para resolver uma EDO Homogênea consiste em transformá-la em uma **EDO de Variáveis Separáveis** através da substituição $y = u \cdot x$.

### Derivação do Diferencial da Substituição

Considerando $u = u(x)$ como uma nova função dependente de $x$, aplica-se a **Regra do Produto** para obter o diferencial total:

$$dy = d(u \cdot x) = u \, dx + x \, du$$

### Passos da Resolução

* **Substituição dos Termos:** Substitui-se $y$ por $u \cdot x$ e $dy$ por $u \, dx + x \, du$ na EDO original.
* **Fatoração e Cancelamento do Grau $k$:** O termo $x^k$ fatora-se universalmente em ambos os coeficientes e cancela-se.
* **Agrupamento de Termos Semelhantes:** Reagrupam-se os termos em $dx$ e $du$.
* **Separação de Variáveis:** Isola-se a variável $u$ de um lado e $x$ do outro.
* **Integração e Retorno à Variável Original:** Integra-se ambos os lados e substitui-se $u = \frac{y}{x}$.

---

## Exemplos Resolvidos

### Exemplo: Resolução de EDO Homogênea de Grau 2

Determine a solução geral da equação diferencial ordinária:

$$(x^2 + y^2) \, dx - 2xy \, dy = 0$$

**Resolução:**

#### Verificação do Grau de Homogeneidade
* $M(x,y) = x^2 + y^2 \implies M(\lambda x, \lambda y) = \lambda^2 x^2 + \lambda^2 y^2 = \lambda^2 M(x,y)$ (Grau 2).
* $N(x,y) = -2xy \implies N(\lambda x, \lambda y) = -2(\lambda x)(\lambda y) = \lambda^2 (-2xy) = \lambda^2 N(x,y)$ (Grau 2).

Como ambos são homogêneos de grau $k = 2$, a EDO é homogênea por substituição (embora $\frac{\partial M}{\partial y} = 2y \neq -2y = \frac{\partial N}{\partial x}$, provando que não é exata).

#### Aplicação da Substituição
Aplica-se $y = u \cdot x$ e $dy = u \, dx + x \, du$:

$$(x^2 + (ux)^2) \, dx - 2x(ux) (u \, dx + x \, du) = 0$$

$$(x^2 + u^2 x^2) \, dx - 2u x^2 (u \, dx + x \, du) = 0$$

Fatorando $x^2$:

$$x^2 \left[ (1 + u^2) \, dx - 2u (u \, dx + x \, du) \right] = 0$$

Dividindo por $x^2$ ($x \neq 0$):

$$(1 + u^2) \, dx - 2u^2 \, dx - 2u x \, du = 0$$

$$(1 - u^2) \, dx - 2u x \, du = 0$$

#### Separação de Variáveis

$$\frac{1}{x} \, dx = \frac{2u}{1 - u^2} \, du$$

#### Integração de Ambos os Lados

$$\int \frac{1}{x} \, dx = \int \frac{2u}{1 - u^2} \, du$$

$$\ln|x| = -\ln|1 - u^2| + C_1 \implies \ln|x(1 - u^2)| = C_1$$

$$x(1 - u^2) = C$$

#### Retorno à Variável Original ($u = y/x$)

$$x \left( 1 - \frac{y^2}{x^2} \right) = C \implies x^2 - y^2 = C x$$