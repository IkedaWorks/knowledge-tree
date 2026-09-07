
# Integral Definida

### Definição e Intuição

A integral definida é o processo de calcular o **acúmulo líquido** de uma grandeza em um intervalo específico $[a, b]$. Enquanto a integral indefinida busca uma função (uma regra), a definida busca um **número real** (um resultado).

**A Intuição:** Imagine que você tem uma função que descreve a velocidade de um objeto. Se você quer saber a distância total percorrida entre o segundo $2$ e o segundo $10$, você não quer apenas a "fórmula" da posição (que a integral indefinida fornece); você quer o **valor final**. A integral definida "fatia" esse intervalo em infinitos pedaços minúsculos, calcula o valor em cada um e soma tudo.

---

### Formalização e Geometria

#### Formalização (Soma de Riemann)

A integral definida é o limite de uma soma de infinitos retângulos cujas larguras tendem a zero:

$$\int_{a}^{b} f(x) \, dx = \lim_{n \to \infty} \sum_{i=1}^{n} f(x_i^*) \Delta x$$

#### Interpretação Geométrica (Área com Sinal)

Diferente da área da geometria plana convencional, a integral definida leva em conta a posição no gráfico:

- **Acima do eixo $x$:** A integral acumula valor **positivo**.
    
- **Abaixo do eixo $x$:** A integral acumula valor **negativo**.
    

O resultado final é o **balanço líquido**: a soma das áreas acima do eixo menos as áreas abaixo dele.

---

### Conclusão e Aplicação Física

#### A Diferença de Natureza

- **Sem limites ($\int f(x) \, dx$):** Retorna uma **Função** (Indefinida/Antiderivada). Responde: _"Qual é a lei de formação?"_.
    
- **Com limites ($\int_{a}^{b} f(x) \, dx$):** Retorna um **Número** (Definida). Responde: _"Quanto foi o total acumulado?"_.
    

#### Interpretação Física

Se $f(t)$ representa uma taxa de variação (como velocidade, corrente elétrica ou densidade de carga), a integral definida no intervalo $[a, b]$ calcula a quantidade total da grandeza acumulada naquele período ou espaço.

**Exemplo:** $\int_{t_1}^{t_2} v(t) \, dt = \Delta s$ (deslocamento total).

> [!NOTE]
> 
> Observe que aqui usamos $dt$ em vez de $dx$ porque, fisicamente, estamos integrando a velocidade (que é a derivada do espaço) em relação ao **tempo**.

**Exemplo Simples:** Para uma função constante $f(x) = 3$ no intervalo de $1$ a $5$, a integral é $3 \cdot (5-1) = 12$. Graficamente, isso é idêntico a calcular a área de um retângulo de base $4$ e altura $3$.

---

> [!TIP]
> 
> **Conclusão:** A integral definida é a ferramenta de medição do Cálculo. Ela transforma funções abstratas em valores concretos (massa, carga, energia, distância). É o fechamento prático de todo o processo de derivação e integração.