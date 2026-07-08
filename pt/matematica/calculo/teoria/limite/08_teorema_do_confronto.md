
# Teorema do Confronto(Teorema do Sanduíche)

**Definição e Intuição:**
O Teorema do Sanduíche (ou Teorema do Confronto) serve para encontrar o limite de uma função "complicada" comprimindo-a entre duas funções "simples" que têm o mesmo limite.

###  A Intuição do Corredor (Realidade)
Imagine que você está caminhando em um corredor estreito:
* À sua esquerda existe uma parede móvel ( $g(x)$ ).
* À sua direita existe outra parede móvel ( $h(x)$ ).
* Se as duas paredes se afunilam e se encontram exatamente em uma porta ( $L$ ), você, que está no meio ( $f(x)$ ), não tem escolha a não ser passar por essa mesma porta.

---

##  Formalização e o Exemplo Clássico

**A Regra Matemática:**
Se $g(x) \leq f(x) \leq h(x)$ para todos os valores próximos de $a$, e se:
$$\lim_{x \to a} g(x) = L \quad \text{e} \quad \lim_{x \to a} h(x) = L$$
Então, obrigatoriamente:
$$\lim_{x \to a} f(x) = L$$



###  Exemplo Passo a Passo: $\lim_{x \to \infty} \frac{\text{sen}(x)}{x}$

1.  **Identifique a oscilação:** O $\text{sen}(x)$ não tem limite no infinito (fica subindo e descendo entre -1 e 1).
2.  **Crie o "Sanduíche" (Limites Físicos):** Sabemos que o seno está sempre preso:
    $$-1 \leq \text{sen}(x) \leq 1$$
3.  **Monte a função do exercício:** Divida todos os lados por $x$ (considerando $x > 0$):
    $$\frac{-1}{x} \leq \frac{\text{sen}(x)}{x} \leq \frac{1}{x}$$
4.  **Aplique o limite nos "pães" (as extremidades):**
    * $\lim_{x \to \infty} \frac{-1}{x} = 0$
    * $\lim_{x \to \infty} \frac{1}{x} = 0$
**Conclusão:** Como a função do meio está espremida entre 0 e 0, o limite é 0.

---

##  Macetes e Casos de Prova

* **O Macete do "Limitado $\times$ Zero":** Sempre que você tiver uma função limitada (como seno ou cosseno) multiplicada por algo que vai a zero, o resultado do limite será sempre **Zero**.
* **Como identificar no papel:** Se você tentar substituir e der "Oscilação / Infinito", é Sanduíche na certa.
* **Cuidado com o Sinal:** Se você estiver dividindo por $x$ e o limite for para $-\infty$, o sinal da desigualdade inverte, mas o resultado do "esmagamento" costuma ser o mesmo.

> [!TIP] 
> **Conclusão**
> O Teorema do Sanduíche é a prova matemática de que uma oscilação finita não consegue resistir a um "esmagamento" em direção a um ponto ou ao zero no infinito. É a forma rigorosa de dizer que o **"zero" ganha de qualquer oscilação limitada**.

---

##  Seção de Exemplos Práticos

### Exemplo 1: O Cosseno ao Quadrado (Intervalo 0 a 1)
Calcule: $\lim_{x \to \infty} \frac{\cos^2(x)}{x^2 + 5}$
1.  **Monte o Sanduíche:** $\cos^2(x)$ está preso entre 0 e 1 (pois é ao quadrado): $0 \leq \cos^2(x) \leq 1$.
2.  **Construa a Função:** $\frac{0}{x^2 + 5} \leq \frac{\cos^2(x)}{x^2 + 5} \leq \frac{1}{x^2 + 5}$.
3.  **Veredito:** Como as extremidades vão para 0 quando $x \to \infty$, o limite é **0**.

### Exemplo 2: A Função com Módulo
Calcule: $\lim_{x \to 0} x^4 \cdot \text{sen}\left(\frac{1}{x}\right)$
1.  **Monte o Sanduíche:** $-1 \leq \text{sen}(1/x) \leq 1$.
2.  **Multiplique por $x^4$:** $-x^4 \leq x^4 \cdot \text{sen}(1/x) \leq x^4$.
3.  **Veredito:** Como $-x^4$ e $x^4$ vão para 0 quando $x \to 0$, o limite é **0**.

### Exemplo 3: Tangente Inversa (Arctan)
Calcule: $\lim_{x \to \infty} \frac{\text{arctg}(x)}{x}$
1.  **Identifique a Limitação:** A função $\text{arctg}(x)$ é limitada entre $-\pi/2$ e $\pi/2$.
2.  **Divida por $x$:** $\frac{-\pi/2}{x} \leq \frac{\text{arctg}(x)}{x} \leq \frac{\pi/2}{x}$.
3.  **Veredito:** Constante dividida por infinito é 0. O limite é **0**.

---

###  Atenção: Por que Tangente e Cossecante NÃO entram no Sanduíche?
* **Tangente ($\text{tg } x$):** Explode para o infinito em vários pontos ($\pi/2, 3\pi/2$). Não é limitada.
* **Cossecante ($\text{cosec } x$):** É $1/\text{sen } x$. Se o seno vai para zero, ela explode.

**O Sanduíche só aceita recheios que "cabem na embalagem" (funções limitadas).**