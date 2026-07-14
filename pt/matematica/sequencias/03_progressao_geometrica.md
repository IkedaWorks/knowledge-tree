
# Progressão Geométrica

## Intuição e Definição

Na Progressão Aritmética, exploramos sistemas que evoluem por meio da adição — passos de tamanho estritamente constante. No entanto, muitos fenômenos naturais, financeiros e físicos não crescem somando uma quantia fixa, mas sim **multiplicando** por um fator de escala a cada etapa.

Quando você observa uma população biológica dobrando a cada hora, juros compostos acumulando em um investimento ou uma bola quicando e atingindo uma fração da altura anterior a cada salto, você está diante de uma **Progressão Geométrica (PG)**.

Uma Progressão Geométrica é qualquer sequência numérica na qual a razão entre dois termos consecutivos é constante ao longo de todo o domínio da sequência. Chamamos esse multiplicador constante de **razão** ($q$, do inglês *quotient*).

Formalmente, dizemos que uma sequência $(a_n)$ de termos não nulos é uma Progressão Geométrica se, e somente se, existe um número real $q$ tal que:

$$\frac{a_n}{a_{n-1}} = q \quad \text{para todo } n \ge 2$$

Ou de forma equivalente:

$$a_n = a_{n-1} \cdot q \quad \text{para todo } n \ge 2$$

> [!NOTE]
> **Restrições Importantes:**
> * **$a_1 \neq 0$:** O termo inicial jamais pode ser zero. Caso contrário, todos os termos subsequentes seriam nulos ($0, 0, 0 \dots$), inviabilizando o cálculo da razão ($\frac{0}{0}$).
> * **$q \neq 0$:** A razão jamais pode ser zero, pois geraria uma sequência que perde a reversibilidade e destrói o comportamento exponencial.
---

## Exemplos e Classificação

Diferente da Progressão Aritmética, onde apenas o sinal da razão determina se a sequência cresce ou decresce, o comportamento de uma Progressão Geométrica depende **tanto da razão ($q$) quanto do sinal do termo inicial ($a_1$)**.

### PG Crescente

Cada termo é estritamente maior que o anterior ($a_n > a_{n-1}$). Isso ocorre em dois cenários:
* Termos positivos ($a_1 > 0$) com razão maior que 1 ($q > 1$):  
  $2, 4, 8, 16, 32 \dots$ ($a_1 = 2, q = 2$)
* Termos negativos ($a_1 < 0$) com razão entre 0 e 1 ($0 < q < 1$):  
  $-100, -50, -25, -12.5 \dots$ ($a_1 = -100, q = 0.5$)

### PG Decrescente

Cada termo é estritamente menor que o anterior ($a_n < a_{n-1}$). Isso ocorre em dois cenários:
* Termos positivos ($a_1 > 0$) com razão entre 0 e 1 ($0 < q < 1$):  
  $81, 27, 9, 3, 1 \dots$ ($a_1 = 81, q = \frac{1}{3}$)
* Termos negativos ($a_1 < 0$) com razão maior que 1 ($q > 1$):  
  $-2, -4, -8, -16 \dots$ ($a_1 = -2, q = 2$)

### PG Constante

Todos os termos permanecem idênticos ao longo de toda a sequência ($a_n = a_{n-1}$). Ocorre quando:
* A razão é igual a 1 ($q = 1$):  
  $7, 7, 7, 7 \dots$ ($a_1 = 7, q = 1$)
### PG Alternante (Oscilante)

O sinal dos termos alterna entre positivo e negativo a cada passo. Esse comportamento é exclusivo das Progressões Geométricas e ocorre **sempre que a razão é negativa ($q < 0$)**:
* $3, -6, 12, -24, 48 \dots$ ($a_1 = 3, q = -2$)

---

## O Termo Geral de uma PG

Assim como na PA, calcular um elemento distante dessa sequência  multiplicando repetidamente é ineficiente. Para encontrar qualquer termo em tempo constante, construímos a equação do termo geral observando os passos multiplicativos a partir do ponto de partida ($a_1$).

### A Construção Intuitiva

* Para chegar ao 2º termo: $a_2 = a_1 \cdot q$
* Para chegar ao 3º termo: $a_3 = a_2 \cdot q = (a_1 \cdot q) \cdot q = a_1 \cdot q^2$
* Para chegar ao 4º termo: $a_4 = a_3 \cdot q = (a_1 \cdot q^2) \cdot q = a_1 \cdot q^3$

Notou o padrão? Em vez de multiplicar a razão por $(n-1)$ como fazíamos na adição, nós elevamos a razão à potência de $(n-1)$.

Portanto, para atingir a posição $n$, você precisa aplicar o fator $q$ ao elemento inicial $a_1$ exatamente $(n - 1)$ vezes.

> [!TIP]
> **Visão Chave:** Compare as duas mecânicas fundamentais:
> * **PA (Linear):** $a_n = a_1 + (n - 1)r \implies$ Adição repetida vira **multiplicação**.
> * **PG (Exponencial):** $a_n = a_1 \cdot q^{n-1} \implies$ Multiplicação repetida vira **exponenciação**.

### A Equação

$$a_n = a_1 \cdot q^{n-1}$$

Onde:
* $a_n$: valor do termo na posição $n$.
* $a_1$: primeiro termo da sequência ($a_1 \neq 0$).
* $n$: índice da posição ($n \in \mathbb{N}^*$).
* $q$: razão constante ($q \neq 0$).

---

## A Propriedade Fundamental: Vinculo com a Média Geométrica

Em qualquer Progressão Geométrica finita com termos positivos, **qualquer termo intermediário é a média geométrica entre o seu antecessor e o seu sucessor imediatos**.

