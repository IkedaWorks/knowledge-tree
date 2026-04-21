
## O que é uma Equação Implícita?

Dizemos que uma função está na forma **explícita** quando a saída $y$ está isolada, similar a uma atribuição de variável em programação: `y = f(x)`.

Já na forma **implícita**, as variáveis $x$ e $y$ estão entrelaçadas em uma relação de dependência. Você sabe que $y$ depende de $x$, mas eles estão "presos" na mesma expressão.

### Exemplos Clássicos:

- **Círculo Trigonométrico:** $x^2 + y^2 = 1$
    
- **Equação Geral da Reta:** $ax + by + c = 0$
    
- **Folium de Descartes:** $x^3 + y^3 - 3axy = 0$
    

> [!ATTENTION] 
> Por que não isolar o "y"?
> 
> No ensino médio, a estratégia era sempre isolar o $y$. No Cálculo de nível superior, isso muitas vezes é:
> 
> 1. **Impossível:** Tente isolar $y$ em $y^5 + 3x^2y^2 + \sin(y) = 10$. Não existe álgebra que permita isolar $y$.
>     
> 2. **Ineficiente:** Mesmo quando isolável (como no círculo, gerando $y = \pm\sqrt{1-x^2}$), a derivada resultante é muito mais complexa do que se derivássemos a equação original.
>     

---

## 2. A Lógica do "Carimbo" (Regra da Cadeia)

O segredo da derivada implícita é tratar $y$ como uma função de $x$ que você ainda não conhece totalmente: $y = y(x)$.

Sempre que derivamos um termo que contém $y$, devemos aplicar a **Regra da Cadeia**. Na prática, toda vez que você derivar um $y$, você deve "carimbar" o resultado com um $\frac{dy}{dx}$ (ou $y'$).

---

## 3. Exercícios Resolvidos (Notação de Leibniz)

A notação de Leibniz ($\frac{dy}{dx}$) é a mais comum em Física, Química e Equações Diferenciais (EDO). Acostumar-se com ela agora facilitará sua transição para as matérias de natureza.

### Exercício 1: O Círculo Unitário

**Problema:** Encontre a inclinação da reta tangente em qualquer ponto do círculo $x^2 + y^2 = 1$.

1. **Derivamos ambos os lados em relação a $x$:**
    
    $$\frac{d}{dx}(x^2) + \frac{d}{dx}(y^2) = \frac{d}{dx}(1)$$
    
2. **Aplicando as regras:**
    
    - $\frac{d}{dx}(x^2) = 2x$
        
    - $\frac{d}{dx}(y^2) = 2y \cdot \frac{dy}{dx}$ (O carimbo aparece aqui!)
        
    - $\frac{d}{dx}(1) = 0$
        
3. **Montando e isolando:**
    
    $$2x + 2y \frac{dy}{dx} = 0 \implies 2y \frac{dy}{dx} = -2x$$
    
    **Resultado:** $\frac{dy}{dx} = -\frac{x}{y}$
    

---

### Exercício 2: A Curva "Misturada" (Produto de $x$ e $y$)

**Problema:** Encontre $\frac{dy}{dx}$ para a equação $x^2 + xy + y^2 = 7$.

Este é um clássico de prova, pois o termo $xy$ exige a **Regra do Produto**: $(uv)' = u'v + uv'$.

1. **Derivando termo a termo:**
    
    - $\frac{d}{dx}(x^2) = 2x$
        
    - $\frac{d}{dx}(xy) = (1 \cdot y) + (x \cdot \frac{dy}{dx})$
        
    - $\frac{d}{dx}(y^2) = 2y \frac{dy}{dx}$
        
2. **Juntando a equação:**
    
    $$2x + y + x \frac{dy}{dx} + 2y \frac{dy}{dx} = 0$$
    
3. **Agrupando os termos com $\frac{dy}{dx}$:**
    
    $$\frac{dy}{dx} (x + 2y) = -2x - y$$
    
    **Resultado Final:** $\frac{dy}{dx} = -\frac{2x + y}{x + 2y}$
    

---

### Exercício 3: O Desafio da Hipérbole

**Problema:** Encontre a derivada da hipérbole unitária $x^2 - y^2 = 1$.

1. **Derivada direta:**
    
    $$2x - 2y \frac{dy}{dx} = 0$$
    
2. **Isolando o termo:**
    
    $$-2y \frac{dy}{dx} = -2x \implies \frac{dy}{dx} = \frac{-2x}{-2y}$$
    
    **Resultado:** $\frac{dy}{dx} = \frac{x}{y}$
    

---

> [!TIP] 
> **Diferença Geométrica**
> 
> Note a simetria:
> 
> - No **Círculo** ($x^2+y^2=1$), a derivada é **$-x/y$**.
>     
> - Na **Hipérbole** ($x^2-y^2=1$), a derivada é **$x/y$**.
>     
>     Essa pequena mudança de sinal no gráfico altera completamente a direção das retas tangentes!
>