
# Diferenciação de Funções Paramétricas
## 1. Explicação e Intuição

No modelo tradicional, $y$ depende diretamente de $x$. Na forma **paramétrica**, tanto $x$ quanto $y$ são funções de uma terceira variável independente: o **parâmetro** ($t$), que geralmente simboliza o tempo ou o ângulo.

> [!TIP] 
> Visão de Desenvolvedor
> 
> Imagine o movimento de um cursor ou de um projétil em um motor de jogo. Em vez de uma trajetória estática, descrevemos a posição da partícula em cada instante:
> 
> - $x = f(t)$ (Posição horizontal no instante $t$)
>     
> - $y = g(t)$ (Posição vertical no instante $t$)
>     

Essa representação permite descrever curvas que "voltam sobre si mesmas" (como espirais ou trajetórias orbitais), algo que funções comuns falham por não passarem no teste da reta vertical.

---

## 2. Regras de Derivação

Para encontrar a inclinação da reta tangente ($\frac{dy}{dx}$) no plano $xy$ a partir de parâmetros, utilizamos a **Regra da Cadeia**.

### I. Primeira Derivada (Inclinação)

A variação de $y$ em relação a $x$ é a razão entre suas taxas de variação temporal:

$$\frac{dy}{dx} = \frac{\frac{dy}{dt}}{\frac{dx}{dt}}, \quad \text{desde que } \frac{dx}{dt} \neq 0$$

### II. Segunda Derivada (Concavidade)

Aqui ocorre o erro mais comum: **não basta derivar o resultado anterior novamente em relação a $t$**. É preciso normalizar o resultado pela velocidade com que o $x$ está mudando:

$$\frac{d^2y}{dx^2} = \frac{\frac{d}{dt} \left( \frac{dy}{dx} \right)}{\frac{dx}{dt}}$$

---

## 3. Exercícios Resolvidos

### Exercício 1: A Cicloide (A curva do pneu)

A cicloide é o rastro deixado por um ponto em um pneu de bicicleta em movimento.

Dada a curva: $x = 2(t - \sin t)$ e $y = 2(1 - \cos t)$, encontre a inclinação da tangente em $t = \pi/2$.

1. **Derivadas temporais:**
    
    - $\frac{dx}{dt} = 2(1 - \cos t)$
        
    - $\frac{dy}{dt} = 2(\sin t)$
        
2. **Razão das taxas:**
    
    $$\frac{dy}{dx} = \frac{2\sin t}{2(1 - \cos t)} = \frac{\sin t}{1 - \cos t}$$
    
3. **Avaliação no ponto $t = \pi/2$:**
    
    $$\frac{\sin(\pi/2)}{1 - \cos(\pi/2)} = \frac{1}{1 - 0} = 1$$
    
    **Resultado:** A inclinação é 1 (o que equivale a um ângulo de 45°).
    

### Exercício 2: Concavidade na Astróide

A astróide assemelha-se a um quadrado com lados curvos para dentro. Suas equações são: $x = \cos^3 t$ e $y = \sin^3 t$.

1. **Primeira Derivada:**
    
    - $\frac{dx}{dt} = -3\cos^2 t \cdot \sin t$
        
    - $\frac{dy}{dt} = 3\sin^2 t \cdot \cos t$
        
    - $\frac{dy}{dx} = \frac{3\sin^2 t \cos t}{-3\cos^2 t \sin t} = -\tan t$
        
2. **Segunda Derivada:**
    
    - Derivada do resultado em relação a $t$: $\frac{d}{dt}(-\tan t) = -\sec^2 t$
        
    - Dividindo pela taxa de $x$ ($\frac{dx}{dt}$):
        
        $$\frac{d^2y}{dx^2} = \frac{-\sec^2 t}{-3\cos^2 t \cdot \sin t}$$
        
        **Resultado:** $\frac{d^2y}{dx^2} = \frac{1}{3\cos^4 t \cdot \sin t}$
        

---

> [!NOTE] 
> Aplicação em Eletromagnetismo (Física 3)
> 
> Embora pareça abstrato, o uso de parametrização simplifica drasticamente equações que envolvem partículas carregadas em campos magnéticos. Em vez de lidar com equações cartesianas "monstruosas", você resolve o problema para $x(t)$ e $y(t)$ separadamente, o que é o padrão ouro na modelagem física moderna.
> Esse é apenas um exemplo que eu achei relevante, você usará em isso em diversas área do conhecimento, principalmente na física.