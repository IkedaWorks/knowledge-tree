---
id: equacoes_modulares
title: Equações Modulares
---

# Equações Modulares

Uma equação modular é qualquer equação na qual a incógnita está contida dentro de pelo menos uma expressão em valor absoluto (módulo).

Neste módulo, exploraremos o **Método Geral Universal** — uma técnica de partição de domínio derivada diretamente da definição por partes do valor absoluto —, seguido por **Atalhos Algébricos** que utilizam as propriedades demonstradas no módulo anterior, e concluindo com um conjunto de **Casos Exóticos e Pegadinhas**.

---

## O Método Geral Universal: Partição de Domínio

O método geral não é uma regra arbitrária: **ele é a aplicação direta da definição por partes do valor absoluto na reta real**.

Lembre-se da definição fundamental:

$$|f(x)| = \begin{cases} f(x), & \text{se } f(x) \ge 0 \\ -f(x), & \text{se } f(x) < 0 \end{cases}$$

Quando uma equação contém múltiplos módulos, o comportamento de cada expressão depende do sinal do seu argumento. Ao encontrar onde cada expressão se anula (os pontos críticos), particionamos a reta real $\mathbb{R}$ em subintervalos onde os sinais de todos os argumentos permanecem constantes, permitindo-nos remover as barras de módulo de forma inequívoca.

---

### O Algoritmo de Resolução

* **Identificar os Pontos Críticos:** Encontre as raízes de todas as expressões dentro das barras de módulo (onde $f(x) = 0$).
* **Particionar o Domínio:** Divida a reta real $\mathbb{R}$ em subintervalos delimitados por esses pontos críticos.
* **Avaliar e Remover as Barras por Intervalo:** Substitua cada $|f(x)|$ por $f(x)$ (se $f(x) \ge 0$) ou por $-f(x)$ (se $f(x) < 0$) dentro de cada intervalo específico.
* **Resolver e Validar:** Resolva a equação algébrica resultante para cada intervalo e faça a **interseção** da solução encontrada com esse intervalo ($S_i = S_{\text{equação}} \cap I_i$).
* **União das Soluções:** O conjunto solução final é a união de todas as soluções válidas:
  $$S = S_1 \cup S_2 \cup \dots \cup S_n$$

---

### Exemplo Demonstrativo

**Problema:** Resolva $|x - 2| + |2x + 4| = 6 - x$.

#### Pontos Críticos
* $x - 2 = 0 \implies x = 2$
* $2x + 4 = 0 \implies x = -2$

#### Partição de Domínio
Os pontos críticos $-2$ e $2$ dividem a reta real em três regiões:
* **Intervalo I:** $x < -2$
* **Intervalo II:** $-2 \le x < 2$
* **Intervalo III:** $x \ge 2$

---

#### Resolução por Intervalo

* **Intervalo I ($x < -2$):**  
  Para $x < -2$, temos $(x - 2) < 0 \implies |x - 2| = -(x - 2)$  
  Para $x < -2$, temos $(2x + 4) < 0 \implies |2x + 4| = -(2x + 4)$  
  
  Substituindo na equação:
  $$-(x - 2) - (2x + 4) = 6 - x$$
  $$-3x - 2 = 6 - x \implies -2x = 8 \implies x = -4$$
  
  **Validação:** $x = -4$ pertence ao Intervalo I ($x < -2$)? **Sim.**  
  $\implies S_1 = \{-4\}$

* **Intervalo II ($-2 \le x < 2$):**  
  Para $x < 2$, temos $(x - 2) < 0 \implies |x - 2| = -(x - 2)$  
  Para $x \ge -2$, temos $(2x + 4) \ge 0 \implies |2x + 4| = 2x + 4$  
  
  Substituindo na equação:
  $$-(x - 2) + (2x + 4) = 6 - x$$
  $$x + 6 = 6 - x \implies 2x = 0 \implies x = 0$$
  
  **Validação:** $x = 0$ pertence ao Intervalo II ($-2 \le x < 2$)? **Sim.**  
  $\implies S_2 = \{0\}$

* **Intervalo III ($x \ge 2$):**  
  Para $x \ge 2$, temos $(x - 2) \ge 0 \implies |x - 2| = x - 2$  
  Para $x \ge 2$, temos $(2x + 4) \ge 0 \implies |2x + 4| = 2x + 4$  
  
  Substituindo na equação:
  $$(x - 2) + (2x + 4) = 6 - x$$
  $$3x + 2 = 6 - x \implies 4x = 4 \implies x = 1$$
  
  **Validação:** $x = 1$ pertence ao Intervalo III ($x \ge 2$)? **Não** ($1 < 2$).  
  $\implies S_3 = \emptyset$

---

#### União das Soluções
$$S = S_1 \cup S_2 \cup S_3 = \{-4\} \cup \{0\} \cup \emptyset \implies S = \{-4, 0\}$$

---

## Atalhos Algébricos Baseados em Propriedades

Quando uma equação se encaixa em padrões estruturais específicos, podemos aproveitar propriedades demonstradas para evitar a partição de domínio.

