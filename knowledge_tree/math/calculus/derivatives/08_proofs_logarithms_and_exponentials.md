

# Demonstração: Derivadas de Logaritmo e Exponencial

Antes de começarmos as demonstrações eu recomendo que você de um revisada nos limites fundamentais e nas propriedade de potenciação e de logaritmos, usaremos elas de forma bem sucinta.

> [!TIP] **RECOMENDAÇÃO:** 
>
>Se vc está estudando isso de última hora é melhor vc só decorar e pular para o próximo tópico.

## 1. O Alicerce: A Definição do Número $e$

Antes de derivar, precisamos aceitar a definição fundamental de $e$ como um limite. Ele é o valor que resolve este problema:

$$\lim_{u \to 0} (1+u)^{1/u} = e$$

Ou, usando o logaritmo natural:

$$\lim_{u \to 0} \frac{\ln(1+u)}{u} = 1$$

---

## 2. Demonstração do Logaritmo: $\frac{d}{dx}(\log_a x)$

Vamos aplicar a definição de derivada para $f(x) = \log_a x$:

**O Limite:**

$$f'(x) = \lim_{h \to 0} \frac{\log_a(x+h) - \log_a(x)}{h}$$

**Propriedade da Divisão (Logaritmos):**

$$f'(x) = \lim_{h \to 0} \frac{1}{h} \log_a\left(\frac{x+h}{x}\right) = \lim_{h \to 0} \frac{1}{h} \log_a\left(1 + \frac{h}{x}\right)$$

**O Ajuste Algébrico (Multiplicar por $x/x$):**

Aqui está o "pulo do gato". Queremos que o termo dentro do logaritmo combine com o expoente para cair na definição de $e$. Vamos multiplicar a fração por $1/x$ e compensar colocando um $x$ lá dentro:

$$f'(x) = \lim_{h \to 0} \frac{1}{x} \cdot \frac{x}{h} \log_a\left(1 + \frac{h}{x}\right)$$

**A Regra do Tombo (Inversa):**

Levamos o $\frac{x}{h}$ para o expoente:

$$f'(x) = \frac{1}{x} \lim_{h \to 0} \log_a\left[\left(1 + \frac{h}{x}\right)^{x/h}\right]$$

**Identificando o $e$:**

Chame $u = h/x$. Quando $h \to 0$, $u \to 0$. O limite vira a própria definição de $e$:

$$f'(x) = \frac{1}{x} \log_a(e)$$

**Mudança de Base:**

Como $\log_a(e) = \frac{1}{\ln a}$, chegamos na regra geral:

**Logo:** $\frac{d}{dx}(\log_a x) = \frac{1}{x \ln a}$

---

## 3. Demonstração da Exponencial: $\frac{d}{dx}(a^x)$

Para a exponencial, usamos o resultado do logaritmo e a Derivada da Função Inversa (aquele "mix" que fizemos antes).

**Defina a Inversa:**

Se $y = a^x$, então $x = \log_a y$.

**Use a Regra da Inversa:**

$$\frac{dy}{dx} = \frac{1}{\frac{dx}{dy}}$$

**Substitua a derivada do logaritmo (que acabamos de provar):**

Sabemos que $\frac{dx}{dy} = \frac{1}{y \ln a}$. Invertendo essa fração:

$$\frac{dy}{dx} = y \ln a$$

**Volte para a variável original:**

Como $y = a^x$:

**Logo:** $\frac{d}{dx}(a^x) = a^x \ln a$