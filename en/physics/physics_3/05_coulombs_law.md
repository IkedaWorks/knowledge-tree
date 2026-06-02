# Lei de Coulomb (Força Elétrica)

A Lei de Coulomb trata da interação de cargas elétricas puntiformes (pontuais) em repouso. Como estamos falando da interação de um campo elétrico com uma carga elétrica, descrevemos esse fenômeno por meio de uma força elétrica, que serve como a fundação de toda a eletrostática.

## 📜 Contexto Histórico e a Balança de Torção

Formulada pelo físico francês Charles Augustin de Coulomb em 1785, esta lei quantifica a força de atração ou repulsão entre duas cargas. Como na época não existiam softwares de simulação ou multímetros, Coulomb desenvolveu um aparato mecânico extremamente sensível chamado Balança de Torção.

### O Processo Experimental: Medindo o Invisível Antes do Elétron

Coulomb publicou seus ensaios mais de 110 anos antes de J.J. Thomson descobrir a existência do elétron (1897). Em vez de conhecer a quantidade absoluta de cargas elementares, Coulomb utilizou a simetria geométrica e proporções para isolar suas variáveis:

* **Controle das Frações de Carga ($q_1 \cdot q_2$):** Para variar a carga sem ter um medidor absoluto, ele usou o princípio da condução por contato. Ele eletrizava uma esfera condutora polida com uma carga desconhecida $Q$ e a tocava em outra esfera idêntica e neutra. Por pura simetria geométrica, a carga líquida era obrigada a se dividir perfeitamente ao meio ($\frac{1}{2}Q$). Repetindo o processo, ele conseguia manipular frações precisas de carga ($\frac{1}{2}, \frac{1}{4}, \frac{1}{8}$) sem nem saber o que era um elétron.
* **Dependência com a Distância ($1/r^2$):** Mantendo as cargas fixas e variando a distância ($r$) entre as esferas, ele mediu o ângulo de rotação do fio de suspensão. Ele observou que:
    * Dobrar a distância ($2r$) tornava a força eletrostática 4 vezes menor ($\frac{1}{4}F$).
    * Triplicar a distância ($3r$) tornava a força 9 vezes menor ($\frac{1}{9}F$).
    * **Conclusão:** A força é inversamente proporcional ao quadrado da distância: $F \propto \frac{1}{r^2}$.

> [!NOTE]
> 
> Observe que o gráfico de força X distância é uma hipérbole de segundo grau, isso indica a proporção indireta.

### Funcionamento Mecânico do Aparato

A balança de torção consistia em um fino fio de prata ou seda que suspendia uma haste horizontal isolante:
* Uma das extremidades continha uma pequena esfera condutora (a carga a ser testada).
* A extremidade oposta continha um contrapeso feito de material isolante neutro (como papel ou cera), servindo puramente para manter o equilíbrio mecânico horizontal, sem sofrer interferência elétrica.

Ao introduzir no sistema uma segunda esfera condutora fixa e carregada, a repulsão eletrostática empurrava a esfera móvel, torcendo o fio de suspensão. O fio exercia um torque restaurador mecânico proporcional ao ângulo de torção (Lei de Hooke para torção). Lendo o deslocamento angular estável em uma escala graduada de vidro, Coulomb calculava a força eletrostática exata.

Unindo essas observações empíricas, chegou-se à famosa relação escalar:
$$F = k \frac{|q_1 \cdot q_2|}{r^2}$$

---

## 🔬 O Conceito Matemático Vetorial

Embora Coulomb tenha deduzido a relação de forma escalar, a engenharia e o Cálculo III exigem a abordagem vetorial para modelar sistemas tridimensionais complexos. 

A magnitude da força é ditada pela constante eletrostática ($k$), que esconde uma profunda propriedade geométrica do espaço:
$$k = \frac{1}{4\pi\epsilon_0} \approx 8,99 \times 10^9 \ \text{N}\cdot\text{m}^2/\text{C}^2$$

* **Permissividade do Vácuo ($\epsilon_0 \approx 8,85 \times 10^{-12} \ \text{C}^2/\text{N}\cdot\text{m}^2$):** É a constante física que dita a "permissão" ou o grau de facilidade que o vácuo oferece para a propagação de linhas de campo elétrico. Ela é a base para o entendimento futuro de Potencial Elétrico, Capacitância (comportamento de dielétricos) e das próprias Equações de Maxwell.

### 🌐 A Geometria Oculta da Lei de Coulomb ($4\pi r^2$)

Se reescrevermos a Lei de Coulomb substituindo o valor de $k$, a equação ganha um significado geométrico brutal:
$$F = \frac{1}{4\pi\epsilon_0} \frac{|q_1 \cdot q_2|}{r^2} \implies F = \frac{|q_1 \cdot q_2|}{\mathbf{(4\pi r^2)} \epsilon_0}$$

