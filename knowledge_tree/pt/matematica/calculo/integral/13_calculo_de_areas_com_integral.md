
# Exercícios de Áreas

### Guia para Exercícios  

Para resolver áreas entre funções complexas, siga este protocolo:

1. **Esboço do Gráfico:** Desenhe as funções. Identifique raízes e interceptos no eixo $y$.
    
2. **Pontos de Interseção:** Iguale as funções ($f(x) = g(x)$) para encontrar os **Limites de Integração**.
    
3. **Identificação da Superior:** Verifique qual função está "por cima" no intervalo. Isso define a montagem: $\int_{a}^{b} (\text{Superior} - \text{Inferior}) \, dx$.
    
4. **Divisão de Intervalos:** Se o "teto" ou o "piso" da região mudar, divida a conta em duas ou mais integrais.
    

---

### Exercício 1: Área Delimitada por Parábola e Reta

**Enunciado:** Determine a área da região fechada pelas funções $f(x) = x^2 - 4$ e $g(x) = 3x$.

1. **Encontrar os Limites (Interseção):**
    
    $x^2 - 4 = 3x \implies x^2 - 3x - 4 = 0$
    
    Raízes (Soma e Produto): $(x - 4)(x + 1) = 0 \implies \mathbf{a = -1}$ e $\mathbf{b = 4}$.
    
2. **Definir a Função Superior:**
    
    Testando $x = 0$ (dentro do intervalo): $f(0) = -4$ e $g(0) = 0$. Como $0 > -4$, a reta $g(x)$ é a superior.
    
3. **Montagem e Integração:**
    
    $$\int_{-1}^{4} [3x - (x^2 - 4)] \, dx = \int_{-1}^{4} (-x^2 + 3x + 4) \, dx$$
    
    **Primitiva:** $F(x) = \left[ -\frac{x^3}{3} + \frac{3x^2}{2} + 4x \right]_{-1}^{4}$
    
4. **Aplicação do TFC:**
    
    - Para $x = 4$: $-\frac{64}{3} + 24 + 16 = \frac{56}{3}$
        
    - Para $x = -1$: $\frac{1}{3} + \frac{3}{2} - 4 = -\frac{13}{6}$
        
        **Resultado:** $\frac{56}{3} - (-\frac{13}{6}) = \frac{112 + 13}{6} = \mathbf{\frac{125}{6} \approx 20,83}$
        

---

### Exercício 2: Área entre Duas Parábolas

**Enunciado:** Calcule a área entre $f(x) = 2 - x^2$ e $g(x) = x^2$.

1. **Limites:** $2 - x^2 = x^2 \implies 2x^2 = 2 \implies x = \pm 1$.
    
2. **Superior:** Para $x = 0$, $f(0) = 2$ e $g(0) = 0$. Logo, $f(x)$ está por cima.
    
3. **Integração:**
    
    $$\int_{-1}^{1} (2 - x^2 - x^2) \, dx = \int_{-1}^{1} (2 - 2x^2) \, dx$$
    
    **Primitiva:** $\left[ 2x - \frac{2x^3}{3} \right]_{-1}^{1}$
    
4. **Aplicação do TFC:**
    
    - Para $x = 1$: $2 - \frac{2}{3} = \frac{4}{3}$
        
    - Para $x = -1$: $-2 + \frac{2}{3} = -\frac{4}{3}$
        
        **Resultado:** $\frac{4}{3} - (-\frac{4}{3}) = \mathbf{\frac{8}{3} \approx 2,67}$
        

---

### Exercício 3: Área com Raiz e Reta (Mudança de "Piso")

**Enunciado:** Área delimitada por $y = \sqrt{x}$, $y = x - 2$ e o eixo $x$ ($y = 0$).

1. **Pontos Críticos:**
    
    - Interseção $\sqrt{x} = x - 2 \implies x = 4$.
        
    - Interseção $\sqrt{x} = 0 \implies x = 0$.
        
    - Interseção $x - 2 = 0 \implies x = 2$.
        
2. **Divisão da Área:** No gráfico, notamos que de $0$ a $2$ o limite inferior é o eixo $x$, mas de $2$ a $4$ o limite inferior passa a ser a reta $x-2$.
    
    - **Parte A (0 a 2):** $\int_{0}^{2} \sqrt{x} \, dx = \left[ \frac{2}{3}x^{3/2} \right]_0^2 = \frac{4\sqrt{2}}{3}$
        
    - **Parte B (2 a 4):** $\int_{2}^{4} (\sqrt{x} - (x-2)) \, dx = \left[ \frac{2}{3}x^{3/2} - \frac{x^2}{2} + 2x \right]_2^4$
        
3. **Cálculo e Soma:**
    
    - Resultado Parte B: $\left(\frac{16}{3} - 8 + 8\right) - \left(\frac{4\sqrt{2}}{3} - 2 + 4\right) = \frac{16}{3} - \frac{4\sqrt{2}}{3} - 2$
        
        **Área Total:** $\frac{4\sqrt{2}}{3} + \frac{16}{3} - \frac{4\sqrt{2}}{3} - 2 = \frac{16}{3} - \frac{6}{3} = \mathbf{\frac{10}{3}}$