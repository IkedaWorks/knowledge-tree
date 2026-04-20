
# Demonstração da Regra da Cadeia

## 1. Objetivo

Provar formalmente que, se uma função $y$ depende de $u$ e $u$ depende de $x$ (função composta $y = f(g(x))$), então a derivada de $y$ em relação a $x$ é o produto das derivadas das funções componentes:

$$\frac{dy}{dx} = f'(g(x)) \cdot g'(x)$$

---

## 2. Definições Iniciais

Seja $u = g(x)$. Quando a variável independente $x$ sofre um acréscimo $\Delta x$, a função interna $u$ sofre um acréscimo proporcional $\Delta u$:

$$\Delta u = g(x + \Delta x) - g(x)$$

Consequentemente, a função externa $y$ sofre um acréscimo $\Delta y$:

$$\Delta y = f(u + \Delta u) - f(u)$$

---

## 3. A Razão Incremental

A ideia central é expressar a variação de $y$ em relação a $x$ utilizando a variação de $u$ como intermediária. Multiplicamos e dividimos a razão incremental por $\Delta u$:

$$\frac{\Delta y}{\Delta x} = \frac{\Delta y}{\Delta u} \cdot \frac{\Delta u}{\Delta x}$$

> [!IMPORTANT] Nota de Rigor
> 
> Esta manipulação assume que $\Delta u \neq 0$ em um intervalo próximo de $x$. Em demonstrações 100% rigorosas (análise matemática), utiliza-se uma função auxiliar para tratar casos onde $g(x)$ é constante em algum intervalo, mas a lógica do limite permanece a mesma para a engenharia.

---

## 4. Aplicação do Limite

Fazemos $\Delta x \to 0$. Como a função $g$ é derivável (e, por extensão, contínua), o acréscimo $\Delta u$ também tenderá a zero conforme $\Delta x$ diminui.

$$\lim_{\Delta x \to 0} \frac{\Delta y}{\Delta x} = \lim_{\Delta x \to 0} \left( \frac{\Delta y}{\Delta u} \cdot \frac{\Delta u}{\Delta x} \right)$$

Pela propriedade de que o limite do produto é o produto dos limites:

$$\frac{dy}{dx} = \left( \lim_{\Delta u \to 0} \frac{\Delta y}{\Delta u} \right) \cdot \left( \lim_{\Delta x \to 0} \frac{\Delta u}{\Delta x} \right)$$

---

## 5. Identificando as Derivadas

Ao observar os limites resultantes, reconhecemos as definições formais de derivada:

1. O primeiro termo $\lim_{\Delta u \to 0} \frac{\Delta y}{\Delta u}$ é a derivada de $f$ em relação a $u$, ou seja, **$f'(u)$**.
    
2. O segundo termo $\lim_{\Delta x \to 0} \frac{\Delta u}{\Delta x}$ é a derivada de $g$ em relação a $x$, ou seja, **$g'(x)$**.
    

---

## 6. Conclusão

Substituindo $u$ pela sua definição original $g(x)$, chegamos à fórmula final:

$$\frac{dy}{dx} = f'(g(x)) \cdot g'(x)$$

**Está provado.**