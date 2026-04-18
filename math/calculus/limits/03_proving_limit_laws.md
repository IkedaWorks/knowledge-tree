
# Proving Limit Laws: The Formal Foundation

Provar as propriedades dos limites significa demonstrar que o controle do erro na entrada ($\delta$) é suficiente para garantir a precisão na saída ($\epsilon$), mesmo quando combinamos duas funções diferentes.

### ⚙️ A Intuição da "Engrenagem Acoplada"
Imagine duas máquinas independentes ($f$ e $g$). Se ambas são precisas, a combinação delas (soma ou produto) também deve ser precisa. O desafio da prova formal é descobrir o novo "ajuste" ($\delta_{total}$) que atenda aos requisitos de ambas as máquinas simultaneamente.

---

## 📐 Formalização das Provas
Para todas as provas abaixo, partimos da premissa que os limites individuais existem:
* $\lim_{x \to a} f(x) = L$ (Para qualquer $\epsilon_f > 0$, existe $\delta_f$)
* $\lim_{x \to a} g(x) = M$ (Para qualquer $\epsilon_g > 0$, existe $\delta_g$)

### 1. Prova da Soma: $\lim [f(x) + g(x)] = L + M$
**O Alvo:** Queremos garantir que $|(f(x) + g(x)) - (L + M)| < \epsilon$.

**A Manobra (Desigualdade Triangular):**
Usamos a propriedade matemática que diz que o módulo da soma é menor ou igual à soma dos módulos:
$$|(f(x) - L) + (g(x) - M)| \leq |f(x) - L| + |g(x) - M|$$

**A Prova:**
1. Escolhemos um erro individual de $\epsilon/2$ para cada função.
2. Pela definição, existem $\delta_1$ e $\delta_2$ tais que $|f(x)-L| < \epsilon/2$ e $|g(x)-M| < \epsilon/2$.
3. Se escolhermos o mais restritivo, $\delta = \min(\delta_1, \delta_2)$, garantimos que ambas as condições são satisfeitas:
   $$|f(x)-L| + |g(x)-M| < \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon$$

**Conclusão:** O limite da soma é rigorosamente a soma dos limites.

---

### 2. Prova da Constante: $\lim [k \cdot f(x)] = k \cdot L$
**O Alvo:** $|k \cdot f(x) - k \cdot L| < \epsilon$.

**A Manobra:** Colocamos a constante em evidência: $|k| \cdot |f(x) - L| < \epsilon$.

**A Prova:**
1. Precisamos que a distância entre a função e seu alvo seja: $|f(x) - L| < \frac{\epsilon}{|k|}$.
2. Como sabemos que $\lim f(x) = L$, a definição de limite garante que existe um $\delta$ para **qualquer** desafio de erro, inclusive para o valor específico $\frac{\epsilon}{|k|}$.

**Conclusão:** A constante apenas escala o erro (como um ganho de amplificador), mas não impede a convergência do limite.

---

## 🧠 Insight de Engenheiro
Nas provas formais, o uso do $\min(\delta_1, \delta_2, \dots)$ é como o **projeto de um sistema tolerante a falhas**: você identifica o componente mais sensível (o menor delta) e ajusta todo o sistema com base nele para garantir que ninguém saia da margem de segurança ($\epsilon$).

> [!TIP]
> **Feynman Style:** A Desigualdade Triangular é basicamente dizer que "o caminho direto entre dois pontos é sempre menor ou igual à soma dos desvios". Se os desvios são pequenos, a distância total também será.