### Caso $|f(x)| = k$ (onde $k \in \mathbb{R}$)
Pelas propriedades de Não-negatividade e Nulidade:
* Se $k < 0 \implies S = \emptyset$
* Se $k = 0 \implies f(x) = 0$
* Se $k > 0 \implies f(x) = k \quad \text{ou} \quad f(x) = -k$

---

### Caso $|f(x)| = g(x)$
Como $|f(x)| \ge 0$, o lado direito também deve ser não-negativo.
1. **Condição de Existência (CE):** $g(x) \ge 0$
2. **Resolução:** $f(x) = g(x) \quad \text{ou} \quad f(x) = -g(x)$
3. **Filtro:** Mantenha apenas as raízes candidatas que satisfaçam a CE.

---

### Igualdade Entre Módulos ($|f(x)| = |g(x)|$)
Pela propriedade da Potência Par ($|a|^2 = a^2$), elevando ambos os lados ao quadrado obtemos:

$$|f(x)|^2 = |g(x)|^2 \implies [f(x)]^2 - [g(x)]^2 = 0$$
$$[f(x) - g(x)][f(x) + g(x)] = 0 \iff f(x) = g(x) \quad \text{ou} \quad f(x) = -g(x)$$

> **Vantagem:** Nenhuma Condição de Existência é necessária, pois ambos os lados são naturalmente não-negativos.

---

### Forma da Desigualdade Triangular ($|a + b| = |a| + |b|$)
Pela propriedade da Condição de Igualdade Triangular:

$$|a + b| = |a| + |b| \iff a \cdot b \ge 0$$

---

## Casos Exóticos e Pegadinhas

### Pegadinha 1: Soluções Extrâneas e Condição de Existência

**Problema:** Resolva $|2x - 3| = x - 3$.

**Resolução:**  
Desmembrar a equação sem testar o lado direito resulta em:
1. $2x - 3 = x - 3 \implies x = 0$
2. $2x - 3 = -(x - 3) \implies 3x = 6 \implies x = 2$

Aplicando a **Condição de Existência (CE)** para $|f(x)| = g(x)$:
$$\text{CE: } g(x) \ge 0 \implies x - 3 \ge 0 \implies x \ge 3$$

**Avaliando os Candidatos:**
* $x = 0$: $0 \ge 3$ é **falso**.
* $x = 2$: $2 \ge 3$ é **falso**.

**Conclusão:** Nenhum dos candidatos é válido.  
$$S = \emptyset$$

---

### Pegadinha 2: Módulos Aninhados (Módulo dentro de Módulo)

**Problema:** Resolva $||x - 3| - 4| = 2$.

**Resolução:**  
Em vez de particionar o domínio imediatamente, aplique a propriedade $|u| = k \implies u = k \text{ ou } u = -k$ ao módulo externo:

Seja $u = |x - 3| - 4$. Como $k = 2 > 0$:

* **Ramo A:**
  $$|x - 3| - 4 = 2 \implies |x - 3| = 6$$
  $$x - 3 = 6 \implies x = 9 \quad \text{ou} \quad x - 3 = -6 \implies x = -3$$

* **Ramo B:**
  $$|x - 3| - 4 = -2 \implies |x - 3| = 2$$
  $$x - 3 = 2 \implies x = 5 \quad \text{ou} \quad x - 3 = -2 \implies x = 1$$

**Conjunto Solução:**
$$S = \{-3, 1, 5, 9\}$$

---

### Pegadinha 3: Equações com Infinitas Soluções (Conjuntos Contínuos)

**Problema:** Resolva $|x - 1| + |x - 5| = 4$.

**Resolução via Igualdade Triangular:**  
Observe que a constante da direita ($4$) é igual a $(x - 1) - (x - 5)$.  
Usando a simetria $|a| = |-a|$, reescreva $|x - 5|$ como $|5 - x|$:

$$|x - 1| + |5 - x| = 4$$

Como $(x - 1) + (5 - x) = 4$, a equação corresponde à forma $|a| + |b| = a + b$.  
A condição necessária e suficiente é $a \cdot b \ge 0$:

$$(x - 1)(5 - x) \ge 0 \iff (x - 1)(x - 5) \le 0$$

Resolvendo a inequação do segundo grau, obtemos:
$$1 \le x \le 5$$

**Conjunto Solução:**
$$S = [1, 5]$$

---

### Pegadinha 4: A Armadilha da Raiz Quadrada do Quadrado

**Problema:** Resolva $\sqrt{x^2 - 6x + 9} + |x - 3| = 8$.

**Resolução:**  
Simplificar $\sqrt{(x-3)^2}$ diretamente para $(x - 3)$ está incorreto.  
Usando a identidade $\sqrt{u^2} = |u|$:

$$\sqrt{x^2 - 6x + 9} = \sqrt{(x - 3)^2} = |x - 3|$$

Substituindo de volta:
$$|x - 3| + |x - 3| = 8 \implies 2|x - 3| = 8 \implies |x - 3| = 4$$

Abrindo o módulo:
* $x - 3 = 4 \implies x = 7$
* $x - 3 = -4 \implies x = -1$

**Conjunto Solução:**
$$S = \{-1, 7\}$$