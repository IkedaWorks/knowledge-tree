
# Derivada da Função Inversa

## 1. O Conceito: A Derivada como o "Inverso da Velocidade"

Imagine que a função $f(x)$ é uma máquina que transforma **Tempo ($x$)** em **Posição ($y$)**. A derivada $f'(x)$ é a sua velocidade: "quantos metros eu ganho por segundo".

A função inversa $f^{-1}(y)$ faz o caminho oposto: transforma **Posição ($y$)** em **Tempo ($x$)**. A derivada da inversa responde: "quantos segundos eu gasto para percorrer cada metro".

### Relação de Reciprocidade

Se você corre a $10$ m/s (velocidade alta), você gasta $1/10$ s/m (tempo baixo). Geometricamente, a inclinação de uma é o **inverso multiplicativo** da inclinação da outra no ponto correspondente.

---

## 2. Demonstração via Regra da Cadeia

Para provar essa relação, usamos o fato de que uma função inversa "anula" a função original, resultando na função identidade.

1. **A Base:**
    
    $$f(f^{-1}(x)) = x$$
    
2. **O Gatilho (Regra da Cadeia):** Derivamos ambos os lados em relação a $x$. O lado direito (derivada de $x$) é $1$. No lado esquerdo, aplicamos a Regra da Cadeia:
    
    $$\frac{d}{dx}[f(f^{-1}(x))] = 1$$
    
    $$f'(f^{-1}(x)) \cdot (f^{-1})'(x) = 1$$
    
3. **O Isolamento:** Isolamos o termo que queremos descobrir, a derivada da inversa $(f^{-1})'(x)$:
    
    $$(f^{-1})'(x) = \frac{1}{f'(f^{-1}(x))}$$
    

---

## 3. Exemplo Prático: A Origem do $1/x$

Podemos provar por que a derivada de $\ln(x)$ é $1/x$ usando sua inversa, a exponencial ($e^x$).

1. Seja $f(y) = e^y$. Sabemos que $f'(y) = e^y$.
    
2. A inversa é $f^{-1}(x) = \ln(x)$.
    
3. Aplicando a fórmula:
    
    $$(\ln x)' = \frac{1}{f'(\ln x)} = \frac{1}{e^{\ln x}}$$
    
4. Como $e$ e $\ln$ são operações opostas, elas se cancelam:
    
    $$(\ln x)' = \frac{1}{x}$$
    

---

## 4. Resumo e Regras Mentais

- **Regra Verbal:** A derivada da inversa em um ponto é "um sobre a derivada da função original aplicada na própria inversa".
    
- **Geometria:** No gráfico, se a reta tangente de $f$ tem inclinação $m$, a reta tangente de $f^{-1}$ no ponto espelhado (refletido sobre a reta $y=x$) terá inclinação $1/m$.
    
- **A Fórmula Mestra:**
    
    $$(f^{-1})'(x) = \frac{1}{f'(y)}$$
    
    _(Onde $y = f^{-1}(x)$)_

## 5. Condição de Existência: O Papel da Bijetividade

Como consequência direta da definição de inversa, a derivada da função inversa **só existe se a função original for bijetora** (injetora e sobrejetora) no intervalo considerado.

### Por que isso é obrigatório?

1. **Injetividade (Teste da Linha Horizontal):** Se uma função não for injetora (como $f(x) = x^2$ em todo o domínio real), um valor de $y$ pode vir de dois valores de $x$ diferentes ($1^2=1$ e $(-1)^2=1$). Nesse caso, a "inversa" não seria uma função, pois teria dois resultados para a mesma entrada.
    
2. **A Derivada Nula:** Pela fórmula $(f^{-1})'(x) = \frac{1}{f'(y)}$, percebemos que se a derivada da função original for **zero** em um ponto ($f'(y) = 0$), a derivada da inversa naquele ponto seria uma divisão por zero (indeterminada). Geometricamente, uma tangente horizontal na original torna-se uma tangente **vertical** na inversa.
    

### Exemplo de Engenharia:

Ao trabalhar com funções trigonométricas (que são periódicas e não bijetoras no domínio real), precisamos **restringir o domínio** (ex: de $-\pi/2$ a $\pi/2$ para o seno) para que a inversa ($\arcsin$) exista e seja derivável.
