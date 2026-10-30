---
id: "dielectrics"
title: "Dielectrics, Polarization Mechanisms, and Bound Charges"
domain: "physics"
module: "electromagnetism"
type: "concept"
schema_version: "2.0"
level: "intermediate"
language: "pt"
prerequisites:
  - "capacitance"
  - "electric-dipole-moment"
  - "vector-calculus-divergence"
tags:
  - "electrostatics"
  - "dielectrics"
  - "polarization"
  - "bound-charges"
  - "susceptibility"
---


# Dielétricos, Mecanismos de Polarização e Cargas Ligadas

## Contexto e Fundamentação Física

Considere um capacitor de placas paralelas no vácuo submetido a uma densidade superficial de carga livre $+\sigma$ na placa esquerda e $-\sigma$ na placa direita. Essas cargas estabelecem um campo elétrico uniforme $\mathbf{E}_0$ orientado para a direita.

Ao preencher o volume entre as placas com um material condutor perfeito, os elétrons livres migram instantaneamente para as fronteiras até que o campo elétrico no interior do material seja completamente anulado ($\mathbf{E} = 0$).

Entretanto, quando o meio interposto é um isolante elétrico (dielétrico), os elétrons permanecem vinculados aos seus respectivos núcleos atômicos por forças de atração coulombiana. O campo elétrico externo $\mathbf{E}_0$ não consegue produzir condução macroscópica de corrente, mas deforma a estrutura atômica do meio:
* As nuvens eletrônicas negativas sofrem um deslocamento no sentido oposto ao campo.
* Os núcleos atômicos positivos são deslocados no sentido do campo.

Esse microdeslocamento transforma os átomos neutros em dipolos elétricos induzidos. A soma desses momentos dipolares microscópicos altera o campo eletrostático resultante no interior do meio, reduzindo a intensidade total do campo sem anulá-lo completamente. A necessidade de quantificar e prever essa atenuação do campo elétrico pela matéria motivou a formulação da teoria dos meios dielétricos.

---

## Formulação Teórica

### O Mecanismo da Polarização e a Oposição de Campos

Considere o modelo atômico em que o núcleo positivo e a nuvem eletrônica negativa estão conectados por uma força restauradora linear (análoga a uma mola atômica). Na ausência de campo externo, o centro de carga positiva coincide com o centro de carga negativa, resultando em um momento de dipolo nulo.

Sob a ação de um campo externo $\mathbf{E}_0$, o dipolo induzido $\mathbf{p}$ alinha-se com o campo. Para descrever o estado de polarização em escala macroscópica, define-se o **Vetor Polarização ($\mathbf{P}$)** como a densidade volumétrica de momentos de dipolo elétrico:

$$\mathbf{P} = \lim_{\Delta V \to 0} \frac{1}{\Delta V} \sum_{i=1}^{N \Delta V} \mathbf{p}_i = \frac{d\mathbf{p}}{dV}$$

No Sistema Internacional (SI), a dimensão de $\mathbf{P}$ é expressa em Coulombs por metro quadrado ($\text{C/m}^2$).

![Mecanismo de polarização em dielétricos.](./../../../../dielectric-polarization-mechanism.svg)
*Figura 1: Mecanismo de polarização em um dielétrico homogêneo. No interior do volume, as cargas opostas de dipolos adjacentes neutralizam-se mutuamente. Nas fronteiras do material, surge uma distribuição não compensada de cargas ligadas ($\sigma_b$).*

---

### Formação de Cargas Ligadas ($\sigma_b$ e $\rho_b$)

No interior do volume de um dielétrico homogêneo e uniformemente polarizado, o polo positivo de um dipolo atômico encontra-se adjacente ao polo negativo do dipolo contíguo, mantendo a neutralidade volumétrica de carga. Nas superfícies limite do material, contudo, essa compensação mútua não ocorre, resultando no acúmulo de **Cargas Ligadas Superficiais ($\sigma_b$)**.

Diferente das cargas livres, as cargas ligadas pertencem à própria estrutura atômica do isolante e não podem ser removidas por condução ou aterramento.

