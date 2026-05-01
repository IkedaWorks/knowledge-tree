
# Riemann Sums (Somas de Riemann e a Origem)

### O Sonho de Medir a Curva

Desde a Antiguidade, o homem sabe medir retângulos ($A = b \cdot h$). O problema surge quando a natureza apresenta curvas. Como medir a área sob uma parábola ou dentro de um círculo?

**A Intuição:** Se não podemos medir a curva diretamente, vamos "espremê-la" entre formas que conhecemos. A integral é, em essência, o processo de tornar essa aproximação tão perfeita que o erro desaparece.

---

### Do Método da Exaustão à Soma de Riemann

#### 1. A Herança Grega: O Método da Exaustão

Antes de Newton e Leibniz, matemáticos como Arquimedes usavam a **exaustão**.

- **O Processo:** Para medir a área de um círculo, ele desenhava polígonos dentro (inscritos) e fora (circunscritos).
    
- **A Lógica:** Conforme você aumenta o número de lados do polígono (hexágono, octógono, dodecágono...), a área do polígono "ocupa" quase todo o círculo.
    
- **O Limite:** Arquimedes "exauria" (esgotava) a área vazia. Ele chegou muito perto do valor de $\pi$ sem possuir o conceito formal de "limite".
    

> [!TIP]
> 
> **Exemplo Prático:** Imagine dividir um círculo em diversos triângulos (como fatias de pizza). Como a área do triângulo é conhecida ($A = \frac{b \cdot h}{2}$), conseguimos estimar a área do círculo. À medida que aumentamos o número de triângulos, a soma de suas áreas se aproxima do valor real da área do círculo.

#### 2. A Formalização: A Integral de Riemann

No século XIX, Bernhard Riemann refinou essa ideia para funções no plano cartesiano, trocando polígonos por **retângulos verticais**.

**A Mecânica da Soma:**

Para calcular a área sob uma função $f(x)$ no intervalo $[a, b]$:

1. **Partição:** Dividimos o intervalo em $n$ pedaços de largura $\Delta x = \frac{b-a}{n}$.
    
2. **Escolha da Altura:** Em cada pedaço, escolhemos um ponto $x_i^*$ para determinar a altura do retângulo $f(x_i^*)$.
    
3. **A Soma:** Somamos a área de todos os $n$ retângulos:
    
    $$S_n = \sum_{i=1}^{n} f(x_i^*) \cdot \Delta x$$
    

---

### O Salto para a Integral

A área real ($A$) é o **limite** dessa soma quando o número de retângulos tende ao infinito e a largura de cada um tende a zero:

$$A = \lim_{n \to \infty} \sum_{i=1}^{n} f(x_i^*) \cdot \Delta x = \int_{a}^{b} f(x) \, dx$$

#### A "Mágica" do S Longo

A notação de integral $\int$ é, na verdade, um **S** estilizado (de _Summa_).

- O $f(x)$ representa a **altura** (o valor da função).
    
- O $dx$ representa a **base infinitesimal** (o $\Delta x$ que ficou infinitamente fino).
    

---

### Conclusão: O que aprendemos?

- **O Erro Diminui:** Quanto mais retângulos, mais precisa é a soma. No infinito, o erro é zero.
    
- **Sinal Importa:** Diferente da geometria grega (onde área é sempre positiva), a Integral de Riemann considera a posição. Se o retângulo está abaixo do eixo $x$, a "altura" $f(x)$ é negativa, gerando uma área negativa.
    
- **Área Líquida:** A integral calcula o balanço entre o que está acima (positivo) e o que está abaixo (negativo) do eixo $x$.