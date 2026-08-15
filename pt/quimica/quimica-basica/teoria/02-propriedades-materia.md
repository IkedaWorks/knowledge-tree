---
id: propriedades_materia
title: Propriedades da Matéria
---
# Propriedades da Matéria e Caracterização de Sistemas

## Introdução

No estudo da Química, a caracterização de um sistema material exige determinar como a matéria responde a estímulos físicos e químicos. Embora toda matéria ocupe espaço e possua massa, diferentes materiais apresentam comportamentos singulares quando submetidos a variações de temperatura, pressão ou interações com outras substâncias.

Para compreender como os materiais são identificados e aplicados, a análise é organizada na distinção entre propriedades gerais e específicas, utilizando grandezas mensuráveis e modelos conceituais.

---

## Classificação Fundamental das Propriedades

As propriedades de um sistema material são divididas em duas categorias principais com base em sua capacidade de identificar a substância que constitui a amostra.

### Propriedades Gerais

Ao comparar um bloco de concreto e uma barra de ouro de volumes idênticos, ambos ocupam espaço no ambiente e oferecem resistência quando se tenta alterá-los de posição. Essas características confirmam a presença de matéria em ambos os corpos, mas não fornecem qualquer informação sobre a composição de cada um.

Propriedades gerais são características inerentes a toda e qualquer amostra de matéria, independentemente de sua constituição química. Elas variam diretamente com a quantidade de matéria presente no sistema.

As principais propriedades gerais incluem:

* **Massa ($m$):** Medida quantitativa da inércia e da quantidade de matéria contida em um corpo.
* **Volume ($V$):** Quantidade de espaço tridimensional ocupado pelo sistema.
* **Impenetrabilidade:** Princípio segundo o qual dois corpos não podem ocupar simultaneamente o mesmo lugar no espaço.
* **Inércia:** Tendência de um corpo de manter seu estado de repouso ou de movimento retilínio uniforme a menos que atue sobre ele uma força resultante não nula.
* **Compressibilidade e Elasticidade:** Capacidade da matéria de reduzir seu volume sob a ação de forças externas e de retornar ao seu formato original quando tais forças são removidas.

Por serem dependentes da extensão da amostra, as propriedades gerais não permitem identificar a substância analisada. Em termos formais e termodinâmicos, pertencem à classe das **propriedades extensivas**. Uma propriedade $P$ é dita extensiva se o seu valor para o sistema global for igual à soma dos valores dessa mesma propriedade para cada um de seus subsistemas componentes.

Para um sistema particionado em $n$ subsistemas independentes, a propriedade extensiva total $P_{\text{total}}$ é expressa por:

$$P_{\text{total}} = \sum_{i=1}^{n} P_i$$

>[!NOTE] Formato Contínuo e Integração de Volume
>Considerando um meio contínuo com densidade de massa local $\rho(\mathbf{r})$ contido em uma região tridimensional do espaço $\Omega$, o volume total $V$ e a massa total $m$ são definidos formalmente por integrais sobre o domínio:
>
>$$V = \iiint_{\Omega} dV$$
>
>$$m = \iiint_{\Omega} \rho(\mathbf{r}) \, dV$$
>
>Em que $\mathbf{r}$ representa o vetor posição no espaço euclidiano.

---

### Propriedades Específicas

Caso dois recipientes idênticos contenham líquidos incolores com volumes e massas absolutamente iguais, essas medições básicas não revelarão qual deles é água e qual é etanol puro. No entanto, ao medir a temperatura na qual cada líquido entra em ebulição ou ao determinar a massa contida em uma unidade de volume específica, a diferenciação ocorre de forma imediata e precisa.

Propriedades específicas dependem exclusivamente da identidade química e do arranjo estrutural da matéria. Elas permanecem inalteradas independentemente da quantidade ou do tamanho da amostra analisada, funcionando como critérios fundamentais para a caracterização e identificação de substâncias puras.

Classificam-se em:
* **Propriedades Físicas:** Podem ser mensuradas ou observadas sem alterar a composição química da substância (ex.: ponto de fusão, ponto de ebulição, densidade, condutividade elétrica e térmica).
* **Propriedades Químicas:** Descrevem a capacidade de uma substância de sofrer reações que transformam sua identidade química (ex.: reatividade com acids, inflamabilidade, potencial de oxidação).
* **Propriedades Organolépticas:** Percebidas pelos órgãos dos sentidos (ex.: cor, odor, sabor e brilho).

As propriedades específicas correspondem às **propriedades intensivas** da termodinâmica, sendo invariantes frente à divisão ou alteração na escala do sistema. O parâmetro de maior destaque na caracterização de materiais é a **densidade ($\rho$)**, definida pela razão entre a massa ($m$) e o volume ($V$) do sistema:

$$\rho = \frac{m}{V}$$

No Sistema Internacional de Unidades (SI), a densidade é expressa em $\text{kg/m}^3$, sendo também comum a utilização das unidades práticas $\text{g/cm}^3$ e $\text{g/mL}$ (onde $1\text{ g/cm}^3 = 1000\text{ kg/m}^3$). As propriedades físicas intensivas são constantes termodinâmicas fixas para substâncias puras sob condições padronizadas de pressão e temperatura.

>[!NOTE] Definição Limite e Meios Heterogêneos
>Uma propriedade intensiva $y(\mathbf{r})$ pode ser definida matematicamente como a razão limite entre duas propriedades extensivas $P_1$ e $P_2$ quando o volume da amostragem tende a um elemento diferencial $dV$:
>
>$$y(\mathbf{r}) = \lim_{\Delta V \to 0} \frac{\Delta P_1}{\Delta P_2}$$
>
>Desta forma, em sistemas não homogêneos, a densidade é definida localmente pela razão diferencial entre a massa $dm$ e o volume $dV$:
>
>$$\rho = \frac{dm}{dV}$$

