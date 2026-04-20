
# Derivadas das Funções Hiperbólicas

> [!NOTE] Nota de Estudo
> 
> Este tópico apresenta um nível de abstração elevado e possui aplicações muito específicas. Na engenharia civil, é utilizado no cálculo de estruturas; na computação, surge em contextos de Machine Learning e Ciência de Dados. Recomenda-se o estudo como complemento acadêmico. Caso este material esteja sendo consultado sob regime de urgência para avaliações, recomenda-se priorizar tópicos com maior incidência.

## 1. Demonstrações via Definição Exponencial

Nesta seção, as fórmulas não serão meramente apresentadas; utilizaremos a definição exponencial para demonstrar que a derivação destas funções é, fundamentalmente, uma operação algébrica simples.

### I. Derivada do Seno Hiperbólico ($\sinh x$)

**Definição:** $\frac{d}{dx}(\sinh x) = \cosh x$

**Demonstração:**

Sabemos que $\sinh(x) = \frac{e^x - e^{-x}}{2}$. Derivando termo a termo:

1. A derivada de $e^x$ é $e^x$.
    
2. A derivada de $-e^{-x}$ (pela regra da cadeia) resulta em $-(-e^{-x}) = e^{-x}$.
    
3. Agrupando sobre a constante: $\frac{e^x + e^{-x}}{2}$.
    
4. Esta é precisamente a definição de **$\cosh x$**.
    

### II. Derivada do Cosseno Hiperbólico ($\cosh x$)

**Definição:** $\frac{d}{dx}(\cosh x) = \sinh x$

> [!IMPORTANT] Diferença Fundamental
> 
> Diferente da trigonometria circular, na derivada do cosseno hiperbólico **não** ocorre a inversão de sinal para negativo.

**Demonstração:**

Sabemos que $\cosh(x) = \frac{e^x + e^{-x}}{2}$:

1. A derivada de $e^x$ é $e^x$.
    
2. A derivada de $e^{-x}$ é $-e^{-x}$.
    
3. Agrupando os termos: $\frac{e^x - e^{-x}}{2}$.
    
4. Esta é a definição de **$\sinh x$**.
    

### III. Derivada da Tangente Hiperbólica ($\tanh x$)

**Definição:** $\frac{d}{dx}(\tanh x) = \text{sech}^2 x$

**Demonstração:**

Aplicamos a **Regra do Quociente** na razão $\frac{\sinh x}{\cosh x}$:

1. $(\text{Derivada do numerador}) \cdot (\text{denominador}) = \cosh x \cdot \cosh x = \cosh^2 x$.
    
2. Subtraímos $(\text{numerador}) \cdot (\text{derivada do denominador}) = \sinh x \cdot \sinh x = \sinh^2 x$.
    
3. Tudo sobre o quadrado do denominador: $\cosh^2 x$.
    
4. Pela Identidade Fundamental Hiperbólica ($\cosh^2 x - \sinh^2 x = 1$):
    
    $$f'(x) = \frac{1}{\cosh^2 x} = \text{sech}^2 x$$
    

---

## 2. Exercícios Resolvidos (Passo a Passo)

**Exercício 1: Regra da Cadeia com Argumento Composto**

Determine a derivada de $f(x) = \sinh(x^3 + 5x)$.

- **Derivada da função externa (Seno Hiperbólico):** $\cosh(x^3 + 5x)$.
    
- **Multiplicação pela derivada da função interna ($3x^2 + 5$):**
    
- **Resultado:** $f'(x) = (3x^2 + 5) \cdot \cosh(x^3 + 5x)$.
    

**Exercício 2: Produto de Exponencial e Hiperbólica**

Determine a derivada de $g(x) = e^{2x} \cdot \cosh(x)$.

- Aplicando a **Regra do Produto** $[(u \cdot v)' = u'v + uv']$:
    
- $u = e^{2x} \implies u' = 2e^{2x}$
    
- $v = \cosh(x) \implies v' = \sinh(x)$
    
- **Resultado:** $2e^{2x}\cosh(x) + e^{2x}\sinh(x) = e^{2x} [2\cosh(x) + \sinh(x)]$.
    

---

## 3. Observação sobre Sinais (Diferenciação Analógica)

Para evitar confusões com a trigonometria circular durante a resolução de problemas:

- **No Círculo:** O cosseno inverte o sinal em sua derivada.
    
- **Na Hipérbole:** As funções fundamentais ($\sinh$ e $\cosh$) mantêm derivadas positivas entre si. O sinal negativo aparecerá apenas nas derivadas das funções inversas ($\text{sech}$, $\text{csch}$ e $\coth$).