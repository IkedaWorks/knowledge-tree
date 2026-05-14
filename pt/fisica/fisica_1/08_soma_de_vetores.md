
# 🏛️ Adição de Forças Planas: Geometria e Rigor

> [!IMPORTANT] 
> 
> **Requisitos Prévios**
> 
> Esta nota assume que você já domina:
> 
> **- Geometria Plana:** Propriedades de paralelogramos, ângulos alternos internos e suplementares.
>     
> **- Trigonometria:** Aplicação direta da Lei dos Senos e Lei dos Cossenos.
>     
> **- Conceito de Vetor:** A distinção fundamental entre grandeza escalar e vetorial.
>     

## O Problema da Composição de Forças

Na estática, raramente lidamos com uma única força isolada. A necessidade de encontrar uma força resultante surge para simplificar sistemas complexos em um único efeito equivalente. No entanto, o método que você vai usar depende inteiramente de quantas forças estão em jogo e da geometria do problema.

## A Regra do Paralelogramo e sua Limitação

Este é o método fundamental, mas cuidado: ele é restrito estritamente à soma de **apenas duas forças** que partem de um mesmo ponto. A resultante é a diagonal do paralelogramo formado pelas componentes. Se você tiver três forças, precisará somar duas, encontrar uma resultante parcial e depois somá-la com a terceira.

![Regra do Paralelogramo](./../../../assets/parallelogram-law.webp)
## A Regra do Triângulo e a Poligonal

Para otimizar o cálculo, usamos a regra do triângulo, que nada mais é do que a metade do paralelogramo. Você posiciona a extremidade da primeira força na origem da segunda; a resultante será o vetor que fecha esse triângulo.

Quando o sistema possui múltiplas forças (três ou mais), evoluímos para a regra da poligonal. O processo é o mesmo: você empilha os vetores um após o outro ("ponta com cauda"). A força resultante será o vetor que liga a origem do primeiríssimo vetor até a ponta do último. Se esse polígono fechar exatamente no ponto de partida, você acabou de provar graficamente que o sistema está em equilíbrio e a resultante é zero.

Exemplo regra do triângulo:


![triangle law](./../../../assets/triangle-law.webp)

Exemplo regra da poligonal:


![Polygonal Law](./../../../assets/polygonal-law.webp)

## Dinâmica do Raciocínio

A matemática por trás disso existe para validar o que o desenho nos diz. Imagine que você está traçando uma rota de navegação. Cada força é um deslocamento. Se você puxa para uma direção e depois para outra, o resultado final é o deslocamento direto do ponto inicial ao ponto final.

A Lei dos Cossenos entra aqui para medir o "comprimento" dessa rota final quando o ângulo entre as puxadas não é de 90 graus. Já a Lei dos Senos serve para ajustar a bússola, determinando o ângulo exato da direção resultante. É um jogo de geometria: você usa as propriedades de retas paralelas para "transportar" os ângulos do enunciado para dentro do seu triângulo de forças.

---
## Aplicação Prática

Para resolver exercícios com precisão, o foco deve estar na montagem do triângulo de forças e na identificação dos ângulos internos.

# 🔩 Exercício 01: Soma Geométrica em Parafuso de Fixação

> [!IMPORTANT] 
> 
> **Requisitos:**
> 
> - Identificação de ângulos suplementares.
>     
> - Aplicação da Lei dos Cossenos para magnitude.
>     
> - Domínio do terminal para conversão de assets.
>     

## Enunciado

Um parafuso de fixação em uma base de aço está sujeito a duas forças de tração exercidas por cordas,  $\vec{F_1}$  e  $\vec{F_2}$ . A força  $\vec{F_1}$  tem intensidade de $200\text{ N}$ a $20^\circ$ com a horizontal, enquanto  $\vec{F_2}$  tem  $300\text{ N}$  a  $10^\circ$  com a vertical. Determine a força resultante ( $\vec{F_R}$ ) que o parafuso deve suportar. Determine a direção da $\vec{F_R}$  em relação ao eixo $x$ positivo.


## Representação Visual

![Exercicio 1](./../../../assets/fisica-1-exemplo-soma-vetores.webp)

---

### Solução do Exercício: Soma Vetorial no Parafuso

**Dados do Problema:**

- $F_1 = 200\text{ N}$ a $20^\circ$ com o eixo $x$ positivo.
    
- $F_2 = 300\text{ N}$ a $10^\circ$ com o eixo $y$ positivo (vertical).
    

#### 1. Análise Geométrica (O Triângulo de Forças)

Para usar a Lei dos Cossenos, precisamos do ângulo interno do triângulo formado ao colocar $\vec{F_2}$ na ponta de $\vec{F_1}$.

- O ângulo entre as duas forças no plano é: $90^\circ - (20^\circ + 10^\circ) = 60^\circ$.
    
- Ao transpor $\vec{F_2}$ para a ponta de $\vec{F_1}$, o ângulo interno $\beta$ será o suplementar:
    
    $$\beta = 180^\circ - 60^\circ = 120^\circ$$
    

#### 2. Intensidade da Força Resultante ($F_R$)

Aplicando a **Lei dos Cossenos**:

$$F_R = \sqrt{F_1^2 + F_2^2 - 2 \cdot F_1 \cdot F_2 \cdot \cos(\beta)}$$

$$F_R = \sqrt{200^2 + 300^2 - 2(200)(300) \cdot \cos(120^\circ)}$$

Como $\cos(120^\circ) = -0,5$:

$$F_R = \sqrt{40000 + 90000 - (120000 \cdot -0,5)}$$

$$F_R = \sqrt{130000 + 60000} = \sqrt{190000}$$

**$F_R \approx 435,9\text{ N}$**

#### 3. Direção da Resultante em relação ao Eixo $x$ Positivo

Primeiro, encontramos o ângulo $\theta$ entre a resultante $F_R$ e a força $F_1$ usando a **Lei dos Senos**:

$$\frac{F_2}{\sin(\theta)} = \frac{F_R}{\sin(120^\circ)}$$

$$\sin(\theta) = \frac{300 \cdot \sin(120^\circ)}{435,9}$$

$$\sin(\theta) = \frac{300 \cdot 0,866}{435,9} \approx 0,596$$

$$\theta = \arcsin(0,596) \approx 36,6^\circ$$

Agora, como $F_1$ já estava a $20^\circ$ do eixo $x$, a direção final $\phi$ em relação ao eixo $x$ positivo é a soma:

$$\phi = \theta + 20^\circ$$

$$\phi = 36,6^\circ + 20^\circ = 56,6^\circ$$

**Resposta Final:**

A força resultante tem intensidade de **$435,9\text{ N}$** e sua direção é de **$56,6^\circ$** medidos no sentido anti-horário a partir do eixo $x$ positivo.