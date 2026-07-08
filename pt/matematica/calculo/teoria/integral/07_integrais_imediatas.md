
# Integrais Imediatas

### Introdução e Definição

As integrais imediatas (ou fundamentais) são aquelas que podem ser resolvidas diretamente, pois são o inverso exato de derivadas conhecidas. Elas não exigem truques algébricos complexos, apenas o reconhecimento da função original.

**A Intuição:** Imagine que você tem uma tabela de "Ida" (Derivadas) e uma de "Volta" (Integrais). Se você sabe que a derivada de $\sin(x)$ é $\cos(x)$, então a integral de $\cos(x)$ é "imediatamente" $\sin(x)$. O objetivo aqui é memorizar os caminhos mais comuns para não precisar deduzi-los do zero toda vez.

---

### Formalização (O Dicionário de Funções)

#### 1. Regra da Potência (Geral)

$$\int x^n \, dx = \frac{x^{n+1}}{n+1} + C \quad (n \neq -1)$$

> [!NOTE]
> 
> Você aumenta o expoente e divide pelo novo valor. É o inverso da "Regra do Tombo" da derivada. Perceba: você **soma 1** no expoente primeiro e depois divide por esse número.

#### 2. Regra do Logaritmo (A exceção)

$$\int \frac{1}{x} \, dx = \ln|x| + C \quad \text{ou} \quad \int \frac{dx}{x} = \ln|x| + C$$

**Por que o módulo?** O logaritmo não aceita valores negativos, mas a função $1/x$ existe para $x < 0$. O módulo garante a validade matemática.

**Dica de Engenharia:** Toda vez que você identificar a derivada do denominador presente no numerador, o resultado será $\ln|x| + C$.

#### 3. Funções Exponenciais e Trigonométricas

- **Exponencial Natural:** $\int e^x \, dx = e^x + C$ (a função que é sua própria integral/derivada).
    
- **Base Geral:** $\int a^x \, dx = \frac{a^x}{\ln a} + C$.
    
- **Seno/Cosseno:** $\int \sin(x) \, dx = -\cos(x) + C$ e $\int \cos(x) \, dx = \sin(x) + C$.
    

---

### Exemplificação e Macetes (Preparação de Alce)

Muitas vezes, é preciso "preparar" a função algebricamente antes de integrar:

- **Exemplo 1 (Raízes):** $\int \sqrt{x} \, dx \rightarrow \int x^{1/2} \, dx = \frac{x^{3/2}}{3/2} + C = \frac{2}{3}x \sqrt{x} + C$.
    
- **Exemplo 2 (Potência no Denominador):** $\int \frac{1}{x^3} \, dx \rightarrow \int x^{-3} \, dx = \frac{x^{-2}}{-2} + C = -\frac{1}{2x^2} + C$.
    

---

###  Tabela de Integrais Imediatas

|**Função f(x)**|**Integral ∫f(x)dx**|**Observação**|
|---|---|---|
|$k$ (Constante)|$kx + C$|Integral da constante gera uma reta.|
|$x^n$|$\frac{x^{n+1}}{n+1} + C$|Válido para $n \neq -1$.|
|$1/x$|$\ln|x|
|$e^x$|$e^x + C$|A "imortal" do cálculo.|
|$a^x$|$\frac{a^x}{\ln a} + C$|Exponencial de base qualquer.|
|$\sin(x)$|$-\cos(x) + C$|Cuidado com o sinal negativo!|
|$\cos(x)$|$\sin(x) + C$||
|$\sec^2(x)$|$\tan(x) + C$||
|$\csc^2(x)$|$-\cot(x) + C$||
|$\sec(x)\tan(x)$|$\sec(x) + C$||