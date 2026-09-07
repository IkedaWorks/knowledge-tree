
# Provando as Regras de Derivação

## Definição
As demonstrações transformam “regras decoradas” em verdades matemáticas fundamentais usando a definição de derivada:

$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

---

## Regra da Soma
**Regra:** $(u + v)' = u' + v'$  
**Objetivo:** Provar que a derivada distribui na soma.

### Passos
1. **Defina:** $F(x) = u(x) + v(x)$
2. **Aplique a definição:** $$\lim_{h \to 0} \frac{[u(x+h) + v(x+h)] - [u(x) + v(x)]}{h}$$
3. **Agrupe os termos:** $$\lim_{h \to 0} \left( \frac{u(x+h) - u(x)}{h} + \frac{v(x+h) - v(x)}{h} \right)$$
4. **Propriedade do limite:** $$\lim_{h \to 0} \frac{u(x+h) - u(x)}{h} + \lim_{h \to 0} \frac{v(x+h) - v(x)}{h}$$

> [!TIP]
> **Conclusão:** $F'(x) = u'(x) + v'(x)$

---

## Regra do Produto
**Regra:** $(u \cdot v)' = u'v + uv'$  
**Objetivo:** Entender por que não é apenas derivar ambos e multiplicar.

### Passos
1. **Definição:** $$\lim_{h \to 0} \frac{u(x+h)v(x+h) - u(x)v(x)}{h}$$
2. **Truque Algébrico:** Somamos e subtraímos o termo $u(x+h)v(x)$.
   $$\lim_{h \to 0} \frac{u(x+h)v(x+h) - u(x+h)v(x) + u(x+h)v(x) - u(x)v(x)}{h}$$
3. **Fatoração:**
   $$\lim_{h \to 0} \left[ u(x+h)\frac{v(x+h) - v(x)}{h} + v(x)\frac{u(x+h) - u(x)}{h} \right]$$

> [!IMPORTANT]
> **Aplique o limite:**
> * $u(x+h) \to u(x)$
> * $\frac{v(x+h) - v(x)}{h} \to v'(x)$
> * $\frac{u(x+h) - u(x)}{h} \to u'(x)$

**Conclusão:** $(u \cdot v)' = u(x)v'(x) + v(x)u'(x)$

---

## Regra do Tombo (caso $n = 2$)
**Exemplo:** $(x^2)' = 2x$

### Passos
1. **Definição:** $$\lim_{h \to 0} \frac{(x+h)^2 - x^2}{h}$$
2. **Desenvolva:** $$\lim_{h \to 0} \frac{x^2 + 2xh + h^2 - x^2}{h}$$
3. **Simplifique:** $$\lim_{h \to 0} \frac{2xh + h^2}{h} = \lim_{h \to 0} (2x + h) = 2x$$

> [!NOTE]
> Para o caso geral $x^n$, a demonstração utiliza o **Binômio de Newton**. Isso exige familiaridade com análise combinatória para entender o cancelamento dos termos.

---

## Regra do Quociente
**Regra:** $\left( \frac{f}{g} \right)' = \frac{f'g - fg'}{g^2}$

### Demonstração
1. **MMC e Reorganização:**
   $$\lim_{h \to 0} \frac{f(x+h)g(x) - f(x)g(x+h)}{h \cdot g(x+h)g(x)}$$
2. **Somar e Subtrair:** Inserimos $f(x)g(x)$ no numerador.
   $$\lim_{h \to 0} \frac{g(x)[f(x+h) - f(x)] - f(x)[g(x+h) - g(x)]}{h \cdot g(x+h)g(x)}$$

> [!CAUTION]
> Lembre-se que no limite o denominador $g(x+h)g(x)$ torna-se $g(x)^2$.

**Resultado final:** $$\frac{g(x)f'(x) - f(x)g'(x)}{g(x)^2}$$