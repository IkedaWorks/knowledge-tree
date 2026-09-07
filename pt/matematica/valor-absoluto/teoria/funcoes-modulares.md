---
id: funcoes-modulares
title: Funções Modulares
---

# Funções Modulares

Uma função modular é qualquer função $f: \mathbb{R} \to \mathbb{R}$ em que a variável independente $x$ aparece dentro de pelo menos uma expressão em valor absoluto (módulo).

Enquanto funções polinomialmente comuns geram curvas suaves, as funções modulares introduzem **mudanças bruscas de direção ("bicos" ou "vértices")** nos seus pontos críticos, tornando-as objetos fundamentais de estudo na análise real e no cálculo.

---

## O Método Geral Universal: Conversão por Partes

O método geral para esboçar e analisar qualquer função modular consiste em **eliminar as barras de módulo convertendo a função em uma função definida por várias sentenças (função por partes)**.

Lembre-se da regra de definição para o argumento de uma função:

$$|g(x)| = \begin{cases} g(x), & \text{se } g(x) \ge 0 \\ -g(x), & \text{se } g(x) < 0 \end{cases}$$

---

### O Algoritmo de Construção

* **Encontrar os Pontos Críticos:** Resolva $g(x) = 0$ para todas as expressões dentro das barras de módulo.
* **Particionar o Domínio:** Divida a reta real $\mathbb{R}$ nos subintervalos delimitados por esses pontos críticos.
* **Definir os Ramos por Partes:** Avalie o sinal de cada argumento dentro de cada subintervalo e substitua $|g(x)|$ adequadamente.
* **Esboçar e Conectar:** Desenhe as funções locais correspondentes a cada intervalo e conecte-as nos pontos de transição (pontos críticos).

---

### Exemplo Demonstrativo: Soma de Módulos

**Função:** $f(x) = |x - 1| + |x - 3|$

#### Pontos Críticos
* $x - 1 = 0 \implies x = 1$
* $x - 3 = 0 \implies x = 3$

#### Construção por Partes

* **Intervalo I ($x < 1$):**  
  Ambos os termos são negativos:
  $$f(x) = -(x - 1) - (x - 3) = -2x + 4$$

* **Intervalo II ($1 \le x \le 3$):**  
  O primeiro termo é não-negativo, o segundo é não-positivo:
  $$f(x) = (x - 1) - (x - 3) = 2$$

* **Intervalo III ($x > 3$):**  
  Ambos os termos são positivos:
  $$f(x) = (x - 1) + (x - 3) = 2x - 4$$

#### Definição Consolidada por Partes

$$f(x) = \begin{cases} -2x + 4, & \text{se } x < 1 \\ 2, & \text{se } 1 \le x \le 3 \\ 2x - 4, & \text{se } x > 3 \end{cases}$$

> **Resultado Geométrico:** Um gráfico em formato de "banheira" (ou calha) com valor mínimo constante $y = 2$ no intervalo $[1, 3]$.
> * **Domínio:** $\text{Dom}(f) = \mathbb{R}$
> * **Conjunto Imagem:** $\text{Im}(f) = [2, +\infty)$


![Gráfico da função da soma  de módulo](./../../../../assets/funcao-soma-modulos.svg)

---

## Transformações Geométricas (Atalhos Gráficos)

Para funções compostas elementares construídas a partir de um gráfico base conhecido $y = g(x)$, os atalhos de reflexão permitem fazer o esboço rapidamente sem a necessidade de particionar o domínio.

### Caso 1: $y = |g(x)|$ (Reflexão Externa)
Reflete as saídas negativas em relação ao eixo x.

1. Esboce o gráfico padrão de $y = g(x)$.
2. Mantenha inalteradas todas as partes onde $g(x) \ge 0$.
3. **Reflita as partes que estão abaixo do eixo x ($g(x) < 0$) para cima** (espelhamento em relação ao eixo x).

$$\text{Im}(f) \subseteq [0, +\infty)$$

---

### Caso 2: $y = g(|x|)$ (Reflexão Interna)
Força a simetria em relação ao eixo y (cria uma função par: $f(-x) = f(x)$).

1. Esboce o gráfico de $y = g(x)$ apenas para a região $x \ge 0$.
2. Descarte a porção do gráfico onde $x < 0$.
3. **Reflita a parte de $x \ge 0$ para o lado esquerdo em relação ao eixo y** para formar a metade onde $x < 0$.

---

## Casos Exóticos e Pegadinhas

### Pegadinha 1: Não-Diferenciabilidade nos Pontos Críticos ("Bicos")
**Conceito:** As funções modulares são contínuas em todo o conjunto $\mathbb{R}$, mas **não são deriváveis (diferenciáveis)** nos seus pontos críticos.

