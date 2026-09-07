
# Aplicações de Derivada: Máximos e Mínimos

## Explicação e Intuição

Imagine que você está em uma cordilheira.

- **O Máximo** é o pico da montanha.
    
- **O Mínimo** é o fundo do vale.
    
- **O Insight do Cálculo:** O que acontece com a sua inclinação (tangente) exatamente quando você está no topo do pico ou no fundo do vale? Você não está nem subindo, nem descendo. Você está "plano" por um instante.
    
- **Matematicamente:** Isso significa que a sua derivada é zero ($f'(x) = 0$).
    

## O Algoritmo da Otimização

Para encontrar esses pontos em qualquer função, seguimos três passos fundamentais:

1. **Encontrar os Pontos Críticos:** Derivamos a função e igualamos a zero ($f'(x) = 0$). Isso nos diz onde a curva "estaciona".
    
2. **O Teste da Segunda Derivada ($f''(x)$):** Como saber se o ponto é um pico (máximo) ou um vale (mínimo) sem olhar o gráfico?
    
    - **Se $f''(x) > 0$:** A concavidade é para cima (sorriso). O ponto é um **Mínimo**.
        
    - **Se $f''(x) < 0$:** A concavidade é para baixo (triste). O ponto é um **Máximo**.
        
3. **Verificar as Extremidades:** Se o problema te der um intervalo fechado (ex: de $x=0$ a $x=10$), você deve testar os valores nesses limites, pois o maior valor pode estar "na borda".
    

## Exemplo

**Cenário:** Você está projetando um novo gabinete para um servidor. Por restrições de espaço, a base deve ser quadrada e o volume total deve ser de exatamente 128 litros ($128.000 \text{ cm}^3$). Qual deve ser a dimensão do lado da base ($x$) e da altura ($h$) para que você gaste a mínima quantidade de metal possível na superfície?

### Resolução:

**Equações:**

- **Volume:** $V = x^2 \cdot h = 128 \implies h = \frac{128}{x^2}$
    
- **Área Total (o que queremos minimizar):** $A = x^2 \text{ (base)} + 4xh \text{ (laterais)}$
    

**Refatoração (Macete):** Substituímos $h$ na área:

$$A(x) = x^2 + 4x\left(\frac{128}{x^2}\right) = x^2 + \frac{512}{x}$$

**Derivada para achar o ponto crítico:**

- $A'(x) = 2x - \frac{512}{x^2}$
    
- $0 = 2x - \frac{512}{x^2} \implies 2x^3 = 512 \implies x^3 = 256$
    
- $x \approx 6,35 \text{ cm}$ (aproximadamente).