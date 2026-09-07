
# Regras de Derivação

## 1. Definição e Intuição

As **Regras de Derivação** são fórmulas fundamentais que surgiram da aplicação repetida da definição formal de derivada (limite de Newton). Na prática, elas funcionam como um "dicionário": você identifica o formato da função e aplica a regra correspondente para obter a taxa de variação.

### A Intuição do Atalho

Em vez de construir uma escada (limite) toda vez que quiser subir um degrau, você usa um elevador (regra). O resultado é o mesmo, mas a velocidade de cálculo é infinitamente maior.

---

## 2. As Regras de Ouro

Considere $k$ como uma constante e $u, v$ como funções de $x$.

### I. Regra da Constante

Se a função é uma linha horizontal, ela não possui inclinação.

- **Regra:** Se $f(x) = k$, então $f'(x) = 0$.
    
- **Exemplo:** Se $f(x) = 10$, a variação é $0$.
    

### II. Regra do Poder (Regra do "Tombo")

É a regra mais utilizada. O expoente "cai" multiplicando e perde uma unidade.

- **Regra:** Se $f(x) = x^n$, então $f'(x) = n \cdot x^{n-1}$.
    
- **Exemplo:** Se $f(x) = x^3$, então $f'(x) = 3x^2$.
    

### III. Regra da Constante por Função

A constante "espera" a derivação acontecer e multiplica o resultado final.

- **Regra:** $\frac{d}{dx}[k \cdot u] = k \cdot u'$
    
- **Exemplo:** Se $f(x) = 5x^4$, então $f'(x) = 5 \cdot (4x^3) = 20x^3$.
    

### IV. Regra da Soma e Subtração

A derivada da soma é a soma das derivadas (o operador de derivada é linear).

- **Regra:** $(u \pm v)' = u' \pm v'$
    
- **Exemplo:** Se $f(x) = x^2 + 3x$, então $f'(x) = 2x + 3$.
    

---

## 3. Exemplos Práticos

### Exemplo 1: Polinômio Completo

Calcule a derivada de $f(x) = 4x^3 - 5x^2 + 8x - 12$.

1. **Termo 1 ($4x^3$):** O $3$ tomba $\to 4 \cdot 3x^2 = 12x^2$.
    
2. **Termo 2 ($-5x^2$):** O $2$ tomba $\to -5 \cdot 2x^1 = -10x$.
    
3. **Termo 3 ($8x$):** O $1$ tomba $\to 8 \cdot 1x^0 = 8$ (Lembre-se: $x^0 = 1$).
    
4. **Termo 4 ($-12$):** É constante $\to 0$.
    

- **Veredito:** $f'(x) = 12x^2 - 10x + 8$.
    

### Exemplo 2: Raiz e Fração (O truque do expoente)

Calcule a derivada de $f(x) = \sqrt{x} + \frac{1}{x}$.

- **Transforme em Poder:** Reescreva como $f(x) = x^{1/2} + x^{-1}$.
    

1. **Aplicando no $x^{1/2}$:** $\frac{1}{2}x^{(1/2 - 1)} = \frac{1}{2}x^{-1/2} = \frac{1}{2\sqrt{x}}$.
    
2. **Aplicando no $x^{-1}$:** $-1x^{(-1 - 1)} = -1x^{-2} = -\frac{1}{x^2}$.
    

- **Veredito:** $f'(x) = \frac{1}{2\sqrt{x}} - \frac{1}{x^2}$.
    

---

## 4. O Conceito de Interdependência

Quando duas funções $u(x)$ e $v(x)$ estão multiplicadas ou divididas, a variação de uma afeta a outra. Por isso, a regra exige que você "reveze" a derivação: enquanto uma deriva, a outra espera.

### I. Regra do Produto

Use quando tiver uma função multiplicando outra ($u \cdot v$).

- **Fórmula:** $(u \cdot v)' = u' \cdot v + u \cdot v'$
    
- **Tradução:** "Deriva a primeira, mantém a segunda $+$ Mantém a primeira, deriva a segunda".
    

**Exemplo:** $f(x) = x^2 \cdot \sin(x)$

1. Identifique: $u = x^2$ e $v = \sin(x)$.
    
2. Derive as partes: $u' = 2x$ e $v' = \cos(x)$.
    
3. **Resultado:** $f'(x) = 2x \cdot \sin(x) + x^2 \cdot \cos(x)$.
    

### II. Regra do Quociente

Use quando tiver uma divisão de funções ($\frac{u}{v}$).

- **Fórmula:** $\left( \frac{u}{v} \right)' = \frac{u' \cdot v - u \cdot v'}{v^2}$
    
- **Tradução:** "Deriva a de cima vezes a de baixo **menos** a de cima vezes a derivada da de baixo, tudo sobre a de baixo ao quadrado".
    

**Exemplo:** $f(x) = \frac{3x - 1}{x^2}$

1. Identifique: $u = 3x - 1$ e $v = x^2$.
    
2. Derive as partes: $u' = 3$ e $v' = 2x$.
    
3. **Aplicação:** $f'(x) = \frac{(3) \cdot (x^2) - (3x - 1) \cdot (2x)}{(x^2)^2}$
    
4. **Simplificação:** $f'(x) = \frac{3x^2 - (6x^2 - 2x)}{x^4} = \frac{-3x^2 + 2x}{x^4} = \frac{-3x + 2}{x^3}$.
    

---

## 5. Seção de Exercícios

**Exercício 1 (Produto):** $f(x) = e^x \cdot (x^3 + 2)$

- $u = e^x \to u' = e^x$
    
- $v = x^3 + 2 \to v' = 3x^2$
    
- **Resultado:** $f'(x) = e^x(x^3 + 2) + e^x(3x^2)$
    
- **Dica de Engenharia:** Colocando em evidência: $f'(x) = e^x(x^3 + 3x^2 + 2)$.
    

**Exercício 2 (Quociente):** $f(x) = \frac{\ln(x)}{x}$

- $u = \ln(x) \to u' = 1/x$
    
- $v = x \to v' = 1$
    
- **Resultado:** $f'(x) = \frac{(1/x) \cdot x - \ln(x) \cdot 1}{x^2}$
    
- **Simplificação:** $f'(x) = \frac{1 - \ln(x)}{x^2}$.