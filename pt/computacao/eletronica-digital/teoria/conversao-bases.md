---
id: "conversao-bases"
title: "Conversão entre Bases Numéricas"
domain: "engineering"
type: "method"
language: "pt"
tags:
  - "digital-electronics"
  - "number-systems"
  - "base-conversion"
  - "binary"
  - "hexadecimal"
prerequisites:
  - "sistemas-numericos-fundamentais"
---

# Conversão entre Bases Numéricas

## Visão Geral dos Métodos

A transição de representação numérica entre diferentes bases é uma operação fundamental para a programação de baixo nível, projeto de hardware e análise de sistemas digitais. Os algoritmos de conversão dividem-se em duas categorias principais:

1. **Métodos Aritméticos:** Utilizados quando uma das bases é a Decimal ($b=10$). Exigem operações explícitas de divisão ou expansão polinomial.
2. **Métodos por Mapeamento Direto (Agrupamento):** Utilizados entre bases que são potências exatas de $2$ ($2^1$ Binário, $2^3$ Octal, $2^4$ Hexadecimal). Não exigem cálculos aritméticos complexos, apenas substituição de blocos de bits.

---

## Conversão de Qualquer Base para Base Decimal

Para converter um número de uma base qualquer $b$ para a base Decimal ($10$), aplica-se o método da **Expansão Posicional Polinomial**.

### Algoritmo
Multiplica-se cada dígito $d_i$ pela base $b$ elevada à sua respectiva posição $i$, somando todos os termos:

$$N_{10} = \sum_{i=0}^{n-1} d_i \cdot b^i = d_{n-1} \cdot b^{n-1} + \dots + d_1 \cdot b^1 + d_0 \cdot b^0$$

### Aplicação do Algoritmo nas Três Bases ($b=2, b=8, b=16$)

A mesma expansão polinomial resolve a conversão para decimal independentemente da base de origem:

#### 1. De Binário ($b=2$) para Decimal
Converter $1101_2$ para decimal:

$$N_{10} = (1 \cdot 2^3) + (1 \cdot 2^2) + (0 \cdot 2^1) + (1 \cdot 2^0)$$
$$N_{10} = 8 + 4 + 0 + 1 = 13_{10}$$

#### 2. De Octal ($b=8$) para Decimal
Converter $157_8$ para decimal:

$$N_{10} = (1 \cdot 8^2) + (5 \cdot 8^1) + (7 \cdot 8^0)$$
$$N_{10} = 64 + 40 + 7 = 111_{10}$$

#### 3. De Hexadecimal ($b=16$) para Decimal
Converter $3\text{F}_{16}$ para decimal (onde $\text{F} = 15$):

$$N_{10} = (3 \cdot 16^1) + (\text{F} \cdot 16^0)$$
$$N_{10} = (3 \cdot 16) + (15 \cdot 1)$$
$$N_{10} = 48 + 15 = 63_{10}$$

---

## Conversão de Decimal para Qualquer Base

Para converter um número decimal inteiro para uma base de destino $b$, aplica-se o algoritmo das **Divisões Sucessivas por $b$**.

### Algoritmo
1. Divide-se o número decimal $N$ pela base de destino $b$.
2. Registra-se o **resto** da divisão.
3. Toma-se o **quociente inteiro** e divide-se novamente por $b$.
4. Repete-se o processo até que o quociente seja igual a zero.
5. O número na base de destino é formado pela leitura dos restos na **ordem inversa** à que foram gerados (do último resto para o primeiro).

### Exemplo Prático: Decimal para Binário
Converter o número $25_{10}$ para a base Binária ($b=2$):

| Divisão | Quociente Inteiro | Resto | Posição no Resultado |
| :--- | :--- | :--- | :--- |
| $25 \div 2$ | $12$ | **1** | LSB (Bit Menos Significativo) |
| $12 \div 2$ | $6$ | **0** | |
| $6 \div 2$ | $3$ | **0** | |
| $3 \div 2$ | $1$ | **1** | |
| $1 \div 2$ | $0$ | **1** | MSB (Bit Mais Significativo) |

Lendo os restos do último ao primeiro: $25_{10} = 11001_2$.

---

## Conversão Direta entre Binário, Hexadecimal e Octal

Como $16 = 2^4$ e $8 = 2^3$, a conversão entre essas bases descarta divisões sucessivas e utiliza o **agrupamento estático de bits**.

> [!NOTE]
> Se a quantidade total de bits não for um múltiplo exato do tamanho do bloco (4 bits para Hexadecimal ou 3 bits para Octal), **adicione zeros à esquerda do bloco mais significativo (MSB)** até completar a quantidade necessária.

---

### Agrupamento Binário $\leftrightarrow$ Hexadecimal (Blocos de 4 bits)

Cada dígito hexadecimal corresponde exatamente a um grupo de 4 bits (nibble).

#### Exemplo Prático: Número de 10 bits não múltiplo de 4
Converter o valor binário de 10 bits $1101011001_2$ para Hexadecimal:

1. **Separação a partir da direita (LSB):** `11` | `0101` | `1001`
2. **Preenchimento de Zeros (Padding à esquerda):** O bloco mais à esquerda tem apenas 2 bits (`11`). Adicionam-se dois zeros à esquerda para completar o nibble de 4 bits: **`0011`** | `0101` | `1001`
3. **Mapeamento dos Nibbles:**
   * `0011` $\rightarrow 0 + 0 + 2 + 1 = 3_{16}$
   * `0101` $\rightarrow 0 + 4 + 0 + 1 = 5_{16}$
   * `1001` $\rightarrow 8 + 0 + 0 + 1 = 9_{16}$
4. **Resultado Final:** $1101011001_2 = 359_{16}$

---

### Agrupamento Binário $\leftrightarrow$ Octal (Blocos de 3 bits)

Cada dígito octal corresponde exatamente a um grupo de 3 bits.

#### Exemplo Prático: Número de 10 bits não múltiplo de 3
Converter o mesmo valor binário $1101011001_2$ para Octal:

1. **Separação a partir da direita (LSB):** `1` | `101` | `011` | `001`
2. **Preenchimento de Zeros (Padding à esquerda):** O bloco mais à esquerda tem apenas 1 bit (`1`). Adicionam-se dois zeros à esquerda para completar o bloco de 3 bits: **`001`** | `101` | `011` | `001`
3. **Mapeamento dos Trincos (3 bits):**
   * `001` $\rightarrow 0 + 0 + 1 = 1_8$
   * `101` $\rightarrow 4 + 0 + 1 = 5_8$
   * `011` $\rightarrow 0 + 2 + 1 = 3_8$
   * `001` $\rightarrow 0 + 0 + 1 = 1_8$
4. **Resultado Final:** $1101011001_2 = 1531_8$

---

## Ponte para Programação de Sistemas

> [!TIP]
> Em linguagens como C e Assembly, notações como `0x359` (Hexadecimal) e `01531` (Octal) são usadas apenas no código-fonte. O compilador converte esses valores diretamente para o binário equivalente na memória. Ao inspecionar registradores e despejos de memória (*memory dumps*), a capacidade de agrupar mentalmente bits em blocos de 3 ou 4 evita a necessidade de realizar conversões decimais intermediárias.