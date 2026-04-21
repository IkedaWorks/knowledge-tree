
# Derivada das Funções Trigonométricas

## 1. Requisitos Prévios

Para o domínio deste tópico, é indispensável a compreensão sólida de trigonometria, especificamente no que tange às identidades e relações fundamentais.

> [!IMPORTANT] 
> Orientação de Estudo
> 
> Recomenda-se a memorização das derivadas do **seno**, **cosseno** e **tangente**. Através delas, é possível demonstrar todas as demais funções. Evite a memorização mecânica de todas as fórmulas, pois a similaridade entre elas pode induzir ao erro. Priorize a compreensão da lógica de derivação para que você seja capaz de reconstruí-las quando necessário.

---

## 2. Definição e Formalização

Nesta seção, assumiremos as derivadas fundamentais de $\sin x$ e $\cos x$ como premissas conhecidas. O objetivo será construir as derivadas das funções derivadas (tangente, secante, cotangente e cossecante) utilizando as regras de derivação previamente estudadas.

**Premissas:**

- Seno: $\frac{d}{dx}(\sin x) = \cos x$
    
- Cosseno: $\frac{d}{dx}(\cos x) = -\sin x$
    

_(Nota: As demonstrações formais destas premissas, baseadas em limites fundamentais, serão abordadas em uma seção posterior)._

---

## 3. Demonstrações das Funções Derivadas

### I. Derivada da Tangente

**Definição:** $\frac{d}{dx}(\tan x) = \sec^2 x$

**Demonstração:**

Utilizamos a identidade $\tan x = \frac{\sin x}{\cos x}$ e aplicamos a **Regra do Quociente**:

1. Derivada do numerador ($\cos x$) multiplicada pelo denominador ($\cos x$): $\cos^2 x$.
    
2. Subtraímos o numerador ($\sin x$) multiplicado pela derivada do denominador ($-\sin x$): $- (-\sin^2 x) = \sin^2 x$.
    
3. O denominador é elevado ao quadrado: $\cos^2 x$.
    
4. Pela **Identidade Trigonométrica Fundamental** ($\cos^2 x + \sin^2 x = 1$), o numerador simplifica-se para $1$.
    
5. Obtemos $\frac{1}{\cos^2 x}$, que equivale a **$\sec^2 x$**.
    

### II. Derivada da Secante

**Definição:** $\frac{d}{dx}(\sec x) = \sec x \cdot \tan x$

**Demonstração:**

Reescrevemos $\sec x$ como $(\cos x)^{-1}$ e aplicamos a **Regra da Cadeia**:

1. Derivada da potência externa: $-1 \cdot (\cos x)^{-2}$.
    
2. Multiplicamos pela derivada da função interna ($\cos x$), que é $-\sin x$.
    
3. Organização algébrica: $\frac{-1 \cdot (-\sin x)}{\cos^2 x} = \frac{\sin x}{\cos^2 x}$.
    
4. Decomposição para simplificação: $\frac{1}{\cos x} \cdot \frac{\sin x}{\cos x} = \mathbf{\sec x \cdot \tan x}$.
    

### III. Derivada da Cotangente

**Definição:** $\frac{d}{dx}(\cot x) = -\csc^2 x$

**Demonstração:**

Aplicamos a Regra do Quociente à relação $\cot x = \frac{\cos x}{\sin x}$:

1. $(-\sin x) \cdot \sin x = -\sin^2 x$.
    
2. Subtraímos $\cos x \cdot (\cos x) = -\cos^2 x$.
    
3. Numerador resultante: $-(\sin^2 x + \cos^2 x) = -1$.
    
4. Denominador: $\sin^2 x$.
    
5. Resultado: $\frac{-1}{\sin^2 x} = \mathbf{-\csc^2 x}$.
    

### IV. Derivada da Cossecante

**Definição:** $\frac{d}{dx}(\csc x) = -\csc x \cdot \cot x$

**Demonstração:**

Reescrevemos como $(\sin x)^{-1}$ e aplicamos a Regra da Cadeia:

1. Derivada da potência: $-1 \cdot (\sin x)^{-2}$.
    
2. Derivada da função interna: $\cos x$.
    
3. Organização: $-\frac{\cos x}{\sin^2 x} = -\frac{1}{\sin x} \cdot \frac{\cos x}{\sin x} = \mathbf{-\csc x \cdot \cot x}$.
    

---

## 4. Seção de Exercícios Técnicos

**Exercício 1: Derivação Composta (Cadeia Tripla)**

Determine a derivada de $f(x) = \sin^3(4x)$.

- **Análise de camadas:** $f(x) = [\sin(4x)]^3$.
    
- **Camada 1 (Potência):** $3 \cdot [\sin(4x)]^2$.
    
- **Camada 2 (Função Seno):** $\cos(4x)$.
    
- **Camada 3 (Argumento):** $4$.
    
- **Resultado:** $f'(x) = 12 \sin^2(4x) \cos(4x)$.
    

**Exercício 2: Produto de Transcendental e Trigonométrica**

Determine a derivada de $y = e^{x} \cdot \sec(2x)$.

- Aplicando a Regra do Produto e da Cadeia no termo secante:
    
- $y' = (e^x) \cdot \sec(2x) + e^x \cdot [\sec(2x) \tan(2x) \cdot 2]$.
    
- **Forma Simplificada:** $y' = e^x \sec(2x) [1 + 2\tan(2x)]$.
    

**Exercício 3: Composição com Radicais**

Determine a derivada de $f(x) = \sqrt{\tan(x^2)}$.

- **Passo 1 (Cadeia - Potência):** $\frac{1}{2\sqrt{\tan(x^2)}}$.
    
- **Passo 2 (Cadeia - Tangente):** $\sec^2(x^2)$.
    
- **Passo 3 (Cadeia - Interna):** $2x$.
    
- **Resultado Final:** $f'(x) = \frac{x \cdot \sec^2(x^2)}{\sqrt{\tan(x^2)}}$.