
# O Comportamento das Funções: f' e f''

## Primeira Derivada (f'): O Sensor de Direção

Mede a inclinação da reta tangente. Responde: "Para onde estamos indo?"

- **f'(x) > 0 (Positiva):** Função **CRESCENTE**.
    
    - _Pense:_ O sistema está ganhando valor (subindo a ladeira).
        
- **f'(x) < 0 (Negativa):** Função **DECRESCENTE**.
    
    - _Pense:_ O sistema está perdendo valor (descendo a ladeira).
        
- **f'(x) = 0 (Zero):** **PONTO CRÍTICO**.
    
    - _Pense:_ O sistema parou momentaneamente para mudar de direção.
        

## Segunda Derivada (f''): O Sensor de Concavidade

Mede a taxa de variação da inclinação. Responde: "Qual a tendência da curva?"

- **f''(x) > 0 (Positiva):** Concavidade para **CIMA** (Formato de Vale/Sorriso).
    
    - _Lógica:_ A inclinação está aumentando. Você está parando de descer para começar a subir.
        
- **f''(x) < 0 (Negativa):** Concavidade para **BAIXO** (Formato de Pico/Guarda-chuva).
    
    - _Lógica:_ A inclinação está diminuindo. Você está perdendo o fôlego na subida.
        
- **f''(x) = 0:** **Ponto de INFLEXÃO**.
    
    - _Lógica:_ É onde a curva muda de "sorriso" para "guarda-chuva" (ou vice-versa).
        

## O Teste de Otimização

Quando você acha um ponto onde a função parou ($f' = 0$), a segunda derivada te diz o que esse ponto é:

1. **Se $f'(x) = 0$ e $f''(x) < 0$ (Negativa):**
    
    - A curva quer "olhar para baixo" (pico).
        
    - **Resultado:** MÁXIMO LOCAL.
        
2. **Se $f'(x) = 0$ e $f''(x) > 0$ (Positiva):**
    
    - A curva quer "olhar para cima" (vale).
        
    - **Resultado:** MÍNIMO LOCAL.
        

## Exemplo Prático

**Função:** $f(x) = x^3 - 3x$

1. **Passo 1 (Derivada 1):** $f'(x) = 3x^2 - 3$
    
    - Igualando a zero: $3x^2 = 3 \implies x^2 = 1 \implies$ Zera em **$x = 1$** e **$x = -1$**.
        
2. **Passo 2 (Derivada 2):** $f''(x) = 6x$
    
    - **No ponto $x = 1$:** $f''(1) = +6$ (Positivo). É um **Mínimo**.
        
    - **No ponto $x = -1$:** $f''(-1) = -6$ (Negativo). É um **Máximo**.
        
    - **No ponto $x = 0$:** $f''(0) = 0$. É o **Ponto de Inflexão**.