---
id: teorema-do-confronto
title: Teorema do Confronto
---
# Teorema do Confronto

Ao calcular limites de funções matemáticas, frequentemente encontramos expressões cuja avaliação direta é inviável devido a oscilações incessantes ou comportamentos indeterminados. Nesses cenários, as técnicas algébricas convencionais, como a fatoração de polinômios ou o cancelamento de termos, revelam-se insuficientes. Surge, então, uma indagação fundamental: como determinar a tendência assintótica de uma função cujo comportamento exato é complexo ou desconhecido, mas cujos limites superior e inferior podem ser estritamente delimitados?

---

## O Princípio do Prensamento

Para compreender a essência desse problema, considere o comportamento de uma partícula confinada a se mover entre dois limites físicos em aproximação. Suponha que três trajetórias contínuas sejam descritas ao longo de um domínio comum. Duas dessas trajetórias funcionam como fronteiras invioláveis: uma delimita a trajetória por baixo, enquanto a outra a delimita por cima.

À medida que a variável independente se aproxima de um determinado valor crítico, observa-se que as trajetórias inferior e superior convergem progressivamente para uma mesma posição final. A partícula situada entre ambas não possui a liberdade de desviar-se além das fronteiras estabelecidas. Consequentemente, se a barreira inferior e a barreira superior se encontram exatamente no mesmo ponto, o estado da trajetória intermediária é inevitavelmente determinado por essa convergência conjunta.

Esse fenômeno de aprisionamento e compressão assintótica constitui a base intuitiva para a análise de funções oscilatórias comprimidas. Se uma função complexa puder ser "prensada" entre duas funções mais simples cujos comportamentos no ponto de interesse sejam conhecidos e idênticos, o limite da função intermediária estará completamente determinado.

---

## Formalização e Mecânica do Teorema

A formalização rigorosa desta intuição geométrica é conhecida como Teorema do Confronto (ou Teorema do Sanduíche).

### Enunciado Formal

Sejam $g(x)$, $f(x)$ e $h(x)$ funções definidas em um intervalo aberto contendo o ponto $a$, exceto possivelmente no próprio ponto $a$. Se, para todo $x$ nesse intervalo (com $x \neq a$), for satisfeita a desigualdade:

$$g(x) \le f(x) \le h(x)$$

e se os limites das funções extremas no ponto $a$ existirem e forem iguais, isto é:

$$\lim_{x \to a} g(x) = L \quad \text{e} \quad \lim_{x \to a} h(x) = L$$

então o limite da função intermediária $f(x)$, quando $x$ tende a $a$, existe e é dado por:

$$\lim_{x \to a} f(x) = L$$

![Representação geométrica do Teorema do Confronto](../../../../../../assets/squeeze-theorem.svg)
*Figura 1: Representação geométrica do Teorema do Confronto (Squeeze Theorem). A função intermediária $f(x)$ permanece comprimida entre a fronteira superior $h(x)$ e a inferior $g(x)$. Como ambas as curvas extremas tendem ao mesmo valor $L$ no ponto $x = a$, a função $f(x)$ é forçada a convergir para o mesmo limite $L$.*

---

## Corolários e Propriedades Derivadas

Uma das aplicações mais férteis do Teorema do Confronto ocorre quando analisamos o produto de uma função que tende a zero por uma função cujo valor permanece limitado em todo o seu domínio.

### O Teorema do Anulamento (Limitada $\times$ Nula)

Seja $f(x) = g(x) \cdot h(x)$. Se $\lim_{x \to a} g(x) = 0$ e se a função $h(x)$ for limitada em uma vizinhança de $a$ (isto é, existem constantes reais $M > 0$ e $N > 0$ tais que $-M \le h(x) \le N$ para todo $x \neq a$), então:

$$\lim_{x \to a} [g(x) \cdot h(x)] = 0$$

#### Demonstração

Pela limitação de $h(x)$, temos que, para todo $x$ na vizinhança considerada:

$$-M \le h(x) \le N$$

Assumindo inicialmente que $g(x) \ge 0$ à medida que $x$ se aproxima de $a$, multiplicamos todos os membros da desigualdade por $g(x)$:

$$-M \cdot g(x) \le g(x) \cdot h(x) \le N \cdot g(x)$$

Aplicando o limite quando $x \to a$ aos termos das extremidades:

$$\lim_{x \to a} [-M \cdot g(x)] = -M \cdot \lim_{x \to a} g(x) = -M \cdot 0 = 0$$

$$\lim_{x \to a} [N \cdot g(x)] = N \cdot \lim_{x \to a} g(x) = N \cdot 0 = 0$$

Como os limites de ambas as extremidades são iguais a $0$, o Teorema do Confronto estabelece diretamente que:

$$\lim_{x \to a} [g(x) \cdot h(x)] = 0$$

Uma análise análoga aplica-se aos casos em que $g(x) < 0$, confirmando a validade geral da propriedade através da limitação em módulo $|g(x) \cdot h(x)| \le K \cdot |g(x)|$.

---