Tomando três termos consecutivos $(a_{k-1}, a_k, a_{k+1})$, sabemos por definição que:

$$\frac{a_k}{a_{k-1}} = q \quad \text{e} \quad \frac{a_{k+1}}{a_k} = q$$

Igualando ambas as expressões para $q$:

$$\frac{a_k}{a_{k-1}} = \frac{a_{k+1}}{a_k}$$

Multiplicando cruzado:

$$a_k^2 = a_{k-1} \cdot a_{k+1} \implies a_k = \sqrt{a_{k-1} \cdot a_{k+1}}$$

Assim como na PA, essa propriedade se estende a qualquer par de termos equidistantes do elemento central $a_k$.

---

## Soma dos Primeiros $n$ Termos (PG Finita)

Para calcular a soma acumulada $S_n = a_1 + a_2 + \dots + a_n$ sem somar cada termo individualmente, usamos um truque de eliminação algébrica.

Escreva a soma expandida:

$$S_n = a_1 + a_1 q + a_1 q^2 + \dots + a_1 q^{n-1}$$

Agora, multiplique a equação inteira pela razão $q$:

$$q \cdot S_n = a_1 q + a_1 q^2 + a_1 q^3 + \dots + a_1 q^n$$

Subtraia a primeira equação da segunda ($q \cdot S_n - S_n$). Note como todos os termos intermediários se cancelam:

$$q \cdot S_n - S_n = a_1 q^n - a_1$$

Fatorando $S_n$ do lado esquerdo e $a_1$ do lado direito:

$$S_n(q - 1) = a_1(q^n - 1)$$

Isolando $S_n$ (para $q \neq 1$):

$$S_n = \frac{a_1(q^n - 1)}{q - 1} \quad \text{ou} \quad S_n = \frac{a_1(1 - q^n)}{1 - q}$$

> [!NOTE]
> **Perceba que chegamos em duas versões da mesma equação, elas são equivalentes, você pode testar em alguma pg pequena para confirmar isso. Isso ocorre porque dependendo da equação que você escolheu para subtrair de outra você chega em uma dessas versões. **
> 

---

## Soma de uma PG Infinita (Série Geométrica)

É possível somar infinitos números e obter um resultado finito?

Para entender esse comportamento, a razão precisa estar estritamente contida no intervalo entre $-1$ e $1$, excluindo o zero: **$|q| < 1$ e $q \neq 0$** (ou seja, $q \in ]-1, 1[ \setminus \{0\}$).

Nessas condições, o comportamento da soma depende de onde a razão se encontra:

### Razão Positiva ($0 < q < 1$): O Encolhimento Contínuo

Considere a sequência de quiques de uma bola caindo de 1 metro, depois subindo até $\frac{1}{2}$ metro, depois $\frac{1}{4}$, depois $\frac{1}{8}$, e assim por diante. Todos os termos são positivos, mas encolhem continuamente:

$$S_\infty = 1 + \frac{1}{2} + \frac{1}{4} + \frac{1}{8} + \dots$$

### Razão Negativa ($-1 < q < 0$): A Oscilação Convergente

Considere agora uma PG alternante com $a_1 = 1$ e $q = -0,5$:

$$1, \, -0,5, \, 0,25, \, -0,125, \, 0,0625 \dots$$

À primeira vista, pode parecer estranho somar termos que ficam alternando entre positivo e negativo. Porém, se observarmos as somas parciais passo a passo:
* $S_1 = 1$
* $S_2 = 1 - 0,5 = \mathbf{0,5}$
* $S_3 = 0,5 + 0,25 = \mathbf{0,75}$
* $S_4 = 0,75 - 0,125 = \mathbf{0,625}$
* $S_5 = 0,625 + 0,0625 = \mathbf{0,6875}$

A soma acumulada oscila de um lado para o outro ($1 \to 0,5 \to 0,75 \to 0,625 \to 0,6875$), mas a cada passo o "salto" fica menor e a soma é **espremida em volta de um valor central**.

---

### A Dedução e a Fórmula

Em ambos os cenários (razão positiva ou negativa), conforme o número de termos cresce rumo ao infinito ($n \to \infty$), a potência $q^n$ encolhe em direção a zero ($q^n \to 0$).

Aplicando esse limite na fórmula da soma finita, chegamos à **fórmula da soma infinita** para séries convergentes ($|q| < 1$ e $q \neq 0$):

$$S_\infty = \lim_{n \to \infty} \frac{a_1(1 - q^n)}{1 - q} = \frac{a_1(1 - 0)}{1 - q} \implies S_\infty = \frac{a_1}{1 - q}$$

Aplicando nos nossos dois cenários:

* **No exemplo da bola ($a_1 = 1, q = 0,5$):**
  $$S_\infty = \frac{1}{1 - 0,5} = \frac{1}{0,5} = 2$$
  Infinitos quiques somam uma distância total finita de exatamente **2 metros**.

* **No exemplo alternante ($a_1 = 1, q = -0,5$):**
  $$S_\infty = \frac{1}{1 - (-0,5)} = \frac{1}{1,5} = \frac{2}{3} \approx 0,6666\dots$$
  A oscilação se espreme exatamente ao redor de **$\frac{2}{3}$**.

---

> [!TIP]
> **Ponte com o Cálculo Avançado:**
> A soma de uma PG infinita é o equivalente discreto de uma **Integral Imprópria** ($\int_a^\infty f(x) \, dx$). 
> 
> Enquanto a integral calcula a área contínua sob uma curva que se estende até o infinito, a PG infinita soma blocos individuais de tamanho decrescente. Ambas provam o mesmo fato fascinante: **é possível somar infinitas parcelas e obter um resultado final perfeitamente finito e delimitado** (convergência).