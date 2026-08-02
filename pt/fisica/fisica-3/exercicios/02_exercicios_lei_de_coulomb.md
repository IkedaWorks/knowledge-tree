# Exercícios de Fixação: Lei de Coulomb

---

## Exercício 1

No vácuo ($k_0$), uma carga pontual $q_1 = +5,0\ \mu\text{C}$ está fixa na coordenada espacial $r_1 = (1, 2, -1)\text{ m}$ e uma segunda carga pontual $q_2 = -3,0\ \mu\text{C}$ está fixa em $r_2 = (-1, 4, 2)\text{ m}$.

Utilizando a formulação vetorial da Lei de Coulomb:
$$\vec{F}_{1\rightarrow 2} = k_0 \frac{q_1 q_2}{|\vec{r}_2 - \vec{r}_1|^3} (\vec{r}_2 - \vec{r}_1)$$

a) Determine o vetor deslocamento relativo $\vec{r}_{12} = \vec{r}_2 - \vec{r}_1$ e o seu respectivo módulo.
b) Calcule o vetor força eletrostática $\vec{F}_{1\rightarrow 2}$ exercido pela carga $1$ sobre a carga $2$, expressando-o analiticamente em componentes cartesianas ($\hat{i}, \hat{j}, \hat{k}$).

---

## Exercício 2

Três cargas pontuais estão dispostas estaticamente no plano $xy$ configuradas da seguinte forma:
* $q_A = +2,0\ \mu\text{C}$ localizada na origem $r_A = (0, 0)\text{ m}$
* $q_B = -4,0\ \mu\text{C}$ localizada em $r_B = (3, 0)\text{ m}$
* $q_C = +1,0\ \mu\text{C}$ localizada em $r_C = (0, 4)\text{ m}$

a) Determine os vetores força individuais $\vec{F}_{A\rightarrow C}$ e $\vec{F}_{B\rightarrow C}$ que atuam sobre a carga $q_C$.
b) Utilizando o princípio da superposição linear, calcule o vetor força resultante $\vec{F}_{\text{res}}$ na carga $q_C$ e determine o ângulo de inclinação deste vetor em relação ao eixo $x$ positivo.

---

## Exercício 3

Uma carga pontual desconhecida $q_1$ está posicionada em $\vec{r}_1 = 2\hat{i} - \hat{j}\ (\text{m})$ e sofre uma força eletrostática devido a uma carga $q_2 = +8,0\ \mu\text{C}$ localizada na posição $\vec{r}_2 = 5\hat{i} + 3\hat{j}\ (\text{m})$. Sabe-se que a força vetorial que $q_2$ exerce sobre $q_1$ é dada por:
$$\vec{F}_{2\rightarrow 1} = (-2,4\hat{i} - 3,2\hat{j}) \times 10^{-3}\text{ N}$$

a) A partir da direção e sentido do vetor força dado, deduza analiticamente se a carga $q_1$ possui sinal positivo ou negativo.
b) Calcule o valor algébrico e o sinal da carga $q_1$.

---

## Exercício 4: 

Duas cargas elétricas fixas, $q_1 = +q$ e $q_2 = +4q$, estão separadas por uma distância estrutural $d$ ao longo do eixo $x$, com $q_1$ posicionada na origem $(0,0)$. Uma terceira carga genérica $Q$ é posicionada no espaço de forma que o sistema inteiro de três cargas fique em equilíbrio estático síncrono (a força resultante em *cada uma* das três cargas é estritamente o vetor nulo $\vec{0}$).

a) Demonstre vetorialmente por que a carga $Q$ não pode estar localizada fora do eixo $x$ (ou seja, sua coordenada $y$ deve ser $0$).
b) Encontre o vetor posição $\vec{r}_Q$ e a magnitude de $Q$ (em termos de $q$) para que a condição de equilíbrio estático completo seja satisfeita.

## Seção: Gabarito Resolvido 

### Exercício 1

**a) Vetor deslocamento relativo $\vec{r}_{12}$ e seu módulo:**

O vetor deslocamento é dado pela diferença das posições:

$$\vec{r}_{12} = \vec{r}_2 - \vec{r}_1 = (-1 - 1)i + (4 - 2)j + (2 - (-1))k$$

$$\vec{r}_{12} = -2i + 2j + 3k\text{ m}$$

Cálculo do módulo $|\vec{r}_{12}|$:

$$|\vec{r}_{12}| = \sqrt{(-2)^2 + (2)^2 + (3)^2} = \sqrt{4 + 4 + 9} = \sqrt{17}\text{ m} \approx 4,123\text{ m}$$

**b) Vetor força eletrostática $\vec{F}_{1\rightarrow 2}$:**

Aplicando a Lei de Coulomb com o cubo do módulo no denominador:

$$\vec{F}_{1\rightarrow 2} = k_0 \frac{q_1 q_2}{|\vec{r}_{12}|^3} \vec{r}_{12}$$

$$\vec{F}_{1\rightarrow 2} = (8,988 \times 10^9) \frac{(5,0 \times 10^{-6}) \cdot (-3,0 \times 10^{-6})}{(\sqrt{17})^3} (-2i + 2j + 3k)$$

Isolando a constante multiplicadora:

$$\text{Constante} = \frac{-0,13482}{17\sqrt{17}} = \frac{-0,13482}{70,093} \approx -1,9234 \times 10^{-3}\text{ N/m}$$

Distribuindo a constante pelas componentes do vetor:

$$\vec{F}_{1\rightarrow 2} = 3,85i - 3,85j - 5,77k\text{ mN}$$

### Exercício 2

**a) Vetores força individuais sobre $q_C$:**

Primeiro, declaramos os vetores posição relativos a partir das coordenadas:

- $\vec{r}_A = (0,0)$, $\vec{r}_B = (3,0)$, $\vec{r}_C = (0,4)$
    
- $\vec{r}_{AC} = \vec{r}_C - \vec{r}_A = (0-0)i + (4-0)j = 4j\text{ m} \implies |\vec{r}_{AC}| = 4\text{ m}$
    
- $\vec{r}_{BC} = \vec{r}_C - \vec{r}_B = (0-3)i + (4-0)j = -3i + 4j\text{ m} \implies |\vec{r}_{BC}| = \sqrt{(-3)^2 + 4^2} = 5\text{ m}$
    

Calculando $\vec{F}_{A\rightarrow C}$:

$$\vec{F}_{A\rightarrow C} = k_0 \frac{q_A q_C}{|\vec{r}_{AC}|^3} \vec{r}_{AC} = (8,988 \times 10^9) \frac{(2,0 \times 10^{-6})(1,0 \times 10^{-6})}{4^3} (4j)$$

$$\vec{F}_{A\rightarrow C} = (8,988 \times 10^9) \frac{2,0 \times 10^{-12}}{64} (4j) = 1,1235 \times 10^{-3} (4j) = 4,49j\text{ mN}$$

Calculando $\vec{F}_{B\rightarrow C}$:

$$\vec{F}_{B\rightarrow C} = k_0 \frac{q_B q_C}{|\vec{r}_{BC}|^3} \vec{r}_{BC} = (8,988 \times 10^9) \frac{(-4,0 \times 10^{-6})(1,0 \times 10^{-6})}{5^3} (-3i + 4j)$$

$$\vec{F}_{B\rightarrow C} = (8,988 \times 10^9) \frac{-4,0 \times 10^{-12}}{125} (-3i + 4j) = -0,2876 \times 10^{-3} (-3i + 4j)$$

$$\vec{F}_{B\rightarrow C} = 0,863i - 1,15j\text{ mN}$$

**b) Vetor força resultante e ângulo de inclinação:**

Pelo princípio da superposição (utilizando o índice contador do somatório):

$$\vec{F}_{\text{res}} = \vec{F}_{A\rightarrow C} + \vec{F}_{B\rightarrow C} = (0,863)i + (4,49 - 1,15)j$$

$$\vec{F}_{\text{res}} = 0,863i + 3,34j\text{ mN}$$

Para encontrar o ângulo $\theta$ com o eixo $x$ positivo:

$$\tan(\theta) = \frac{F_y}{F_x} = \frac{3,34\text{ mN}}{0,863\text{ mN}} \approx 3,870$$

$$\theta = \arctan(3,870) \approx 75,5^\circ$$

### Exercício 3

**a) Dedução analítica do sinal de $q_1$:**

O vetor deslocamento de $2$ para $1$ é:

$$\vec{r}_{21} = \vec{r}_1 - \vec{r}_2 = (2 - 5)i + (-1 - 3)j = -3i - 4j\text{ m}$$