O termo $4\pi r^2$ é rigorosamente a fórmula da área superficial de uma esfera. Como o nosso espaço é tridimensional e isotrópico, a perturbação elétrica gerada por uma carga pontual se propaga igualmente em todas as direções, expandindo-se como uma onda esférica. 

À medida que a distância ($r$) aumenta, a "energia" do campo da carga fonte precisa se espalhar (diluir) por uma área esférica cada vez maior. O decaimento da força com o inverso do quadrado da distância ($1/r^2$) nada mais é do que a consequência geométrica do campo se distribuindo uniformemente pela superfície dessa esfera tridimensional em expansão.

---

## 🎯 Notação Vetorial (A Transição para o Cálculo Vetorial)

Para entender a formulação de engenharia, precisamos dividir o fenômeno entre a sua intensidade pura e a sua orientação no espaço, compreendendo que ambas as informações nascem do mesmo lugar: o vetor posição relativo.

### 1. O Vetor Posição Relativo ($\vec{r}_{1\to2}$) como Origem de Tudo

No espaço tridimensional, a primeira coisa que fazemos é traçar um vetor que conecta as duas cargas. Este é o vetor posição relativo $\vec{r}_{1\to2}$, que nasce na carga de origem ($q_1$, a fonte que modifica o espaço) e morre na carga de destino ($q_2$, o alvo que sente a força):
$$\vec{r}_{1\to2} = (x_2 - x_1)i + (y_2 - y_1)j + (z_2 - z_1)k$$

Tanto o módulo da distância quanto a direção da força vão depender exclusivamente desse cara. 

Perceba que $\vec{r}_{1\to2}$ é um vetor relativo porque o posicionamento está entre as cargas envolvidas na interação. Geometricamente, ele é composto por $\vec{r}_1$ e $\vec{r}_2$, que são os vetores posição absolutos — eles dão a localização exata de cada carga em relação à referência do espaço, que por padrão é a origem $(0,0,0)$. Pela lei de soma de vetores, temos:
$$\vec{r}_{1\to2} = \vec{r}_2 - \vec{r}_1$$

> [!NOTE]
> 
> **A Importância da Álgebra Linear:** Como a grande maioria das grandezas em Teoria de Campos são vetoriais, é aqui na Física Elétrica que tudo aquilo que você aprendeu em Álgebra Linear (transformações, subpaços, vetores e bases) começa a fazer sentido prático na engenharia.

### 2. A Visão do Ensino Médio: O Módulo Escalar Puro

A equação clássica do ensino médio calcula apenas a intensidade (o tamanho) da força. Para isso, ela extrai o módulo absoluto do vetor posição relativo (representado por $|\vec{r}_{1\to2}|$ ou simplesmente $r$). O $r^2$ no denominador é o quadrado do comprimento desse vetor relativo, ignorando para onde ele aponta:
$$F = k \frac{|q_1 \cdot q_2|}{r^2} \quad \text{onde } r = |\vec{r}_{1\to2}| = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2 + (z_2 - z_1)^2}$$

> [!WARNING]
> 
> **A Falha Fatal:** Essa equação brilhava no ensino médio, mas ela tem uma limitação crítica: só calcula a intensidade da força. Na realidade da engenharia, quase sempre precisamos saber a direção e o sentido, pois são essas características que ditarão o comportamento dinâmico real da interação tridimensional.

### 3. O Casamento de Naturezas: A Entrada do Versor

Dizer que a força vale $5\text{ N}$ não basta; o software de simulação precisa saber para onde ela empurra. Como o lado esquerdo da equação é um vetor ($\vec{F}$), o lado direito obrigatoriamente precisa de uma operação vetorial para a igualdade ser verdadeira. Não se pode igualar um vetor a um número escalar puro.

Para "vetorizar" a intensidade sem alterar o tamanho que já calculamos, multiplicamos a sopa de escalares pelo versor unitário ($\hat{r}_{1\to2}$). Esse versor é o próprio vetor posição relativo dividido pelo seu próprio módulo:
$$\vec{F}_{1\to2} = \underbrace{\left( k \frac{q_1 \cdot q_2}{r^2} \right)}_{\text{Intensidade (Módulo)}} \cdot \underbrace{\hat{r}_{1\to2}}_{\text{Orientação (Versor)}}$$

Como o comprimento de $\hat{r}_{1\to2}$ é rigidamente igual a $1$, ele cumpre a função exclusiva de injetar as coordenadas espaciais na fórmula sem distorcer o valor físico da força.

### 4. A Formulação Computacional (O porquê do $r^3$)

No código ou em cálculos complexos, abrir a fórmula para achar o versor gera uma operação de divisão extra. Substituindo a definição geométrica do versor ($\hat{r}_{1\to2} = \frac{\vec{r}_{1\to2}}{r}$) diretamente na equação, o módulo do vetor relativo que estava ao quadrado ($r^2$) é multiplicado por ele mesmo mais uma vez, resultando em $r^3$:
$$\vec{F}_{1\to2} = k \frac{q_1 \cdot q_2}{r^2} \cdot \left( \frac{\vec{r}_{1\to2}}{r} \right) \implies \vec{F}_{1\to2} = k \frac{q_1 \cdot q_2}{r^3} \vec{r}_{1\to2}$$

