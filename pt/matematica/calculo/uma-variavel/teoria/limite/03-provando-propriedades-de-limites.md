---
id: provando_propriedades_limites
title: Provas Formais das Propriedades de Limites
---
# Provas Formais das Propriedades de Limites

Este documento constitui o módulo rigoroso de demonstrações matemáticas para as propriedades algébricas dos limites. Todas as provas aqui apresentadas utilizam estritamente a **definição formal de limite ($\epsilon-\delta$)** e teoremas de análise real.

Para tornar a construção dos limitadores ($\delta$) transparente e pedagogicamente acessível, as demonstrações mais complexas são acompanhadas por uma **Análise Regressiva (Análise Prévia)**. Essa etapa explicita o raciocínio dedutivo de trás para frente utilizado para determinar as tolerâncias antes da escrita da prova formal.

---

## Hipóteses Formais e Definições Básicas

Para todas as demonstrações subsequentes, assumimos a definição formal de limite:

$$\lim_{x \to a} f(x) = L \iff \forall \epsilon > 0, \exists \delta > 0 \text{ tal que } 0 < |x - a| < \delta \implies |f(x) - L| < \epsilon$$

Sempre que declararmos que $\lim_{x \to a} f(x) = L$ e $\lim_{x \to a} g(x) = M$, entende-se que para quaisquer $\epsilon_f, \epsilon_g > 0$, existem $\delta_f, \delta_g > 0$ correspondentes.

---

## 1. Limites Elementares (Propriedades Atômicas)

### Teorema 1.1: Limite da Função Constante
Se $f(x) = c$ para todo $x \in \mathbb{R}$, então $\lim_{x \to a} c = c$.

* **Análise Prévia:**  
  Queremos $|c - c| < \epsilon$. Como $|c - c| = 0$, a desigualdade $0 < \epsilon$ é identicamente verdadeira para todo $\epsilon > 0$. Logo, a escolha de $\delta$ é independente e arbitrária.

* **Demonstração Formal:**  
  Dado $\epsilon > 0$, escolha $\delta = 1$ (ou qualquer $\delta > 0$). Se $0 < |x - a| < \delta$, então $|c - c| = 0 < \epsilon$. $\blacksquare$

---

### Teorema 1.2: Limite da Função Identidade
Se $f(x) = x$, então $\lim_{x \to a} x = a$.

* **Análise Prévia:**  
  Queremos $|x - a| < \epsilon$. Como a condição de hipótese é $0 < |x - a| < \delta$, a relação entre $\delta$ e $\epsilon$ é direta ($1:1$). Basta definir $\delta = \epsilon$.

* **Demonstração Formal:**  
  Dado $\epsilon > 0$, defina $\delta = \epsilon$. Se $0 < |x - a| < \delta$, a implicação $0 < |x - a| < \epsilon$ é imediata. $\blacksquare$

---

## 2. Propriedades Aritméticas Fundamentais

### Teorema 2.1: Prova da Soma e Subtração
$$\lim_{x \to a} [f(x) \pm g(x)] = L \pm M$$

* **Análise Regressiva:**
  1. **Objetivo:** Garantir que $|(f(x) \pm g(x)) - (L \pm M)| < \epsilon$.
  2. **Rearranjo:** Pela Desigualdade Triangular, $|(f(x) - L) \pm (g(x) - M)| \le |f(x) - L| + |g(x) - M|$.
  3. **Partição de Erro:** Para que a soma seja estritamente menor que $\epsilon$, atribuímos a cada cota de erro o valor $\frac{\epsilon}{2}$.
  4. **Compatibilidade:** Definindo $\delta = \min(\delta_1, \delta_2)$, garantimos a validade simultânea para ambas as funções no mesmo vizinhança.