#### Densidade Superficial de Carga Ligada ($\sigma_b$)
A carga total que atravessa uma área $A$ na fronteira do dielétrico é dada pelo produto escalar entre o vetor polarização e o vetor normal unitário $\hat{\mathbf{n}}$ apontando para fora do meio:

$$\sigma_b = \mathbf{P} \cdot \hat{\mathbf{n}}$$

#### Densidade Volumétrica de Carga Ligada ($\rho_b$)
Caso a polarização seja não uniforme no espaço, o cancelamento de cargas no interior do volume falha, gerando um acúmulo volumétrico de carga ligado à divergência espacial do vetor $\mathbf{P}$:

$$\rho_b = -\nabla \cdot \mathbf{P}$$

Em meios homogêneos submetidos a campos uniformes, $\nabla \cdot \mathbf{P} = 0$, o que implica $\rho_b = 0$. As cargas ligadas manifestam-se unicamente nas superfícies do dielétrico.

---

### O Campo Elétrico Resultante e Meios Lineares

As cargas ligadas superficiais $+\sigma_b$ e $-\sigma_b$ geram um campo elétrico induzido interno $\mathbf{E}_{\text{induzido}}$ orientado no sentido oposto ao campo aplicado $\mathbf{E}_0$. O campo elétrico líquido resultante $\mathbf{E}$ no interior do dielétrico é dado pela superposição:

$$\mathbf{E} = \mathbf{E}_0 - \mathbf{E}_{\text{induzido}}$$

Para **Meios Lineares, Isotrópicos e Homogêneos (LIH)**, a magnitude da polarização $\mathbf{P}$ é diretamente proporcional ao campo elétrico líquido interno $\mathbf{E}$:

$$\mathbf{P} = \varepsilon_0 \chi_e \mathbf{E}$$

em que:
* $\chi_e$ é a **Suscetibilidade Elétrica** do meio (uma constante adimensional).
* $\varepsilon_0$ é a permissividade elétrica do vácuo ($\approx 8{,}854 \times 10^{-12} \text{ F/m}$).

Define-se a **Permissividade Relativa ($\varepsilon_r$)** (ou constante dielétrica) como:

$$\varepsilon_r = 1 + \chi_e$$

A relação entre o campo elétrico aplicado e o campo resultante interno no dielétrico simplifica-se para:

$$\mathbf{E} = \frac{\mathbf{E}_0}{\varepsilon_r}$$

---

## Exemplos e Exercícios Resolvidos

### Determinação do Campo e Cargas em um Dielétrico Linear

**Problema:** Uma placa homogênea de Teflon ($\varepsilon_r = 2{,}10$) é posicionada perpendicularmente a um campo elétrico aplicado no vácuo de módulo $E_0 = 4{,}2 \times 10^4 \text{ V/m}$ orientado na direção $+x$. Determine:
* O campo elétrico líquido resultante $\mathbf{E}$ no interior do teflon.
* O vetor polarização $\mathbf{P}$ do material.
* As densidades superficiais de carga ligada $\sigma_b$ em ambas as faces normais ao eixo $x$.

#### Resolução:

##### Campo Elétrico Resultante
O campo interno reduz-se pelo fator da permissividade relativa $\varepsilon_r$:

$$\mathbf{E} = \frac{\mathbf{E}_0}{\varepsilon_r} = \frac{4{,}2 \times 10^4 \hat{\mathbf{a}}_x}{2{,}10} = 2{,}0 \times 10^4 \hat{\mathbf{a}}_x \text{ V/m}$$

##### Suscetibilidade e Vetor Polarização
A suscetibilidade do teflon é dada por:

$$\chi_e = \varepsilon_r - 1 = 2{,}10 - 1 = 1{,}10$$

Aplicando a relação constitutiva para meios lineares:

$$\mathbf{P} = \varepsilon_0 \chi_e \mathbf{E}$$

$$\mathbf{P} = (8{,}854 \times 10^{-12} \text{ F/m}) \cdot (1{,}10) \cdot (2{,}0 \times 10^4 \hat{\mathbf{a}}_x \text{ V/m})$$

$$\mathbf{P} = 1{,}948 \times 10^{-7} \hat{\mathbf{a}}_x \text{ C/m}^2 \approx 0{,}195 \hat{\mathbf{a}}_x \, \mu\text{C/m}^2$$

