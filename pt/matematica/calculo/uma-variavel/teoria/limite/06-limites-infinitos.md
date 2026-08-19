---
id: limites_infinitos
title: Limites no Infinito e Limites Infinitos
---
# Limites no Infinito e Limites Infinitos

O estudo de limites envolvendo o infinito analisa duas condições fundamentais: a tendência dos valores de saída $f(x)$ quando a variável independente cresce ou decresce sem limite ($x \to \pm\infty$), e o crescimento ilimitado de $f(x)$ quando a entrada se aproxima de um ponto crítico $a$ ($x \to a$).

> [!NOTE]
> 
> Este nó do grafo analisa o comportamento algébrico de funções em regiões de acumulação infinita e em descontinuidades infinitas:
> 
> - As indeterminações do tipo $\frac{\infty}{\infty}$ e $\infty - \infty$ são resolvidas por análise de dominância algébrica.
>     
> - A interpretação geométrica desses resultados em gráficos de funções é abordada no nó **Assíntotas**.
>     
> - Para indeterminações da forma $1^\infty$, consulte o nó **Limites Fundamentais Exponenciais**.
>     

## Limites no Infinito ($x \to \pm\infty$) e Análise de Dominância

Quando a variável $x$ assume valores arbitrariamente grandes em magnitude, a avaliação do limite exige identificar o termo de maior dominância na expressão.

### A Identidade Fundamental do Limite Nulo

Para qualquer constante real $k$ e qualquer expoente racional $n > 0$, o comportamento limite de uma razão cujo denominador cresce sem limite é dado por:

$$\lim_{x \to \pm\infty} \frac{k}{x^n} = 0$$

Essa relação estabelece que a divisão de uma grandeza fixa por uma quantidade infinitamente grande tende a zero.

### Método da Divisão pelo Termo Dominante

A indeterminação do tipo $\frac{\infty}{\infty}$ em funções racionais é resolvida fatorando ou dividindo o numerador e o denominador pela maior potência de $x$ presente no denominador.

Considere a avaliação do limite:

$$\lim_{x \to \infty} \frac{2x^2 + 3}{5x^2 - x}$$

1. **Identificação da Maior Potência do Denominador:**
    
    A maior potência de $x$ no denominador é $x^2$.
    
2. **Normalização da Razão:**
    
    Divide-se cada termo do numerador e do denominador por $x^2$:
    
    $$\lim_{x \to \infty} \frac{\frac{2x^2}{x^2} + \frac{3}{x^2}}{\frac{5x^2}{x^2} - \frac{x}{x^2}} = \lim_{x \to \infty} \frac{2 + \frac{3}{x^2}}{5 - \frac{1}{x}}$$
    
3. **Aplicação das Propriedades de Limite:**
    
    Como $\lim_{x \to \infty} \frac{3}{x^2} = 0$ e $\lim_{x \to \infty} \frac{1}{x} = 0$:
    
    $$\frac{\lim_{x \to \infty} 2 + \lim_{x \to \infty} \frac{3}{x^2}}{\lim_{x \to \infty} 5 - \lim_{x \to \infty} \frac{1}{x}} = \frac{2 + 0}{5 - 0} = \frac{2}{5}$$
    

## Limites Infinitos ($x \to a$) e Análise de Sinal Lateral

Um limite infinito ocorre quando $f(x)$ cresce ou decresce sem limite na vizinhança de um ponto $x = a$. Nesses casos, o denominador aproxima-se de zero enquanto o numerador aproxima-se de uma constante não nula $k \neq 0$.

### A Identidade do Crescimento Ilimitado

Se $k > 0$, o comportamento do limite depende exclusivamente do sinal do denominador ao se aproximar de zero:

$$\lim_{x \to a} \frac{k}{(x - a)^n} = \pm\infty$$

> [!IMPORTANT]
> 
> A expressão $\frac{k}{0}$ (com $k \neq 0$) não é uma indeterminação algébrica. Ela sinaliza uma divergência para $+\infty$ ou $-\infty$. O sinal correto do infinito é determinado estritamente pela análise dos limites laterais.

### Análise de Limites Laterais

Considere a avaliação do limite lateral:

$$\lim_{x \to 2^+} \frac{1}{x - 2}$$

1. **Análise do Comportamento do Denominador:**
    
    Quando $x \to 2^+$, a variável $x$ aproxima-se de $2$ por valores estritamente maiores que $2$ ($x > 2$).
    
2. **Determinação do Sinal da Vizinhança:**
    
    Pela condição $x > 2$, a diferença $(x - 2)$ é estritamente positiva ($x - 2 > 0$). Denota-se que o denominador aproxima-se de zero por valores positivos ($0^+$).
    
3. **Conclusão Formal:**
    
    A razão entre uma constante positiva e uma quantidade infinitesimal positiva resulta em uma divergência positiva:
    
    $$\lim_{x \to 2^+} \frac{1}{x - 2} = +\infty$$
    

Para potências pares no denominador, o termo $(x - a)^n$ assume valores estritamente positivos para todo $x \neq a$, garantindo que $\lim_{x \to a} \frac{1}{(x - a)^n} = +\infty$ para $n$ par, independentemente de a aproximação ocorrer pela esquerda ou pela direita.

## Exemplos Trabalhados e Casos Limite

### Exemplo 1: Dominância com Radicais e Tópico Crítico de Sinal ($x \to -\infty$)

Calcule o limite:

$$\lim_{x \to -\infty} \frac{\sqrt{4x^2 + 1}}{3x - 2}$$

1. **Análise de Dominância:**
    
    Sob o radical, o termo dominante é $x^2$. Como $\sqrt{x^2} = \vert{}x\vert{}$, a expressão comporta-se linearmente no infinito.
    
2. **Fatoração e Extração do Radical:**
    
    Fatoramos $x^2$ dentro da raiz:
    
    $$\sqrt{4x^2 + 1} = \sqrt{x^2 \left(4 + \frac{1}{x^2}\right)} = \vert{}x\vert{} \sqrt{4 + \frac{1}{x^2}}$$
    
3. **Aplicação do Domínio Negativo ($x \to -\infty$):**
    
    Como $x$ assume apenas valores estritamente negativos ($x < 0$), aplica-se a definição $\vert{}x\vert{} = -x$:
    
    $$\lim_{x \to -\infty} \frac{-x \sqrt{4 + \frac{1}{x^2}}}{x \left(3 - \frac{2}{x}\right)}$$
    
4. **Simplificação e Reavaliação:**
    
    Cancelando o fator $x \neq 0$:
    
    $$\lim_{x \to -\infty} \frac{-\sqrt{4 + \frac{1}{x^2}}}{3 - \frac{2}{x}} = \frac{-\sqrt{4 + 0}}{3 - 0} = -\frac{2}{3}$$
    

### Exemplo 2: Limite Infinito Lateral com Fatoração de Polinômio

Calcule o limite lateral:

$$\lim_{x \to 3^-} \frac{2x}{x^2 - 5x + 6}$$

1. **Teste de Substituição Direta:**
    
    A substituição $x = 3$ resulta em $\frac{2(3)}{3^2 - 5(3) + 6} = \frac{6}{0}$, confirmando a divergência infinita.
    
2. **Fatoração do Denominador:**
    
    Fatoramos o quadrático em suas raízes: $x^2 - 5x + 6 = (x - 3)(x - 2)$.
    
    $$\lim_{x \to 3^-} \frac{2x}{(x - 3)(x - 2)}$$
    
3. **Análise do Sinal da Vizinhança ($x \to 3^-$):**
    
    Para $x \to 3^-$, considera-se $x < 3$:
    
    - Numerador: $2x \to 6 > 0$ (positivo).
        
    - Fator $(x - 2) \to (3 - 2) = 1 > 0$ (positivo).
        
    - Fator $(x - 3)$: como $x < 3$, a diferença é estritamente negativa ($x - 3 < 0$), aproximando-se de zero por valores negativos ($0^-$).
        
4. **Conclusão pelo Sinal Resultante:**
    
    O denominador é o produto de um número positivo por um infinitesimal negativo, resultando em $0^-$:
    
    $$\lim_{x \to 3^-} \frac{2x}{(x - 3)(x - 2)} = \frac{+6}{0^-} = -\infty$$