* **Demonstração Formal:**  
  Dado $\epsilon > 0$. Por hipótese, existem $\delta_1, \delta_2 > 0$ tais que:
  * $0 < |x - a| < \delta_1 \implies |f(x) - L| < \frac{\epsilon}{2}$
  * $0 < |x - a| < \delta_2 \implies |g(x) - M| < \frac{\epsilon}{2}$

  Seja $\delta = \min(\delta_1, \delta_2)$. Para $0 < |x - a| < \delta$:

  $$|(f(x) \pm g(x)) - (L \pm M)| \le |f(x) - L| + |g(x) - M| < \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon \quad \blacksquare$$

---

### Teorema 2.2: Prova do Produto por Constante
$$\lim_{x \to a} [k \cdot f(x)] = k \cdot L$$

* **Análise Regressiva:**
  1. **Objetivo:** $|k \cdot f(x) - k \cdot L| < \epsilon \iff |k| \cdot |f(x) - L| < \epsilon$.
  2. **Isolamento de Termos:** Para $k \neq 0$, exige-se $|f(x) - L| < \frac{\epsilon}{|k|}$.
  3. **Conclusão:** O parâmetro $\epsilon_f$ da função $f(x)$ deve ser ajustado proporcionalmente ao escalar $|k|$.

* **Demonstração Formal:**  
  * **Caso $k = 0$:** $|0 \cdot f(x) - 0 \cdot L| = 0 < \epsilon$, válido para todo $\delta > 0$.
  * **Caso $k \neq 0$:** Dado $\epsilon > 0$, escolha $\epsilon_f = \frac{\epsilon}{|k|} > 0$. Pela definição de limite, existe $\delta > 0$ tal que $0 < |x - a| < \delta \implies |f(x) - L| < \frac{\epsilon}{|k|}$.

  Multiplicando a desigualdade por $|k|$:

  $$|k \cdot f(x) - k \cdot L| = |k| \cdot |f(x) - L| < |k| \cdot \frac{\epsilon}{|k|} = \epsilon \quad \blacksquare$$

---

### Teorema 2.3: Prova do Produto Geral
$$\lim_{x \to a} [f(x) \cdot g(x)] = L \cdot M$$

* **Análise Regressiva:**
  1. **Objetivo:** $|f(x)g(x) - LM| < \epsilon$.
  2. **Identidade Algébrica:** Somando e subtraindo $Lg(x)$, obtemos:
     $$f(x)g(x) - LM = g(x)(f(x) - L) + L(g(x) - M)$$
  3. **Majorando pela Desigualdade Triangular:**
     $$|f(x)g(x) - LM| \le |g(x)||f(x) - L| + |L||g(x) - M|$$
  4. **Limitando o Termo $g(x)$:** Para evitar dependência funcional no limite, limitamos $g(x)$ em uma vizinhança restrita: escolhendo $|g(x) - M| < 1$, garante-se $|g(x)| < |M| + 1$.
  5. **Distribuição de Erros:** Exige-se que cada uma das duas parcelas seja menor que $\frac{\epsilon}{2}$:
     * $|f(x) - L| < \frac{\epsilon}{2(|M| + 1)}$
     * $|g(x) - M| < \frac{\epsilon}{2(|L| + 1)}$

* **Demonstração Formal:**  
  Dado $\epsilon > 0$:
  1. Existe $\delta_1 > 0$ tal que $0 < |x - a| < \delta_1 \implies |g(x) - M| < 1 \implies |g(x)| < |M| + 1$.
  2. Existe $\delta_2 > 0$ tal que $0 < |x - a| < \delta_2 \implies |f(x) - L| < \frac{\epsilon}{2(|M| + 1)}$.
  3. Existe $\delta_3 > 0$ tal que $0 < |x - a| < \delta_3 \implies |g(x) - M| < \frac{\epsilon}{2(|L| + 1)}$.

  Definindo $\delta = \min(\delta_1, \delta_2, \delta_3)$, para $0 < |x - a| < \delta$:

  $$|f(x)g(x) - LM| \le |g(x)||f(x) - L| + |L||g(x) - M|$$
  $$< (|M| + 1) \frac{\epsilon}{2(|M| + 1)} + |L| \frac{\epsilon}{2(|L| + 1)} = \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon \quad \blacksquare$$

---

