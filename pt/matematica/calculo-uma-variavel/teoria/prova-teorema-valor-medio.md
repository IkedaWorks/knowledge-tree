
# Demonstração: Por que o Rolle e o TVM são verdade?

## Por que o Teorema de Rolle é verdade?

Antes de provar o TVM, precisamos aceitar o Rolle.

**A lógica:** Se você sai do chão, sobe e depois volta para o chão ($f(a) = f(b)$), e você faz isso de forma suave (derivável), em algum momento você parou de subir para começar a descer.

### Demonstração Lógica:

1. **Caso Constante:** Se a função for constante (uma linha reta horizontal), a derivada é zero em todos os pontos. Provado.
    
2. **Caso Não-Constante:** Se ela não for constante, ela tem que subir ou descer. Se ela sobe, ela atinge um valor máximo ou mínimo em um ponto $c$.
    
3. **Ponto de Extremo:** Como $c$ é um ponto de máximo ou mínimo e a função é derivável, a reta tangente ali tem que ser horizontal ($f'(c) = 0$). Se a inclinação fosse positiva, você ainda estaria subindo; se fosse negativa, você já teria passado do topo.
    

---

## Demonstração do Teorema do Valor Médio (TVM)

Agora, vamos provar o TVM usando o Rolle. O truque aqui é "entortar" a nossa visão para que a reta média pareça horizontal.

### O Passo a Passo:

1. **Definir a Reta Secante:**
    
    A reta que liga os pontos $(a, f(a))$ e $(b, f(b))$ tem a equação:
    
    $$y = f(a) + \frac{f(b) - f(a)}{b - a}(x - a)$$
    
2. **Criar a Função Auxiliar ($h(x)$):**
    
    Imagine uma nova função que mede a distância vertical entre a nossa curva complexa $f(x)$ e a reta secante.
    
    $$h(x) = f(x) - \left[ f(a) + \frac{f(b) - f(a)}{b - a}(x - a) \right]$$
    
3. **Testar os Extremos de $h(x)$:**
    
    - Se você colocar $x = a$, o resultado é $0$.
        
    - Se você colocar $x = b$, o resultado também é $0$.
        
    - **Conclusão:** $h(a) = h(b)$. A função $h(x)$ começa e termina no "zero"!
        
4. **Chamar o Teorema de Rolle:**
    
    Como $h(x)$ é contínua, derivável e $h(a) = h(b)$, o Teorema de Rolle garante que existe um ponto $c$ onde a derivada de $h$ é zero: $h'(c) = 0$.
    
5. **Finalizar a Álgebra:**
    
    Derivando $h(x)$ em relação a $x$:
    
    $$h'(x) = f'(x) - \frac{f(b) - f(a)}{b - a}$$
    
    No ponto $c$, onde $h'(c) = 0$:
    
    $$0 = f'(c) - \frac{f(b) - f(a)}{b - a} \implies f'(c) = \frac{f(b) - f(a)}{b - a}$$
    

---

## Por que isso faz sentido agora?

Imagine que a reta secante (a média) é o seu **horizonte**.

- **Rolle** diz que se você sobe e volta para o horizonte, houve um pico.
    
- **TVM** diz que não importa se o seu horizonte está inclinado ou reto; se você se afasta dele e depois volta, em algum momento você teve que se mover paralelamente a ele.