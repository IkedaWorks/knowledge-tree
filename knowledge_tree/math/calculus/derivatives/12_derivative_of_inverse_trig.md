
# Derivada das Funções Trigonométricas Inversas

## Requisitos Prévios

Para a compreensão deste tópico, é necessário o domínio de funções trigonométricas, identidades fundamentais e a aplicação da Derivada da Função Inversa.

> [!CAUTION] RECOMENDAÇÃO
> 
> Se o estudo deste tema estiver sendo realizado em regime de urgência para avaliações, recomenda-se focar na memorização das fórmulas finais, visto que este assunto possui menor frequência de incidência em provas iniciais.

---

## 1. Intuição (A Transição para Medidas Geométricas)

As funções inversas alteram a natureza da pergunta matemática:

- **Seno:** "Dado o ângulo, qual é a razão (altura)?"
    
- **Arco-Seno:** "Dada a razão, qual é o ângulo?"
    

Ao derivar o arco-seno, questionamos a taxa de variação do ângulo em relação à mudança da altura. O resultado final não apresenta funções trigonométricas ($\sin$ ou $\cos$) porque utilizamos a geometria do triângulo retângulo para converter relações angulares em medidas algébricas de comprimento.

---

## 2. Demonstração e Formalização

Utilizaremos a Regra da Função Inversa e o Teorema de Pitágoras como ferramentas centrais.

### I. Derivada do Arco-Seno ($\arcsin x$)

**Definição:** $\frac{d}{dx}(\arcsin x) = \frac{1}{\sqrt{1-x^2}}$

**Demonstração:**

1. Seja $y = \arcsin x$, o que implica que $\sin y = x$.
    
2. Aplicamos a regra da inversa: $\frac{dy}{dx} = \frac{1}{\frac{d}{dy}(\sin y)} = \frac{1}{\cos y}$.
    
3. Para expressar $\cos y$ em termos de $x$, utilizamos a Identidade Fundamental: $\sin^2 y + \cos^2 y = 1$.
    
4. Substituindo $\sin y = x$, temos: $x^2 + \cos^2 y = 1 \implies \cos y = \sqrt{1-x^2}$.
    
5. **Resultado:** $\frac{d}{dx}(\arcsin x) = \frac{1}{\sqrt{1-x^2}}$.
    

### II. Derivada do Arco-Tangente ($\arctan x$)

**Definição:** $\frac{d}{dx}(\arctan x) = \frac{1}{1+x^2}$

**Demonstração:**

1. Seja $y = \arctan x$, logo, $\tan y = x$.
    
2. Pela regra da inversa: $\frac{dy}{dx} = \frac{1}{\sec^2 y}$.
    
3. Utilizamos a identidade derivada da relação fundamental: $\sec^2 y = 1 + \tan^2 y$.
    
4. Como $\tan y = x$, então $\sec^2 y = 1 + x^2$.
    
5. **Resultado:** $\frac{d}{dx}(\arctan x) = \frac{1}{1+x^2}$.
    

---

## 3. Exercícios Resolvidos (Regra da Cadeia)

O segredo para processar estas expressões é a derivação por camadas.

**Exercício 1: Cadeia no Arco-Seno**

Derive $f(x) = \arcsin(e^x)$.

- **Camada Externa (Arco-Seno):** $\frac{1}{\sqrt{1 - (e^x)^2}}$.
    
- **Camada Interna ($e^x$):** $e^x$.
    
- **Resultado:** $\frac{e^x}{\sqrt{1 - e^{2x}}}$.
    

**Exercício 2: Argumento Quadrático**

Derive $f(x) = \arctan(3x^2)$.

- **Camada Externa (Arco-Tangente):** $\frac{1}{1 + (3x^2)^2}$.
    
- **Camada Interna ($3x^2$):** $6x$.
    
- **Resultado:** $\frac{6x}{1 + 9x^4}$.
    

---

## 4. Simetria e Notação

### O Ajuste das "Co-funções"

As derivadas das funções trigonométricas inversas iniciadas em "C" (co-funções) seguem a mesma lógica das funções diretas: elas recebem o sinal negativo.

- Se $(\arcsin x)' = \frac{1}{\sqrt{1-x^2}}$, então $(\arccos x)' = -\frac{1}{\sqrt{1-x^2}}$.
    
- Se $(\arctan x)' = \frac{1}{1+x^2}$, então $(\text{arccotg } x)' = -\frac{1}{1+x^2}$.
    

### Alerta sobre Notação: $\sin^{-1}(x) \neq \csc(x)$

É um equívoco comum confundir a inversa com a recíproca. A cossecante não é a função inversa do seno; ela não retorna o ângulo original. O conflito ocorre devido a convenções históricas:

1. **Expoentes Positivos ($2, 3, 4...$):** Indicam potências, como $\sin^2(x)$. Esta notação foi criada para simplificar a escrita.
    
2. **Expoente Negativo ($-1$):** Por convenção matemática pré-existente, o $-1$ sobre o nome da função denota a **Função Inversa (Arco)** e não uma potência de inversão aritmética.
    

Portanto, ao encontrar $\sin^{-1}(x)$, deve-se interpretar imediatamente como $\arcsin x$.