### Teorema 2.4: Prova do Quociente
$$\lim_{x \to a} \frac{f(x)}{g(x)} = \frac{L}{M} \quad (\text{com } M \neq 0)$$

* **Análise Regressiva:**
  Reduz-se o problema ao cálculo do limite do inverso $\lim \frac{1}{g(x)} = \frac{1}{M}$ e aplica-se o Teorema 2.3.
  1. **Objetivo do Inverso:** $\left|\frac{1}{g(x)} - \frac{1}{M}\right| = \frac{|M - g(x)|}{|M||g(x)|} < \epsilon$.
  2. **Cota Inferior para $|g(x)|$:** Para evitar que o denominador se aproxime de zero, impõe-se $|g(x) - M| < \frac{|M|}{2}$. Isso garante $|g(x)| > \frac{|M|}{2} \implies \frac{1}{|g(x)|} < \frac{2}{|M|}$.
  3. **Majorativo do Erro:**
     $$\frac{|M - g(x)|}{|M||g(x)|} < \frac{2 |g(x) - M|}{|M|^2}$$
  4. **Isolamento de $\epsilon_g$:** Para limitar a expressão por $\epsilon$, impõe-se $|g(x) - M| < \frac{|M|^2 \epsilon}{2}$.

* **Demonstração Formal:**  
  Dado $\epsilon > 0$:
  1. Existe $\delta_1$ tal que $0 < |x - a| < \delta_1 \implies |g(x) - M| < \frac{|M|}{2} \implies \frac{1}{|g(x)|} < \frac{2}{|M|}$.
  2. Existe $\delta_2$ tal que $0 < |x - a| < \delta_2 \implies |g(x) - M| < \frac{|M|^2 \epsilon}{2}$.

  Para $\delta = \min(\delta_1, \delta_2)$:

  $$\left| \frac{1}{g(x)} - \frac{1}{M} \right| = \frac{|M - g(x)|}{|M||g(x)|} < \frac{2}{|M|^2} \cdot \frac{|M|^2 \epsilon}{2} = \epsilon$$

  Por aplicação direta do Teorema 2.3 para o produto de $f(x)$ por $\frac{1}{g(x)}$, conclui-se que $\lim \frac{f(x)}{g(x)} = \frac{L}{M}$. $\blacksquare$

---

## 3. Substituição Direta em Polinômios

### Teorema 3.1: Potência Inteira ($x^n$)
$$\lim_{x \to a} x^n = a^n \quad (\forall n \in \mathbb{N})$$

* **Demonstração (Por Indução Finita sobre $n$):**
  * **Base Indutiva ($n=1$):** $\lim_{x \to a} x = a^1 = a$ (Provado no Teorema 1.2).
  * **Passo Indutivo:** Assuma a validade para $n = k$, isto é, $\lim_{x \to a} x^k = a^k$. Para $n = k+1$:
    $$\lim_{x \to a} x^{k+1} = \lim_{x \to a} (x^k \cdot x) = \left(\lim_{x \to a} x^k\right) \cdot \left(\lim_{x \to a} x\right) = a^k \cdot a = a^{k+1}$$
    (pela propriedade do produto — Teorema 2.3). Por indução finita, a igualdade é válida para todo $n \in \mathbb{N}$. $\blacksquare$

---

### Teorema 3.2: Substituição Polinomial Geral
Se $P(x) = c_n x^n + c_{n-1} x^{n-1} + \dots + c_0$, então $\lim_{x \to a} P(x) = P(a)$.

* **Demonstração:**  
  Por encadeamento finito das propriedades operatórias de soma (Teorema 2.1), produto por constante (Teorema 2.2) e potência inteira (Teorema 3.1):

  $$\lim_{x \to a} P(x) = \lim_{x \to a} \left( \sum_{i=0}^n c_i x^i \right) = \sum_{i=0}^n c_i \left( \lim_{x \to a} x^i \right) = \sum_{i=0}^n c_i a^i = P(a) \quad \blacksquare$$

---

## 4. Potência Geral e Radiciação