**Exemplo:** $f(x) = |x|$ em $x = 0$.
* Derivada à esquerda: $\lim_{h \to 0^-} \frac{|0+h| - 0}{h} = \frac{-h}{h} = -1$
* Derivada à direita: $\lim_{h \to 0^+} \frac{|0+h| - 0}{h} = \frac{h}{h} = 1$

Como os limites laterais da taxa de variação não são iguais, a derivada $f'(0)$ não existe. O gráfico apresenta um "bico" pontiagudo em $(0,0)$.

---

### Pegadinha 2: Diferença de Módulos (Imagem Limitada)
**Problema:** Analise o domínio, imagem e esboce $f(x) = |x + 2| - |x - 2|$.

**Resolução via Método Geral:**
Pontos críticos em $x = -2$ e $x = 2$.

* **Intervalo I ($x < -2$):** $f(x) = -(x + 2) - [-(x - 2)] = -x - 2 + x - 2 = -4$
* **Intervalo II ($-2 \le x \le 2$):** $f(x) = (x + 2) - [-(x - 2)] = x + 2 + x - 2 = 2x$
* **Intervalo III ($x > 2$):** $f(x) = (x + 2) - (x - 2) = 4$

$$\text{Definição por Partes: } f(x) = \begin{cases} -4, & \text{se } x < -2 \\ 2x, & \text{se } -2 \le x \le 2 \\ 4, & \text{se } x > 2 \end{cases}$$

> **Conclusão Chave:** Ao contrário da soma de módulos que cresce para $+\infty$, a diferença de módulos gera patamares horizontais (assíntotas horizontais).
> * **Domínio:** $\mathbb{R}$
> * **Imagem:** $\text{Im}(f) = [-4, 4]$

![Função diferença de módulos](./../../../../assets/funcao-diferenca-modulos.svg)
---

### Pegadinha 3: Reflexões Aninhadas $y = ||g(x)| - k|$
**Problema:** Esboce $f(x) = ||x| - 2|$.

**Resolução por Transformações:**
1. Comece com a reta base $y = x$.
2. Aplique a reflexão interna $y = |x|$ (formato de V com vértice na origem).
3. Desloque $2$ unidades para baixo: $y = |x| - 2$ (vértice em $(0, -2)$).
4. Aplique a reflexão externa $y = ||x| - 2|$ (rebate para cima a parte do V invertido que ficou entre $x \in [-2, 2]$).

> **Resultado:** Um gráfico em formato de "W" com mínimos absolutos em $(-2, 0)$ e $(2, 0)$, e um máximo local em $(0, 2)$.
> * **Imagem:** $\text{Im}(f) = [0, +\infty)$

---

## Conclusão: O Método Geral vs. Casos Exóticos

Para provar que a partição de domínio lida com qualquer comportamento contínuo ou não-suave sem depender apenas de intuição geométrica, resolveremos o caso de reflexão aninhada $f(x) = ||x| - 2|$ **puramente por via algébrica usando o Método Geral**.

---

### Pegadinha 3 pelo Método Geral: $f(x) = ||x| - 2|$

Ponto crítico interno: $x = 0$.

* **Ramo I ($x < 0$):**  
  Aqui $|x| = -x \implies f(x) = |-x - 2| = |-(x + 2)| = |x + 2|$.  
  Ponto crítico secundário: $x = -2$.
  * **Sub-intervalo $x < -2$:** $(x + 2) < 0 \implies f(x) = -(x + 2) = -x - 2$
  * **Sub-intervalo $-2 \le x < 0$:** $(x + 2) \ge 0 \implies f(x) = x + 2$

* **Ramo II ($x \ge 0$):**  
  Aqui $|x| = x \implies f(x) = |x - 2|$.  
  Ponto crítico secundário: $x = 2$.
  * **Sub-intervalo $0 \le x < 2$:** $(x - 2) < 0 \implies f(x) = -(x - 2) = -x + 2$
  * **Sub-intervalo $x \ge 2$:** $(x - 2) \ge 0 \implies f(x) = x - 2$

#### Formulação Final por Partes
$$f(x) = \begin{cases} -x - 2, & \text{se } x < -2 \\ x + 2, & \text{se } -2 \le x < 0 \\ -x + 2, & \text{se } 0 \le x < 2 \\ x - 2, & \text{se } x \ge 2 \end{cases}$$

A avaliação dos pontos críticos confirma o formato em W: $f(-2) = 0$, $f(0) = 2$, $f(2) = 0$.