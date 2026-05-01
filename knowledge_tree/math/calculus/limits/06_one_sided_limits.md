
# One-Sided Limits: The Consistency Test

**Definição e Intuição:**
Limites laterais são a investigação do comportamento de uma função quando nos aproximamos de um ponto $a$ por apenas um dos lados. É o teste de "concordância" da matemática.

### 🌉 A Intuição da Ponte Rompida (Realidade)
Imagine uma estrada que leva a uma ponte:
* **Cenário A:** Se você vem pela esquerda e a estrada te leva a uma altura de 10 metros, e pela direita ela também te leva a 10 metros, a ponte existe e é contínua naquele ponto.
* **Cenário B:** Se o lado esquerdo te leva a 10 metros e o direito te leva a um abismo de 2 metros, há um salto (**descontinuidade**). Você não tem um "destino único", portanto, não tem um limite global.

---

## 📐 Formalização e Exemplos

Dizemos que o limite lateral existe se a função tende a um valor conforme $x$ se aproxima de $a$ por valores estritamente maiores ($a^+$) ou menores ($a^-$).

### 🏆 O Teorema da Existência
O limite global $\lim_{x \to a} f(x) = L$ só existe se, e somente se:
$$\lim_{x \to a^-} f(x) = \lim_{x \to a^+} f(x) = L$$



### 📝 Exemplo 1: O Salto (Limite Inexistente)
Função: $f(x) = \frac{|x-3|}{x-3}$ no ponto $a = 3$.

1.  **Pela Direita ($3^+$):** Para $x > 3$, o módulo é positivo:
    $$\lim_{x \to 3^+} \frac{x-3}{x-3} = 1$$
2.  **Pela Esquerda ($3^-$):** Para $x < 3$, o módulo inverte o sinal:
    $$\lim_{x \to 3^-} \frac{-(x-3)}{x-3} = -1$$
**Veredito:** Como $1 \neq -1$, o limite $\lim_{x \to 3} f(x)$ **não existe**.



### 📝 Exemplo 2: A Conexão (Limite Existente)
Função definida por partes:

$$ 
f(x) = \begin{cases} 2x + 1, & x < 3 \\ x^2 - 2, & x \ge 3 \end{cases}
$$



1.  **Pela Esquerda ($x \to 3^-$):** Usamos a primeira sentença:
    $$\lim_{x \to 3^-} (2x + 1) = 2(3) + 1 = 7$$
2.  **Pela Direita ($x \to 3^+$):** Usamos a segunda sentença:
    $$\lim_{x \to 3^+} (x^2 - 2) = 3^2 - 2 = 7$$
**Veredito:** Como os dois lados "miram" no 7, o limite global existe e é 7.

---

## 💡 Macetes 

* **O Macete do Expoente:** O sinal de menos ($a^-$) ou mais ($a^+$) no expoente do número não indica o sinal do número, mas a **direção do vento**.
    * $0^-$ significa "venho da esquerda do zero" (ex: $-0,001$).
    * $0^+$ significa "venho da direita do zero" (ex: $0,001$).
* **O Teste do Desenho:** Se você consegue desenhar o gráfico sem tirar o lápis do papel no ponto $a$, os limites laterais com certeza são iguais.

> [!IMPORTANT]
> **Nota de Engenharia:** Limites laterais são usados para descrever interruptores (on/off) e degraus de tensão em circuitos digitais. O momento exato da troca é uma descontinuidade.


### 🔗 Connections
- [09. Continuity of Functions](./09_continuity_of_functions.md)
- [07. Limits at Infinity](./07_Limits_at_Infinity_and_Infinite_Limits.md)