### Teorema 4.1: Prova da Raiz Quadrada ($\sqrt{f(x)}$)
$$\lim_{x \to a} \sqrt{f(x)} = \sqrt{L} \quad (\text{para } L > 0 \text{ e } f(x) \ge 0)$$

* **Análise Regressiva:**
  1. **Objetivo:** $|\sqrt{f(x)} - \sqrt{L}| < \epsilon$.
  2. **Racionalização de Expressão:**
     $$|\sqrt{f(x)} - \sqrt{L}| \cdot \frac{\sqrt{f(x)} + \sqrt{L}}{\sqrt{f(x)} + \sqrt{L}} = \frac{|f(x) - L|}{\sqrt{f(x)} + \sqrt{L}}$$
  3. **Majorante Conservador:** Como $f(x) \ge 0$, temos $\sqrt{f(x)} \ge 0$. Logo, $\sqrt{f(x)} + \sqrt{L} \ge \sqrt{L}$. Substituindo o denominador por um valor estritamente menor, majora-se a fração:
     $$\frac{|f(x) - L|}{\sqrt{f(x)} + \sqrt{L}} \le \frac{|f(x) - L|}{\sqrt{L}}$$
  4. **Condição sobre $f(x)$:** Para que $\frac{|f(x) - L|}{\sqrt{L}} < \epsilon$, impõe-se $|f(x) - L| < \epsilon \sqrt{L}$.

* **Demonstração Formal:**  
  Dado $\epsilon > 0$, defina a cota de erro da função interna como $\epsilon_f = \epsilon \sqrt{L} > 0$.  
  Como $\lim_{x \to a} f(x) = L$, existe $\delta > 0$ tal que $0 < |x - a| < \delta \implies |f(x) - L| < \epsilon \sqrt{L}$.

  Aplicando a estimativa majorante:

  $$|\sqrt{f(x)} - \sqrt{L}| \le \frac{|f(x) - L|}{\sqrt{L}} < \frac{\epsilon \sqrt{L}}{\sqrt{L}} = \epsilon \quad \blacksquare$$

---

## 5. Funções Transcendentes e Compostas

### Teorema 5.1: Limite da Função Composta
Se $\lim_{x \to a} g(x) = L$ e $f$ é uma função **contínua em $L$** ($\lim_{y \to L} f(y) = f(L)$), então:

$$\lim_{x \to a} f(g(x)) = f\left(\lim_{x \to a} g(x)\right) = f(L)$$

* **Análise Regressiva:**
  A continuidade de $f$ em $L$ garante que a variação de saída $|f(y) - f(L)|$ seja arbitrariamente pequena desde que a variação de entrada $|y - L|$ esteja sob controle. A função interna $g(x)$ atua como o gerador do argumento $y$, devendo ter sua imagem contida no raio de tolerância de $f$.

* **Demonstração Formal:**  
  1. Pela continuidade de $f$ em $L$, dado $\epsilon > 0$, existe $\eta > 0$ tal que:
     $$|y - L| < \eta \implies |f(y) - f(L)| < \epsilon$$
  2. Como $\lim_{x \to a} g(x) = L$, tomando $\eta > 0$ como a cota de erro para $g(x)$, existe $\delta > 0$ tal que:
     $$0 < |x - a| < \delta \implies |g(x) - L| < \eta$$
  3. Substituindo $y = g(x)$, encadeiam-se as implicações:  
     $$0 < |x - a| < \delta \implies |g(x) - L| < \eta \implies |f(g(x)) - f(L)| < \epsilon \quad \blacksquare$$

---

### Corolário 5.2: Aplicação às Funções Transcendentes
Se $h(y)$ representa uma função transcendente elementar ($\sin(y)$, $\cos(y)$, $\ln(y)$, $e^y$) contínua no ponto $L$:

$$\lim_{x \to a} h(f(x)) = h\left(\lim_{x \to a} f(x)\right) = h(L)$$

* **Demonstração:**  
  Consequência direta do Teorema 5.1, considerando a continuidade da função $h$ em seu respectivo domínio real. $\blacksquare$