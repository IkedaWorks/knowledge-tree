

# 🏛️ Física I — Mecânica Clássica

Bem-vindo ao núcleo de estudos de Física I. Este espaço é dedicado à exploração conceitual, matemática e intuitiva da **Mecânica Clássica** — a fundação analítica que descreve o movimento da matéria em escala macroscópica e as interações fundamentais que regem a engenharia, desde o equilíbrio de estruturas rígidas até a dinâmica de sistemas em rotação.

O objetivo destas notas é construir uma compreensão profunda de como corpos e sistemas interagem com forças, focando em desenvolver a **intuição geométrica** para montar e interpretar as equações do movimento a partir do cálculo, rejeitando a simples memorização de fórmulas prontas.

---

## 🛠️ Pré-requisitos e o Papel do Cálculo

Física I usa a matemática do Cálculo Diferencial e Integral como a sua linguagem natural de modelagem. Não estudamos o movimento apenas através de variações médias ($\Delta$), mas sim como taxas de variação instantâneas e acúmulos contínuos no tempo e no espaço:

* **Cálculo Diferencial e Integral I:** Entender profundamente o conceito de derivadas como taxas de variação instantâneas ($v = dx/dt$, $a = dv/dt$) e integrais como o acúmulo contínuo de grandezas (área sob a curva e cálculo de trabalho).
* **Geometria Analítica e Vetores:** Decomposição vetorial em componentes cartesianas, produto escalar (fundamental para o conceito de Trabalho e Energia) e **produto vetorial** (essencial para definir torque, eixos de rotação e momento angular).
* **Sistemas de Coordenadas:** Intuição sobre o uso de coordenadas polares e cilíndricas ao lidar com problemas que possuem simetria circular ou eixos de rotação.

---

## 🗺️ Fluxo de Aprendizado (Roadmap)

O conteúdo avança de forma linear, partindo da pura geometria da trajetória até as leis que regem as forças e as dinâmicas de rotação em múltiplas dimensões:

###  Bloco 1: Cinemática (A Geometria do Movimento)

* **Fundamentos e Ferramentas Vetoriais:** O escopo da mecânica, análise dimensional, grandezas do SI e operações fundamentais com vetores (decomposição, produto escalar e vetorial).
* **Cinemática Diferencial (1D, 2D e 3D):** Posição, velocidade e aceleração vistas estritamente como derivadas e integrais no tempo. O movimento de projéteis e trajetórias sob aceleração variável.
* **Cinemática Angular e Movimento Circular:** A definição geométrica do radiano ($\theta = s/r$), a velocidade angular ($\omega$) e a dedução da aceleração centrípeta ($a_c$) via taxas relacionadas do vetor velocidade.

###  Bloco 2: Dinâmica e Leis de Newton (As Causas do Movimento)

* **As Leis de Newton e o Momento Linear:** O conceito moderno de Força como a taxa de variação temporal da quantidade de movimento ( $\vec{F} = d\vec{p}/dt$ ). Aplicações em atrito, planos inclinados e forças de arrasto.
* **Trabalho, Energia e Conservação:** O cálculo do trabalho através da integral de linha do produto escalar ( $\int \vec{F} \cdot d\vec{r}$ ), o Teorema da Energia Cinética e a conservação de energia mecânica em sistemas conservativos.
* **Sistemas de Partículas e Impulso:** Centro de massa, conservação do momento linear em colisões e a variação da massa ao longo do tempo (sistemas de massa variável).

### Bloco 3: Estática e Equilíbrio (A Física das Estruturas)

* **Equilíbrio de Ponto Material:** A primeira condição de equilíbrio ( $\sum \vec{F} = 0$ ) e a análise de forças concorrentes.
* **Equilíbrio de Corpos Extensos e Torque:** A introdução ao conceito de Torque ( $\vec{\tau} = \vec{r} \times \vec{F}$ ) como o agente gerador de rotação. A segunda condição de equilíbrio ( $\sum \vec{\tau} = 0$ ) aplicada a estruturas rígidas, vigas e alavancas.


### Bloco 4: Rotações Avançadas e Dinâmica de Rígidos

* **Momento de Inércia e Segunda Lei para Rotações:** A resistência escalar de um corpo ao giro e a relação fundamental entre torque e aceleração angular ($\tau = I\alpha$).
* **Momento Angular ($\vec{L}$) e Torque como Derivada:** O desdobramento do movimento linear para o espaço rotacional. O momento angular definido via produto vetorial ($\vec{L} = \vec{r} \times \vec{p}$) e o torque provado como a sua derivada temporal direta ($\vec{\tau} = d\vec{L}/dt$).
* **Conservação do Momento Angular:** Fenômenos onde o torque externo é nulo ($\vec{\tau} = 0$), gerando a conservação de $\vec{L}$ e efeitos como a precessão e o comportamento giroscópico.