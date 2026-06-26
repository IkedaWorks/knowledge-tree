
# 📐 Teoria: Distribuições Superficiais — A Dedução Genérica do Disco Carregado

O cálculo do campo elétrico para superfícies carregadas bidimensionais expande nossa modelagem infinitesimal de uma linha 1D para uma superfície 2D. Utilizando as fundações cilíndricas já estabelecidas nos problemas de linhas de carga, conseguimos resolver distribuições superficiais com o mínimo de atrito algébrico. Este documento apresenta a dedução geral para um disco plano uniformemente carregado, um precursor clássico para entender planos infinitos e capacitores de placas paralelas.

---

## 🌎 O Cenário de Análise e a Escolha dos Eixos

Imagine um disco plano, circular e não-condutor de raio $R$ que carrega uma carga superficial uniforme. Para maximizar a simetria geométrica, posicionamos o disco plano sobre o plano $xy$, centrado perfeitamente na origem $(0, 0, 0)$. Nosso objetivo é calcular o campo elétrico líquido $\vec{E}$ em um ponto alvo $P$ localizado ao longo do eixo de simetria central (o eixo $z$) a uma altura $z$.



> 💡 **Insight de Engenharia:** Por que travar o ponto $P$ estritamente no eixo central $z$? Assim como no caso do fio, escolher o eixo central cria uma estrutura de simetria rotacional. Se tentássemos calcular o campo em um ponto fora do eixo central, a simetria azimutal seria quebrada, forçando-nos a resolver o problema usando integrais elípticas que não podem ser avaliadas em termos de funções elementares. Manter $P$ no eixo transforma um potencial pesadelo em cálculo limpo e manejável.

---

## 🛠️ O Pipeline de Resolução (Algoritmo de 4 Passos)

### Passo 1: Transição do Modelo de Linha para o de Superfície (A Física)

Quando lidamos com uma superfície bidimensional, monitoramos a distribuição de carga por unidade de área. Definimos a **Densidade Superficial de Carga ($\sigma$)**:

$$
\sigma = \frac{\text{Carga Total}}{\text{Área Total}} = \frac{Q}{A} \quad \left[\text{Unidade: } \frac{\text{Coulomb}}{\text{metro}^2}\right]
$$

Para uma distribuição contínua e uniforme, essa razão se mantém na escala de um remendo infinitesimal de área $dA$:

$$
\sigma = \frac{dq}{dA} \implies dq = \sigma \cdot dA
$$

Para integrar ao longo de um disco circular, não dividimos o corpo em quadrados cartesianos ($dx \cdot dy$), o que levaria a limites com radicais miseráveis. Em vez disso, decompomos o disco em **anéis** concêntricos e microscópicos de raio $r'$ e espessura radial infinitesimal $dr'$.