---

### Síntese Comparativa das Propriedades

| Critério de Classificação | Propriedades Extensivas (Gerais) | Propriedades Intensivas (Específicas / Estado) |
| :--- | :--- | :--- |
| **Dependência da Massa/Tamanho** | Dependem da quantidade de matéria na amostra. | Não dependem da quantidade de matéria na amostra. |
| **Comportamento ao Dividir a Amostra** | O valor total é a soma das partes ($P_{\text{total}} = \sum P_i$). | O valor permanece invariante em qualquer fração da amostra. |
| **Capacidade de Identificação** | Não identificam a substância (apenas medem dimensões). | Identificam a substância (funcionam como "impressão digital"). |
| **Exemplos Físicos Diretos** | Massa ($m$), Volume ($V$), Capacidade calorífica ($C$), Energia interna ($U$). | Densidade ($\rho$), Ponto de fusão ($\text{PF}$), Ponto de ebulição ($\text{PE}$), Solubilidade ($C_s$). |
| **Exemplos de Estado do Sistema** | Quantidade de matéria ($n$), Área de superfície ($A$). | Temperatura ($T$), Pressão ($P$), Viscosidade ($\eta$). |

---

## Medições Quantitativas e Propriedades Físicas Específicas

A caracterização rigorosa da matéria exige a quantificação de suas propriedades físicas por meio de grandezas padronizadas.

### Pontos de Transição de Fase

Ao aquecer uma barra de chumbo e um bloco de alumínio, cada metal atinge o estado líquido em temperaturas inteiramente distintas. Essas temperaturas fixas funcionam como marcas registradas de cada elemento ou composto.

* **Ponto de Fusão ($\text{PF}$):** Temperatura exata na qual uma substância pura transita do estado sólido para o estado líquido sob uma dada pressão atmosférica.
* **Ponto de Ebulição ($\text{PE}$):** Temperatura na qual a pressão de vapor de um líquido iguala-se à pressão externa exercida sobre a sua superfície, promovendo a passagem para o estado gasoso ao longo de toda a massa do sistema.

Durante a transição de fase de uma substância pura sob pressão constante, a temperatura permanece estritamente constante. A quantidade de calor $q$ necessária para promover a mudança de fase é diretamente proporcional à massa $m$ da amostra e ao calor latente específico $L$:

$$q = m \cdot L$$

Em que $L$ é uma propriedade específica expressa no SI em Joules por quilograma ($\text{J/kg}$) ou em caloria por grama ($\text{cal/g}$).

>[!NOTE] Visão Estatística e Intermolecular
>Do ponto de vista estatístico, os pontos de fusão e ebulição representam temperaturas críticas onde a energia de agitação térmica média ($k_B T$) atinge o valor necessário para superar as energias potenciais de atração intermolecular do reticulado cristalino ou da fase líquida.

---

### Solubilidade como Propriedade Específica

Ao adicionar sal de cozinha à água, o sólido se dissolve até determinado limite. A partir de um certo ponto, por mais que se agite o sistema, o sal adicional acumula-se no fundo do recipiente. Existe uma capacidade máxima de dissolução ditada pela natureza do solvente e do soluto.

A solubilidade é a quantidade máxima de uma substância (soluto) capaz de se dissover em uma quantidade fixa de outra substância (solvente) a uma determinada temperatura e pressão, formando um sistema homogêneo. Sistemas que atingiram esse limite são denominados **soluções saturadas**.

O coeficiente de solubilidade ($C_s$) é definido quantitativamente como a massa máxima de soluto ($m_{\text{soluto, máx}}$) solúvel em uma massa fixa de solvente ($m_{\text{solvente}}$) a uma temperatura $T$:

$$C_s(T) = \frac{m_{\text{soluto, máx}}}{m_{\text{solvente}}}$$

Geralmente, expressa-se o coeficiente na unidade prática de gramas de soluto por $100\text{ g}$ de solvente ($\text{g soluto} / 100\text{ g } \text{H}_2\text{O}$).

>[!NOTE] Equilíbrio Termodinâmico de Fases
>Termodinamicamente, o equilíbrio de solubilidade ocorre quando o potencial químico do soluto na fase sólida ($\mu_{\text{sólido}}$) iguala-se ao seu potencial químico na fase de solução ($\mu_{\text{solução}}$):
>
>$$\mu_{\text{sólido}}(T, P) = \mu_{\text{solução}}(T, P, x)$$
>
>Em que $x$ representa a fração molar do soluto dissolvido.

---

## Mapa de Progressão do Módulo

Os conceitos apresentados neste capítulo consolidam a base de identificação dos sistemas materiais:

* **Propriedades Gerais (Extensivas):** Medem aspectos dimensionais da matéria, mas não identificam a substância.
* **Propriedades Específicas (Intensivas):** Dependem do arranjo estrutural e são critério direto de caracterização.
* **Grandezas Mensuráveis:** Densidade ($\rho = \frac{m}{V}$), pontos de transição de fase ($\text{PF}$ e $\text{PE}$) e solubilidade ($C_s$) são constantes intensivas em condições fixas.

Com a caracterização das propriedades finalizada, o passo seguinte compreende a análise de como a energia térmica altera a organização dessas partículas no capítulo dedicado aos estados da matéria e mudanças de fase.