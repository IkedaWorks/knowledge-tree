
# Integração Imprópria

### O Conceito de Impropriedade

Uma integral é dita **imprópria** quando o intervalo de integração ou a própria função desafiam as regras da Integral de Riemann (que exige intervalo fechado e função limitada). No cálculo, não operamos diretamente com o infinito; usamos o **Limite** para descrever o comportamento da área conforme nos aproximamos do "proibido".

---

### Classificação das Integrais Impróprias

#### Tipo 1: Intervalos Infinitos

Ocorre quando um ou ambos os limites de integração são infinitos ($\infty$ ou $-\infty$).

- **Formalismo:** $\int_{a}^{\infty} f(x) \, dx = \lim_{t \to \infty} \int_{a}^{t} f(x) \, dx$
    

#### Tipo 2: Descontinuidades Infinitas (Assíntotas)

Ocorre quando o intervalo $[a, b]$ é finito, mas a função $f(x)$ explode para o infinito em algum ponto (geralmente nos extremos ou no meio do intervalo).

- **Formalismo:** $\int_{0}^{1} \frac{1}{\sqrt{x}} \, dx = \lim_{t \to 0^{+}} \int_{t}^{1} \frac{1}{\sqrt{x}} \, dx$
    

---

### O Veredito: Convergência vs. Divergência

Após aplicar o limite ao resultado da integral, temos dois destinos possíveis:

1. **Convergente:** O limite resulta em um número real finito. A "cauda" da função diminui tão rápido que a área total acumulada é limitada.
    
2. **Divergente:** O limite resulta em $\pm\infty$ ou não existe. A função não decai o suficiente e a área "foge".
    

> [!TIP]
> 
> **A Regra-p (P-test):** Para $\int_{1}^{\infty} \frac{1}{x^p} \, dx$:
> 
> - Se **$p > 1$**, a integral **converge**. (Ex: $1/x^2$ vai a zero rápido o suficiente).
>     
> - Se **$p \leq 1$**, a integral **diverge**. (Ex: $1/x$ é "lenta" demais e acumula área infinita).
>     

---

### Exemplo Resolvido 1: Convergência

**Problema:** Calcule a área sob $f(x) = \frac{1}{x^2}$ para $x \ge 1/2$.

1. **Montagem:** $\int_{1/2}^{\infty} \frac{1}{x^2} \, dx$
    
2. **Limite:** $\lim_{b \to \infty} \int_{1/2}^{b} x^{-2} \, dx$
    
3. **Integral:** $\lim_{b \to \infty} \left[ -\frac{1}{x} \right]_{1/2}^{b}$
    
4. **Aplicação:** $\lim_{b \to \infty} \left( -\frac{1}{b} - (-\frac{1}{1/2}) \right) = \lim_{b \to \infty} \left( -\frac{1}{b} + 2 \right)$
    
5. **Resultado:** Como $1/b \to 0$ quando $b \to \infty$, o resultado é **2**.
    
    - **Conclusão:** A integral **converge** para 2. Mesmo o intervalo sendo infinito, a área é finita!
        

---

### Exemplo Resolvido 2: Integrando Infinito (Tipo 2)

**Problema:** $\int_{0}^{16} \frac{1}{\sqrt[4]{x}} \, dx$

Aqui, o problema está no **zero**, pois $1/0$ é uma assíntota vertical.

1. **Limite:** $\lim_{t \to 0^{+}} \int_{t}^{16} x^{-1/4} \, dx$
    
2. **Primitiva:** $\lim_{t \to 0^{+}} \left[ \frac{x^{3/4}}{3/4} \right]_{t}^{16} = \lim_{t \to 0^{+}} \left[ \frac{4\sqrt[4]{x^3}}{3} \right]_{t}^{16}$
    
3. **Cálculo:** $\frac{4\sqrt[4]{16^3}}{3} - \frac{4\sqrt[4]{t^3}}{3}$
    
    - $\sqrt[4]{16^3} = (\sqrt[4]{16})^3 = 2^3 = 8$.
        
    - $\lim_{t \to 0} \sqrt[4]{t^3} = 0$.
        
4. **Resultado:** $\frac{4 \cdot 8}{3} = \mathbf{\frac{32}{3} \approx 10,66}$
    
    - **Conclusão:** A função explode no zero, mas a área sob ela é finita. **Converge!**
        

---

### ⚠️ Observações de Engenharia

- **Assíntotas Verticais:** Sempre use limites laterais ($t \to a^+$ ou $t \to b^-$) para garantir que você está dentro do domínio da função.
    
- **Assíntotas Oblíquas:** Como você bem notou, se a função segue uma reta inclinada no infinito, ela nunca vai "fechar" a área. O resultado será sempre **divergente**.