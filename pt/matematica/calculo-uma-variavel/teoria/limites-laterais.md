---
id: limites-laterais
title: Limites Laterais
---
# A Geometria da Aproximação Unilateral

Quando examinamos o comportamento de uma função real $f(x)$ nas proximidades de um ponto $a$, a primeira intuição do Cálculo sugere observar a tendência dos valores de $f(x)$ à medida que $x$ se aproxima de $a$. No entanto, a reta real possui uma propriedade topológica fundamental: ela é unidimensional e orientável. Isso significa que existem apenas dois caminhos possíveis para nos aproximarmos de um ponto $a$ ao longo do eixo real: caminhando a partir de valores estritamente maiores do que $a$, ou seja, vindo pela direita; ou caminhando a partir de valores estritamente menores do que $a$, vindo pela esquerda.

Para uma ampla classe de funções elementares — como os polinômios, as funções exponenciais e as funções trigonométricas em seus domínios de definição —, a direção de abordagem não altera o comportamento local da função. A curva é suave e contínua, e o limite quando $x$ tende a $a$ é idêntico não importa a direção escolhida. Contudo, a natureza e a física do mundo real são repletas de fenômenos que exibem mudanças abruptas. Pense na força eletrostática através da superfície de uma esfera carregada, na densidade de um material na interface entre o líquido e o vapor durante uma transição de fase, ou na variação de potencial em um circuito quando uma chave é acionada. 

Nesses cenários, a função que descreve o sistema sofre uma ruptura. Se tentarmos analisar o comportamento global em torno do ponto de transição sem discriminar a direção, a descrição matemática colapsa. É aqui que a ideia de limite lateral se estabelece não como um mero artifício formal, mas como a ferramenta natural para compreender a anatomia das descontinuidades.

Ao investigar a aproximação por um único lado, percebe-se que para uma mesma entrada $a$, a função pode apresentar tendências completamente assimétricas. Se tomarmos valores $x > a$ e os encurtarmos continuamente em direção a $a$, a imagem $f(x)$ pode estabilizar em um valor $L_1$. Se repetirmos o processo tomando valores $x < a$, a imagem $f(x)$ pode tender a um valor inteiramente distinto $L_2$. O estudo dos limites laterais é precisamente a investigação isolada dessas duas tendências direcionais.

---

# Construção Conceitual e Definições Formais

Para construir uma imagem intuitiva precisa do que ocorre em um limite lateral, considere o gráfico de uma função $y = f(x)$ desenhado no plano cartesiano. Imagine que você está rastreando o traçado dessa curva com a ponta de um lápis, movendo-se ao longo do gráfico da direita para a esquerda, em direção à reta vertical $x = a$. Conforme sua coordenada horizontal se aproxima de $a$ (permanecendo sempre no domínio $x > a$), a ponta do seu lápis se aproxima de uma determinada altura no eixo vertical $y$. Essa altura de convergência é o limite lateral à direita.

Se você repetir o experimento, mas desta vez deslizar a ponta do lápis ao longo do gráfico da esquerda para a direita, aproximando-se da mesma reta vertical $x = a$ a partir de valores onde $x < a$, a ponta do lápis poderá convergir para uma altura totalmente diferente. Essa segunda altura é o limite lateral à esquerda. Quando essas duas alturas não coincidem no ponto $a$, o gráfico apresenta uma quebra — uma descontinuidade de salto —, demonstrando que o comportamento da função depende criticamente da direção de onde se vem.

## Limite Lateral à Direita

Dizemos que o limite de $f(x)$ quando $x$ se aproxima de $a$ pela direita é igual a $L_1$, denotado por:

$$\lim_{x \to a^+} f(x) = L_1$$

Se, para todo $\epsilon > 0$, existir um correspondente $\delta > 0$ tal que $|f(x) - L_1| < \epsilon$ sempre que $a < x < a + \delta$. 

A notação $a^+$ especifica que a variável $x$ está restrita ao intervalo aberto $(a, a + \delta)$, garantindo que $x$ seja estritamente maior do que $a$.

## Limite Lateral à Esquerda

Dizemos que o limite de $f(x)$ quando $x$ se aproxima de $a$ pela esquerda é igual a $L_2$, denotado por:

$$\lim_{x \to a^-} f(x) = L_2$$

Se, para todo $\epsilon > 0$, existir um correspondente $\delta > 0$ tal que $|f(x) - L_2| < \epsilon$ sempre que $a - \delta < x < a$.

A notação $a^-$ restringe a variável $x$ ao intervalo aberto $(a - \delta, a)$, impondo que a aproximação ocorra exclusivamente por valores estritamente menores do que $a$.

