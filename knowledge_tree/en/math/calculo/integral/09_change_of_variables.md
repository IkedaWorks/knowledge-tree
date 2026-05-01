
# Change of Variables (Substituição com Mudança de Limites)

### Definição

Ao realizar uma substituição de variável ($u = g(x)$) em uma integral definida, os limites de integração originais ($a$ e $b$) devem ser atualizados para os valores correspondentes na nova variável ($u(a)$ e $u(b)$). Isso permite resolver a integral e aplicar o Teorema Fundamental do Cálculo (TFC) sem precisar retornar à variável original $x$.

#### Vantagens Estratégicas

- **Consistência Matemática:** Evita o erro de notação de escrever limites de $x$ em uma função de $u$.
    
- **Velocidade:** Elimina a etapa de "destrocar" a variável no final da conta.
    
- **Simplificação:** Frequentemente, os novos limites em $u$ resultam em números mais fáceis de calcular (como $0$, $1$ ou $e$).
    

---

### Protocolo de Execução (Passo a Passo)

1. **Escolha do $u$:** Identifique a função interna $g(x)$ cuja derivada $g'(x)$ também esteja presente.
    
2. **Diferencial:** Calcule $du = g'(x) \, dx$.
    
3. **Atualização dos Limites (Crucial):**
    
    - Substitua o limite inferior original ($x = a$) na fórmula de $u$: $u_{inf} = g(a)$.
        
    - Substitua o limite superior original ($x = b$) na fórmula de $u$: $u_{sup} = g(b)$.
        
4. **Reescrita:** Monte a nova integral usando apenas $u, du$ e os novos limites $u_{inf}$ e $u_{sup}$.
    
5. **Resolução Direta:** Encontre a primitiva em $u$ e aplique os novos limites.
    

---

### Exemplo Prático Resolvido

**Problema:** Calcule $\int_{1}^{2} (2x + 1)^2 \, dx$

1. **Escolha de $u$ e diferencial:**
    
    - $u = 2x + 1$
        
    - $du = 2 \, dx \implies dx = \frac{du}{2}$
        
2. **Mudança de Limites:**
    
    - Se $x = 1$ (inferior): $u = 2(1) + 1 = \mathbf{3}$.
        
    - Se $x = 2$ (superior): $u = 2(2) + 1 = \mathbf{5}$.
        
3. **Nova Integral Definida:**
    
    $$\frac{1}{2} \int_{3}^{5} u^2 \, du$$
    
4. **Resolução:**
    
    $$\frac{1}{2} \left[ \frac{u^3}{3} \right]_{3}^{5} = \frac{1}{6} (5^3 - 3^3) = \frac{1}{6} (125 - 27) = \frac{98}{6} = \mathbf{\frac{49}{3}}$$
    

> [!NOTE]
> 
> Perceba que ao usar o método direto você resolveu uma integral muito mais simples. Como você reescreveu os limites, **não é necessário** substituir o $u$ de volta para $x$ no final.

---

### Por que isso é verdade? (A Mudança de Escala)

Quando você faz $u = g(x)$, você está mudando a "régua" que usa para medir o eixo horizontal. Se a sua função original está em um intervalo "apertado", mas a função $u$ expande esse intervalo, o diferencial $du$ compensa exatamente essa expansão ou contração.

#### A "Mágica" Geométrica

Imagine uma área torta e difícil de calcular em $x$. Ao mudar para $u$, você está "esticando" ou "encolhendo" o gráfico de modo que a área se torne uma forma simples. O Teorema da Mudança de Variável garante que:

$$\int_{a}^{b} f(g(x)) \cdot g'(x) \, dx = \int_{g(a)}^{g(b)} f(u) \, du$$

#### Analogia das Moedas

Pense nisso como moedas diferentes:

- Você pode ter 10 Reais em uma nota de 10 (**Integral simples em $x$**).
    
- Você pode ter 10 Reais em duas notas de 5 (**Integral substituída em $u$**).
    
- Você pode ter 10 Reais em dez moedas de 1 (**Outra variável $v$**).
    

O valor final (o poder de compra / a área) é o mesmo, mas a "cara" da conta mudou. Quando você redefine os limites, você está apenas ajustando a "carteira" para a nova moeda ($u$).

---

> [!TIP]
> 
> **O TFC no Universo $u$:** Uma vez que você transformou a integral, a variável $x$ deixa de existir para aquele problema. O TFC funciona perfeitamente em qualquer "universo" (variável), desde que a função seja contínua naquele intervalo.