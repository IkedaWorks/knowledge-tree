
# Aumentos e Descontos Sucessivos

Este assunto é sutil e costuma induzir muitas pessoas ao erro. Intuitivamente, pode-se pensar: _"Se um produto aumentou $20\%$ e depois diminuiu $20\%$, ele voltou ao seu preço original"_.

No entanto, a matemática financeira mostra que **aplicar aumentos ou descontos sucessivos com a mesma porcentagem nunca faz o valor retornar ao ponto de partida**.

## O Paradoxo do Livro de Cálculo

Vamos entender a mecânica por trás disso usando um exemplo prático. Suponha que um livro de Cálculo custe $R\$\,100,00$. Ele sofre um aumento de $10\%$ e, logo em seguida, um desconto de $10\%$.

### Etapa 1: O Aumento

Aplicando o fator de multiplicação que aprendemos no módulo anterior ($1 + 0,1 = 1,1$):

$$\text{Preço Após Aumento} = 100 \cdot 1,1 = 110$$

### Etapa 2: O Desconto

Aqui está o ponto crítico. O desconto de $10\%$ não será aplicado sobre os $R\$\,100,00$ originais, mas sim sobre o novo valor de mercado. **O nosso "100%" mudou; agora ele é $R\$\,110,00$.**

Aplicando o fator de desconto ($1 - 0,1 = 0,9$):

$$\text{Preço Final} = 110 \cdot 0,9 = 99$$

### Análise do Resultado

O preço final foi de $R\$\,99,00$. O valor não retornou aos $R\$\,100,00$ iniciais. Utilizando a equação da variação percentual para analisar o cenário global:

$$\text{Fator de Variação} = \frac{\text{Valor Final}}{\text{Valor Inicial}} = \frac{99}{100} = 0,99$$

Como $0,99$ representa $99\%$ do valor original, provamos que o saldo líquido de um aumento de $10\%$ seguido de um desconto de $10\%$ é, na realidade, um **desconto real de $1\%$** ($1 - 0,99 = 0,01$).

> ⚠️ **Lei Acumulativa:** Toda vez que aplicamos porcentagens de forma sucessiva sobre uma mesma grandeza, os efeitos se multiplicam em cadeia porque a base de cálculo é dinâmica:
> 
> - Aumentos sucessivos acumulam **mais** do que a soma das taxas.
>     
> - Descontos sucessivos reduzem **menos** do que a soma das taxas.
>     

##  A Generalização Algorítmica (O Produto dos Fatores)

Computacionalmente, para calcular o impacto de $n$ variações sucessivas, não precisamos fazer regras de três ou quebrar o cálculo em dezenas de linhas de código. Basta multiplicar a cadeia de fatores de variação ($f_1, f_2, \dots, f_n$):

$$\text{Valor Final} = \text{Valor Inicial} \cdot (f_1 \cdot f_2 \cdots f_n)$$

No caso do nosso livro de cálculo:

$$\text{Valor Final} = 100 \cdot (1,1 \cdot 0,9) = 100 \cdot 0,99 = 99$$

## Engenharia Reversa: Como retornar ao valor original?

Para fazer com que um valor retorne exatamente ao ponto original após sofrer uma alteração percentual, é necessário calcular a **taxa de compensação** utilizando o inverso multiplicativo do fator atual.

Se um ativo sofreu uma alteração e passou a valer sob um fator $f$, para fazê-lo retornar ao estado original de equilíbrio ($1$), deve-se multiplicá-lo pelo inverso: $\frac{1}{f}$.

### Exemplo de Aplicação:

Um livro de cálculo de $R\$\,100,00$ sofreu um aumento de $25\%$ ($f = 1,25$), passando a custar $R\$\,125,00$. Qual deve ser a taxa de desconto aplicada sobre o novo preço para que ele volte a custar os $R\$\,100,00$ originais?

1. Encontra-se o fator de retorno:
    
    $$\text{Fator de Retorno} = \frac{1}{1,25} = 0,80$$
    
2. Analisa-se o fator obtido:
    
    Como $0,80$ é menor que $1$, identifica-se a necessidade de um desconto. A taxa exata do desconto será a diferença necessária para atingir a unidade:
    
    $$\text{Desconto} = 1 - 0,80 = 0,20 \implies 20\%$$
    

> 🎯 **Conclusão:** Para anular um aumento de $25\%$, não se aplica um desconto de $25\%$, mas sim um desconto exato de $20\%$. A variação percentual estruturada garante o controle matemático e a previsibilidade dos fluxos dinâmicos de preço.