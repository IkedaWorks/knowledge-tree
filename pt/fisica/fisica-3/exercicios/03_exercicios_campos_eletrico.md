# Problemas Práticos: Campos Elétricos em Múltiplos Níveis e Mecânica Vetorial

Este módulo contém um conjunto progressivo de problemas projetados para avaliar sua intuição espacial, habilidades de integração contínua e o domínio de conceitos fundamentais de física e matemática.

> [!TIP]
> **Regra Metacognitiva para Estudos de Engenharia:** Não pule direto para o Manual de Soluções. Force seu cérebro a modelar as condições de contorno, esboce os vetores posição relativos no papel e execute a análise dimensional de sua expressão algébrica final antes de checar a resolução. A verdadeira competência em engenharia é construída durante o esforço de tradução do problema, não na leitura passiva de respostas.

---

##  Seção 1: Fundamentos e Cinemática (Nível Fácil)

### Problema 1.1 (Cinemática e Equilíbrio de Múltiplas Cargas)

Uma carga pontual $q_1 = +4,0\ \mu\text{C}$ está fixa na origem espacial $(0,0,0)$ no vácuo. Uma segunda carga pontual $q_2 = -9,0\ \mu\text{C}$ está fixa na posição $\vec{r}_2 = 4\hat{i}\ (\text{m})$. Uma pequena bola não condutora que carrega uma carga genérica $Q$ é colocada em um ponto $P$ ao longo do eixo x.

* **a)** Determine analiticamente a coordenada exata $x_P$ onde a bola pode ser colocada de modo que o campo elétrico líquido gerado por $q_1$ e $q_2$ seja estritamente o vetor nulo $\vec{0}$.
* **b)** Se a bola tem uma massa $m = 2,0\text{ g}$ e carga $Q = +1,0\ \mu\text{C}$, e é liberada do repouso em $x = 1,0\text{ m}$, calcule seu vetor aceleração inicial instantânea $\vec{a}$ usando a Segunda Lei de Newton.

---

##  Seção 2: Simetria e Integração de Contorno (Nível Médio)

### Problema 2.1 (Halliday Modificado - Haste Carregada Finita com Deflexão Linear)
Uma haste fina e não condutora de comprimento finito $L$ está posicionada ao longo do eixo x, estendendo-se de $x = -L/2$ até $x = +L/2$. Uma carga líquida total $Q$ está distribuída uniformemente ao longo de seu comprimento com uma densidade linear constante $\lambda$. Um ponto $P$ está localizado no eixo y positivo a uma distância estrutural $\vec{r}_P = y\hat{j}$.
* **a)** Monte o elemento diferencial de carga $dq$ e escreva o vetor posição relativo $\vec{r}'$ que aponta de um elemento arbitrário $dx$ na haste para o ponto alvo $P$.
* **b)** Use integração contínua para encontrar a expressão vetorial exata para o campo elétrico $\vec{E}(y)$ no ponto $P$.
* **c)** Mostre que quando a distância se torna macroscópica ($y \gg L$), a expressão integral complexa colapsa assintoticamente de volta na equação de Coulomb padrão para cargas pontuais $\vec{E} \approx \frac{1}{4\pi\epsilon_0}\frac{Q}{y^2}\hat{j}$.

### Problema 2.2 (Sadiku Modificado - Discos Carregados e Densidades Superficiais)
Um disco plano circular de raio $R$ é posicionado horizontalmente no plano $xy$, centrado na origem. Ele carrega uma densidade superficial de carga uniforme $\sigma_0$.
* **a)** Fatie o disco em anéis concêntricos de raio $r$ e espessura $dr$ para montar a integral do campo elétrico total $\vec{E}(z)$ a uma altura $z$ ao longo do eixo de simetria (o eixo z).
* **b)** Avalie a integral para determinar o vetor campo elétrico $\vec{E}(z)$.
* **c)** Se o raio $R \to \infty$ (representando uma placa infinita de carga), deduza o vetor campo elétrico resultante e explique por que sua magnitude se torna completamente invariante (independente) em relação à distância $z$.

---

