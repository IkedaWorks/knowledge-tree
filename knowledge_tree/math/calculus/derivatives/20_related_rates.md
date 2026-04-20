
# Taxas Relacionadas: O Cálculo em Movimento

## 1. O Conceito e a Intuição

Até agora, analisamos como $y$ muda em relação a $x$. Nas **Taxas Relacionadas**, o cenário muda: temos duas ou mais variáveis (como raio, volume, altura ou distância) que dependem de uma terceira variável invisível e onipresente: o **tempo ($t$)**.

> [!TIP] A Intuição do Balão
> 
> Imagine encher um balão esférico. À medida que você injeta ar (variação do Volume no tempo: $dV/dt$), o raio do balão aumenta ($dr/dt$).
> 
> Essas taxas estão "amarradas" pela geometria. Se você conhece a velocidade da bomba de ar, você descobre a velocidade de expansão da borracha.

---

## 2. O Algoritmo de Resolução (Pipeline)

Para resolver problemas de taxas, o Engenheiro segue um fluxo lógico:

1. **Identificar as Variáveis:** Liste as taxas conhecidas e a taxa desejada (Ex: Tenho $dV/dt$, quero $dh/dt$).
    
2. **Equação de Ligação:** Encontre a fórmula geométrica que conecta as variáveis (Volume, Área, Pitágoras).
    
3. **Derivação Implícita no Tempo:** Derive ambos os lados em relação a $t$.
    
    - _O Pulo do Gato:_ Como todas as variáveis dependem de $t$, toda derivada ganha o "carimbo" de Leibniz ($\frac{dV}{dt}, \frac{dr}{dt}, \frac{dh}{dt}$).
        
4. **Substituição Instantânea:** Coloque os valores conhecidos para o **instante exato** pedido e isole a incógnita.
    

---

## 3. Exercício 1: O Tanque Cônico (Clássico de Sensores)

**Problema:** Um tanque cônico invertido tem 10m de altura e 4m de raio no topo. Água é bombeada a $2\text{ m}^3/\text{min}$. Qual a velocidade de subida do nível ($\frac{dh}{dt}$) quando a profundidade $h$ for 5m?

### Resolução Passo a Passo:

1. **Dados:** $\frac{dV}{dt} = 2$. Queremos $\frac{dh}{dt}$ quando $h = 5$.
    
2. **Equação:** $V = \frac{1}{3}\pi r^2 h$.
    
3. **Redução de Variáveis (Semelhança de Triângulos):**
    
    O raio e a altura mantêm a proporção do tanque: $\frac{r}{h} = \frac{4}{10} \implies r = 0,4h$.
    
    Substituindo no volume: $V = \frac{1}{3}\pi (0,4h)^2 h \implies V = \frac{0,16\pi}{3} h^3$.
    
4. **Derivando no Tempo:**
    
    $$\frac{dV}{dt} = \frac{0,16\pi}{3} \cdot 3h^2 \cdot \frac{dh}{dt} \implies \frac{dV}{dt} = 0,16\pi h^2 \frac{dh}{dt}$$
    
5. **Cálculo Final:**
    
    $$2 = 0,16\pi (5^2) \frac{dh}{dt} \implies 2 = 4\pi \frac{dh}{dt}$$
    
    $$\frac{dh}{dt} = \frac{1}{2\pi} \approx 0,16\text{ m/min}$$
    

---

## 4. Exercício 2: O Vazamento de Petróleo (Nível Petrobrás)

**Cenário:** Óleo vaza em formato circular. A área aumenta a uma taxa constante de $6\pi \text{ km}^2/\text{h}$. Quão rápido o raio cresce ($\frac{dr}{dt}$) quando $r = 3 \text{ km}$?

### Resolução:

1. **Equação:** $A = \pi r^2$.
    
2. **Derivação Implícita:**
    
    $$\frac{dA}{dt} = 2\pi r \frac{dr}{dt}$$
    
3. **Substituição:**
    
    $$6\pi = 2\pi (3) \frac{dr}{dt} \implies 6\pi = 6\pi \frac{dr}{dt}$$
    
    **Resultado:** $\frac{dr}{dt} = 1 \text{ km/h}$.
    

> [!IMPORTANT] Interpretação de Engenharia
> 
> Note que, se a taxa de área ($\frac{dA}{dt}$) é constante, a velocidade do raio ($\frac{dr}{dt}$) **diminui** conforme o círculo cresce. Isso ocorre porque manter o mesmo aumento de área em um círculo gigante exige muito menos avanço no raio do que em um círculo pequeno.

---

## 5. Macetes de Estudo

- **Abstração:** O cálculo não é estático. Não veja o círculo como um desenho, veja-o como um evento que está "acontecendo".
    
- **Geometria é Base:** Se você não souber as fórmulas de volume ($V_{esfera} = \frac{4}{3}\pi r^3$) ou área, você trava antes de começar o cálculo.
    
- **As Taxas Constantes:** Quando o problema diz que algo varia a uma taxa constante, questione: "Quem precisa mudar de velocidade para que essa proporção se mantenha?". No cone, conforme ele fica mais largo no topo, a água precisa subir mais devagar para manter o mesmo fluxo de entrada.