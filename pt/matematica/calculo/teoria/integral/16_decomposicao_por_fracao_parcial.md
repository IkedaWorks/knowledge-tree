


# Decomposição por Frações Parcias(DFP)

### Definição e Intuição

A DFP é uma técnica algébrica para "desmontar" uma fração cujo denominador é um polinômio difícil de integrar. O objetivo é transformar uma única fração complexa em uma soma de frações simples do tipo $1/(x+a)$, cuja integral resulta quase sempre em um **Logaritmo Natural ($\ln$)**.

**Condição de Uso:** O grau do numerador deve ser estritamente **menor** que o grau do denominador. Se o denominador puder ser fatorado, a técnica é aplicável.

---

### Protocolo de Resolução (Fatores Lineares)

1. **Fatoração do Denominador:** Transforme o polinômio em um produto de termos simples.
    
    - _Exemplo:_ $x^2 + x \implies x(x + 1)$.
        
2. **Montagem da Identidade:** Atribua uma constante ($A, B, \dots$) para cada fator.
    
    $$\frac{1}{x(x+1)} = \frac{A}{x} + \frac{B}{x+1}$$
    
3. **Cálculo dos Coeficientes (Método dos Zeros):** Elimine os denominadores multiplicando tudo pelo MMC e escolha valores de $x$ que anulem os termos para isolar as constantes.
    
    - $1 = A(x+1) + Bx$
        
    - Se $x = 0 \implies \mathbf{A = 1}$
        
    - Se $x = -1 \implies \mathbf{B = -1}$
        
4. **Integração Final:** Integre os termos simplificados.
    
    $$\int \frac{1}{x} dx - \int \frac{1}{x+1} dx = \ln|x| - \ln|x+1| + C$$
    

---

### O Problema do Grau (Frações Impróprias)

Se o grau do numerador for $\ge$ ao do denominador, a DFP não pode ser aplicada diretamente. Você deve realizar a **Divisão Polinomial** primeiro.

#### A Prova da Estrutura:

Você já sabe que: $\text{Dividendo} = (\text{Divisor} \cdot \text{Quociente}) + \text{Resto}$.

Ao dividir toda essa equação pelo **Divisor**, obtemos a identidade usada no Cálculo:

$$\frac{P(x)}{Q(x)} = \text{Quociente}(x) + \frac{Resto(x)}{Q(x)}$$

> [!NOTE]
> 
> Integrar o Quociente é simples (é um polinômio). A DFP entra em cena apenas para resolver a fração que sobra ($\frac{Resto}{Divisor}$), que agora é uma fração própria.

---

### Exercício Resolvido: Integração Completa

**Problema:** Calcule $\int \frac{x^2 + 1}{x^2 - x} \, dx$

1. **Divisão (Graus iguais):**
    
    $\frac{x^2 + 1}{x^2 - x} = 1 + \frac{x+1}{x^2-x}$
    
2. **DFP no Resto:**
    
    $\frac{x+1}{x(x-1)} = \frac{A}{x} + \frac{B}{x-1} \implies x+1 = A(x-1) + Bx$
    
    - Se $x = 0 \implies \mathbf{A = -1}$
        
    - Se $x = 1 \implies \mathbf{B = 2}$
        
3. **Montagem Final:**
    
    $$\int 1 \, dx + \int \frac{-1}{x} \, dx + \int \frac{2}{x-1} \, dx$$
    
    **Resultado:** $x - \ln|x| + 2\ln|x-1| + C$
    

---

### 💡 Casos Especiais: Arco Tangente

Se o denominador for um polinômio de grau 2 que **não possui raízes reais** (como $x^2 + 4$), a DFP não resulta em $\ln$, mas sim em **Arco Tangente**:

$$\int \frac{1}{x^2 + a^2} \, dx = \frac{1}{a} \arctan\left(\frac{x}{a}\right) + C$$