> [!NOTE]
> É fundamental notar que os sobrescritos $+$ e $-$ não afetam o sinal algébrico do número $a$. A expressão $x \to -5^+$ significa que $x$ se aproxima do número negativo $-5$ por valores à sua direita no eixo real (como $-4,99$), enquanto $x \to 5^-$ indica uma aproximação do número positivo $5$ por valores à sua esquerda (como $4,99$).

# O Teorema Fundamental de Existência do Limite

A conexão fundamental entre os limites laterais e o limite ordinário (bilateral) é estabelecida pelo seguinte teorema:

$$\lim_{x \to a} f(x) = L \iff \lim_{x \to a^-} f(x) = L \quad \text{e} \quad \lim_{x \to a^+} f(x) = L$$

Este resultado afirma que o limite bilateral de $f(x)$ quando $x \to a$ existe e é igual a $L$ se, e somente se, ambos os limites laterais existirem e forem ambos iguais a $L$. 

A consequência lógica imediata deste teorema é que o limite bilateral $\lim_{x \to a} f(x)$ deixa de existir se qualquer uma de duas condições se verificar: ou os limites de cada lado existem mas convergem para valores numéricos diferentes ($\lim_{x \to a^-} f(x) \neq \lim_{x \to a^+} f(x)$), ou pelo menos um dos limites laterais não existe por apresentar comportamento infinito ou oscilatório.


## Exemplo Prático: Analisando Limites Laterais na Prática

Para ilustrar esse comportamento com números, considere a função $f(x)$ definida por:

$$f(x) = \frac{|x - 2|}{x - 2} + 3$$

Vamos analisar o comportamento dessa função ao nos aproximarmos do ponto $a = 2$ por ambos os lados.

### 1. Aproximação pela Direita ($x \to 2^+$)

Escolhemos valores de $x$ estritamente maiores que $2$ ($x > 2$). Como $(x - 2)$ resulta em um valor positivo, o módulo não altera o resultado ($|x - 2| = x - 2$):

* Para $x = 2,1$: 
  $$f(2,1) = \frac{|2,1 - 2|}{2,1 - 2} + 3 = \frac{0,1}{0,1} + 3 = 1 + 3 = 4$$

* Para $x = 2,01$: 
  $$f(2,01) = \frac{|2,01 - 2|}{2,01 - 2} + 3 = \frac{0,01}{0,01} + 3 = 1 + 3 = 4$$

* Para $x = 2,001$: 
  $$f(2,001) = \frac{|2,001 - 2|}{2,001 - 2} + 3 = \frac{0,001}{0,001} + 3 = 1 + 3 = 4$$

Aproximando-se de $2$ pela direita, os valores de $y$ convergem para a altura **$4$**:

$$\lim_{x \to 2^+} f(x) = 4$$

---

### 2. Aproximação pela Esquerda ($x \to 2^-$)

Agora, escolhemos valores de $x$ estritamente menores que $2$ ($x < 2$). Como $(x - 2)$ é um número negativo, o módulo inverte o seu sinal ($|x - 2| = -(x - 2)$):

* Para $x = 1,9$: 
  $$f(1,9) = \frac{|1,9 - 2|}{1,9 - 2} + 3 = \frac{|-0,1|}{-0,1} + 3 = \frac{0,1}{-0,1} + 3 = -1 + 3 = 2$$

* Para $x = 1,99$: 
  $$f(1,99) = \frac{|1,99 - 2|}{1,99 - 2} + 3 = \frac{|-0,01|}{-0,01} + 3 = \frac{0,01}{-0,01} + 3 = -1 + 3 = 2$$

* Para $x = 1,999$: 
  $$f(1,999) = \frac{|1,999 - 2|}{1,999 - 2} + 3 = \frac{|-0,001|}{-0,001} + 3 = \frac{0,001}{-0,001} + 3 = -1 + 3 = 2$$

Aproximando-se de $2$ pela esquerda, os valores de $y$ convergem para a altura **$2$**:

$$\lim_{x \to 2^-} f(x) = 2$$


### Conclusão do Exemplo

Como o limite à direita ($L_1 = 4$) e o limite à esquerda ($L_2 = 2$) chegam a valores completamente diferentes ($4 \neq 2$), o gráfico apresenta um salto no ponto $x = 2$, provando numericamente que **o limite global $\lim_{x \to 2} f(x)$ não existe**.

---

# A Mecânica Operacional da Notação Lateral

Ao realizar manipulações algébricas para avaliar limites laterais, as regras fundamentais da álgebra — como fatoração, cancelamento de fatores comuns, racionalização e simplificação de expressões racionais — permanecem rigorosamente idênticas às empregadas nos limites bilaterais. O símbolo $+$ ou $-$ no limite não altera a estrutura das transformações algébricas equivalentes.

