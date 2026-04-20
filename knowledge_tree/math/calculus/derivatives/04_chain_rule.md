
# Regra da Cadeia (Funções Compostas)

## 1. Definição e Intuição

A **Regra da Cadeia** é utilizada para derivar funções que estão "dentro" de outras funções (composição). Ela estabelece que a variação total é o produto das variações de cada camada.

### A Analogia das Bonecas Russas (Matrioskas)

Para chegar na boneca menor (a função interna), você precisa primeiro abrir a boneca maior (a função externa). A derivada total é a "velocidade de abertura" da externa multiplicada pela "velocidade" da interna.

---

## 2. A Regra e a Notação

Se $y = f(u)$ e $u = g(x)$, temos a função composta $y = f(g(x))$.

### I. Notação de Lagrange

$$(f \circ g)'(x) = f'(g(x)) \cdot g'(x)$$

- **Tradução:** "Derive a de fora (mantendo a de dentro intacta) e multiplique pela derivada da de dentro."
    

### II. Notação de Leibniz

$$\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx}$$

- **Dica de Engenharia:** Esta notação é extremamente útil pois visualmente parece uma simplificação de frações onde o $du$ se "cancela", restando $\frac{dy}{dx}$.
    

---

## 3. Exemplos Passo a Passo

### Exemplo 1: Potência de Função ($f(x) = (3x^2 + 1)^5$)

1. **Identifique as camadas:**
    
    - **Fora:** $(u)^5 \to$ Derivada: $5u^4$
        
    - **Dentro:** $3x^2 + 1 \to$ Derivada: $6x$
        
2. **Aplique a Cadeia:** $f'(x) = 5(3x^2 + 1)^4 \cdot (6x)$
    
3. **Simplifique:** $f'(x) = 30x(3x^2 + 1)^4$.
    

### Exemplo 2: Trigonométrica Composta ($f(x) = \sin(x^3)$)

1. **Identifique as camadas:**
    
    - **Fora:** $\sin(u) \to$ Derivada: $\cos(u)$
        
    - **Dentro:** $x^3 \to$ Derivada: $3x^2$
        
2. **Aplique a Cadeia:** $f'(x) = \cos(x^3) \cdot 3x^2$
    

- **Resultado:** $f'(x) = 3x^2 \cos(x^3)$.
    

### Exemplo 3: A "Cadeia Tripla" ($f(x) = e^{\sin(5x)}$)

1. **Exponencial (Externa):** $e^{\sin(5x)} \cdot (\text{derivada do expoente})$
    
2. **Seno (Meio):** $\cos(5x) \cdot (\text{derivada do argumento})$
    
3. **Polinômio (Interna):** $5$
    

- **Veredito:** $f'(x) = 5 \cos(5x) e^{\sin(5x)}$.
    

---

## 4. Macetes e Cuidados

- **O Erro Fatal:** Tentar derivar a de dentro ao mesmo tempo que a de fora.
    
    - _Errado:_ $(\sin(x^2))' = \cos(2x)$.
        
    - _Correto:_ Você mantém o $x^2$ intacto enquanto troca o seno por cosseno, e **só depois** multiplica por $2x$.
        
- **Casca de Cebola:** Sempre trabalhe da operação mais externa para a mais interna.
    
- **Raízes são Cadeias:** Lembre-se que $\sqrt{g(x)} = [g(x)]^{1/2}$.
    
    - **Atalho Útil:** $(\sqrt{u})' = \frac{u'}{2\sqrt{u}}$.
        

---

## 5. Demonstração Intuitiva via Leibniz

Embora a demonstração rigorosa envolva o limite de Newton e ajustes para evitar divisão por zero, a forma mais clara de visualizar é através das razões de variação:

$$\frac{\Delta y}{\Delta x} = \frac{\Delta y}{\Delta u} \cdot \frac{\Delta u}{\Delta x}$$

Ao aplicarmos o limite $\Delta x \to 0$ (o que implica $\Delta u \to 0$ em funções contínuas), as razões médias tornam-se derivadas instantâneas:

$$\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx}$$