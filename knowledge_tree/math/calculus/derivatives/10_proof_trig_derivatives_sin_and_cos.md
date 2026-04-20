

# Demonstração: Derivadas Trigonométricas Fundamentais

Esta seção dedica-se à construção das derivadas de seno e cosseno a partir do "zero absoluto", utilizando a definição formal de limite. Para isso, fundamentamos a álgebra em duas ferramentas essenciais da geometria analítica e do cálculo.

## 1. Ferramentas Necessárias

### I. Limites Fundamentais

- **O Limite Fundamental Trigonométrico:** Quando um ângulo $h$ (em radianos) tende a zero, o valor do seno desse ângulo aproxima-se do valor do próprio ângulo.
    
    $$\lim_{h \to 0} \frac{\sin h}{h} = 1$$
    
- **O Limite do Cosseno:** Derivado da mesma lógica geométrica:
    
    $$\lim_{h \to 0} \frac{\cos h - 1}{h} = 0$$
    

### II. Identidades de Soma de Arcos

Caso não estejam memorizadas, estas relações são cruciais para a expansão dos termos:

- $\sin(a \pm b) = \sin a \cdot \cos b \pm \sin b \cdot \cos a$
    
- $\cos(a \pm b) = \cos a \cdot \cos b \mp \sin a \cdot \sin b$
    

---

## 2. Demonstração: Derivada do Seno

**Definição:** $\frac{d}{dx}(\sin x) = \cos x$

1. **Aplicação do Limite Formal:**
    
    $$f'(x) = \lim_{h \to 0} \frac{\sin(x+h) - \sin(x)}{h}$$
    
2. **Expansão da Soma de Arcos:**
    
    $$f'(x) = \lim_{h \to 0} \frac{\sin(x)\cos(h) + \sin(h)\cos(x) - \sin(x)}{h}$$
    
3. **Agrupamento por Termos Comuns ($\sin x$):**
    
    $$f'(x) = \lim_{h \to 0} \left[ \sin(x) \cdot \frac{\cos(h) - 1}{h} + \cos(x) \cdot \frac{\sin(h)}{h} \right]$$
    
4. **Aplicação dos Limites Fundamentais:**
    
    - O termo $\frac{\cos(h) - 1}{h}$ tende a **$0$**.
        
    - O termo $\frac{\sin(h)}{h}$ tende a **$1$**.
        
5. **Resultado:**
    
    $$f'(x) = \sin(x) \cdot (0) + \cos(x) \cdot (1) = \cos x$$
    
    **Está provado.**
    

---

## 3. Demonstração: Derivada do Cosseno

**Definição:** $\frac{d}{dx}(\cos x) = -\sin x$

1. **Aplicação do Limite Formal:**
    
    $$f'(x) = \lim_{h \to 0} \frac{\cos(x+h) - \cos(x)}{h}$$
    
2. **Expansão da Soma de Arcos:**
    
    $$f'(x) = \lim_{h \to 0} \frac{\cos(x)\cos(h) - \sin(x)\sin(h) - \cos(x)}{h}$$
    
3. **Agrupamento por Termos Comuns ($\cos x$):**
    
    $$f'(x) = \lim_{h \to 0} \left[ \cos(x) \cdot \frac{\cos(h) - 1}{h} - \sin(x) \cdot \frac{\sin(h)}{h} \right]$$
    
4. **Aplicação dos Limites Fundamentais:**
    
    - O termo $\frac{\cos(h) - 1}{h}$ tende a **$0$**.
        
    - O termo $\frac{\sin(h)}{h}$ tende a **$1$**.
        
5. **Resultado:**
    
    $$f'(x) = \cos(x) \cdot (0) - \sin(x) \cdot (1) = -\sin x$$
    
    **Está provado.** O sinal negativo surge naturalmente da álgebra da soma de arcos.
    

---

> [!NOTE] Observação de Engenharia
> 
> Note que, para ângulos muito pequenos ($h \approx 0$), o comportamento do seno é linear (como a função $y=x$), enquanto o cosseno comporta-se como uma constante próxima a $1$. Isso explica por que a taxa de variação (derivada) do seno é máxima na origem, enquanto a do cosseno é nula.