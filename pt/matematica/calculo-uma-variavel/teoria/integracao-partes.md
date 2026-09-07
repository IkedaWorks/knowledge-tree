
# Integração por Partes

### Introdução e Definição

A Integração por Partes é a técnica utilizada para integrar o produto de duas funções de naturezas diferentes (ex: um polinômio multiplicado por uma exponencial). Ela é o processo inverso da **Regra do Produto** da derivada.

**A Intuição:** Nem todo produto pode ser resolvido por substituição simples. Quando as funções "não se conversam" (uma não é a derivada da outra), usamos a Integração por Partes para "transferir" a dificuldade da conta. Nós escolhemos uma parte para derivar (fazendo-a simplificar) e outra para integrar.

---

### Formalização e a Escolha Estratégica

A fórmula fundamental é:

$$\int u \, dv = uv - \int v \, du$$

- **$u$:** A parte que você escolhe para **derivar**. O objetivo é que $du$ seja mais simples que $u$.
    
- **$dv$:** A parte que você escolhe para **integrar**. O objetivo é que $v$ seja calculável.
    

#### O Macete de Escolha (LIATE)

Para decidir quem será o seu $u$ (quem você vai "matar" na derivada), siga a ordem de prioridade. Quem aparecer primeiro na lista abaixo deve ser o seu $u$:

1. **L**ogarítmicas ($\ln x$)
    
2. **I**nversas Trigonométricas ($\arcsin, \arctan$)
    
3. **A**lgebricas ($x^2, 3x, 5$)
    
4. **T**rigonométricas ($\sin, \cos$)
    
5. **E**xponenciais ($e^x, 2^x$)
    

---

### Por que isso funciona? (Demonstração)

A Integração por Partes é o "Caminho de Volta" da Regra do Produto.

1. **Regra do Produto:** $\frac{d}{dx}(uv) = u \frac{dv}{dx} + v \frac{du}{dx}$
    
2. **Diferenciais:** $d(uv) = u \, dv + v \, du$
    
3. **Integrando os dois lados:** $\int d(uv) = \int u \, dv + \int v \, du$
    
4. **Pelo TFC:** $uv = \int u \, dv + \int v \, du$
    
5. **Isolando a "Integral Problema":**
    
    $$\int u \, dv = uv - \int v \, du$$
    

---

### Exemplo Prático: $\int x \cdot e^x \, dx$

1. **Identificação (LIATE):** Temos uma Algébrica ($x$) e uma Exponencial ($e^x$). No LIATE, o **A** vem antes do **E**, então $u = x$.
    
2. **Definição das Partes:**
    
    - $u = x \implies du = dx$
        
    - $dv = e^x \, dx \implies v = e^x$
        
3. **Aplicação da Fórmula:**
    
    $$\int x \cdot e^x \, dx = \underbrace{x \cdot e^x}_{uv} - \int \underbrace{e^x \cdot dx}_{v \, du}$$
    
4. **Resolução Final:**
    
    $$x e^x - e^x + C$$
    

> [!NOTE]
> 
> Perceba que a integral "difícil" ($\int x e^x$) foi trocada por uma integral imediata ($\int e^x$). O $x$ "sumiu" porque foi derivado e transformado em $1$. Se tivéssemos escolhido integrar o $x$, ele viraria $x^2/2$, tornando a conta muito pior!

---

###  Regras de Ouro para Não Errar

1. **Simplificação:** Antes de resolver a segunda integral ($\int v \, du$), simplifique ao máximo o que estiver lá dentro. A multiplicação de integrais não é direta; você precisa ter um termo limpo para integrar.
    
2. **Use Parênteses:** Sempre coloque parênteses no conteúdo da integral para não confundir o que faz parte do integrando e o que é o diferencial $dx$.
    
3. **Persistência:** Às vezes, você precisará aplicar a integração por partes duas vezes (como em $\int x^2 e^x \, dx$) até que o termo algébrico finalmente desapareça.