> [!CAUTION]
> 
> ###  SEÇÃO DE ENGENHARIA ANALÍTICA AVANÇADA
> As questões desta seção apresentam um salto drástico de complexidade e foram extraídas de exames de altíssimo nível (JEE Advanced e ITA). Elas exigem ferramentas matemáticas e conceitos que extrapolam as distribuições contínuas homogêneas padrão apresentadas até aqui, tais como:
> * **Densidades de Carga Heterogêneas ($\lambda(x)$ não-constante):** Exigem integração por frações parciais ou substituições avançadas onde a geometria não ajuda a simplificar o integrando.
> * **Aproximações Macroscópicas via Expansão Binomial:** Uso do Teorema do Binômio de Newton para aproximar campos elétricos locais ($x \ll a$), transformando equações de Coulomb em forças lineares restauradoras.
> * **Acoplamento de Sistemas (Eletromagnetismo + Mecânica):** Dedução de equações diferenciais de segunda ordem para provar Movimentos Harmônicos Simples (MHS).
>
> Recomenda-se avançar apenas se você já domina as técnicas de expansão em séries e integrais de linha em Cálculo.

##  Seção 3: Engenharia Analítica Avançada (Nível Difícil)

### Problema 3.1 (JEE Advanced - Dipolo Não-Uniforme Semi-Infinito)
Uma haste fina não condutora semi-infinita está posicionada ao longo do eixo x positivo, de $x = d$ até $x \to \infty$. A haste possui uma densidade linear de carga não-uniforme dada por $\lambda(x) = \lambda_0 \frac{d}{x}$, onde $\lambda_0$ é uma constante positiva. Uma carga pontual desconhecida $q$ é colocada na origem $(0,0,0)$.
* **a)** Monte o elemento diferencial vetorial $d\vec{E}$ na origem devido a um segmento infinitesimal $dx$ da haste.
* **b)** Calcule o vetor campo elétrico total $\vec{E}_{\text{rod}}$ na origem avaliando a integração contínua.
* **c)** Determine o valor da carga pontual $q$ (em termos de $\lambda_0$ e $d$) de modo que uma carga de teste positiva colocada em $x = \frac{d}{2}$ experimente uma força líquida absoluta igual a $\vec{0}$.

### Problema 3.2 (ITA - Limite Relativístico e Oscilações Harmônicas Simples)
Duas cargas pontuais positivas idênticas $+Q$ estão fixas no eixo y nas coordenadas $(0, a, 0)$ e $(0, -a, 0)$. Uma terceira carga pontual $-q$ (com massa $m$) é restrita a se mover exclusivamente ao longo do eixo x. Ela é liberada do repouso em uma coordenada genérica $(x, 0, 0)$.
* **a)** Derive a expressão vetorial exata para o campo elétrico total $\vec{E}(x)$ gerado pelas duas cargas positivas em qualquer ponto do eixo x.
* **b)** Assumindo a restrição estrutural microscópica $x \ll a$, aplique a expansão binomial para provar que o campo elétrico se comporta de forma linear com a distância perto da origem.
* **c)** Mostre que para pequenos deslocamentos ($x \ll a$), a carga alvo $-q$ executa um Movimento Harmônico Simples (MHS) e derive a expressão algébrica para sua frequência angular $\omega$.

---

#  Seção: Manual de Soluções

## Solução 1.1 (Fácil)

**a) Encontrando o Ponto de Campo Nulo:**

Como $q_1$ e $q_2$ têm sinais opostos, o ponto nulo não pode estar entre elas. Como $|q_1| < |q_2|$, o ponto nulo deve estar à esquerda de $q_1$, o que significa $x_P < 0$. Seja $d = |x_P|$.

$$
E_{\text{líquido}} = \frac{1}{4\pi\epsilon_0} \frac{|q_1|}{d^2} - \frac{1}{4\pi\epsilon_0} \frac{|q_2|}{(4 + d)^2} = 0 \implies \frac{4}{d^2} = \frac{9}{(4 + d)^2}
$$

Extraindo a raiz quadrada de ambos os lados:

$$
\frac{2}{d} = \frac{3}{4 + d} \implies 8 + 2d = 3d \implies d = 8\text{ m}
$$

Como o ponto está à esquerda da origem, a coordenada espacial é $x_P = -8,0\text{ m}$.

**b) Vetor Aceleração Inicial:**

Em $x = 1,0\text{ m}$, a distância até $q_1$ é $1\text{ m}$ (repulsão $\to +\hat{i}$) e a distância até $q_2$ é $3\text{ m}$ (atração $\to +\hat{i}$).