> [!NOTE]
> 
> **Atenção Física (Análise Dimensional):** A Lei de Coulomb nunca deixou de ser do inverso do quadrado. O expoente 3 no denominador não indica uma lei do inverso do cubo. Ele surge porque o vetor posição completo ($\vec{r}_{1\to2}$) no numerador traz consigo uma dimensão extra de comprimento ($[\text{L}]$) que precisa ser matematicamente cancelada pelo termo extra no denominador, mantendo a unidade final estritamente em Newtons.

### 💡 Intuição de Engenharia (Separação de Papéis)

Olhando para a fórmula final expansiva, a separação de propriedades fica evidente:
$$\vec{F}_{1\to2} = \underbrace{\left( k \frac{q_1 \cdot q_2}{|\vec{r}_{1\to2}|^3} \right)}_{\text{Sopa de Escalares (Tamanho)}} \cdot \underbrace{\vec{r}_{1\to2}}_{\text{Vetor Relativo (Direção)}}$$

* **O Bloco Escalar:** Tudo dentro dos parênteses opera como números puros. O módulo do vetor relativo ($r$) é calculated e elevado ao cubo, ditando a intensidade do impacto.
* **O Bloco Vetorial:** O vetor posição relativo $\vec{r}_{1\to2}$ entra multiplicando no final para "carimbar" os eixos cartesianos ($i, j, k$), transformando o número puro em um vetor geométrico real.

---

## 🧩 Princípio da Superposição e Geometria no Espaço (3D)

Quando um sistema possui múltiplas cargas atuando no espaço, a força resultante sobre uma carga específica é a soma vetorial de todas as forças exercidas sobre ela individualmente pelas outras cargas:
$$\vec{F}_{\text{res}} = \vec{F}_{1} + \vec{F}_{2} + \vec{F}_{3} + \dots = \sum_{i=1}^{n} \vec{F}_{i}$$

> [!CAUTION]
> 
> **Erro Clássico de Engenharia:** Nunca some os módulos das forças diretamente, a menos que todas as cargas estejam na mesma linha reta (colineares). Sempre decomponha as forças em suas componentes cartesianas ($i, j, k$) antes de efetuar a soma.

### 📐 Determinação da Direção Espacial: Cossenos Diretores

No plano bidimensional ($xy$), a inclinação de $\vec{F}_{\text{res}}$ é obtida facilmente via trigonometria simples utilizando a tangente ($\tan(\theta) = F_y / F_x$). No entanto, no espaço tridimensional ($xyz$), a força resultante aponta para uma direção livre e sua orientação não pode ser descrita por um único ângulo. Em vez disso, utilizamos **três ângulos direcionais** ($\alpha, \beta, \gamma$), que medem a inclinação do vetor força em relação aos eixos cartesianos positivos $x, y, z$, respectivamente.

A determinação de cada ângulo é feita de forma independente por meio dos **Cossenos Diretores**, que projetam a componente de cada eixo sobre o módulo total do vetor força resultante $|\vec{F}_{\text{res}}| = \sqrt{F_x^2 + F_y^2 + F_z^2}$:

$$\cos(\alpha) = \frac{F_x}{|\vec{F}_{\text{res}}|} \implies \alpha = \arccos\left(\frac{F_x}{|\vec{F}_{\text{res}}|}\right)$$
$$\cos(\beta) = \frac{F_y}{|\vec{F}_{\text{res}}|} \implies \beta = \arccos\left(\frac{F_y}{|\vec{F}_{\text{res}}|}\right)$$
$$\cos(\gamma) = \frac{F_z}{|\vec{F}_{\text{res}}|} \implies \gamma = \arccos\left(\frac{F_z}{|\vec{F}_{\text{res}}|}\right)$$

> [!TIP]
> 
> **Conexão com a Estática (Física 1):**
> Lembra que em Mecânica/Estática operávamos com a equação $\vec{F} = |\vec{F}| \cdot \hat{u}_F$? O papel do versor da força ($\hat{u}_F$) é justamente carregar esses cossenos. Se abrirmos o versor geométrico dividindo suas componentes cartesianas pelo módulo, as novas coordenadas geradas são rigorosamente os cossenos diretores:
> $$\hat{u}_F = \frac{F_x}{|\vec{F}|}i + \frac{F_y}{|\vec{F}|}j + \frac{F_z}{|\vec{F}|}k = \cos(\alpha)i + \cos(\beta)j + \cos(\gamma)k$$
> Como prova real matemática para validação de algoritmos e scripts de análise, a soma geométrica desses cossenos direcionais deve sempre obedecer à identidade unitária: $\cos^2(\alpha) + \cos^2(\beta) + \cos^2(\gamma) = 1$.