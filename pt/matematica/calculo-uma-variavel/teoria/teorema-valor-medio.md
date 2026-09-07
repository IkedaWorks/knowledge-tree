
# Teorema de Rolle e Teorema do Valor Médio (TVM)

## Teorema de Rolle (O caso específico)

O Teorema de Rolle diz que, se uma função é contínua e derivável, e ela começa e termina na mesma "altura" (mesmo valor de $y$), então em algum momento ela teve que parar de subir para começar a descer (ou vice-versa).

### Condições:

- $f(x)$ é contínua no intervalo fechado $[a, b]$.
    
- $f(x)$ é derivável no intervalo aberto $(a, b)$.
    
- $f(a) = f(b)$ (Pontos de partida e chegada iguais).
    

### Conclusão:

Existe pelo menos um ponto $c$ entre $a$ e $b$ onde a inclinação é zero:

$$f'(c) = 0$$

## Teorema do Valor Médio (A Generalização)

O TVM é o Rolle "inclinado". Ele diz que existe um ponto onde a inclinação instantânea (derivada) é exatamente igual à inclinação média de todo o percurso.

- **Intuição de Engenharia:** Se você viajou de São Paulo a São José dos Campos (100 km) em 1 hora, sua velocidade média foi de 100 km/h. O TVM garante que, em pelo menos um milissegundo da viagem, o seu velocímetro marcou exatamente 100 km/h.
    

### Conclusão:

Existe um ponto $c$ no intervalo $(a, b)$ tal que:

$$f'(c) = \frac{f(b) - f(a)}{b - a}$$

## Por que isso é importante?

Sem esses teoremas, não poderíamos provar coisas fundamentais como:

1. Se a derivada é sempre zero, a função é constante.
    
2. Se a derivada é sempre positiva, a função é crescente.
    
3. A própria regra de L'Hôpital que usamos lá atrás depende do TVM para ser demonstrada.
    

## O "Pulo do Gato":

- **Rolle:** Garante um ponto de repouso ($f' = 0$).
    
- **TVM:** Garante que a realidade instantânea reflete a média do percurso.