$$
E_{\text{líquido}} = (8,99 \times 10^9) \left[ \frac{4,0 \times 10^{-6}}{1^2} + \frac{9,0 \times 10^{-6}}{3^2} \right] = 44950\text{ N/C
}
$$

$$
\vec{F} = Q\vec{E} = (1,0 \times 10^{-6}\text{ C})(44950\hat{i}\text{ N/C}) = 0,04495\hat{i}\text{ N}
$$

$$
\vec{a} = \frac{\vec{F}}{m} = \frac{0,04495\hat{i}\text{ N}}{2,0 \times 10^{-3}\text{ kg}} = \mathbf{22,48\hat{i}\ \text{m/s}^2}
$$

---

## Solução 2.1 (Médio)

**a) Montagem:**

Um elemento da haste na posição $x$ tem carga $dq = \lambda dx = (Q/L)dx$. O vetor posição relativo de $dx$ até $P(0,y)$ é $\vec{r}' = -x\hat{i} + y\hat{j}$. O módulo da distância é $r' = \sqrt{x^2 + y^2}$.

**b) Integração:**

$$
d\vec{E} = \frac{1}{4\pi\epsilon_0} \frac{dq}{(r')^3}\vec{r}' = \frac{1}{4\pi\epsilon_0} \frac{\lambda dx}{(x^2 + y^2)^{3/2}} (-x\hat{i} + y\hat{j})
$$

Por simetria geométrica, as componentes $\hat{i}$ se cancelam perfeitamente ao longo dos limites de $-L/2$ até $+L/2$. Integramos apenas a componente $\hat{j}$:

$$
E_y = \frac{\lambda y}{4\pi\epsilon_0} \int_{-L/2}^{L/2} \frac{1}{(x^2 + y^2)^{3/2}} \, dx
$$

Usando a integral de substituição trigonométrica padrão do cálculo:

$$
E_y = \frac{\lambda y}{4\pi\epsilon_0} \left[ \frac{x}{y^2\sqrt{x^2+y^2}} \right]_{-L/2}^{L/2} = \frac{\lambda y}{4\pi\epsilon_0} \left( \frac{L}{y^2\sqrt{(L/2)^2 + y^2}} \right)
$$

Como $\lambda L = Q$, o campo vetorial final é:

$$
\vec{E}(y) = \mathbf{\frac{Q}{4\pi\epsilon_0 y \sqrt{\frac{L^2}{4} + y^2}} \hat{j}}
$$

**c) Limite Assintótico ($y \gg L$):**

Se $y \gg L$, então o termo $L^2/4$ dentro da raiz quadrada torna-se completamente desprezível se comparado a $y^2$. Assim, $\sqrt{L^2/4 + y^2} \approx \sqrt{y^2} = y$. Substituir isso de volta resulta em $\vec{E} \approx \frac{1}{4\pi\epsilon_0}\frac{Q}{y^2}\hat{j}$.

---

## Solução 2.2 (Médio)

**a) Montagem:**

Um anel de raio $r$ e largura $dr$ tem uma área $dA = 2\pi r dr$ e carga $dq = \sigma_0 (2\pi r dr)$. A distância até um ponto $z$ no eixo é $\sqrt{r^2+z^2}$. As componentes horizontais se cancelam, deixando apenas a componente axial multiplicada por $\cos\theta = \frac{z}{\sqrt{r^2+z^2}}$.

$$
dE_z = \frac{1}{4\pi\epsilon_0} \frac{\sigma_0 (2\pi r dr)}{r^2 + z^2} \left( \frac{z}{\sqrt{r^2+z^2}} \right) = \frac{\sigma_0 z}{4\epsilon_0} \frac{2r\,dr}{(r^2 + z^2)^{3/2}}
$$

**b) Avaliação:**

$$
\vec{E}(z) = \frac{\sigma_0 z}{4\epsilon_0} \int_{0}^{R} (r^2 + z^2)^{-3/2} (2r\,dr) \hat{k} = \frac{\sigma_0 z}{4\epsilon_0} \left[ \frac{-2}{\sqrt{r^2 + z^2}} \right]_{0}^{R} \hat{k
}
$$

