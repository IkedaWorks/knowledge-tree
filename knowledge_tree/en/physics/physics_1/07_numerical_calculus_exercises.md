

# 🏛️ Numerical Calculus Exercises — (Prática de Precisão e SI)

> [!IMPORTANT]
> 
> **Introdução e Recomendações**
> 
> Esta seção é fundamental para você se acostumar a usar a **notação de engenharia**. Para facilitar sua vida, utilize uma calculadora científica para realizar os cálculos.
> 
> **Fonte:** Problemas selecionados de _Mecânica para Engenharia: Estática_ (R. C. Hibbeler).

### 📝 Exercício 1.1 — Operações com Algarismos Significativos

**Enunciado:** Avalie cada uma das seguintes operações com três algarismos significativos e expresse cada resposta em unidades SI utilizando um prefixo apropriado.

**(a) $(430 \text{ kg})^2$**

- **Análise Numérica:** $430 \times 430 = 184.900$.
    
- **Aplicação dos 3 AS:** No número $184.900$, o quarto dígito ($9$) força o arredondamento do terceiro ($4$) para cima. Resultado: $185.000$.
    
- **Ajuste SI:** Em engenharia, usamos $185 \cdot 10^3$.
    
- **Resposta Final:** $\mathbf{185(10^3) \text{ kg}^2}$
    

**(b) $(0,002 \text{ mg})^2$**

- **Análise Numérica:** $(2 \cdot 10^{-3})^2 = 4 \cdot 10^{-6}$.
    
- **Aplicação dos 3 AS:** Para demonstrar a precisão requerida, adicionamos zeros à direita: $4,00 \cdot 10^{-6}$.
    
- **Ajuste SI:** Converter para a unidade base ($g$) revela a escala real: $4 \cdot 10^{-6} \cdot (10^{-3} \text{ g})^2 = 4 \cdot 10^{-12} \text{ g}^2$.
    
- **Resposta Final:** $\mathbf{4,00 \cdot 10^{-6} \text{ mg}^2}$
    

**(c) $(230 \text{ m})^3$**

- **Análise Numérica:** $230 \times 230 \times 230 = 12.167.000$.
    
- **Aplicação dos 3 AS:** O quarto dígito ($6$) arredonda o terceiro ($1$) para cima. Resultado: $12,2 \cdot 10^6$.
    
- **Resposta Final:** $\mathbf{12,2 \cdot 10^6 \text{ m}^3}$
    

---

### 📝 Exercício 1.2 — Simplificação de Prefixos Compostos

**Enunciado:** Represente cada uma das seguintes combinações de unidades na forma correta do SI utilizando um prefixo apropriado.

**(a) $\text{Mg/ms}$**

- **Conversão:** $\frac{10^6 \text{ g}}{10^{-3} \text{ s}} = 10^9 \text{ g/s}$.
    
- **Lógica SI:** Aplicamos o prefixo à grama para evitar prefixos duplos.
    
- **Resposta Final:** $\mathbf{1 \text{ Gg/s}}$
    

**(b) $\text{N/mm}$**

- **Conversão:** $\frac{\text{N}}{10^{-3} \text{ m}} = 10^3 \text{ N/m}$.
    
- **Resposta Final:** $\mathbf{1 \text{ kN/m}}$
    

**(c) $\text{mN/(kg} \cdot \mu\text{s)}$**

- **Conversão:** $\frac{10^{-3} \text{ N}}{1 \text{ kg} \cdot 10^{-6} \text{ s}} = \frac{10^{-3}}{10^{-6}} \text{ N/(kg} \cdot \text{s)} = 10^3 \text{ N/(kg} \cdot \text{s)}$.
    
- **Resposta Final:** $\mathbf{1 \text{ kN/(kg} \cdot \text{s)}}$
    

---

### 📝 Exercício 1.4 — Conversão de Grandezas Complexas

**Enunciado:** Represente cada uma das seguintes quantidades na forma correta do SI utilizando um prefixo apropriado.

**(a) $\text{kN/}\mu\text{s}$**

- **Cálculo:** $\frac{10^3 \text{ N}}{10^{-6} \text{ s}} = 10^9 \text{ N/s}$.
    
- **Resposta Final:** $\mathbf{1 \text{ GN/s}}$
    

**(b) $\text{Mg/mN}$**

- **Cálculo:** $\frac{10^6 \text{ g}}{10^{-3} \text{ N}} = 10^9 \text{ g/N}$.
    
- **Resposta Final:** $\mathbf{1 \text{ Gg/N}}$
    

---

> [!TIP]
> 
> **Dica de Estudo**
> 
> Observe que nos exercícios de divisão, o prefixo do denominador sempre "sobe" invertendo o sinal da potência. Dominar isso elimina $90\%$ dos erros de unidade em provas de física e estática.