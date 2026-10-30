---
id: "biot-savart-law"
title: "Lei de Biot-Savart e Fundamentos do Campo Magnético"
domain: "physics"
module: "electromagnetism"
type: "concept"
schema_version: "2.0"
level: "intermediate"
language: "pt"
prerequisites:
  - "coulomb-law"
  - "electric-current-density"
  - "vector-cross-product"
tags:
  - "magnetostatics"
  - "magnetic-field"
  - "biot-savart"
  - "vector-calculus"
---

# Lei de Biot-Savart e Fundamentos do Campo Magnético

## Motivação e Contexto

Na eletrostática, a configuração espacial de cargas estacionárias determina o campo elétrico $\mathbf{E}$ via Lei de Coulomb. Contudo, quando as cargas entram em movimento, elas geram um campo fundamentalmente distinto: o campo magnético $\mathbf{B}$. Ao contrário das linhas de campo elétrico, que se originam e terminam em cargas elétricas discretas, as linhas de campo magnético formam laços fechados e contínuos. A natureza não possui cargas magnéticas isoladas (monopolos).

Historicamente, Hans Christian Ørsted descobriu que uma corrente elétrica deflete a agulha de uma bússola, provando uma ligação profunda entre cargas em movimento e o magnetismo. Jean-Baptiste Biot e Félix Savart quantificaram esse fenômeno medindo a força exercida sobre polos magnéticos próximos a correntes elétricas estacionárias.

O problema fundamental que forçou a formulação da Lei de Biot-Savart foi determinar a contribuição diferencial exata $d\mathbf{B}$ criada em um ponto espacial $P$ por um segmento infinitesimal de linha de corrente $I d\mathbf{l}$. Ela atua como o equivalente magnetostático da Lei de Coulomb, fornecendo a base integral para calcular campos magnéticos em configurações arbitrárias de corrente em regimes estáticos.

## Formulação Teórica

### A Lei de Biot-Savart Diferencial

Considere um fio condutor fino transportando uma corrente elétrica estacionária $I$. Seja $d\mathbf{l}$ um elemento vetorial infinitesimal ao longo do fio apontando na direção da corrente, e seja $\mathbf{r}'$ o vetor posição deste elemento fonte. O campo magnético $d\mathbf{B}$ produzido em um ponto de observação $\mathbf{r}$ é dado por:

$$d\mathbf{B}(\mathbf{r}) = \frac{\mu_0}{4\pi} \frac{I d\mathbf{l} \times \hat{\boldsymbol{\mathcal{R}}}}{\mathcal{R}^2} = \frac{\mu_0}{4\pi} \frac{I d\mathbf{l} \times \boldsymbol{\mathcal{R}}}{\mathcal{R}^3}$$

Onde:
- $\boldsymbol{\mathcal{R}} = \mathbf{r} - \mathbf{r}'$ é o vetor deslocamento apontando do elemento fonte $I d\mathbf{l}$ para o ponto de campo $\mathbf{r}$.
- $\mathcal{R} = |\boldsymbol{\mathcal{R}}|$ é a magnitude da distância de deslocamento.
- $\hat{\boldsymbol{\mathcal{R}}} = \boldsymbol{\mathcal{R}} / \mathcal{R}$ é o vetor unitário apontando na direção do ponto de observação.
- $\mu_0$ é a permeabilidade magnética do vácuo, definida como $\mu_0 = 4\pi \times 10^{-7} \text{ T}\cdot\text{m/A}$ (ou $\text{N/A}^2$).

Observe por que o produto vetorial $d\mathbf{l} \times \hat{\boldsymbol{\mathcal{R}}}$ é fisicamente indispensável: ele força $d\mathbf{B}$ a ser estritamente perpendicular tanto à direção do elemento de corrente $d\mathbf{l}$ quanto à linha que conecta a fonte ao observador $\boldsymbol{\mathcal{R}}$. Essa restrição geométrica dita a regra da mão direita característica da magnetostática.

### Campo Total via Integração de Linha

Para avaliar o campo magnético total produzido por um circuito condutor completo $C$, integram-se as contribuições diferenciais ao longo de toda a geometria do fio:

$$\mathbf{B}(\mathbf{r}) = \frac{\mu_0 I}{4\pi} \int_C \frac{d\mathbf{l} \times \hat{\boldsymbol{\mathcal{R}}}}{\mathcal{R}^2}$$

### Generalização para Densidade Volumétrica de Corrente

Para distribuições tridimensionais de corrente caracterizadas por uma densidade volumétrica de corrente $\mathbf{J}(\mathbf{r}')$, o elemento de corrente $I d\mathbf{l}$ se generaliza para $\mathbf{J}(\mathbf{r}') dV'$. A equação global do campo torna-se:

$$\mathbf{B}(\mathbf{r}) = \frac{\mu_0}{4\pi} \iiint_V \frac{\mathbf{J}(\mathbf{r}') \times \hat{\boldsymbol{\mathcal{R}}}}{\mathcal{R}^2} dV'$$

## Exemplos e Problemas Resolvidos

### Exemplo 1: Campo Magnético no Eixo de uma Espira Circular de Corrente

Uma espira circular fina de raio $R$ encontra-se no plano $xy$, centralizada na origem, transportando uma corrente estacionária $I$ no sentido anti-horário quando vista de cima. Calcule o campo magnético em um ponto arbitrário $P = (0, 0, z)$ sobre o eixo $z$.

#### Solução:
1. **Definir a geometria:**
   Um ponto na espira é parametrizado em coordenadas cilíndricas como $\mathbf{r}' = R\hat{\boldsymbol{\rho}}'$. O elemento diferencial de comprimento é $d\mathbf{l} = R d\phi' \hat{\boldsymbol{\phi}}'$.
   O ponto de campo é $\mathbf{r} = z\hat{\mathbf{z}}$.

2. **Calcular os vetores deslocamento:**
   $$\boldsymbol{\mathcal{R}} = \mathbf{r} - \mathbf{r}' = z\hat{\mathbf{z}} - R\hat{\boldsymbol{\rho}}'$$
   $$\mathcal{R} = |\boldsymbol{\mathcal{R}}| = \sqrt{R^2 + z^2}$$

3. **Avaliar o produto vetorial:**
   $$d\mathbf{l} \times \boldsymbol{\mathcal{R}} = (R d\phi' \hat{\boldsymbol{\phi}}') \times (z\hat{\mathbf{z}} - R\hat{\boldsymbol{\rho}}') = R z d\phi' \hat{\boldsymbol{\rho}}' + R^2 d\phi' \hat{\mathbf{z}}$$

4. **Aplicar a simetria cilíndrica:**
   À medida que $\phi'$ varia de $0$ a $2\pi$, a componente radial $\hat{\boldsymbol{\rho}}'$ gira completamente no plano $xy$ e resulta em zero após a integração. Apenas a componente axial ao longo de $\hat{\mathbf{z}}$ sobrevive.

5. **Executar a integração:**
   $$B_z(z) = \frac{\mu_0 I}{4\pi} \int_{0}^{2\pi} \frac{R^2 d\phi'}{(R^2 + z^2)^{3/2}} = \frac{\mu_0 I R^2}{4\pi (R^2 + z^2)^{3/2}} \int_{0}^{2\pi} d\phi'$$

   $$B_z(z) = \frac{\mu_0 I R^2}{2(R^2 + z^2)^{3/2}}$$

   $$\mathbf{B}(0, 0, z) = \frac{\mu_0 I R^2}{2(R^2 + z^2)^{3/2}} \hat{\mathbf{z}}$$

### Exemplo 2: Campo Magnético de um Fio Retilíneo Infinito

Calcule o campo magnético a uma distância perpendicular $s$ de um fio retilíneo infinitamente longo transportando uma corrente estacionária $I$ ao longo do eixo $z$.

#### Solução:
1. **Montar a integral:**
   Considere o fio ao longo do eixo $z$ ($d\mathbf{l} = dz' \hat{\mathbf{z}}$). O ponto de campo está localizado em $\mathbf{r} = s \hat{\boldsymbol{\rho}}$.
   $\boldsymbol{\mathcal{R}} = s \hat{\boldsymbol{\rho}} - z' \hat{\mathbf{z}}$, resultando em $\mathcal{R} = \sqrt{s^2 + (z')^2}$.

2. **Calcular o produto vetorial:**
   $$d\mathbf{l} \times \boldsymbol{\mathcal{R}} = (dz' \hat{\mathbf{z}}) \times (s \hat{\boldsymbol{\rho}} - z' \hat{\mathbf{z}}) = s dz' \hat{\boldsymbol{\phi}}$$

3. **Integrar ao longo do comprimento infinito:**
   $$\mathbf{B}(s) = \frac{\mu_0 I s \hat{\boldsymbol{\phi}}}{4\pi} \int_{-\infty}^{\infty} \frac{dz'}{(s^2 + (z')^2)^{3/2}}$$

   Utilizando a substituição trigonométrica padrão $z' = s \tan\theta$:
   $$\int_{-\infty}^{\infty} \frac{dz'}{(s^2 + (z')^2)^{3/2}} = \frac{2}{s^2}$$

4. **Expressão final do campo:**
   $$\mathbf{B}(s) = \frac{\mu_0 I}{2\pi s} \hat{\boldsymbol{\phi}}$$

## Aplicações e Conexões Avançadas

### Conexão com a Lei de Ampère

A Lei de Biot-Savart é a formulação integral localizada da magnetostática. Ao aplicar o rotacional na forma volumétrica contínua de Biot-Savart, obtém-se a forma diferencial da Lei de Ampère:

$$\boldsymbol{\nabla} \times \mathbf{B} = \mu_0 \mathbf{J}$$

Enquanto a Lei de Ampère fornece um método eficiente para calcular campos magnéticos em sistemas com alta simetria (ex.: cilindros infinitos, solenoide), a Lei de Biot-Savart permanece universalmente aplicável a geometrias de corrente complexas ou com baixa simetria, onde os laços de integração amperiamos não podem ser explorados.

### Equivalência do Momento de Dipolo Magnético

No limite de campo distante ($z \gg R$), o campo magnético da espira circular derivado no Exemplo 1 simplifica-se para:

$$\mathbf{B}(z) \approx \frac{\mu_0 I R^2}{2 z^3} \hat{\mathbf{z}} = \frac{\mu_0}{2\pi} \frac{\mathbf{m}}{z^3}$$

Onde $\mathbf{m} = I A \hat{\mathbf{z}} = I (\pi R^2) \hat{\mathbf{z}}$ é o momento de dipolo magnético da espira. Isso demonstra que, a grandes distâncias, laços de corrente localizados se comportam de forma idêntica a dipolos elétricos, estabelecendo as bases para o magnetismo atômico e modelos de magnetização da matéria.