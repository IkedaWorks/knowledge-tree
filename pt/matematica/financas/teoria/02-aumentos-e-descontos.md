
# Aplicação em Aumentos e Descontos

Esses dois mecanismos são muito usados em problemas de "parte por um todo", geralmente associados ao dinheiro, que é sua aplicação mais comum.

## O que é um Aumento?

Imagine que você trabalha em uma empresa de tecnologia e, nesse mês, você foi um funcionário extraordinário. Por isso, ganhou um acréscimo no seu salário além do que recebe normalmente. Isso é conhecido como **aumento**.

Em outras palavras, um aumento é o acréscimo em relação ao todo, que nós referenciamos como $100\%$ ,  $\frac{100}{100}$  ou simplesmente $1$. No fim das contas, o valor final será:

$$\text{Valor Final} = 100\% + \text{aumento} \quad \text{ou} \quad 1 + \text{taxa de aumento}$$

### Exemplo Prático:

Suponha que você ganhe $R\$\,1000,00$ de salário e recebeu um aumento de $10\%$. O seu salário final será o seu todo ($100\%$) mais $10\%$ desse todo (ou seja, $0,1$ de $R\$\,1000,00$).

Você pode calcular o aumento de $10\%$ de forma isolada e depois somar:

$$\text{Salário Final} = \text{Salário Inicial} + \text{Aumento}$$

$$\text{Salário Final} = 1000 + (1000 \cdot 10\%) = 1000 + (1000 \cdot 0,1) = 1000 + 100 = 1100$$

Ou você pode ser **mais inteligente** e pensar direto pelo **Fator de Multiplicação**:

- Se $R\$\,1000,00$ é o seu todo ($100\%$ ou $1$).
    
- E o seu aumento é de $10\%$.
    

Isso significa que, em relação ao seu salário original, você agora tem uma parcela de $110\%$ ($100\% + 10\%$) ou $1,1$ ($1 + 0,1$). Então, basta multiplicar esse fator direto pelo seu todo para encontrar o salário real:

$$\text{Salário Final} = 1000 \cdot 1,1 = 1100$$

Você chegará exatamente ao mesmo resultado com apenas uma operação.

> [!NOTE]
> 
> Perceba que esse segundo jeito é o mais utilizado no dia a dia, porque é mais eficaz. 
> Se você for programador deveriar usar essa segunda operação, porque com menos iteração mais eficiente é o seu código.
> 


## O que é um Desconto?

Agora vamos supor o cenário oposto: você não fez um bom trabalho na empresa, foi irresponsável e faltou ao dever. Como consequência, foi tirada uma parcela de $10\%$ dos $R\$\,1000,00$ que você iria receber. Isso é chamado de **desconto** — quando você perde ou diminui uma parte do seu todo.

O desconto segue a mesma lógica matemática do aumento:

$$\text{Salário Final} = 1000 - (1000 \cdot 10\%) = 1000 - 100 = 900$$

De um jeito muito mais prático e linear, você pode pensar que se o todo era $100\%$ ($1$) e você perdeu $10\%$ ($0,1$), você passou a ter $90\%$ ($0,9$) do valor original:

$$\text{Salário Final} = 1000 \cdot (100\% - 10\%) = 1000 \cdot 90\% = 1000 \cdot 0,9 = 900$$

## Variação Percentual (O Caminho Inverso)

Existe um conceito chamado **Variação Percentual** que usa exatamente essa lógica para fazer o caminho inverso. Se você já sabe o valor final e o valor inicial, como descobrir qual foi a porcentagem de aumento ou de desconto?

Basta extrair a razão entre os dois momentos:

$$\text{Fator de Variação} = \frac{\text{Valor Final}}{\text{Valor Inicial}}$$

A análise do resultado é direta e baseia-se no valor de referência $1$:

- **Se o resultado for maior que 1 (Aumento):** Se der $1,25$, você subtrai $1$ e descobre na hora que o aumento foi de $0,25$, ou seja, $25\%$.
    
- **Se o resultado for menor que 1 (Desconto):** Se der $0,80$, você vê o quanto falta para chegar a $1$ ($1 - 0,80 = 0,20$) e descobre que o desconto foi de $20\%$.