A utilidade operacional da notação lateral manifesta-se no momento de determinar o comportamento de expressões cujo sinal ou definição depende explicitamente da direção da aproximação. Três situações demandam essa atenção especial:

Primeiramente, no estudo de limites infinitos onde a substituição direta produz uma forma da classe $k/0$ (com $k \neq 0$), a notação lateral define o sinal do infinitésimo no denominador. Se $x \to a^+$, analisamos se o denominador se aproxima de zero mantendo valores positivos ($0^+$) ou negativos ($0^-$). Um numerador positivo dividido por $0^+$ resulta em $+\infty$, ao passo que dividido por $0^-$ resulta em $-\infty$.

Em segundo lugar, em expressões que contêm valores absolutos, a definição de módulo $|u| = u$ para $u \ge 0$ e $|u| = -u$ para $u < 0$ exige saber de qual lado de $a$ a variável se encontra. Se temos a expressão $|x - a|$ e o limite especifica $x \to a^+$, então $x - a > 0$, o que nos permite substituir $|x - a|$ diretamente por $(x - a)$. Por outro lado, se o limite especifica $x \to a^-$, então $x - a < 0$, e devemos substituir $|x - a|$ por $-(x - a)$.

Por fim, no manuseio de radicais de índice par, a identidade algébrica fundamental $\sqrt{x^2} = |x|$ revela a necessidade do limite lateral. Ao simplificar a expressão $\sqrt{x^2}/x$ quando $x \to 0^-$, a presença do limite à esquerda determina que $|x| = -x$, conduzindo à razão $-x/x = -1$. Caso a aproximação fosse à direita ($x \to 0^+$), teríamos $|x| = x$, resultando na razão $x/x = 1$.

---

# Exemplos Resolvidos: Limites Laterais

## Padrão 1: Análise de Limites em Funções Definidas por Partes

### Exemplo 1

Considere a função $f(x)$ definida por:

$$f(x) = \begin{cases} x^2, & \text{se } x < 2 \\ x + 1, & \text{se } x = 2 \\ -x^2 + 2x + 4, & \text{se } x > 2 \end{cases}$$

Avalie os seguintes itens:

1. $\lim_{x \to 2^-} f(x)$
    
2. $\lim_{x \to 2^+} f(x)$
    
3. $\lim_{x \to 2} f(x)$
    
4. $f(2)$
    

**Resolução:**

1. **Cálculo do limite lateral à esquerda ($\lim_{x \to 2^-} f(x)$):**
    
    Para $x \to 2^-$, consideram-se apenas valores tais que $x < 2$. A sentença correspondente é $f(x) = x^2$.
    
    $$\lim_{x \to 2^-} f(x) = \lim_{x \to 2^-} x^2 = (2)^2 = 4$$
    
2. **Cálculo do limite lateral à direita ($\lim_{x \to 2^+} f(x)$):**
    
    Para $x \to 2^+$, consideram-se apenas valores tais que $x > 2$. A sentença correspondente é $f(x) = -x^2 + 2x + 4$.
    
    $$\lim_{x \to 2^+} f(x) = \lim_{x \to 2^+} (-x^2 + 2x + 4) = -(2)^2 + 2(2) + 4 = -4 + 4 + 4 = 4$$
    
3. **Análise de existência do limite bilateral ($\lim_{x \to 2} f(x)$):**
    
    Como os limites laterais à esquerda e à direita são iguais ($\lim_{x \to 2^-} f(x) = 4$ e $\lim_{x \to 2^+} f(x) = 4$), conclui-se que o limite bilateral existe e é igual a $4$:
    
    $$\lim_{x \to 2} f(x) = 4$$
    
4. **Determinação do valor da função no ponto ($f(2)$):**
    
    Pela definição da função, para $x = 2$, utiliza-se a sentença $x + 1$:
    
    $$f(2) = 2 + 1 = 3$$
    

_(Nota: Observe que $\lim_{x \to 2} f(x) = 4 \neq f(2) = 3$, o que exemplifica que o valor do limite independe do valor que a função assume exatamente no ponto $x = 2$.)_

## Padrão 2: Análise de Sinal no Denominador ($0^+$ vs $0^-$)

### Exemplo 2

Determine o limite lateral $\lim_{x \to 3^+} \frac{5}{3 - x}$.

**Resolução:**

Ao aplicar a substituição direta, observa-se que o numerador tende à constante $5$ e o denominador tende a $0$. Para determinar o comportamento do limite, analisa-se o sinal do denominador quando $x$ se aproxima de $3$ pela direita ($x > 3$).

Como $x \to 3^+$, assume-se $x > 3$ (por exemplo, $x = 3{,}1$). Logo:

