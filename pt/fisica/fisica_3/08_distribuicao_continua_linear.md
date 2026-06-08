# 📐 Teoria: Distribuições Lineares — A Dedução Genérica do Fio Carregado

O cálculo do campo elétrico para corpos macroscópicos consiste em transformar a Lei de Coulomb discreta em uma operação de limite contínuo. Compreender a mecânica desta dedução evita a necessidade de decorar fórmulas e constrói a base geométrica necessária para o eletromagnetismo de nível superior.

---

## 🌎 O Cenário de Análise e a Escolha dos Eixos

Imagine um fio condutor retilíneo, de espessura e volume desprezíveis, posicionado exatamente ao longo do **eixo $z$**. Nosso objetivo é mapear o campo elétrico gerado por esse corpo em um ponto $P$ qualquer localizado no espaço.



> 💡 **Insight de Engenharia:** Por que engessamos o problema em um eixo específico? Escolhemos o eixo $z$ para criar simetria artificial. Se o fio estivesse jogado na diagonal de um cubo, o problema exigiria trabalhar com equações diferenciais tridimensionais simultâneas em Álgebra Linear. Ao alinhar o fio ao eixo $z$ e escolher o ponto $P$ perpendicular a ele, simplificamos radicalmente a trigonometria nativa da natureza.

---

## 🛠️ O Pipeline de Resolução (Algoritmo de 4 Passos)

### Passo 1: Transição do Modelo Pontual para o Infinitesimal (A Física)

A equação clássica de Coulomb para cargas pontuais discretas baseia-se no somatório dos vetores de campos:

$$
\vec{E} = \frac{1}{4\pi\epsilon_0} \sum_{i} \frac{q_i}{|\vec{r}_{\text{rel}}|^3} \vec{r}_{\text{rel}}
$$

Para corpos macroscópicos, o cenário muda. Não podemos usar o operador de variação média ($\Delta$) porque ele calcularia apenas uma distribuição média e homogênea (escopo de ensino médio). No mundo real e de engenharia, a carga pode estar concentrada mais em uma ponta do que na outra. 

Para resolver isso, usamos o **cálculo diferencial**: dividimos o fio em infinitos pedacinhos de comprimento tão pequenos que tendem a zero ($dl$). Cada pedacinho microscópico conterá uma quantidade infinitesimal de carga ($dq$). 

Como não conseguimos integrar (somar) em relação à variável "carga" ($dq$), precisamos traduzir essa física para geometria. É aqui que entra a **Densidade Linear de Carga ($\lambda$)**:

$$\lambda = \frac{\text{Carga Total}}{\text{Comprimento Total}} = \frac{Q}{L} \quad \left[\text{Unidade: } \frac{\text{Coulomb}}{\text{metro}}\right]$$

Se a carga for distribuída continuamente, a razão se mantém na escala microscópica:

$$\lambda = \frac{dq}{dl} \implies dq = \lambda \cdot dl$$

Como o nosso fio está estrito ao longo do eixo $z$, o elemento de comprimento infinitesimal $dl$ nada mais é do que um tiquinho de variação na altura $z$, ou seja, $dl = dz'$. Assim, nossa tradução de carga fica:

$$dq = \lambda \, dz'$$

Substituindo essa identidade na Lei de Coulomb infinitesimal e aplicando a integral (que pelo Teorema Fundamental do Cálculo desfaz o efeito da derivada do campo $\int d\vec{E} = \vec{E}$), temos a nossa equação de montagem:

