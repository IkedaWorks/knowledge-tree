---
id: inequacoes-modulares
title: Inequações Modulares
---

# Inequações Modulares

Uma inequação modular é qualquer desigualdade ($\le, <, \ge, >$) em que a incógnita aparece sob a ação de pelo menos um valor absoluto.

A lógica de resolução se divide novamente entre o **Método Geral Universal** (à prova de falhas e derivado da definição) e os **Atalhos Algébricos** para estruturas específicas.

## O Método Geral Universal: Partição de Domínio

O algoritmo para inequações segue os mesmos passos exatos de uma equação modular:

1. **Pontos Críticos:** Encontre as raízes de todas as expressões dentro dos módulos.
    
2. **Partição da Reta Real:** Divida o domínio $\mathbb{R}$ nos subintervalos delimitados por esses pontos.
    
3. **Remoção dos Módulos:** Em cada intervalo, substitua $\vert{}f(x)\vert{}$ por $+f(x)$ ou $-f(x)$ conforme o sinal da expressão nessa região.
    
4. **Resolução e Interseção:** Resolva a inequação simples resultante e faça a interseção da solução com o próprio intervalo:
    
    $$S_i = S_{\text{inequação}} \cap I_i$$
    
5. **União:** A solução final é a união dos resultados de todos os intervalos:
    
    $$S = S_1 \cup S_2 \cup \dots \cup S_n$$
    

### Exemplo Demonstrativo do Método Geral

**Problema:** Resolva $\vert{}x - 1\vert{} + \vert{}x - 3\vert{} < 4$.

#### Pontos Críticos

- $x - 1 = 0 \implies x = 1$
    
- $x - 3 = 0 \implies x = 3$
    

Reta dividida em três regiões: $I_1 = (-\infty, 1)$, $I_2 = [1, 3]$ e $I_3 = (3, +\infty)$.

#### Resolução por Intervalo

- **Intervalo I ($x < 1$):**
    
    Ambos os argumentos são negativos.
    
    $$-(x - 1) - (x - 3) < 4 \implies -2x + 4 < 4 \implies -2x < 0 \implies x > 0$$
    
    **Interseção com $I_1$:** $(x > 0) \cap (x < 1) \implies \mathbf{S_1 = (0, 1)}$.
    
- **Intervalo II ($1 \le x \le 3$):**
    
    Primeiro é positivo, segundo é negativo.
    
    $$(x - 1) - (x - 3) < 4 \implies x - 1 - x + 3 < 4 \implies 2 < 4 \quad \text{(Sempre Verdadeiro!)}$$
    
    **Interseção com $I_2$:** Como a desigualdade é válida para todo o intervalo $\implies \mathbf{S_2 = [1, 3]}$.
    
- **Intervalo III ($x > 3$):**
    
    Ambos os argumentos são positivos.
    
    $$(x - 1) + (x - 3) < 4 \implies 2x - 4 < 4 \implies 2x < 8 \implies x < 4$$
    
    **Interseção com $I_3$:** $(x < 4) \cap (x > 3) \implies \mathbf{S_3 = (3, 4)}$.
    

#### União das Soluções

$$S = S_1 \cup S_2 \cup S_3 = (0, 1) \cup [1, 3] \cup (3, 4) \implies \mathbf{S = (0, 4)}$$

## Atalhos Algébricos Baseados em Propriedades

Para casos com apenas um módulo de um dos lados e uma constante $k > 0$, as propriedades provadas no Módulo 02 reduzem o trabalho drasticamente.

### Caso 1: $\vert{}f(x)\vert{} < k$ (Comprimindo o Intervalo)

Pela interpretação geométrica de distância (o módulo indica pontos cuja distância até a origem é menor que $k$):

$$\vert{}f(x)\vert{} < k \iff -k < f(x) < k$$

_(Válido analogamente para $\le$)._

### Caso 2: $\vert{}f(x)\vert{} > k$ (Expulsando para as Pontas)

Pontos cuja distância até a origem é maior que $k$:

$$\vert{}f(x)\vert{} > k \iff f(x) > k \quad \text{ou} \quad f(x) < -k$$

_(Válido analogamente para $\ge$)._

### Caso 3: $\vert{}f(x)\vert{} < \vert{}g(x)\vert{}$ (Elevando ao Quadrado)

Como ambos os lados são naturalmente não-negativos, elevamos ambos ao quadrado via propriedade da **Potência Par**:

$$\vert{}f(x)\vert{}^2 < \vert{}g(x)\vert{}^2 \iff [f(x)]^2 - [g(x)]^2 < 0$$

$$[f(x) - g(x)][f(x) + g(x)] < 0$$

> **Vantagem:** Evita estudar o sinal de ambos os módulos separadamente.

### Caso 4: Desigualdade Triangular ($\vert{}a + b\vert{} \le \vert{}a\vert{} + \vert{}b\vert{}$)

Lembrando que a desigualdade triangular é **sempre verdadeira** para quaisquer números reais:

- Se a questão pede $\vert{}a + b\vert{} \le \vert{}a\vert{} + \vert{}b\vert{} \implies S = \mathbb{R}$ (se os domínios existirem).
    
- Se pede $\vert{}a + b\vert{} > \vert{}a\vert{} + \vert{}b\vert{} \implies S = \emptyset$ (impossível pela propriedade).
    

## Casos Exóticos e Pegadinhas

### Pegadinha 1: Constante Negativa ($\vert{}f(x)\vert{} \le k$ com $k < 0$)

**Problema:** Resolva $\vert{}3x - 5\vert{} \le -2$.

- **Análise:** Pela propriedade da **Não-Negatividade**, $\vert{}3x - 5\vert{} \ge 0$ para qualquer $x$. Um número nunca pode ser menor ou igual a $-2$.
    
- **Solução:** $S = \emptyset$ em uma única linha, sem cálculo!
    

### Pegadinha 2: Constante Negativa ($\vert{}f(x)\vert{} > k$ com $k < 0$)

**Problema:** Resolva $\vert{}x^2 + 1\vert{} > -5$.

- **Análise:** Como o valor absoluto é sempre $\ge 0$, ele é automaticamente maior do que qualquer número negativo para todo $x \in \mathbb{R}$.
    
- **Solução:** $S = \mathbb{R}$.
    

### Pegadinha 3: Inequações Fracionárias com Módulo no Denominador

**Problema:** Resolva $\dfrac{2}{\vert{}x - 1\vert{}} \ge 1$.

- **Condição de Existência (CE):** O denominador não pode ser zero $\implies x \neq 1$.
    
- Como $\vert{}x - 1\vert{} > 0$ para todo $x \neq 1$, podemos multiplicar ambos os lados pelo denominador **sem inverter a desigualdade**:
    
    $$2 \ge \vert{}x - 1\vert{} \iff \vert{}x - 1\vert{} \le 2$$
    
- Aplicando o Atalho 1 (Caso $\vert{}u\vert{} \le k$):
    
    $$-2 \le x - 1 \le 2 \implies -1 \le x \le 3$$
    
- **Aplicando a CE ($x \neq 1$):**
    
    $$S = [-1, 3] \setminus \{1\} \quad \text{ou} \quad S = [-1, 1) \cup (1, 3]$$