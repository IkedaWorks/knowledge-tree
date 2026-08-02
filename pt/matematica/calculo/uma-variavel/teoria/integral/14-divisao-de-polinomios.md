
# Divisão de Polinômios

### Introdução e Contexto

A divisão polinomial é uma ferramenta de pré-cálculo essencial para integrar **Funções Racionais** (frações de polinômios).

**Quando usar:** Sempre que você tiver uma fração onde o **grau do Numerador $\ge$ grau do Denominador**. Nestes casos, a fração é chamada de "imprópria" e deve ser simplificada antes da integração.

---

### O Algoritmo da Divisão (Método da Chave)

O processo busca escrever a relação:

$$\frac{\text{Dividendo}}{\text{Divisor}} = \text{Quociente} + \frac{\text{Resto}}{\text{Divisor}}$$

#### Passo a Passo:

1. **Ordenação:** Escreva os polinômios em ordem decrescente de potência.
    
2. **Divisão do Líder:** Divida o termo de maior grau do dividendo pelo termo de maior grau do divisor.
    
3. **Multiplicação e Subtração:** Multiplique o resultado pelo divisor inteiro e subtraia do dividendo (inverta os sinais).
    
4. **Repetição:** Repita o processo com o novo polinômio resultante até que o grau do resto seja **menor** que o grau do divisor.
    

---

### Exemplo Completo

Vamos dividir: $\frac{x^3 + 2x + 1}{x - 1}$

1. **Primeiro Termo:** $x^3 \div x = \mathbf{x^2}$.
    
    - Multiplica: $x^2(x - 1) = x^3 - x^2$.
        
    - Subtrai: $(x^3 + 2x + 1) - (x^3 - x^2) = \mathbf{x^2 + 2x + 1}$.
        
2. **Segundo Termo:** $x^2 \div x = \mathbf{x}$.
    
    - Multiplica: $x(x - 1) = x^2 - x$.
        
    - Subtrai: $(x^2 + 2x + 1) - (x^2 - x) = \mathbf{3x + 1}$.
        
3. **Terceiro Termo:** $3x \div x = \mathbf{3}$.
    
    - Multiplica: $3(x - 1) = 3x - 3$.
        
    - Subtrai: $(3x + 1) - (3x - 3) = \mathbf{4}$ (Resto).
        

**Estrutura Final:** $\frac{x^3 + 2x + 1}{x - 1} = x^2 + x + 3 + \frac{4}{x - 1}$

---

### Aplicação no Cálculo Integral

A divisão transforma uma integral impossível em uma soma de integrais simples:

- O **Quociente** vira uma integral de polinômio (Regra da Potência).
    
- O **Resto/Divisor** geralmente resulta em um Logaritmo ou Arco Tangente.
    

#### Exemplo de Integração:

$$\int \frac{x^3 + 2x + 1}{x - 1} \, dx = \int \left( x^2 + x + 3 + \frac{4}{x - 1} \right) \, dx$$

**Resultado Final:**

$$\frac{x^3}{3} + \frac{x^2}{2} + 3x + 4\ln|x - 1| + C$$

---

###  Dicas e Curiosidades

- **Briot-Ruffini:** Se o seu divisor for do tipo $(x - a)$, você pode usar o dispositivo prático de Briot-Ruffini para ganhar tempo. É muito mais rápido que o método da chave!
    
- **A "Malandragem" dos Produtos Notáveis:** Se você perceber que o numerador pode ser fatorado (ex: uma diferença de quadrados), você pode simplificar a fração direto, sem precisar da divisão longa.
    
- **Teorema Fundamental da Álgebra:** Esse teorema garante que todo polinômio de grau $n$ tem exatamente $n$ raízes (reais ou complexas). É a base que permite faturarmos qualquer polinômio para usar em Frações Parciais.