$$
\vec{E} = \frac{1}{4\pi\epsilon_0} \int \frac{\lambda dz'}{|\vec{r}_{\text{rel}}|^3} \vec{r}_{\text{rel}}
$$
> [!NOTE]
> 
> **Perceba, se você não entendeu o que aconteceu no processo acima, seu problema não é com essa matéria e sim com cálculo. Você deve revisar essa matéria porque senão sentirá uma dificuldade extrema mesmo com essa explicação, convido você ver a demonstração do Halliday, ele nem perde tempo mostrando o passo a passo, ele faz saltos gigantescos na resolução porque assume que você já domina o pré-requesitos dessa matéria.**

---

### Passo 2: O Kit de Conversão (A Tradução Cilíndrica e o Círculo Trigonométrico)

Se tentarmos resolver o vetor de distância relativa $|\vec{r}_{\text{rel}}|$ usando coordenadas cartesianas convencionais ($x, y, z$), cairemos em equações polinomiais tridimensionais pesadas (o equivalente a calcular a diagonal espacial de um prisma para cada pedaço de fio). Para contornar isso, fazemos uma transição de coordenadas.

#### De onde vem essa matemática? (O Salto Cartesiano $\to$ Polar $\to$ Cilíndrico)

Você provavelmente já conhece o **Círculo Trigonométrico** clássico, onde o raio é sempre igual a 1. Nele, qualquer ponto na borda do círculo é mapeado projetando a sombra do raio nos eixos horizontais e verticais: o eixo $x$ vira $\cos(\phi)$ e o eixo $y$ vira $\sin(\phi)$.

As **Coordenadas Polares** expandem esse conceito para engenharia. Em vez de prender o raio em 1, permitimos que o círculo cresça para qualquer tamanho (raio variável que chamaremos de $\rho$). Agora, para achar qualquer ponto em uma mesa bidimensional ($xy$), você só precisa saber a distância em linha reta até o centro ($\rho$) e o ângulo de inclinação $\phi$ em relação ao horizonte:

$$x = \rho \cos(\phi)$$

$$y = \rho \sin(\phi)$$

As **Coordenadas Cilíndricas** são a evolução final desse sistema para o espaço tridimensional: elas pegam a base circular das coordenadas polares e adicionam um eixo vertical de altura ($z$). Imagine um mastro vertical fincado bem no centro da mesa polar. Esse mastro é o eixo $z$. Um círculo que ganha altura se transforma geometricamente em um **Cilindro**.



> ✈️ **A Analogia do Radar de Caça:** Imagine que você pilota um caça militar. Se o visor do seu radar exibisse um míssil inimigo em coordenadas cartesianas como $(3, 4, 5)$, você morreria tentando calcular mentalmente a diagonal tridimensional desse vetor.
>
> Por isso, telas de radar utilizam o sistema cilíndrico/polar. O painel é composto por círculos concêntricos: a distância direta até o alvo é o raio ($\rho$), a direção no horizonte (360°) é dada pelo ângulo ($\phi$), e a diferença de altitude é o eixo $z$ (altura). Você bate o olho e localiza a ameaça instantaneamente com apenas alguns eixos e um ângulo de varredura.

> [!IMPORTANT]
> 
> **Por que ignoramos as Coordenadas Polares puras em Física III?**
> Você raramente (ou nunca) vai resolver um problema real de eletromagnetismo usando apenas coordenadas polares bidimensionais. Na Física III, os problemas reais possuem volume ou geram efeitos tridimensionais no espaço.
>
> O sistema **Cilíndrico** é o verdadeiro soberano das provas. Quando você chegar na Lei de Gauss, verá que superfícies gaussianas cilíndricas são usadas para resolver fios, cabos coaxiais e placas planas infinitas (onde a base do cilindro fica no plano $xy$ e a altura acompanha as linhas de campo). Dominar o kit cilíndrico agora é o que vai te poupar de chorar no próximo capítulo.

#### 🧰 O Kit de Conversão Cilíndrico Completo

Para transitar livremente entre os dois mundos durante a montagem das integrais, você precisa ter em mente as equações de ida e de volta do sistema:

**1. Tradução de Cilíndricas para Cartesianas (Ida):**
Utilizada para decompor os vetores radiais nas direções fixas do laboratório ($\hat{i}, \hat{j}, \hat{k}$).

$$x = \rho \cos(\phi)$$

$$y = \rho \sin(\phi)$$

$$z = z$$

> [!TIP]
> 
> **Eu gosto de imaginar o seguinte cenário para entender isso:**
> Eu percebo o mundo em coordenadas cartesianas, então temos os clássicos eixo (x,y,z), para converter eles nessa nova coordenada , basta a usar o plano xy como a base do seu cilindro. Então a base é um círculo, então preciso de um raio ($\rho$) rodando 360º nesse plano para formar ela, se desenhar esse raio, perceberá que poderá decompor ele no eixo x ou y de diversos jeitos, você pode ver isso com uma soma de vetores posições , pode usar trigonometria para chegar na relação acima, just do it.
> Agora temos nossa base só falta nosso mastro(altura desse cilíndro), por enquanto esse processo converteu cartesiano $\rightarrow$ em polar , agora precisamos converter isso em coordenadas cilíndricas, convenhamos um círculo com altura é o que chamamos de cilindro, por isso o nosso eixo $z$ serve de mastro, perceba que ele não muda de cartesiano $\rightarrow$ cilíndrico, é o mesmo vetor.


**2. Tradução de Cartesianas para Cilíndricas (Volta):**
Utilizada para simplificar os denominadores polinomiais da integral através do Teorema de Pitágoras no plano.

$$\rho = \sqrt{x^2 + y^2}$$

$$\phi = \arctan\left(\frac{y}{x}\right)$$

$$z = z$$

#### Mapeando os Vetores de Posição no Nosso Cenário:

1. **Vetor onde está a carga ($\vec{r}'$):** O elemento de carga está localizado sobre o fio (o mastro central $z$). Logo, sua distância radial até o centro é zero ($\rho = 0$). Esse vetor só possui altura: $\vec{r}' = z'\hat{k}$.
2. **Vetor onde está o ponto alvo $P$ ($\vec{r}$):** Usando o modo radar, dizemos que o ponto $P$ está a uma distância radial $\rho$ do mastro, apontando para fora em uma direção unitária que chamaremos de $\hat{a}_\rho$: $\vec{r} = \rho\hat{a}_\rho + z\hat{k}$.

> 🚨 **O Versor Radial  ($\hat{a}_\rho$):** Ao contrário dos vetores cartesianos fixos ($\hat{i}, \hat{j}, \hat{k}$), o versor $\hat{a}_\rho$ é dinâmico e depende estritamente do ângulo de rotação $\phi$ do radar:

$$\hat{a}_\rho = \cos(\phi)\hat{i} + \sin(\phi)\hat{j}$$

> Como o círculo possui uma varredura completa de $2\pi$ (360°), o computador ou engenheiro escolhe onde quer olhar:
> * Se posicionarmos o ponto $P$ estrategicamente no eixo $x$ ($\phi = 0^\circ$), temos $\hat{a}_\rho = (1, 0, 0) = \hat{i}$.
> * Se posicionarmos no eixo $y$ ($\phi = 90^\circ$), temos $\hat{a}_\rho = (0, 1, 0) = \hat{j}$.
>
> Ele age como uma infinidade de vetores unitários disponíveis para definir para qual direção perpendicular o campo está empurrando.

> [!TIP]
> 
> Perceba que ele chama versor radial, então independente do ângulo que você selecionar, o módulo dele sempre será 1, teste e chegue nas suas próprias conclusões.
> 

Subtraindo os vetores para obter o **Vetor Posição Relativo ($\vec{r}_{\text{rel}}$)**:

$$\vec{r}_{\text{rel}} = \vec{r} - \vec{r}' = \rho\hat{a}_\rho + (z - z')\hat{k}$$
> [!NOTE]
> 
> Aqui você só lida com raio e eixo $z$ , bem mais fácil que lidar com 3 eixos.

#### O Módulo da Intensidade (O Denominador):

Aplicando a equação de volta do nosso kit ($\rho^2 = x^2+y^2$), a magnitude do vetor no espaço cilíndrico engole as componentes horizontais cartesianas por Pitágoras:

$$|\vec{r}_{\text{rel}}| = \sqrt{\rho^2 + (z - z')^2}$$

Substituindo a tradução de $dq = \lambda dz'$ e a geometria cilíndrica na nossa integral, ela assume esta forma estruturada:

$$\vec{E} = \frac{1}{4\pi\epsilon_0} \int \frac{\lambda dz'}{[\rho^2 + (z - z')^2]^{3/2}} \left[ \rho\hat{a}_\rho + (z - z')\hat{k} \right]$$
### Passo 3: O Filtro de Simetria Vetorial

Se expandirmos a integral, teremos duas componentes separadas: uma empurrando radialmente para longe do fio ($\hat{a}_\rho$) e outra empurrando verticalmente para cima ou para baixo ao longo do mastro ($\hat{k}$).

Analisando a componente vertical associada ao termo $(z - z')$: se o fio for considerado infinito ou se o nosso ponto de análise estiver localizado exatamente no centro (mediatriz) de um fio finito, essa função se comporta como uma **Função Ímpar** sob limites de integração simétricos.

Pelas propriedades do cálculo integral, a integração de uma função ímpar em intervalos espelhados resulta em zero ($\int dE_z = 0$). Fisicamente, isso significa que para cada pedacinho de carga $dz'$ na parte de cima do mastro que empurra o ponto $P$ para baixo, existirá um pedacinho gêmeo na parte de baixo empurrando-o para cima com a mesma força. As componentes verticais se anulam mutuamente.



A componente do mastro desaparece, restando apenas a componente radial pura:

$$
\vec{E} = \frac{\lambda \rho \hat{a}_\rho}{4\pi\epsilon_0} \int \frac{dz'}{[\rho^2 + (z - z')^2]^{3/2}}
$$

---

### Passo 4: O Motor de Cálculo (Substituição Trigonométrica)

Para resolver esse monstro algébrico com potência fracionária sem precisar de tabelas prontas de cálculo, fazemos o "hack" geométrico. Em vez de rastrear as cargas medindo o fio em metros ($dz'$), passamos a rastrear as cargas medindo a inclinação do nosso olhar através do ângulo $\theta$.



#### 1. O Mecanismo de Tradução Angular:
Olhando para o triângulo retângulo formado pela distância fixa $\rho$ e a altura variável $(z - z')$, aplicamos a tangente:

$$
\tan(\theta) = \frac{z - z'}{\rho} \implies (z - z') = \rho\tan(\theta)
$$

Derivando a equação em relação ao ângulo, convertemos o diferencial de espaço em diferencial angular (lembrando que a derivada da tangente é a secante ao quadrado):

$$
dz' = \rho\sec^2(\theta)d\theta
$$

Para limpar o denominador, aplicamos a identidade trigonométrica fundamental $1 + \tan^2(\theta) = \sec^2(\theta)$:

$$
\left[ \rho^2 + (\rho\tan(\theta))^2 \right]^{3/2} = \left[ \rho^2(1 + \tan^2(\theta)) \right]^{3/2} = \left[ \rho^2\sec^2(\theta) \right]^{3/2} = \rho^3\sec^3(\theta)
$$

#### 2. O Cancelamento e Simplificação:
Ao substituir essas traduções na integral principal, as funções complexas sofrem uma simplificação drástica:

$$
\int \frac{\rho\sec^2(\theta)d\theta}{\rho^3\sec^3(\theta)} \implies \frac{1}{\rho^2} \int \frac{1}{\sec(\theta)}d\theta \implies \frac{1}{\rho^2} \int \cos(\theta)d\theta
$$

O segredo desse método foi transformar uma soma polinomial com potência fracionária em uma integral direta de cosseno.

---

## 🏁 O Salto Final: Fronteiras de Contorno

Como a integral do cosseno é o seno ($\int \cos\theta d\theta = \sin\theta$), basta aplicar os limites geométricos do corpo físico analisado.

### Cenário A: O Fio Infinito ($\infty$)
Para um fio que se estende infinitamente em ambas as direções do mastro, o ângulo de visão do nosso "radar" precisa varrer todo o horizonte, indo de $-90^\circ$ a $+90^\circ$ (ou de $-\pi/2$ a $+\pi/2$ radianos):

$$
\int_{\pi/2}^{\pi/2} \cos(\theta)d\theta = \sin\left(\frac{\pi}{2}\right) - \sin\left(-\frac{\pi}{2}\right) = 1 - (-1) = 2
$$

Unindo o resultado numérico com a constante que isolamos fora do bloco da integral no **Passo 3**:

$$
\vec{E} = \frac{\lambda \rho \hat{a}_\rho}{4\pi\epsilon_0} \cdot \left( \frac{2}{\rho^2} \right) \implies \vec{E} = \frac{\lambda}{2\pi\epsilon_0\rho}\hat{a}_\rho
$$

---

### Cenário B: O Fio Finito
Se a barra tiver um comprimento delimitado real de $L_1$ a $L_2$, o nosso radar não conseguirá abrir até $90^\circ$. A integral assumirá os limites dos ângulos físicos $\theta_1$ e $\theta_2$ que apontam para as extremidades da barra:

$$
\int_{\theta_1}^{\theta_2} \cos(\theta)d\theta = \left[ \sin(\theta_2) - \sin(\theta_1) \right]
$$

> ⚠️ **Atenção à Quebra de Simetria:** Se o ponto $P$ estiver deslocado para perto de uma das pontas do fio finito (fora da mediatriz), o Filtro de Simetria do **Passo 3** falha. Como as cargas de cima e de baixo não se balanceiam perfeitamente, a componente vertical $\hat{k}$ não zera. O campo elétrico resultará em uma força diagonal oblíqua, empurrando o ponto para longe na direção radial ($\hat{a}_\rho$) e puxando/empurrando lateralmente na direção do mastro ($\hat{k}$).

Para não ter que calcular ângulos abstratos em graus na prova, os engenheiros extraem o valor do seno diretamente do triângulo retângulo ($\sin(\theta) = \frac{\text{Cateto Oposto}}{\text{Hipotenusa}}$):

$$
\sin(\theta) = \frac{z - z'}{\sqrt{\rho^2 + (z - z')^2}}
$$

Substituindo esses limites em uma barra linear que se estende simetricamente de $-L/2$ até $+L/2$, o campo elétrico radial assume a seguinte equação consolidada:

$$
\vec{E} = \frac{\lambda}{4\pi\epsilon_0\rho} \left[ \frac{L_2}{\sqrt{\rho^2 + L_2^2}} - \frac{L_1}{\sqrt{\rho^2 + L_1^2}} \right] \hat{a}_\rho
$$