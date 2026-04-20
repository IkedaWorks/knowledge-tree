

# Derivada de Exponenciais e Logaritmos

## 1. O "Pedágio" do $\ln(a)$

Toda vez que derivamos uma exponencial ou um logaritmo que **não** esteja na base $e$, a matemática nos cobra um "pedágio" de ajuste de escala. Esse pedágio é sempre o $\ln(a)$ (logaritmo natural da base $a$).

---

## 2. A Exponencial Geral

Para qualquer base $a > 0$:

$$\frac{d}{dx}(a^x) = a^x \cdot \ln(a)$$

- **A lógica:** A função se repete ($a^x$), mas multiplicamos pelo logaritmo da base para ajustar a taxa de crescimento à escala natural.
    
- **O caso específico ($e^x$):** Se a base for $e$, teríamos $e^x \cdot \ln(e)$. Como $\ln(e) = 1$, o pedágio é invisível. Por isso $e^x$ é tão prático: sua derivada é ele mesmo.
    

> [!WARNING] Condição de Existência
> 
> A base $a$ da exponencial deve ser sempre maior que zero ($a > 0$) e diferente de $1$ para que a função seja bem definida e não constante.

---

## 3. O Logaritmo Geral

Para qualquer base $a$:

$$\frac{d}{dx}(\log_a x) = \frac{1}{x \cdot \ln(a)}$$

- **A lógica:** A derivada do logaritmo é sempre o inverso da variável ($1/x$), mas dividimos pelo $\ln(a)$ para ajustar a base.
    
- **O caso específico ($\ln x$):** Se a base for $e$, temos $\frac{1}{x \cdot \ln(e)} = \frac{1}{x}$.
    

> [!NOTE] Domínio e Condições
> 
> - **Base ($a$):** Deve ser $a > 0$ e $a \neq 1$.
>     
> - **Logaritmando ($x$):** Deve ser $x > 0$. Não existe expoente real que resulte em um número zero ou negativo para uma base positiva.
>     

---

## 4. Exemplos com Bases "Não-Amigáveis"

**Exemplo 1: Potência de Base 10**

$f(x) = 10^x \implies f'(x) = 10^x \cdot \ln(10)$

**Exemplo 2: Logaritmo de Base 2 (Computação)**

$f(x) = \log_2(x) \implies f'(x) = \frac{1}{x \ln(2)}$

**Exemplo 3: Misturando com a Regra da Cadeia**

$f(x) = 3^{\sin(x)}$

1. Derivada da base 3: $3^{\sin(x)} \cdot \ln(3)$
    
2. Multiplicamos pela derivada do expoente (Cadeia): $\cos(x)$
    

- **Resultado:** $f'(x) = 3^{\sin(x)} \cdot \ln(3) \cdot \cos(x)$
    

---

## 5. Macetes Estruturais (Filtros Mentais)

Para não depender da dedução por limites na hora da prova, use estes filtros:

### I. O Filtro do Multiplicador (Exponencial)

Se a variável $x$ está no **expoente**, a função cresce rápido.

- **Ação:** Copia a função e **multiplica** pelo pedágio $\ln(a)$.
    
- _Dica:_ Pense no $e^x$ como a âncora; se você sabe o geral, o $e^x$ sai automático.
    

### II. O Filtro do Divisor (Logaritmo)

Se a variável $x$ está **dentro** do logaritmo, a função cresce devagar.

- **Ação:** Usa o inverso $1/x$ e **divide** pelo pedágio $\ln(a)$ (o $\ln(a)$ vai para o denominador).
    

### III. A "Âncora" do $\ln(x)$

Se bater a dúvida: $\ln(x)$ é a base $e$. Se a derivada dele é $1/x$, qualquer outro logaritmo tem que ser um "parente" próximo, apenas ajustado pelo fator de correção $\frac{1}{\ln(base)}$.