Desenrolar um desses anéis finos resulta em um retângulo de comprimento igual à circunferência ($2\pi r'$) e largura $dr'$. Portanto, nosso elemento de área diferencial é:

$$
dA = 2\pi r' dr'
$$

Substituir isso em nossa equação de densidade de carga nos dá a tradução física para a nossa fonte:

$$
dq = \sigma (2\pi r' dr')
$$

---

### Passo 2: O Kit de Conversão (Reutilizando a Estrutura Cilíndrica)

Como já dominamos o kit de conversão cilíndrico, pulamos a dedução completa e mapeamos diretamente nossos vetores de posição. Como as cargas fontes vivem inteiramente na base plana do nosso cilindro (plano $xy$ em $z=0$) e o ponto alvo $P$ senta no mastro (eixo $z$), nossos vetores espaciais se simplificam diretamente:

1. **Vetor onde o elemento de carga está localizado ($\vec{r}'$):** O elemento de anel está sobre o plano a uma distância radial $r'$ do centro, apontando na direção radial dinâmica $\hat{a}_\rho$. Ele possui altura zero: $\vec{r}' = r'\hat{a}_\rho$.
2. **Vetor onde o ponto alvo $P$ está localizado ($\vec{r}$):** O ponto $P$ possui distância radial zero em relação ao eixo e está inteiramente na altura $z$: $\vec{r} = z\hat{k}$.

Subtrair esses vetores resulta no **Vetor Posição Relativo ($\vec{r}_{\text{rel}}$)** que aponta do elemento de carga para o ponto alvo:

$$
\vec{r}_{\text{rel}} = \vec{r} - \vec{r}' = -r'\hat{a}_\rho + z\hat{k}
$$

#### O Módulo da Intensidade (O Denominador):
Aplicando nosso kit de conversão reversa, a magnitude desse vetor relativo é encontrada através de um triângulo retângulo direto no nosso mastro:

$$
|\vec{r}_{\text{rel}}| = \sqrt{(r')^2 + z^2}
$$

Juntar esses componentes na forma infinitesimal contínua da Lei de Coulomb nos dá a nossa equação primordial de montagem:

$$
\vec{E} = \frac{1}{4\pi\epsilon_0} \int_{0}^{R} \frac{\sigma (2\pi r' dr')}{[(r')^2 + z^2]^{3/2}} \left( -r'\hat{a}_\rho + z\hat{k} \right)
$$

---

### Passo 3: O Filtro de Simetria Vetorial

Expandir a integral expõe duas ações direcionais distintas: uma componente radial ($-\hat{a}_\rho$) puxando para dentro/empurrando para fora paralelamente ao disco, e uma componente vertical ($\hat{k}$) empurrando ao longo do eixo.

Como nosso elemento de anel dá uma volta completa de $2\pi$ ao redor da origem, cada pedaço de carga individual $dq$ em um lado do anel possui um "gêmeo" simétrico diretamente oposto ($180^\circ$ de distância).



Enquanto suas contribuições verticais se reforçam, seus empurrões radiais horizontais ($\hat{a}_\rho$) apontam em direções diametralmente opostas e se cancelam completamente ao longo de toda a varredura da integração:

$$
\int_{0}^{2\pi} \hat{a}_\rho d\phi = 0 \implies \vec{E}_rho = 0
$$

Toda a componente horizontal desaparece, restando exclusivamente a projeção axial vertical:

$$
\vec{E} = \frac{2\pi\sigma z \hat{k}}{4\pi\epsilon_0} \int_{0}^{R} \frac{r' dr'}{[(r')^2 + z^2]^{3/2}}
$$

Simplificar as constantes fora do bloco da integral resulta em:

$$
\vec{E} = \frac{\sigma z \hat{k}}{2\epsilon_0} \int_{0}^{R} \frac{r' dr'}{[(r')^2 + z^2]^{3/2}}
$$

---

### Passo 4: O Motor de Cálculo (Substituição por $u$)

Ao contrário do problema da linha de carga que exigiu o "hack" da substituição trigonométrica, esta integral de superfície contém sua própria ferramenta de derivada interna. Como o numerador abriga um termo $r' dr'$, podemos resolver isso rapidamente usando a **substituição por $u$** padrão.

Deixemos que nosso polinômio interno seja $u$:

$$
u = (r')^2 + z^2
$$

Tomando o diferencial em relação à nossa variável de integração $r'$ (lembrando que a altura $z$ age como uma constante em relação à superfície do disco):

$$
du = 2r' dr' \implies r' dr' = \frac{du}{2}
$$

Agora mapeamos nossos limites de fronteira de $r'$ para $u$:
* Limite inferior: Quando $r' = 0 \implies u = z^2$
* Limite superior: Quando $r' = R \implies u = R^2 + z^2$

Substituir essas traduções em nosso motor de cálculo transforma a expressão em uma integral básica da regra da potência:

$$
\int_{z^2}^{R^2 + z^2} \frac{1}{u^{3/2}} \frac{du}{2} = \frac{1}{2} \int_{z^2}^{R^2 + z^2} u^{-3/2} du
$$

Executando a integração:

$$
\frac{1}{2} \left[ \frac{u^{-1/2}}{-1/2} \right]_{z^2}^{R^2 + z^2} = -\left[ \frac{1}{\sqrt{u}} \right]_{z^2}^{R^2 + z^2} = \left[ \frac{1}{\sqrt{z^2}} - \frac{1}{\sqrt{R^2 + z^2}} \right]
$$

Como $\sqrt{z^2} = |z|$, e assumindo que estamos analisando um ponto no eixo $z$ positivo ($z > 0$), isso se simplifica diretamente para:

$$
\left( \frac{1}{z} - \frac{1}{\sqrt{R^2 + z^2}} \right)
$$

---

## 🏁 O Salto Final: Fronteiras de Contorno

Recombinando este valor de integração concluído com as constantes que isolamos fora do bloco no **Passo 3**, obtemos nossa equação de engenharia consolidada para o campo elétrico de um disco finito:

$$
\vec{E} = \frac{\sigma z \hat{k}}{2\epsilon_0} \left( \frac{1}{z} - \frac{1}{\sqrt{R^2 + z^2}} \right)
$$

Distribuir o termo $z$ para dentro dos colchetes nos dá a forma padrão dos livros-texto:

$$
\vec{E} = \frac{\sigma}{2\epsilon_0} \left( 1 - \frac{z}{\sqrt{R^2 + z^2}} \right) \hat{k}
$$

### Cenário A: O Plano Infinito ($R \to \infty$)
Se o raio do disco se expandir infinitamente, ou se nosso ponto alvo $P$ for posicionado tão incrivelmente perto da superfície que o disco pareça um horizonte sem fim ($z \ll R$), o termo da fração cai para zero:

$$
\lim_{R \to \infty} \frac{z}{\sqrt{R^2 + z^2}} = 0
$$

Isso isola a fórmula fundamental de campo constante para um **Plano Infinito de Carga**:

$$
\vec{E} = \frac{\sigma}{2\epsilon_0} \hat{k}
$$

> [!IMPORTANT]
> **O Spoiler Supremo da Lei de Gauss**
> 
> Note que o campo elétrico de um plano infinito não depende da distância ($z$). Esteja você a $1\text{ mm}$ ou a $10\text{ metros}$ de distância, o campo que te empurra tem exatamente a mesma intensidade.
> 
> Você encontrará esta mesmíssima equação no próximo capítulo usando a **Lei de Gauss** com uma superfície gaussiana em formato de "caixa de pílulas" cilíndrica. Deduzi-la aqui via integração por força bruta prova *o porquê* de a geometria funcionar e mostra por que a Lei de Gauss é um atalho tão poderoso para os engenheiros.