A força dada é $\vec{F}_{2\rightarrow 1} = -2,4i - 3,2j\text{ mN}$. Podemos observar que $\vec{F}_{2\rightarrow 1}$ aponta na **mesma direção e sentido** de $\vec{r}_{21}$ (ambas as componentes são negativas). Como a força é de **repulsão** (afastando $q_1$ de $q_2$), as cargas obrigatoriamente possuem o mesmo sinal. Dado que $q_2$ é positiva, **$q_1$ deve ser positiva**.

**b) Cálculo algébrico da carga $q_1$:**

Módulo de $\vec{r}_{21}$: $|\vec{r}_{21}| = \sqrt{(-3)^2 + (-4)^2} = 5\text{ m}$.

Tomando o módulo da força: $|\vec{F}_{2\rightarrow 1}| = \sqrt{(-2,4)^2 + (-3,2)^2} \times 10^{-3} = 4,0 \times 10^{-3}\text{ N}$.

Pela magnitude da Lei de Coulomb:

$$|\vec{F}_{2\rightarrow 1}| = k_0 \frac{|q_1 q_2|}{r^2} \implies 4,0 \times 10^{-3} = (8,988 \times 10^9) \frac{|q_1| \cdot (8,0 \times 10^{-6})}{5^2}$$

$$4,0 \times 10^{-3} = 2,87616 \times 10^3 \cdot |q_1| \implies |q_1| = \frac{4,0 \times 10^{-3}}{2,87616 \times 10^3} \approx 1,39 \times 10^{-6}\text{ C}$$

Como deduzido que $q_1 > 0$: **$q_1 \approx +1,39\ \mu\text{C}$**.

_(Nota: Se o livro adotar $k_0 = 9 \times 10^9$, o valor crava perfeitamente em $+1,39\ \mu\text{C}$ ou $25/18\ \mu\text{C}$)_.

### Exercício 4

**a) Demonstração vetorial do equilíbrio colinear:**

Suponha que a carga $Q$ esteja localizada em uma coordenada fora do eixo $x$, ou seja, $\vec{r}_Q = (x_Q, y_Q)$ com $y_Q \neq 0$. As forças exercidas por $q_1$ (na origem) e $q_2$ (no eixo $x$) sobre $Q$ terão componentes no eixo $y$ dadas por:

$$F_{1\rightarrow Q, y} = k_0 \frac{q Q}{|\vec{r}_Q|^3} y_Q \quad \text{e} \quad F_{2\rightarrow Q, y} = k_0 \frac{4q Q}{|\vec{r}_Q - d i|^3} y_Q$$

Como $q_1$ e $q_2$ têm o mesmo sinal ($+q$ e $+4q$), as forças que elas exercem sobre $Q$ na direção $y$ terão o mesmo sentido (ambas empurram ou ambas atraem no eixo $y$). Portanto, a soma das componentes em $y$ nunca poderá ser nula:

$$F_{\text{res, } y} = F_{1\rightarrow Q, y} + F_{2\rightarrow Q, y} \neq 0 \quad (\text{para } y_Q \neq 0)$$

Para que $\vec{F}_{\text{res}} = \vec{0}$, a componente $y$ deve ser zero, provando que **$Q$ deve estar no eixo $x$**.

**b) Determinação de $\vec{r}_Q$ e da magnitude de $Q$:**

Para que $Q$ balanceie duas cargas de mesmo sinal, ela deve estar posicionada **entre** elas ($0 < x_Q < d$) e possuir **sinal oposto (negativo)**.

Igualando as magnitudes das forças que $q_1$ e $q_2$ exercem em $Q$:

$$k_0 \frac{q |Q|}{x_Q^2} = k_0 \frac{4q |Q|}{(d - x_Q)^2} \implies \frac{1}{x_Q^2} = \frac{4}{(d - x_Q)^2}$$

Tirando a raiz quadrada de ambos os lados:

$$\frac{1}{x_Q} = \frac{2}{d - x_Q} \implies d - x_Q = 2x_Q \implies 3x_Q = d \implies x_Q = \frac{d}{3}$$

Portanto, o vetor posição é **$\vec{r}_Q = \frac{d}{3}i$**.

Agora, para o sistema inteiro estar em equilíbrio, a força resultante em $q_1$ (na origem) também deve ser zero devido à ação de $q_2$ e $Q$:

$$F_{\text{res on } q_1} = k_0 \frac{q \cdot 4q}{d^2} + k_0 \frac{q \cdot Q}{(d/3)^2} = 0$$

$$\frac{4q^2}{d^2} + \frac{9qQ}{d^2} = 0 \implies 4q + 9Q = 0 \implies Q = -\frac{4}{9}q$$