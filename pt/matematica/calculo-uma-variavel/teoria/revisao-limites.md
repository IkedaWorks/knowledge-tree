
# Revisão de Limites

Esta nota contém a resolução detalhada dos problemas de nível médio para fácil. O foco aqui não é o resultado, mas a **estratégia de ataque**.

---

###  1. O Limite Geométrico (Conexão Arco-Corda)
**Problema:** Calcule $\lim_{x \to 0} \frac{1 - \cos(x)}{x^2}$

* **A Estratégia:** Multiplicar pelo conjugado para transformar cosseno em seno.
* **Passo a Passo:**
    1. Multiplicamos em cima e embaixo por $(1 + \cos x)$:
       $$\lim_{x \to 0} \frac{(1 - \cos x)(1 + \cos x)}{x^2(1 + \cos x)}$$
    2. Identidade Trigonométrica ($1 - \cos^2 x = \text{sen}^2 x$):
       $$\lim_{x \to 0} \frac{\text{sen}^2 x}{x^2(1 + \cos x)}$$
    3. Separar o Limite Fundamental:
       $$\left( \lim_{x \to 0} \frac{\text{sen } x}{x} \right)^2 \cdot \lim_{x \to 0} \frac{1}{1 + \cos x}$$
    4. Aplicar os valores: $(1)^2 \cdot \frac{1}{1 + 1} = 1 \cdot \frac{1}{2}$
* **Veredito:** $\mathbf{1/2}$. (Este valor é a base para provar a derivada do cosseno).

---

###  2. A "Mágica" da Substituição de Euler
**Problema:** Calcule $\lim_{x \to \infty} \left( \frac{x + 6}{x + 1} \right)^{x+3}$

* **A Estratégia:** Transformar na base $e$ usando a forma $\lim (1 + 1/u)^u$.
* **Passo a Passo:**
    1. Manipular o interior da fração: $\frac{x+1+5}{x+1} = 1 + \frac{5}{x+1}$.
    2. Agora temos $\lim_{x \to \infty} (1 + \frac{5}{x+1})^{x+3}$.
    3. Queremos que o expoente seja o inverso do termo interno ($\frac{x+1}{5}$). Vamos forçar isso:
       $$\left[ \left( 1 + \frac{5}{x+1} \right)^{\frac{x+1}{5}} \right]^{\frac{5}{x+1} \cdot (x+3)}$$
    4. O termo dentro dos colchetes tende a $e$. Agora calculamos o limite do novo expoente:
       $$\lim_{x \to \infty} \frac{5(x+3)}{x+1} = \lim_{x \to \infty} \frac{5x+15}{x+1} = 5$$
* **Veredito:** $\mathbf{e^5}$.

---

###  3. Manipulação Exponencial Dupla
**Problema:** Calcule $\lim_{x \to 0} \frac{a^x - b^x}{x}$

* **A Estratégia:** Fazer aparecer a estrutura do Limite Fundamental Exponencial ($\frac{a^x-1}{x}$).
* **Passo a Passo:**
    1. "Truque do Zero Somado": Subtrair e somar 1 no numerador.
       $$\lim_{x \to 0} \frac{(a^x - 1) - (b^x - 1)}{x}$$
    2. Separar em duas frações:
       $$\lim_{x \to 0} \frac{a^x - 1}{x} - \lim_{x \to 0} \frac{b^x - 1}{x}$$
    3. Aplicar a definição ($\ln a$ e $\ln b$):
       $$\ln(a) - \ln(b)$$
    4. Propriedade de logaritmo: $\ln(a/b)$.
* **Veredito:** $\mathbf{\ln(a/b)}$.

---

###  4. O Sanduíche com Parte Inteira (Padrão JEE)
**Problema:** Calcule $\lim_{x \to \infty} \frac{\lfloor x \rfloor}{x}$, onde $\lfloor x \rfloor$ é a parte inteira de $x$.

* **A Estratégia:** Usar a definição da função escada para esmagar o limite.
* **Passo a Passo:**
    1. Definição: $x - 1 < \lfloor x \rfloor \le x$.
    2. Dividir tudo por $x$ (como $x \to \infty$, $x$ é positivo):
       $$\frac{x-1}{x} < \frac{\lfloor x \rfloor}{x} \le \frac{x}{x}$$
    3. Calcular os limites das pontas:
       - Esquerda: $\lim_{x \to \infty} \frac{x-1}{x} = 1$.
       - Direita: $\lim_{x \to \infty} \frac{x}{x} = 1$.
* **Veredito:** Pelo Teorema do Confronto, o limite é $\mathbf{1}$.

---

###  5. Limite com Raiz Conjugada de Alta Ordem
**Problema:** Calcule $\lim_{x \to 7} \frac{\sqrt{x+2} - 3}{x - 7}$

* **A Estratégia:** Eliminar a raiz que causa o $0/0$ usando o conjugado.
* **Passo a Passo:**
    1. Multiplicar pelo conjugado $\sqrt{x+2} + 3$:
       $$\lim_{x \to 7} \frac{(\sqrt{x+2} - 3)(\sqrt{x+2} + 3)}{(x - 7)(\sqrt{x+2} + 3)}$$
    2. O numerador vira Diferença de Quadrados: $(x+2) - 9 = x - 7$.
    3. Simplificar o termo problemático:
       $$\lim_{x \to 7} \frac{x - 7}{(x - 7)(\sqrt{x+2} + 3)} = \lim_{x \to 7} \frac{1}{\sqrt{x+2} + 3}$$
    4. Substituir $x=7$: $\frac{1}{\sqrt{9} + 3} = \frac{1}{3+3}$.
* **Veredito:** $\mathbf{1/6}$.