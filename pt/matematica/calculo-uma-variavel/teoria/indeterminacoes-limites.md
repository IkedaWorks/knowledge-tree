---
id: indeterminacoes-limites
title: Indeterminações em Limites
---
# Indeterminações em Limites e Técnicas Algébricas

Ao aplicar as propriedades operacionais dos limites, a avaliação direta por substituição simples em uma função pode resultar em uma expressão cujo valor numérico não pode ser determinado de imediato. Essa ocorrência é denominada indeterminação matemática.

Uma indeterminação não indica que o limite não existe ou que o problema é insolúvel. Ela representa apenas a falha do método de substituição direta, sinalizando que a função precisa ser reescrita de forma algebricamente equivalente em uma vizinhança do ponto para revelar o seu verdadeiro comportamento limite.

> [!NOTE]
> 
> Este nó do grafo foca estritamente na indeterminação algébrica local da forma $\frac{0}{0}$ e em suas técnicas de resolução por fatoração e racionalização. Outras formas indeterminadas são analisadas em nós específicos:
> 
> - Formas $\frac{\infty}{\infty}$ e $\infty - \infty$: desenvolvidas no nó **Limites Infinitos e Assíntotas**.
>     
> - Forma $1^\infty$: desenvolvida no nó **Limites Fundamentais Exponenciais**.
>     
> - Formas $0^0$, $\infty^0$ e $0 \cdot \infty$: desenvolvidas no módulo de **Derivadas** via Regra de L'Hôpital.
>     

## O Diagnóstico da Forma Indeterminada $\frac{0}{0}$

No estudo de limites locais, a forma indeterminada mais fundamental ocorre na razão de duas funções quando a substituição direta $x = a$ resulta em:

$$\lim_{x \to a} \frac{f(x)}{g(x)} = \frac{0}{0}$$

Essa expressão indica que tanto o numerador $f(x)$ quanto o denominador $g(g)$ aproximam-se de zero simultaneamente quando $x$ tende a $a$.

> [!IMPORTANT]
> 
> A expressão $\frac{0}{0}$ não é um número real, nem equivale a $1$ ou $0$. Ela representa uma taxa limite entre duas grandezas infinitesimais. O valor do limite depende de qual das duas funções se aproxima do zero com maior velocidade na vizinhança de $a$.

Como a definição formal de limite analisa estritamente os pontos do domínio onde $x \neq a$, podemos manipular algebricamente a função para eliminar os fatores responsáveis pelo anulamento simultâneo antes de reavaliar o limite.

## Resolução via Fatoração Polinomial

Quando $f(x)$ e $g(x)$ são polinômios e a substituição direta em $x = a$ resulta na indeterminação $\frac{0}{0}$, o Teorema do Resto garante que o termo $(x - a)$ é um fator comum de ambos os polinômios.

Essa propriedade permite fatorar o numerador e o denominador para simplificar o termo crítico $(x - a)$, uma operação perfeitamente válida para todo $x \neq a$.

### Aplicação Prática: Fatoração de Polinômios

Considere a avaliação do limite abaixo:

$$\lim_{x \to 2} \frac{x^2 - 4}{x^2 - 3x + 2}$$

1. **Teste de Substituição Direta:**
    
    Ao substituir $x = 2$, obtemos $\frac{2^2 - 4}{2^2 - 3(2) + 2} = \frac{0}{0}$, confirmando a indeterminação.
    
2. **Fatoração dos Termos:**
    
    Fatoramos o numerador por diferença de quadrados e o denominador pela identificação de suas raízes:
    
    $$x^2 - 4 = (x - 2)(x + 2)$$
    
    $$x^2 - 3x + 2 = (x - 2)(x - 1)$$
    
3. **Cancelamento do Fator Crítico:**
    
    Como a condição $x \to 2$ estabelece que $x \neq 2$, a divisão pelo termo $(x - 2)$ é algebricamente válida:
    
    $$\lim_{x \to 2} \frac{(x - 2)(x + 2)}{(x - 2)(x - 1)} = \lim_{x \to 2} \frac{x + 2}{x - 1}$$
    
4. **Reavaliação do Limite:**
    
    Aplicando a substituição direta na expressão simplificada:
    
    $$\lim_{x \to 2} \frac{x + 2}{x - 1} = \frac{2 + 2}{2 - 1} = 4$$
    

## Resolução via Racionalização de Radicais

A indeterminação $\frac{0}{0}$ também surge frequentemente em expressões irracionais que contêm radicais no numerador ou no denominador. Nestes casos, a fatoração por inspeção direta não é aplicável.

A técnica de racionalização consiste em multiplicar o numerador e o denominador pelo conjugado da expressão radical. Esse procedimento utiliza a identidade da diferença de quadrados, $(A - B)(A + B) = A^2 - B^2$, para eliminar o radical e expor o fator crítico responsável pela indeterminação.

### Aplicação Prática: Racionalização com Conjugado

Considere a avaliação do limite abaixo:

$$\lim_{x \to 0} \frac{\sqrt{x + 9} - 3}{x}$$

1. **Teste de Substituição Direta:**
    
    Ao substituir $x = 0$, obtemos $\frac{\sqrt{0 + 9} - 3}{0} = \frac{0}{0}$.
    
2. **Multiplicação pelo Conjugado:**
    
    O conjugado da expressão do numerador $(\sqrt{x + 9} - 3)$ é $(\sqrt{x + 9} + 3)$. Multiplicamos o numerador e o denominador por esse termo:
    
    $$\lim_{x \to 0} \left( \frac{\sqrt{x + 9} - 3}{x} \cdot \frac{\sqrt{x + 9} + 3}{\sqrt{x + 9} + 3} \right)$$
    
3. **Desenvolvimento Algébrico:**
    
    Aplicando o produto notável no numerador:
    
    $$\lim_{x \to 0} \frac{(\sqrt{x + 9})^2 - (3)^2}{x(\sqrt{x + 9} + 3)} = \lim_{x \to 0} \frac{(x + 9) - 9}{x(\sqrt{x + 9} + 3)} = \lim_{x \to 0} \frac{x}{x(\sqrt{x + 9} + 3)}$$
    
4. **Cancelamento do Fator Crítico e Avaliação Final:**
    
    Simplificando o fator $x$ para a condição $x \neq 0$:
    
    $$\lim_{x \to 0} \frac{1}{\sqrt{x + 9} + 3} = \frac{1}{\sqrt{0 + 9} + 3} = \frac{1}{3 + 3} = \frac{1}{6}$$