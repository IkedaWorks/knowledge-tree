---
id: propriedades_modulo
title: Propriedades do Módulo
---
# Propriedades do Valor Absoluto

Após definir o módulo como a distância geométrica até a origem e formalizá-lo por partes, podemos derivar suas propriedades fundamentais. Nenhuma dessas propriedades nasce do nada: todas são consequências diretas da própria definição algébrica.

---

## Visão Geral das Propriedades

Para quaisquer números reais $x, y \in \mathbb{R}$:

* **Não-negatividade:** $|x| \ge 0$  
  Como o módulo representa uma distância física, seu valor nunca pode ser negativo.

* **Nulidade:** $|x| = 0 \iff x = 0$  
  A única distância igual a zero ocorre na própria origem.

* **Simetria:** $|-x| = |x|$ e $|a - b| = |b - a|$  
  A distância de um ponto até a origem (ou entre dois pontos) não depende da direção.

* **Multiplicatividade:** $|x \cdot y| = |x| \cdot |y|$  
  O módulo do produto é o produto dos módulos.

* **Divisibilidade:** $\left|\dfrac{x}{y}\right| = \dfrac{|x|}{|y|}$ (com $y \neq 0$)  
  O módulo da divisão é a divisão dos módulos.

* **Identidade com Potência Par:** $\sqrt{x^2} = |x|$  
  A raiz quadrada principal de um número elevado ao quadrado sempre resulta no seu valor absoluto.

* **Limitação:** $-|x| \le x \le |x|$  
  Qualquer número real $x$ é limitado inferiormente pelo oposto do seu módulo e superiormente pelo seu próprio módulo.

* **Idempotência e Potência Par:** $||x|| = |x|$ e $|x^2| = x^2 = |x|^2$  
  Aplicar o módulo múltiplas vezes é redundante, e elevar ao quadrado elimina a necessidade das barras modulares.

* **Propriedades de Inequação Modular (para $k > 0$):**  
  * $|x| \le k \iff -k \le x \le k$ (define um intervalo limitado em torno do zero).  
  * $|x| \ge k \iff x \le -k \text{ ou } x \ge k$ (define as regiões fora do intervalo).

* **Desigualdade Triangular:** $|x + y| \le |x| + |y|$  
  A soma dos módulos é sempre maior ou igual ao módulo da soma.

* **Desigualdade Triangular Inversa:** $||x| - |y|| \le |x - y|$  
  A diferença entre os módulos de dois números nunca supera o módulo da diferença entre eles.

---

## Demonstrações Baseadas na Definição

Para provar qualquer propriedade sem incorrer em raciocínio circular, recorremos **apenas** à definição elementar:

$$|x| = \begin{cases} x, & \text{se } x \ge 0 \\ -x, & \text{se } x < 0 \end{cases}$$

---

### Simetria ($|-x| = |x|$)

Queremos provar que o módulo de um número e o módulo do seu oposto produzem o mesmo resultado.

* **Caso 1 ($x \ge 0$):**  
  Pela definição, $|x| = x$.  
  Se $x \ge 0$, então seu oposto $-x \le 0$.  
  * Se $x = 0$, temos $|0| = 0$ e $|-0| = 0$, logo $|-x| = |x|$.  
  * Se $x > 0$, então $-x < 0$. Pela definição, aplicamos a inversão de sinal:  
    $$|-x| = -(-x) = x$$  
  Como $|x| = x$ e $|-x| = x$, concluímos que $|-x| = |x|$.

* **Caso 2 ($x < 0$):**  
  Pela definição, $|x| = -x$.  
  Se $x < 0$, multiplicando por $-1$ temos que seu oposto é positivo ($-x > 0$).  
  Aplicando a definição ao argumento $(-x)$, como ele é positivo, o valor é mantido:  
    $$|-x| = -x$$  
  Como $|x| = -x$ e $|-x| = -x$, concluímos que $|-x| = |x|$. $\blacksquare$

---

### Multiplicatividade ($|x \cdot y| = |x| \cdot |y|$)

Dividimos a análise no sinal do produto $x \cdot y$:

* **Caso 1 ($x \cdot y \ge 0$):**  
  Se o produto é não-negativo, pela definição de módulo temos:
  $$|x \cdot y| = x \cdot y$$
  Analisamos os fatores individuais:
  * Se $x \ge 0$ e $y \ge 0$, temos $|x| = x$ e $|y| = y$. Logo, $|x| \cdot |y| = x \cdot y$.
  * Se $x \le 0$ e $y \le 0$, temos $|x| = -x$ e $|y| = -y$. Logo, $|x| \cdot |y| = (-x)(-y) = x \cdot y$.  
  Em ambos os subcasos, $|x \cdot y| = |x| \cdot |y|$.

* **Caso 2 ($x \cdot y < 0$):**  
  Se o produto é negativo, pela definição aplicamos a inversão de sinal:
  $$|x \cdot y| = -(x \cdot y)$$
  Como o produto é negativo, os fatores têm sinais opostos. Sem perda de generalidade, assuma $x > 0$ e $y < 0$:
  * Como $x > 0$, pela definição $|x| = x$.
  * Como $y < 0$, pela definição $|y| = -y$.  
  Multiplicando os módulos:
  $$|x| \cdot |y| = x \cdot (-y) = -(x \cdot y)$$
  Como $|x \cdot y| = -(x \cdot y)$ e $|x| \cdot |y| = -(x \cdot y)$, concluímos que $|x \cdot y| = |x| \cdot |y|$. $\blacksquare$

