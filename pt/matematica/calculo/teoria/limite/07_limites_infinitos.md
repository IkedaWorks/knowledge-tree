
# Limites no Infinito e Limites Infinitos

Esta nota explora o comportamento das funções nos extremos: quando a entrada  ( $x$ ) cresce sem parar ou quando a saída ( $f(x)$ ) explode para valores imensuráveis.

---

##  As Identidades Fundamentais

Para resolver esses limites de forma rigorosa, baseamo-nos em duas identidades fundamentais:

1. **A Identidade do Horizonte ($x \to \infty$):**
   $$\lim_{x \to \infty} \frac{k}{x^n} = 0$$
   *(Um número fixo **K** dividido por algo que cresce sem parar tende a zero).*

2. **A Identidade da Explosão ($x \to a$):**
   $$\lim_{x \to a} \frac{k}{(x-a)^n} = \pm \infty$$
   *(Um número fixo **k** dividido por algo que diminui até quase zero explode para o infinito).*

---

##  Como Aplicar: Limites no Infinito ($x \to \infty$)

O objetivo aqui é forçar o aparecimento de termos na forma $k/x^n$ para que eles se tornem zero. 

**Algoritmo de Resolução:**
1. Identifique o **maior grau de $x$** presente no denominador.
2. Divida todos os termos do numerador e do denominador por esse valor.

**Exemplo:** Calcule $\lim_{x \to \infty} \frac{2x^2 + 3}{5x^2 - x}$

* **Divisão pelo maior grau ($x^2$):**
  $$\lim_{x \to \infty} \frac{\frac{2x^2}{x^2} + \frac{3}{x^2}}{\frac{5x^2}{x^2} - \frac{x}{x^2}}$$
* **Simplificação:**
  $$\lim_{x \to \infty} \frac{2 + \frac{3}{x^2}}{5 - \frac{1}{x}}$$
* **Aplicação da Identidade:**
  $$\frac{2 + 0}{5 - 0} = \frac{2}{5}$$

---

##  Como Aplicar: Limites Infinitos ($x \to a$)

Neste caso, o $x$ tende a um número real, mas o denominador tende a zero, causando uma divisão por "quase nada".

**Exemplo:** Calcule $\lim_{x \to 2^+} \frac{1}{x-2}$

1. **Análise de Tendência:** Se $x=2$, temos $1/0$, o que indica um resultado infinito ($\infty$).
2. **Análise de Sinal (Lateral):** Como $x \to 2^+$, pegamos valores ligeiramente maiores que 2 (ex: $2.1$, $2.01$).
3. **Formalização:** Se $x > 2$, então $(x-2) > 0$. 
   Logo, $\frac{1}{\text{positivo pequeno}} \to +\infty$.

---

##  Macetes

* **No Infinito ($x \to \infty$):**  Se o resultado deu **0**, é porque sobrou um $x$ no denominador após a simplificação. 
    * Se deu **$\infty$**, é porque sobrou um $x$ no numerador.
* **No Ponto Crítico ($x \to a$):** O limite só resultará em $\pm \infty$ se o numerador **não** for zero. Se for $0/0$, trata-se de uma indeterminação que exige fatoração prévia.
* **A Regra da Potência Par:** $\lim_{x \to a} \frac{1}{(x-a)^n}$ com $n$ par será sempre $+\infty$, independentemente do lado, pois a potência par elimina sinais negativos.



---
> [!IMPORTANT]
> **Definição de Assíntota:** > - Se $\lim_{x \to \pm \infty} f(x) = L$, então $y = L$ é uma **Assíntota Horizontal**.
> - Se $\lim_{x \to a^{\pm}} f(x) = \pm \infty$, então $x = a$ é uma **Assíntota Vertical**.

---