$$3 - x < 0 \implies (3 - x) \to 0^-$$

Substituindo essa análise de sinal no limite:

$$\lim_{x \to 3^+} \frac{5}{3 - x} = \frac{5}{0^-} = -\infty$$

### Exemplo 3

Determine o limite lateral $\lim_{x \to 3^-} \frac{5}{3 - x}$.

**Resolução:**

Para $x \to 3^-$, consideram-se valores à esquerda de $3$, isto é, $x < 3$ (por exemplo, $x = 2{,}9$). Logo:

$$3 - x > 0 \implies (3 - x) \to 0^+$$

Substituindo essa análise de sinal no limite:

$$\lim_{x \to 3^-} \frac{5}{3 - x} = \frac{5}{0^+} = +\infty$$

### Exemplo 4

Determine o limite lateral $\lim_{x \to 0^+} \frac{5}{x^2 - x}$.

**Resolução:**

Fatora-se o denominador para isolar o termo associado à indeterminação:

$$x^2 - x = x(x - 1)$$

Reescrevendo o limite:

$$\lim_{x \to 0^+} \frac{5}{x(x - 1)}$$

Análise dos termos quando $x \to 0^+$ ($x > 0$, com $x$ muito próximo de $0$, como $x = 0{,}1$):

- O numerador permanece $5$.
    
- O fator $x$ tende a $0^+$.
    
- O fator $(x - 1)$ tende a $(0 - 1) = -1$ (um valor negativo).
    

A combinação de sinais no denominador resulta em:

$$x(x - 1) \to (0^+) \cdot (-1) = 0^-$$

Portanto:

$$\lim_{x \to 0^+} \frac{5}{x(x - 1)} = \frac{5}{0^-} = -\infty$$

### Exemplo 5

Determine o limite lateral $\lim_{x \to -1^+} \frac{3x^2 - 4}{1 - x^2}$.

**Resolução:**

Avaliando o numerador quando $x \to -1$:

$$3(-1)^2 - 4 = 3(1) - 4 = -1$$

Fatorando o denominador por diferença de quadrados:

$$1 - x^2 = (1 - x)(1 + x)$$

Quando $x \to -1^+$ ($x > -1$, por exemplo $x = -0{,}9$):

- O fator $(1 - x)$ tende a $1 - (-1) = 2 > 0$.
    
- O fator $(1 + x)$ tende a $1 + (-0{,}9) = 0{,}1 > 0 \implies (1 + x) \to 0^+$.
    

Assim, o denominador se aproxima de:

$$(1 - x)(1 + x) \to (2) \cdot (0^+) = 0^+$$

Substituindo os resultados no limite:

$$\lim_{x \to -1^+} \frac{3x^2 - 4}{1 - x^2} = \frac{-1}{0^+} = -\infty$$

## Padrão 3: Leitura Gráfica de Limites Laterais

### Exemplo 6

Considere uma função $f(x)$ cujo gráfico possui as seguintes características no entorno de $x = -2$:

- Uma curva vinda do quadrante esquerdo que termina em um ponto aberto ("bolinha aberta") na coordenada $(-2, 2)$.
    
- Uma curva que parte da mesma altura $y = 2$ a partir do ponto aberto $(-2, 2)$ em direção à origem $(0,0)$.
    
- Um ponto preenchido ("bolinha cheia") localizado no eixo $x$ na coordenada $(-2, 0)$.
    

Determine:

1. $\lim_{x \to -2^-} f(x)$
    
2. $\lim_{x \to -2^+} f(x)$
    
3. $\lim_{x \to -2} f(x)$
    
4. $f(-2)$
    

**Resolução:**

1. **$\lim_{x \to -2^-} f(x)$:**
    
    Acompanhando o gráfico à esquerda de $x = -2$ ($x < -2$), a curva se aproxima da altura $y = 2$.
    
    $$\lim_{x \to -2^-} f(x) = 2$$
    
2. **$\lim_{x \to -2^+} f(x)$:**
    
    Acompanhando o gráfico à direita de $x = -2$ ($x > -2$), a curva também se aproxima da altura $y = 2$.
    
    $$\lim_{x \to -2^+} f(x) = 2$$
    
3. **$\lim_{x \to -2} f(x)$:**
    
    Como ambos os limites laterais convergem para a mesma altura ($\lim_{x \to -2^-} f(x) = \lim_{x \to -2^+} f(x) = 2$), o limite bilateral existe:
    
    $$\lim_{x \to -2} f(x) = 2$$
    
4. **$f(-2)$:**
    
    O valor da função é dado pela posição da "bolinha cheia" no ponto $x = -2$, localizada na altura $y = 0$.
    
    $$f(-2) = 0$$