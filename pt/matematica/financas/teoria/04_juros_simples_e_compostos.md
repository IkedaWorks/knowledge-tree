# Regimes de Capitalização: Juros Simples e Compostos

O conceito de juros corresponde, de forma simplificada, a um "aluguel" cobrado sobre um capital que foi confiado a alguém. Uma vez que esse dinheiro não está com o seu legítimo dono, ele deixa de ser aplicado de outras maneiras (custo de oportunidade). 

Em outras palavras, os juros representam o rendimento obtido ao emprestar um valor monetário ou ao realizar investimentos (onde o dinheiro retorna acrescido de uma parcela). No cenário oposto, como no uso de cartões de crédito ou empréstimos bancários, os juros compensam a instituição por antecipar um capital que ela poderia utilizar para outros fins.

---

> [!NOTE] 
> **Nota de Notação Matemática (Padrão LaTeX):**  Os blocos matemáticos deste repositório seguem o padrão internacional do LaTeX. Portanto:
> * O **ponto (`.`)** é utilizado estritamente para indicar **casas decimais** (ex:  $1.025$  ).
> * O **ponto central (`\cdot`)** é utilizado exclusivamente como **operador de multiplicação** (ex:  $1025 \cdot 1.025$ ).


## Juros Simples

Este é o regime de capitalização mais básico. O acréscimo surge sempre em relação ao **valor inicial (capital)**. Independentemente do rendimento acumulado ao longo dos meses, a taxa de juros será calculada estritamente sobre a base do primeiro mês.

### Dedução e Padrão Matemático

Suponha um capital inicial de R$ 1000,00 aplicado a uma taxa de juros simples de 2,5% ao mês ($i = 0.025$). O comportamento da evolução do montante pode ser mapeado ciclo a ciclo:

* **Mês 1:** $$1000 + 1000 \cdot 0.025 = 1025$$

* **Mês 2:** $$1025 + 1000 \cdot 0.025 = 1050$$

* **Mês 3:** $$1050 + 1000 \cdot 0.025 = 1075$$

Percebe-se que a parcela de juros adicionada a cada mês é constante ($1000 \cdot 0.025 = 25$). Generalizando esse padrão para um tempo $n$ qualquer, definem-se as variáveis:
* **Montante ($M$):** O valor total retornado após o período de aplicação.
* **Capital ($C$):** O valor monetário investido inicialmente.
* **Taxa de juros ($i$):** A taxa percentual aplicada por ciclo.
* **Tempo ($n$):** A quantidade de períodos acumulados.

Dessa forma, a equação geral do montante em juros simples é modelada por:

$$M = C \cdot ( 1 + i \cdot n )$$

Por distribuição algébrica, a equação pode ser remodelada como:

$$M = C + C \cdot i \cdot n$$

Esta segunda forma evidencia que o montante final depende diretamente do capital inicial somado à quantidade de lucros fixos gerados a cada ciclo de tempo.

---

## Juros Compostos

Este regime de capitalização é consideravelmente mais agressivo e mapeia a maioria das operações do mercado financeiro real (como financiamentos, investimentos de longo prazo e dívidas de cartão de crédito). 

Diferente do regime simples, o acréscimo é aplicado diretamente sobre o **valor atualizado do período anterior**, e não sobre o capital inicial.

### O "Motor" da Multiplicação Sucessiva

Utilizando o mesmo exemplo de R$ 1000,00 sob uma taxa de 2,5% ao mês, mas agora no regime composto, o fator de variação individual de cada mês é de $1 + 0.025 = 1.025$. A evolução se comporta da seguinte maneira:

* **Mês 0 (Início):** 1000
* **Mês 1:** $$1000 \cdot 1.025 = 1025$$

* **Mês 2:** $$1025 \cdot 1.025 = 1050{,}625$$

* **Mês 3:** $$1050{,}625 \cdot 1.025 = 1076{,}89$$

Substituindo as variáveis de forma analítica, revela-se o acúmulo em cadeia:

* **Mês 1:** $$M_1 = C \cdot 1.025$$

* **Mês 2:** O "novo todo" passa a ser $M_1$. Aplicando o fator sobre ele:
$$M_2 = M_1 \cdot 1.025 \implies ( C \cdot 1.025 ) \cdot 1.025 = C \cdot ( 1.025 )^2$$

* **Mês 3:** O "novo todo" passa a ser $M_2$:
$$M_3 = M_2 \cdot 1.025 \implies ( C \cdot ( 1.025 )^2 ) \cdot 1.025 = C \cdot ( 1.025 )^3$$

A multiplicação repetida pelo fator $( 1 + i )$ garante que o valor acumulado até ali não se perca (garantido pelo número 1) e calcula o novo juro sobre a base já inflada (garantido pela taxa $i$).



---

## A Conexão com a Geometria (PA vs PG)

A mecânica de crescimento dos dois regimes pode ser mapeada diretamente dentro das progressões matemáticas estudadas em álgebra:

* **Juros Simples como uma Progressão Aritmética (PA):** Como a razão dos juros é somada fixamente ao capital inicial a cada ciclo, o crescimento é linear. A equação simula o termo geral de uma PA.
* **Juros Compostos como uma Progressão Geométrica (PG):** Como a razão (fator de variação) é multiplicada sucessivamente ao montante do período anterior, o crescimento é exponencial. 

A equação clássica de juros compostos:

$$M = C \cdot ( 1 + i )^t$$

Nada mais é do que a aplicação direta do termo geral de uma PG exponencial, onde cada novo andar financeiro é construído com base na estrutura acumulada do período imediatamente anterior.