$$
\vec{E}(z) = \mathbf{\frac{\sigma_0}{2\epsilon_0} \left( 1 - \frac{z}{\sqrt{R^2 + z^2}} \right) \hat{k}}
$$

**c) Limite Infinito ($R \to \infty$):**

Conforme $R \to \infty$, a fração $\frac{z}{\sqrt{R^2 + z^2}} \to 0$. A expressão colapsa para $\vec{E} = \frac{\sigma_0}{2\epsilon_0}\hat{k}$. O parâmetro de distância $z$ desaparece completamente porque as linhas de campo infinitas correm perfeitamente paralelas entre si, mantendo uma concentração de fluxo constante pelo espaço.

---

## Solução 3.1 (Difícil)

**a) Vetor campo diferencial:**

$$
dq = \lambda(x)dx = \lambda_0 \frac{d}{x}dx \implies d\vec{E} = -\frac{1}{4\pi\epsilon_0} \left( \frac{\lambda_0 d \cdot dx}{x^3} \right) \hat{i}
$$

**b) Avaliação via Integral Imprópria:**

$$
\vec{E}_{\text{rod}} = -\frac{\lambda_0 d}{4\pi\epsilon_0} \left( \int_{d}^{\infty} x^{-3} \, dx \right) \hat{i} = -\frac{\lambda_0 d}{4\pi\epsilon_0} \left[ \frac{x^{-2}}{-2} \right]_{d}^{\infty} \hat{i} = \mathbf{- \frac{\lambda_0}{8\pi\epsilon_0 d} \hat{i}}
$$

**c) Equilíbrio em $x = d/2$:**

O campo da carga pontual $q$ (na origem) agindo no ponto $d/2$ é $\vec{E}_q = \frac{4q}{4\pi\epsilon_0 d^2}\hat{i}$. O campo da haste avaliado na posição $d/2$ exige deslocar a variável de distância para $(x - d/2)$:

$$
\vec{E}_{\text{rod}}(d/2) = -\frac{\lambda_0 d}{4\pi\epsilon_0} \int_{d}^{\infty} \frac{1}{x(x - d/2)^2} \, dx \, \hat{i}
$$

Resolvendo por decomposição em frações parciais:

$$
\vec{E}_{\text{rod}}(d/2) = -\frac{\lambda_0}{4\pi\epsilon_0 d} \left[ 4\ln(2) - 2 \right]\hat{i}
$$

Definir $\vec{E}_q + \vec{E}_{\text{rod}}(d/2) = \vec{0}$ fornece a solução algébrica absoluta da carga:

$$
\mathbf{q = \frac{\lambda_0 d}{4} \left[ 2 \ln(2) - 1 \right]}
$$

---

## Solução 3.2 (Difícil)

**a) Expressão Vetorial:**

$$
\vec{E}(x) = 2 \cdot \left( \frac{1}{4\pi\epsilon_0} \frac{Q}{x^2 + a^2} \right) \cos\theta \, \hat{i} = \mathbf{\frac{2Qx}{4\pi\epsilon_0 (x^2 + a^2)^{3/2}} \hat{i}}
$$

**b) Aproximação Binomial ($x \ll a$):**

$$
\vec{E}(x) = \frac{2Qx}{4\pi\epsilon_0 a^3} \left(1 + \frac{x^2}{a^2}\right)^{-3/2} \approx \frac{2Qx}{4\pi\epsilon_0 a^3} \left( 1 - \frac{3}{2}\frac{x^2}{a^2} \dots \right)
$$

Como $x \ll a$, os termos de ordem superior colapsam ($x^3/a^5 \to 0$):

$$
\vec{E}(x) \approx \mathbf{\frac{Q}{2\pi\epsilon_0 a^3} x \, \hat{i}}
$$

**c) Estrutura do MHS:**

A força restauradora dinâmica em $-q$ é $\vec{F} = -q\vec{E}(x) = - \left( \frac{qQ}{2\pi\epsilon_0 a^3} \right) x \, \hat{i}$. Isso obedece estritamente ao formato da Lei de Hooke $\vec{F} = -k_{\text{eff}}x$, confirmando o movimento harmônico simples.

$$
\omega = \sqrt{\frac{k_{\text{eff}}}{m}} = \mathbf{\sqrt{\frac{qQ}{2\pi\epsilon_0 m a^3}}}
$$