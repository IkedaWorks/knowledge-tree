
# Proof: Fundamental Theorem of Calculus (Demonstração do TFC)

### A Intuição da Demonstração

Para demonstrar que a derivada da área acumulada é a própria função ($A'(x) = f(x)$), precisamos recorrer à **Definição de Derivada por Limite**.

**A Intuição:** Imagine que você tem uma área acumulada $A(x)$ sob uma curva. Se você avança um passo minúsculo $h$ no eixo $x$, você adiciona uma pequena "fatia" de área.

- Essa fatia tem largura $h$ e altura aproximadamente $f(x)$.
    
- A variação da área ($\Delta A$) é quase um retângulo: $\Delta A \approx \text{base} \cdot \text{altura} = h \cdot f(x)$.
    
- Se a taxa de variação da área é $\frac{\Delta A}{h}$, então $\frac{h \cdot f(x)}{h} = f(x)$.
    

---

### A Formalização Matemática

Vamos definir a função área como $A(x) = \int_{a}^{x} f(t) \, dt$. Pela definição de derivada:

$$A'(x) = \lim_{h \to 0} \frac{A(x+h) - A(x)}{h}$$

#### Passo 1: Subtração das Integrais

Pelas propriedades de integral, a diferença entre a área total até $x+h$ e a área até $x$ é exatamente a integral no pequeno intervalo $[x, x+h]$:

$$A(x+h) - A(x) = \int_{x}^{x+h} f(t) \, dt$$

#### Passo 2: Teorema do Valor Médio (TVM) para Integrais

Sim, até aqui essa "assombração" aparece! O TVM para integrais garante que existe um valor $c$ dentro do intervalo $[x, x+h]$ tal que a área da fatia é exatamente igual a um retângulo de altura $f(c)$ e largura $h$:

$$\int_{x}^{x+h} f(t) \, dt = f(c) \cdot h$$

#### Passo 3: Aplicando o Limite

Substituindo na fórmula da derivada:

$$A'(x) = \lim_{h \to 0} \frac{f(c) \cdot h}{h} = \lim_{h \to 0} f(c)$$

Conforme $h$ tende a zero, o intervalo $[x, x+h]$ "espreme" o ponto $c$ até que ele seja forçado a se tornar o próprio $x$ (pelo Teorema do Confronto/Sanduíche). Logo, $f(c)$ tende a $f(x)$.

**Resultado:** $A'(x) = f(x)$.

---

### Conclusão

A demonstração prova que a integral "guarda" a função original dentro de si. Ao derivar o acúmulo, você remove a "casca" da soma e revela a altura da função naquele exato instante.

- **Derivar a Integral:** É como tirar uma "foto" da velocidade instantânea de um processo de enchimento.
    
- **Integrar a Derivada:** É como somar todas as fotos instantâneas para reconstruir o filme completo.
    

> [!IMPORTANT]
> 
> Essa demonstração é o que valida o uso da **Parte 2 do TFC** ($\int_{a}^{b} f = F(b) - F(a)$), pois agora sabemos com certeza que a integral e a derivada são operações que se anulam.