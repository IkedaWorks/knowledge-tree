
# Continuity of Functions: The Seamless Flow

**Definição e Intuição:**
Uma função é contínua se você consegue desenhar o gráfico dela sem tirar a caneta do papel. Se houver um buraco, um salto ou uma explosão vertical, a continuidade foi quebrada.

### 💡 A Intuição do Interruptor (Realidade)
* **Contínuo:** É como um *dimmer* de luz. Você gira e a luminosidade aumenta suavemente de 0% a 100%, passando por todos os valores intermediários.
* **Descontínuo:** É um interruptor comum (liga/desliga). Você está no 0 e, num estalo, pula para o 1. Não existe o "0,5" no momento do clique. Há um salto.

---

## 📐 Formalização (O Teste dos 3 Passos)

Para dizer que uma função é contínua em um ponto específico $x = a$, ela precisa passar em três testes obrigatórios:

1.  **A função existe no ponto?** $f(a)$ precisa estar definido (não pode resultar em $0/0$ ou raiz de número negativo).
2.  **O limite existe no ponto?** $\lim_{x \to a} f(x)$ precisa existir (limites laterais iguais).
3.  **O limite é igual ao valor da função?** $\lim_{x \to a} f(x) = f(a)$. O "alvo" da tendência tem que ser exatamente onde o ponto real está desenhado.

### 📝 Exemplo Passo a Passo: Verificando a Continuidade
Verifique se $f(x) = \frac{x^2 - 1}{x - 1}$ é contínua em $x = 1$.
* **Passo 1 ($f(1)$ existe?):** $f(1) = \frac{1^2 - 1}{1 - 1} = \frac{0}{0}$. Não existe.
* **Veredito:** A função é **descontínua** em $x = 1$. Há um "buraco" no gráfico.

---

## 🛠️ Tipos de Descontinuidade e Macetes

Existem três formas principais de "quebrar" uma função:

1.  **Removível (Buraco):** O limite existe, mas o ponto não está lá ou está no lugar errado. 
    * *Macete:* É quando você consegue simplificar a fração (cortar termos).
2.  **Salto (Pulo):** Os limites laterais são diferentes. Comum em funções por partes.
    * *Macete:* O "trem" da esquerda chega em uma altura e o da direita em outra.
3.  **Infinita (Assíntota):** A função explode para o infinito.
    * *Macete:* Divisão por zero onde o numerador não é zero.



---

## 📝 Seção de Exemplos e Exercícios

### Exemplo 1: O "Conserto" de Função
Determine $k$ para que $f(x)$ seja contínua em $x = 2$:


$$
f(x) = \begin{cases} x + 3, & x < 2 \\\\ k, & x = 2 \\\\ 3x - 1, & x > 2 \end{cases}
$$


1. **Limite pela esquerda:** $2 + 3 = 5$.
2. **Limite pela direita:** $3(2) - 1 = 5$.
3. **Veredito:** O limite global é 5. Para fechar o buraco e ser contínua, o ponto $f(2)$ deve ser igual ao limite. Logo, **$k = 5$**.

### Exemplo 2: A Função com "Buraco"
Verifique se $f(x) = \frac{x^2 - 4}{x - 2}$ é contínua em $x = 2$.
1. **Teste 1 ($f(2)$ existe?):** $f(2) = 0/0$. Não definido.
2. **Teste 2 (O limite existe?):** $\lim_{x \to 2} \frac{(x-2)(x+2)}{x-2} = \lim_{x \to 2} (x+2) = 4$.
3. **Veredito:** Descontínua no ponto $x = 2$, mas o limite existe e vale 4.

### Exemplo 3: Encontrando a Incógnita $k$
Determine $k$ para que $f(x)$ seja contínua em todo o domínio:

$$
f(x) = \begin{cases} kx^2, & x \le 2 \\\\ 10 - kx, & x > 2 \end{cases}
$$


1. **Igualando os lados no ponto de transição ($x=2$):**
   * Lado esquerdo: $k(2)^2 = 4k$.
   * Lado direito: $10 - k(2) = 10 - 2k$.
2. **Resolvendo:** $4k = 10 - 2k \implies 6k = 10 \implies k = 5/3$.

---

## 📜 O Teorema do Valor Intermediário (TVI)
Se uma função é contínua em um intervalo e ela começa no $y = -2$ e termina no $y = 5$, ela obrigatoriamente passou pelo zero (ou por qualquer valor entre -2 e 5) em algum momento.
* **Macete:** Se você atravessou a rua, em algum momento você esteve exatamente no meio dela. Isso prova que equações têm raízes sem precisar resolvê-las.



---

## 💡 Macetes de Resolução
* **Polinômios são "Bonzinhos":** Se a função for apenas um polinômio simples, ela é contínua em toda a reta real.
* **Onde procurar problemas:** As descontinuidades moram onde o **denominador zera** ou onde a função **"muda de regra"**.
* **Dica Visual:** Se o limite lateral deu diferente, é um **Salto**. Se o limite deu igual, mas a função não existe ali, é um **Buraco**.

### 🔗 Connections
- [10. Intermediate Value Theorem (TVI)](10_intermediate_value_theorem.md)
- [06. One-Sided Limits](06_one_sided_limits.md)
- [11. Asymptotes](11_asymptotes.md)