## Aplicações Estruturais e Limitações do Modelo

O Teorema do Confronto desempenha um papel fundamental na construção dos alicerces do Cálculo Diferencial e Integral. Ele é a ferramenta primordial utilizada na demonstração do **Limite Fundamental Trigonométrico**:

$$\lim_{x \to 0} \frac{\sin(x)}{x} = 1$$

Esta identidade, estabelecida geometricamente por meio da comparação entre as áreas de triângulos e do setor circular unitário, permite derivar posteriormente as propriedades de todas as funções trigonométricas.

### Restrições de Aplicabilidade

A escolha das funções limitantes $g(x)$ e $h(x)$ requer rigor. Uma falha comum na aplicação do teorema ocorre quando se utilizam funções limitantes cujos limites no ponto $a$ não coincidem. Se $\lim_{x \to a} g(x) = L_1$ e $\lim_{x \to a} h(x) = L_2$, com $L_1 \neq L_2$, o teorema não fornece qualquer informação sobre a existência ou o valor do limite de $f(x)$.

Além disso, o método exige que a função intermediária seja estritamente limitada no intervalo considerado. Funções como a tangente ($\tan(x)$) ou a cossecante ($\csc(x)$) possuem descontinuidades assintóticas verticais no domínio real, não sendo limitadas em vizinhanças de seus pontos singulares e inviabilizando o enquadramento direto.

---

## Resolução de Problemas

### Exemplo 1: Convergência no Infinito de Razões Trigonométricas

Determine o valor do limite:

$$\lim_{x \to \infty} \frac{\sin(x)}{x}$$

#### Solução

1. **Identificação do comportamento das componentes:** A função seno satisfaz a limitação de amplitude padrão para todo $x \in \mathbb{R}$:

   $$-1 \le \sin(x) \le 1$$

2. **Construção das desigualdades:** Considerando o domínio em que $x > 0$ (visto que $x \to \infty$), dividimos todos os termos da desigualdade por $x$:

   $$-\frac{1}{x} \le \frac{\sin(x)}{x} \le \frac{1}{x}$$

3. **Cálculo dos limites das extremidades:**

   $$\lim_{x \to \infty} \left(-\frac{1}{x}\right) = 0$$

   $$\lim_{x \to \infty} \left(\frac{1}{x}\right) = 0$$

4. **Conclusão via Teorema do Confronto:** Como a função $f(x) = \frac{\sin(x)}{x}$ está limitada entre duas expressões que tendem a $0$ quando $x \to \infty$, conclui-se rigorosamente que:

   $$\lim_{x \to \infty} \frac{\sin(x)}{x} = 0$$

---

### Exemplo 2: Amortecimento Polinomial em Torno da Origem

Calcule o limite:

$$\lim_{x \to 0} x^4 \sin\left(\frac{1}{x}\right)$$

#### Solução

1. **Análise da descontinuidade:** A expressão $\sin(1/x)$ apresenta oscilação de frequência infinita à medida que $x$ se aproxima de $0$. O limite direto por substituição é indefinido.

2. **Aplicação do enquadramento:** Sabendo que a imagem da função seno está contida no intervalo $[-1, 1]$, temos:

   $$-1 \le \sin\left(\frac{1}{x}\right) \le 1 \quad \forall x \neq 0$$

3. **Multiplicação pelo fator $x^4$:** Como $x^4 > 0$ para todo $x \neq 0$, preserva-se o sentido das desigualdades:

   $$-x^4 \le x^4 \sin\left(\frac{1}{x}\right) \le x^4$$

4. **Avaliação dos limites extremos:**

   $$\lim_{x \to 0} (-x^4) = 0$$

   $$\lim_{x \to 0} x^4 = 0$$

5. **Aplicação do Teorema do Anulamento:** Ambas as extremidades convergem para $0$. Portanto:

   $$\lim_{x \to 0} x^4 \sin\left(\frac{1}{x}\right) = 0$$

---

### Exemplo 3: Limites Envolvendo Relações de Arco-Tangente

Calcule o limite:

$$\lim_{x \to \infty} \frac{\arctan(x)}{x}$$

#### Solução

1. **Análise da limitação do arco-tangente:** A imagem da função $y = \arctan(x)$ é estritamente limitada por assíntotas horizontais em $y = \pm \frac{\pi}{2}$:

   $$-\frac{\pi}{2} < \arctan(x) < \frac{\pi}{2} \quad \forall x \in \mathbb{R}$$

2. **Divisão pela variável $x$ ($x > 0$):**

   $$-\frac{\pi}{2x} < \frac{\arctan(x)}{x} < \frac{\pi}{2x}$$

3. **Cálculo dos limites:**

   $$\lim_{x \to \infty} \left(-\frac{\pi}{2x}\right) = 0$$

   $$\lim_{x \to \infty} \left(\frac{\pi}{2x}\right) = 0$$

4. **Veredito:** Pelo Teorema do Confronto:

   $$\lim_{x \to \infty} \frac{\arctan(x)}{x} = 0$$