---

### Divisibilidade ($\left|\dfrac{x}{y}\right| = \dfrac{|x|}{|y|}$)

Para $y \neq 0$, provamos primeiro que $\left|\dfrac{1}{y}\right| = \dfrac{1}{|y|}$:

Pela propriedade da multiplicatividade:
$$|y| \cdot \left|\frac{1}{y}\right| = \left|y \cdot \frac{1}{y}\right| = |1| = 1$$

Isolando $\left|\dfrac{1}{y}\right|$:
$$\left|\frac{1}{y}\right| = \frac{1}{|y|}$$

Agora, reescrevemos a fração $\dfrac{x}{y}$ como um produto $x \cdot \dfrac{1}{y}$:
$$\left|\frac{x}{y}\right| = \left|x \cdot \frac{1}{y}\right| = |x| \cdot \left|\frac{1}{y}\right| = |x| \cdot \frac{1}{|y|} = \frac{|x|}{|y|} \quad \blacksquare$$

---

### A Identidade $\sqrt{x^2} = |x|$

> [!warning] Erro Comum
> A expressão $\sqrt{x^2}$ **não** é simplesmente $x$. O radical $\sqrt{\phantom{x}}$ indica por convenção a raiz quadrada **não-negativa**.

Analisando a operação $\sqrt{x^2}$:

* **Se $x \ge 0$:** O valor $x^2$ é não-negativo e sua raiz positiva é o próprio $x$. Como $|x| = x$, temos $\sqrt{x^2} = |x|$.
* **Se $x < 0$:** O valor $x^2$ continua sendo positivo, mas sua raiz positiva será o oposto de $x$ (isto é, $-x$). Como para $x < 0$ a definição nos dá $|x| = -x$, temos novamente $\sqrt{x^2} = |x|$.

---

### Propriedades de Inequação Modular ($|x| \le k$)

Para uma constante real $k > 0$:

$$|x| \le k \iff -k \le x \le k$$

*Demonstração:*  
* **Pela esquerda ($\implies$):**  
  Se $|x| \le k$, então:
  * Se $x \ge 0$, temos $|x| = x \le k$. Como $k > 0$, também vale $-k < 0 \le x$, logo $-k \le x \le k$.
  * Se $x < 0$, temos $|x| = -x \le k$. Multiplicando por $-1$, invertemos a desigualdade: $x \ge -k$. Como $x < 0 < k$, unindo as partes temos $-k \le x \le k$.

* **Pela direita ($\impliedby$):**  
  Se $-k \le x \le k$, temos duas condições simultâneas: $x \le k$ e $x \ge -k \implies -x \le k$.  
  Pela definição de $|x|$, como $|x|$ é igual a $x$ ou a $-x$, e ambos são $\le k$, conclui-se que $|x| \le k$. $\blacksquare$

---

### Desigualdade Triangular ($|x + y| \le |x| + |y|$)

Aplicamos a propriedade da limitação a $x$ e $y$:

$$-|x| \le x \le |x|$$
$$-|y| \le y \le |y|$$

Somando as duas desigualdades termo a termo:

$$-(|x| + |y|) \le x + y \le (|x| + |y|)$$

Como a expressão $x + y$ está presa entre $-k$ e $+k$ (com $k = |x| + |y|$), pela propriedade das inequações modulares provada acima, isso é equivalente a:

$$|x + y| \le |x| + |y| \quad \blacksquare$$

---

### Condição de Igualdade da Desigualdade Triangular ($|a + b| = |a| + |b| \iff a \cdot b \ge 0$)

Elevando ambos os lados ao quadrado:

$$|a + b|^2 = (|a| + |b|)^2$$

Usando $|x|^2 = x^2$ e expandindo o produto notável:

$$(a + b)^2 = |a|^2 + 2|a||b| + |b|^2$$
$$a^2 + 2ab + b^2 = a^2 + 2|a \cdot b| + b^2$$

Subtraindo $a^2 + b^2$ de ambos os lados:

$$2ab = 2|a \cdot b| \implies ab = |a \cdot b|$$

Pela definição, a igualdade $x = |x|$ só ocorre se $x \ge 0$.  
Logo, $ab = |ab|$ se e somente se:

$$a \cdot b \ge 0 \quad \blacksquare$$

---

### Idempotência ($||x|| = |x|$)

Seja $y = |x|$.  
Pela propriedade da não-negatividade, $y \ge 0$.  
Aplicando a definição de módulo para um argumento não-negativo:

$$|y| = y \implies ||x|| = |x| \quad \blacksquare$$

---

### Potência Par ($|x^2| = x^2 = |x|^2$)

1. **Provando $|x^2| = x^2$:**  
   Como $x^2 \ge 0$ para todo $x \in \mathbb{R}$, pela definição de argumento não-negativo, $|x^2| = x^2$.

2. **Provando $|x|^2 = x^2$:**  
   * Se $x \ge 0$: $|x| = x \implies |x|^2 = x^2$.
   * Se $x < 0$: $|x| = -x \implies |x|^2 = (-x)^2 = x^2$.

Conclusão: $|x^2| = x^2 = |x|^2$. $\blacksquare$