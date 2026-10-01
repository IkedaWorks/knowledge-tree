---
id: "vector-addition"
title: "Adição de Forças Planas: Geometria e Rigor"
domain: "physics"
module: "classical-mechanics"
type: "concept"
schema_version: "2.0"
level: "beginner"
language: "pt"
prerequisites: []
tags:
  - "physics"
  - "kinematics"
  - "vectors"
  - "vector-addition"
  - "statics"
---


# Adição de Forças Planas: Geometria e Rigor

Na estática e na cinemática vetorial, raramente se lida com uma única força isolada. A determinação da força resultante simplifica sistemas físicos complexos em um único efeito equivalente. A escolha do método geométrico depende diretamente do número de forças concorrentes e da geometria espacial do sistema.

---

## Motivação e Definição Formal

A adição de vetores físicos difere da aritmética escalar porque a magnitude e a direção espacial devem ser preservadas simultaneamente. 

Para forças concorrentes atuando em um único ponto, a composição vetorial estabelece um sistema equivalente:

$$\vec{F}_R = \sum_{i=1}^{n} \vec{F}_i = \vec{F}_1 + \vec{F}_2 + \dots + \vec{F}_n$$

Onde $\vec{F}_R$ representa o vetor força resultante que produz o mesmo efeito translacional que todas as forças individuais combinadas.

---

## Classificação e Casos Limite

### A Regra do Paralelogramo e suas Limitações

A Regra do Paralelogramo é o método geométrico fundamental para combinar **exatamente duas forças concorrentes**. As forças componentes formam os lados adjacentes de um paralelogramo, e o vetor resultante se estende ao longo da diagonal originada do ponto comum.

> [!NOTE]
> **Limitação do Método:** A Regra do Paralelogramo não consegue combinar três ou mais forças simultaneamente. Para $n > 2$ forças, os vetores devem ser somados iterativamente em pares ou processados pela Regra da Poligonal.

![Regra do Paralelogramo](./../../../../../assets/physics/classical-mechanics/parallelogram-law.webp)

### A Regra do Triângulo e da Poligonal

Para otimizar o cálculo, a **Regra do Triângulo** secciona o paralelogramo ao meio. A origem do segundo vetor é posicionada na extremidade do primeiro; o vetor resultante fecha o triângulo partindo da origem inicial até a extremidade final.

Ao avaliar três ou mais forças ($n \ge 3$), o método se generaliza na **Regra da Poligonal**:

1. Os vetores são dispostos sequencialmente em uma configuração "ponta com cauda".
2. A força resultante $\vec{F}_R$ é traçada da origem do primeiro vetor até a extremidade do último.
3. Se o polígono vetorial fechar exatamente na origem, o vetor resultante é nulo ($\vec{F}_R = \vec{0}$), provando graficamente o equilíbrio estático.

| Método | Forças Aplicáveis ($n$) | Topologia Geométrica | Condição Resultante |
| :--- | :---: | :--- | :--- |
| **Regra do Paralelogramo** | $n = 2$ | Diagonal do paralelogramo formado | $\vec{F}_R = \vec{F}_1 + \vec{F}_2$ |
| **Regra do Triângulo** | $n = 2$ | Fechamento triangular ponta-cauda | $\vec{F}_R = \vec{F}_1 + \vec{F}_2$ |
| **Regra da Poligonal** | $n \ge 3$ | Polígono aberto ou fechado ponta-cauda | $\vec{F}_R = \sum \vec{F}_i$ |

![Regra do Triângulo](./../../../../../assets/physics/classical-mechanics/triangle-law.webp)

![Regra da Poligonal](./../../../../../assets/physics/classical-mechanics/polygonal-law.webp)

---

## Demonstração e Formulação Matemática

### Resolução Trigonométrica via Lei dos Cossenos e Lei dos Senos

Quando duas forças $\vec{F}_1$ e $\vec{F}_2$ formam um ângulo interno $\beta$ em um triângulo ponta-cauda, a intensidade da força resultante $F_R$ é calculada pela **Lei dos Cossenos**:

$$F_R = \sqrt{F_1^2 + F_2^2 - 2 F_1 F_2 \cos(\beta)}$$

O ângulo de direção $\theta$ em relação ao vetor $\vec{F}_1$ é obtido pela **Lei dos Senos**:

$$\frac{F_2}{\sin(\theta)} = \frac{F_R}{\sin(\beta)} \implies \sin(\theta) = \frac{F_2 \sin(\beta)}{F_R}$$

---

## Aplicação Prática e Caso Resolvido

### Exercício Resolvido: Soma Geométrica em Parafuso de Fixação

Um parafuso de fixação em uma base de aço está sujeito a duas forças de tração exercidas por cordas, $\vec{F}_1$ e $\vec{F}_2$. A força $\vec{F}_1$ tem intensidade de $200\text{ N}$ a $20^\circ$ acima do eixo $x$ positivo. A força $\vec{F}_2$ tem $300\text{ N}$ a $10^\circ$ à esquerda do eixo $y$ positivo (vertical).

Determine a intensidade da força resultante $\vec{F}_R$ e o seu ângulo de direção $\phi$ medido no sentido anti-horário a partir do eixo $x$ positivo.

![Exemplo Parafuso de Fixação](./../../../../../assets/physics/classical-mechanics/vector-addition-example.webp)

#### 1. Análise Geométrica (Montagem do Triângulo de Forças)

O ângulo entre $\vec{F}_1$ e $\vec{F}_2$ no plano cartesiano é:

$$\theta_{\text{plano}} = 90^\circ - (20^\circ + 10^\circ) = 60^\circ$$

Ao transpor $\vec{F}_2$ ponta-cauda sobre a extremidade de $\vec{F}_1$, forma-se um ângulo interno $\beta$ suplementar a $\theta_{\text{plano}}$:

$$\beta = 180^\circ - 60^\circ = 120^\circ$$

#### 2. Intensidade da Força Resultante ($F_R$)

Aplicando a Lei dos Cossenos com $\cos(120^\circ) = -0{,}5$:

$$F_R = \sqrt{200^2 + 300^2 - 2(200)(300) \cos(120^\circ)}$$

$$F_R = \sqrt{40000 + 90000 - (120000 \cdot (-0{,}5))}$$

$$F_R = \sqrt{130000 + 60000} = \sqrt{190000} \approx 435{,}89 \text{ N}$$

Expressando $F_R$ com 3 algarismos significativos:

$$F_R = 436\text{ N}$$

#### 3. Direção em Relação ao Eixo $x$ Positivo ($\phi$)

Aplicando a Lei dos Senos para encontrar o ângulo $\theta$ entre $F_1$ e $F_R$:

$$\frac{300}{\sin(\theta)} = \frac{435{,}89}{\sin(120^\circ)}$$

$$\sin(\theta) = \frac{300 \cdot \sin(120^\circ)}{435{,}89} = \frac{300 \cdot 0{,}86603}{435{,}89} \approx 0{,}5960$$

$$\theta = \arcsin(0{,}5960) \approx 36{,}58^\circ$$

Somando $\theta$ com a elevação inicial de $20^\circ$ da força $\vec{F}_1$:

$$\phi = \theta + 20^\circ = 36{,}58^\circ + 20^\circ = 56{,}58^\circ \approx 56{,}6^\circ$$

---

### Armadilha Conceitual: Confusão com Ângulo Suplementar

Um erro frequente na construção do triângulo de forças é utilizar o ângulo do plano ($60^\circ$) diretamente na Lei dos Cossenos em vez do ângulo interno suplementar ($120^\circ$).

$$\text{Incorreto: } F_R = \sqrt{200^2 + 300^2 - 2(200)(300) \cos(60^\circ)} = \sqrt{70000} \approx 264{,}6\text{ N}$$

#### Desconstrução

O uso de $60^\circ$ calcula a diferença vetorial $|\vec{F}_1 - \vec{F}_2|$ em vez da soma vetorial $|\vec{F}_1 + \vec{F}_2|$. Quando os vetores são transpostos na configuração ponta-cauda, o ângulo interno do triângulo resultante é sempre $180^\circ - \theta_{\text{concorrente}}$.

---

## Conexões e Aplicações Avançadas

> [!TIP]
> **Aplicações na Engenharia:** A adição geométrica vetorial forma a base para a análise de treliças na engenharia estrutural. Ao avaliar sistemas de forças concorrentes em nós estruturais, verificar o fechamento do polígono de forças é o equivalente gráfico direto à aplicação da Primeira Lei de Newton ($\sum \vec{F} = \vec{0}$).