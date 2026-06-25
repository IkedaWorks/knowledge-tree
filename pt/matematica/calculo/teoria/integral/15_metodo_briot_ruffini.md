
# Briot-Ruffini & Redução Polinomail (Redução de Grau)

### Recomendações e Contexto

O Briot-Ruffini é uma ferramenta de **agilidade**. Ele é extremamente útil em provas para ganhar tempo, mas é um especialista: só funciona para divisões pelo binômio linear $(x - a)$.

> [!IMPORTANT]
> 
> **Regra de Ouro:** Para o caso geral (dividir por qualquer polinômio), domine a **Divisão Longa**. O Briot-Ruffini é o seu atalho quando você já conhece uma raiz do denominador e precisa fatorá-lo para aplicar a **DFP**.

---

### A Caça à Raiz: Onde tudo começa

Antes de usar o dispositivo, você precisa de uma raiz ($a$). Como encontrá-la sem sofrer?

1. **Dica de Mestre (Soma dos Coeficientes):** Se a soma de todos os coeficientes do polinômio for **zero**, o número **1** é uma raiz garantida.
    
    - _Por que?_ Porque $P(1)$ resulta na soma dos coeficientes. Se $P(1) = 0$, então $1$ é raiz.
        
2. **Teorema das Raízes Racionais:** Se a soma não der zero, olhe para o **termo independente** (o número sem $x$). As possíveis raízes inteiras são os divisores desse número.
    
    - _Exemplo:_ Para $P(x) = x^3 - 6x^2 + 11x - 6$, teste os divisores de $-6$: $\{\pm 1, \pm 2, \pm 3, \pm 6\}$.
        
3. **Teorema do Resto (Validação):** Para confirmar se um candidato é raiz antes de fazer o dispositivo, basta calcular $P(a)$. Se o resultado for $0$, a raiz é válida.
    

---

### O Algoritmo (Passo a Passo)

Vamos dividir $P(x) = x^3 - 6x^2 + 11x - 6$ por $(x - 1)$. Raiz $a = 1$.

#### A Estrutura (O "Chiqueirinho")

Organize a raiz à esquerda e os coeficientes do dividendo à direita:

|**Raiz (a)**|**x3**|**x2**|**x1**|**Termo indep.**|
|---|---|---|---|---|
|**1**|1|-6|11|-6|
||↓||||
||**1**||||

#### O Processo: Desce, Multiplica e Soma

1. **Desce:** O primeiro coeficiente ($1$) desce direto.
    
2. **Multiplica e Soma:** Multiplique o número que desceu pela raiz e some com o próximo vizinho de cima.
    
    - $1 \cdot (1) + (-6) = \mathbf{-5}$
        
    - $-5 \cdot (1) + 11 = \mathbf{6}$
        
    - $6 \cdot (1) + (-6) = \mathbf{0}$ (O último número é sempre o **Resto**).
        

---

### Leitura do Resultado

A linha de baixo contém os coeficientes do novo polinômio, que terá sempre **um grau a menos** que o original:

- Coeficientes: $1, -5, 6$.
    
- Novo Polinômio: $1x^2 - 5x + 6$.
    

Agora, a expressão original $x^3 - 6x^2 + 11x - 6$ pode ser escrita como:

$$(x - 1)(x^2 - 5x + 6)$$

---

### Conexão com a DFP (Decomposição em Frações Parciais)

Este é o fluxo de trabalho real em uma questão de integral:

1. **Investigação:** O denominador é grau 3? Ache a primeira raiz por inspeção ou Teorema das Raízes Racionais.
    
2. **Execução:** Use Briot-Ruffini para baixar para grau 2.
    
3. **Fatoração Final:** Use Bhaskara ou Soma e Produto no polinômio de grau 2 resultante.
    
    - No nosso exemplo: $x^2 - 5x + 6 \implies$ raízes $2$ e $3$.
        
4. **Montagem da DFP:** Agora você tem três fatores lineares:
    
    $$\frac{\text{Numerador}}{(x-1)(x-2)(x-3)} = \frac{A}{x-1} + \frac{B}{x-2} + \frac{C}{x-3}$$
    
5. **Integração:** Resolva como uma soma de logaritmos simples.