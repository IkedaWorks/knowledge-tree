


# Regras de Derivação
## Definição

As demonstrações transformam “regras decoradas” em verdades matemáticas fundamentais usando a definição de derivada:

$$
f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}
$$

---

## Regra da Soma

**Regra:**
$$
(u + v)' = u' + v'
$$

**Objetivo:** Provar que a derivada distribui na soma.

### Passos

- Defina:
$$
F(x) = u(x) + v(x)
$$

- Aplique a definição:
$$
\lim_{h \to 0} \frac{[u(x+h) + v(x+h)] - [u(x) + v(x)]}{h}
$$

- Agrupe os termos:
$$
\lim_{h \to 0} \left( \frac{u(x+h) - u(x)}{h} + \frac{v(x+h) - v(x)}{h} \right)
$$

- Aplique a propriedade do limite:
$$
\lim_{h \to 0} \frac{u(x+h) - u(x)}{h} + \lim_{h \to 0} \frac{v(x+h) - v(x)}{h}
$$

### Conclusão

$$
F'(x) = u'(x) + v'(x)
$$

---

## Regra do Produto

**Regra:**
$$
(u \cdot v)' = u'v + uv'
$$

**Objetivo:** Entender por que não é apenas derivar ambos e multiplicar.

### Passos

- Aplique a definição:
$$
\lim_{h \to 0} \frac{u(x+h)v(x+h) - u(x)v(x)}{h}
$$

- Some e subtraia o mesmo termo:
$$
u(x+h)v(x)
$$

$$
\lim_{h \to 0} \frac{
u(x+h)v(x+h) - u(x+h)v(x) + u(x+h)v(x) - u(x)v(x)
}{h}
$$

- Fatore:
$$
\lim_{h \to 0} \left[
u(x+h)\frac{v(x+h) - v(x)}{h}
+ v(x)\frac{u(x+h) - u(x)}{h}
\right]
$$

- Aplique o limite:

$$
u(x+h) \to u(x)
$$

$$
\frac{v(x+h) - v(x)}{h} \to v'(x)
$$

$$
\frac{u(x+h) - u(x)}{h} \to u'(x)
$$

### Conclusão

$$
(u \cdot v)' = u(x)v'(x) + v(x)u'(x)
$$

---

## Regra do Tombo (caso n = 2)

**Exemplo:**
$$
(x^2)' = 2x
$$

**Objetivo:** Ver a álgebra por trás do expoente que “cai”.

### Passos

- Aplique a definição:
$$
\lim_{h \to 0} \frac{(x+h)^2 - x^2}{h}
$$

- Desenvolva:
$$
\lim_{h \to 0} \frac{x^2 + 2xh + h^2 - x^2}{h}
$$

- Simplifique:
$$
\lim_{h \to 0} \frac{2xh + h^2}{h} = \lim_{h \to 0} (2x + h)
$$

- Aplique o limite:
$$
2x + 0 = 2x
$$

### Conclusão

$$
(x^2)' = 2x
$$

**Nota:**  
Para o caso geral \(x^n\), a demonstração utiliza o Binômio de Newton. Isso exige familiaridade com análise combinatória e o triângulo de Pascal para entender o cancelamento dos termos.

---

## Regra do Quociente (Demonstração via Limite)

**Regra:**
$$
\left( \frac{f}{g} \right)' = \frac{f'g - fg'}{g^2}
$$

### Passo 1 — Definição

$$
\lim_{h \to 0} \frac{\frac{f(x+h)}{g(x+h)} - \frac{f(x)}{g(x)}}{h}
$$

---

### Passo 2 — MMC

$$
\lim_{h \to 0} \frac{\frac{f(x+h)g(x) - f(x)g(x+h)}{g(x+h)g(x)}}{h}
$$

Reorganizando:

$$
\lim_{h \to 0} \frac{f(x+h)g(x) - f(x)g(x+h)}{h \cdot g(x+h)g(x)}
$$

---

### Passo 3 — Somar e Subtrair

Inserimos:
$$
f(x)g(x)
$$

$$
\lim_{h \to 0} \frac{
f(x+h)g(x) - f(x)g(x) + f(x)g(x) - f(x)g(x+h)
}{
h \cdot g(x+h)g(x)
}
$$

---

### Passo 4 — Fatoração

$$
\lim_{h \to 0} \frac{
g(x)[f(x+h) - f(x)] - f(x)[g(x+h) - g(x)]
}{
h \cdot g(x+h)g(x)
}
$$

---

### Passo 5 — Aplicar limites

$$
\frac{f(x+h) - f(x)}{h} \to f'(x)
$$

$$
\frac{g(x+h) - g(x)}{h} \to g'(x)
$$

$$
g(x+h) \to g(x)
$$

---

### Passo 6 — Resultado final

$$
\frac{g(x)f'(x) - f(x)g'(x)}{g(x)^2}
$$

### Conclusão

$$
 \left( \frac{f}{g} \right)' = \frac{f'g - fg'}{g^2}
$$
