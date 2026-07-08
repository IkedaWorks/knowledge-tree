# Física III - Eletromagnetismo

Bem-vindo ao núcleo de estudos de Física III. Este espaço é dedicado à exploração conceitual, matemática e intuitiva do Eletromagnetismo — a força fundamental por trás de quase toda a tecnologia moderna, desde motores elétricos até a propagação de sinais de rede e a luz.

O objetivo destas notas é construir uma compreensão sólida de como os campos elétricos e magnéticos operam, focando em desenvolver a intuição geométrica para montar as equações e entender o significado físico de cada componente.

---

##  Pré-requisitos e o Papel do Cálculo

Física III usa a matemática do Cálculo como uma ferramenta prática de modelagem. Não buscaremos deduções matemáticas puras do zero, mas sim a habilidade de traduzir um problema físico em ferramentas matemáticas conhecidas:

* **Ferramentas de Cálculo (I, II e III):** Entender o conceito de taxas de variação (derivadas) e acúmulo/soma de pedaços infinitesimais (integrais). Saber aplicar técnicas básicas de integração para resolver os problemas montados.
* **Geometria e Vetores:** Decomposição vetorial, produto escalar (crucial para fluxos e trabalho) e produto vetorial (essencial no magnetismo). Noções básicas de como coordenadas cilíndricas e esféricas facilitam a nossa vida ao lidar com simetrias espaciais.
* **Conceitos de Mecânica (Física I):** Conservação de energia, trabalho de uma força e as Leis de Newton aplicadas ao movimento de partículas e cargas.

> Quando eu aprendi essa matéria, ter um certo domínio em Cálculo I e II ajudou bastante na compreensão inicial. No entanto, você precisa fundamentalmente de Cálculo III (Cálculo Vetorial/Multivariável) para entender a física direito e não ficar apenas decorando equações prontas. Portanto, o ideal é fazer esse módulo em conjunto com o módulo de Cálculo III ou já dominar os conceitos de integrais de linha, superfície e volume para compreender essa matéria de verdade.

---

##  Fluxo de Aprendizado (Roadmap)

O conteúdo avança linearmente partindo dos fenômenos estáticos isolados até a unificação completa dos campos dinâmicos e ondas eletromagnéticas:

### Bloco 1: Eletrostática (Campos Elétricos Fixos)

* **Carga Elétrica e Lei de Coulomb:** O comportamento fundamental das cargas (quantização e conservação) e a força vetorial entre cargas pontuais.
* **Campo Elétrico e Distribuições Contínuas:** A ideia de campo como uma perturbação no espaço. Como fatiar um objeto carregado (barra, anel, disco) em pedacinhos infinitesimais $dq$ e usar integrais para somar o campo total.
* **Fluxo Elétrico e Lei de Gauss:** A interpretação geométrica de linhas de campo atravessando superfícies fechadas. O uso de superfícies gaussianas para encontrar o campo elétrico de formas simétricas de um jeito muito mais eficiente.

### Bloco 2: Potencial, Energia e Dielétricos

* **Potencial Elétrico:** O conceito de voltagem ($V$) associado ao trabalho e à energia potencial do sistema. A relação matemática entre o gradiente do campo elétrico e a diferença de potencial.
* **Capacitância e Dielétricos:** Como armazenar energia diretamente em campos elétricos usando capacitores, e como materiais isolantes (dielétricos) alteram o comportamento desse campo microscopicamente.

### Bloco 3: Magnetostática (Campos Magnéticos Fixos)

* **O Campo Magnético ($\vec{B}$) e a Lei de Gauss do Magnetismo:** A origem do magnetismo, o significado físico por trás da ausência de monopolos magnéticos e como os campos magnéticos desviam cargas em movimento (Força de Lorentz). 
* **Fontes de Campo Magnético (Biot-Savart e Lei de Ampère):** Como cargas em movimento e correntes estacionárias geram campos magnéticos. O uso da Lei de Biot-Savart para integrar elementos diferenciais de corrente ($Id\vec{s}$) e a Lei de Ampère como ferramenta de simetria para o campo $\vec{B}$. 

### Bloco 4: Eletromagnetismo Dinâmico e Equações de Maxwell

* **Lei de Faraday e Indução Eletromagnética:** A fundação das máquinas elétricas. Como a variação de um campo magnético no tempo induz uma força eletromotriz (FEM) e gera um campo elétrico induzido (incorporando a Lei de Lenz para a conservação da energia). 
* **A Corrente de Deslocamento e as Equações de Maxwell:** Entender a assimetria que Maxwell resolveu ao introduzir o termo da corrente de deslocamento em capacitores. A síntese de todo o núcleo de física nas quatro equações definitivas. 
* **Ondas Eletromagnéticas:** A conclusão lógica do curso: a luz e as ondas de rádio vistas como perturbações eletromagnéticas que se autopropagam e viajam pelo espaço, transportando energia e momento linear.