##### Densidades Superficiais de Carga Ligada
* **Face Direita ($\hat{\mathbf{n}} = +\hat{\mathbf{a}}_x$):**
  $$\sigma_{b,\text{direita}} = \mathbf{P} \cdot (+\hat{\mathbf{a}}_x) = +0{,}195 \, \mu\text{C/m}^2$$

* **Face Esquerda ($\hat{\mathbf{n}} = -\hat{\mathbf{a}}_x$):**
  $$\sigma_{b,\text{esquerda}} = \mathbf{P} \cdot (-\hat{\mathbf{a}}_x) = -0{,}195 \, \mu\text{C/m}^2$$

---

### Densidade Volumétrica de Carga em Polarização Não Uniforme

**Problema:** Considere uma região cilíndrica onde o vetor polarização de um dielétrico varia radialmente segundo a função $\mathbf{P}(r) = k r^2 \hat{\mathbf{a}}_r$ em coordenadas cilíndricas, em que $k$ é uma constante positiva. Calcule a densidade volumétrica de carga ligada $\rho_b$ no interior do meio.

#### Resolução:
A densidade volumétrica de carga ligada liga-se ao divergente do vetor polarização:

$$\rho_b = -\nabla \cdot \mathbf{P}$$

Em coordenadas cilíndricas, o divergente de um campo vetorial que possui apenas componente radial $P_r(r) = k r^2$ é dado por:

$$\nabla \cdot \mathbf{P} = \frac{1}{r} \frac{\partial}{\partial r} (r P_r) = \frac{1}{r} \frac{\partial}{\partial r} (r \cdot k r^2) = \frac{1}{r} \frac{\partial}{\partial r} (k r^3)$$

Calculando a derivada parcial:

$$\nabla \cdot \mathbf{P} = \frac{1}{r} (3 k r^2) = 3 k r$$

Substituindo na expressão da carga ligada volumétrica:

$$\rho_b = -3 k r$$

A dependência espacial indica um acúmulo não nulo de carga ligada negativa no volume do meio, cuja magnitude cresce linearmente com o raio $r$.

---

## Aplicações e Relações Avançadas

### Limite de Ruptura Dielétrica e Rigidez Dielétrica
A resposta elástica da polarização possui um limite físico crítico. Caso a intensidade do campo elétrico aplicado exceda a **Rigidez Dielétrica ($E_{\text{máx}}$)** do isolante, a força eletrostática exercida sobre os elétrons superará a força de atração nuclear. Ocorre a ionização do meio (ruptura dielétrica), transformando o isolante em um condutor e gerando uma descarga elétrica destrutiva.

| Material | Permissividade Relativa ($\varepsilon_r$) | Rigidez Dielétrica ($E_{\text{máx}}$ em $\text{kV/mm}$) |
| :--- | :--- | :--- |
| **Vácuo** | $1{,}00000$ | Infinito |
| **Ar Seco (1 atm)** | $1{,}00059$ | $3{,}0$ |
| **Teflon (PTFE)** | $2{,}10$ | $60{,}0$ |
| **Papel Transformador** | $3{,}50$ | $16{,}0$ |
| **Vidro Pyrex** | $4{,}70$ | $14{,}0$ |
| **Titanato de Bário ($\text{BaTiO}_3$)** | $1250{,}00$ | $5{,}0$ |

### Reformulação da Lei de Gauss e o Vetor Deslocamento Elétrico ($\mathbf{D}$)
Para contornar a necessidade de rastrear explicitamente as cargas ligadas em problemas eletrostáticos complexos, define-se o **Vetor Deslocamento Elétrico ($\mathbf{D}$)**:

$$\mathbf{D} = \varepsilon_0 \mathbf{E} + \mathbf{P}$$

A forma diferencial da Lei de Gauss na matéria depende exclusivamente da densidade de **cargas livres ($\rho_f$)**:

$$\nabla \cdot \mathbf{D} = \rho_f$$

Em meios lineares, a relação simplifica-se para $\mathbf{D} = \varepsilon \mathbf{E}$, permitindo calcular campos elétricos em geometrias complexas com dielétricos aplicando os mesmos métodos analíticos utilizados para o vácuo.