# Exercícios: Carga Elementar e Quantização

Nesta nota estão concentrados os problemas práticos para calibração dos conceitos de quantização de carga e conservação de sistemas eletrostáticos.

---
##  Enunciados dos Exercícios

### Questão 01
Um corpo condutor inicialmente neutro é eletrizado e passa a exibir uma carga elétrica líquida estável de $Q = 4,8\ \mu\text{C}$.

**a)** Esse corpo encontra-se com excesso ou falta de elétrons? Justifique microscopicamente.  
**b)** Determine a quantidade exata de elétrons ($n$) que foram transferidos durante o processo de eletrização.

### Questão 02
Um condutor metálico (fio de cobre) é percorrido por uma corrente elétrica estável. Uma análise microscópica revela que, a cada segundo, exatamente $5,0 \times 10^{18}$ elétrons atravessam a seção reta do fio.

**a)** Qual é o valor absoluto da carga elétrica total ($Q$) que flui por essa seção a cada segundo?  
**b)** Se a intensidade da corrente elétrica ($I$) é definida pela variação da carga pelo tempo ($I = \Delta Q / \Delta t$), qual é a corrente que alimenta esse condutor em Amperes ($\text{A}$)?


### Questão 03 

Três esferas condutoras idênticas, $A$, $B$ e $C$, estão isoladas. Inicialmente, a esfera $A$ possui carga $Q_A = +12\ \mu\text{C}$, enquanto $B$ e $C$ estão totalmente neutras ($Q_B = 0$ e $Q_C = 0$).

1. A esfera $A$ é colocada em contato com a esfera $B$ e, em seguida, separada.
    
2. Logo após, a esfera $A$ é colocada em contato com a esfera $C$ e separada.
    

Determine a carga elétrica final de cada uma das três esferas após esses processos.

### Questão 04

Duas esferas condutoras distantes, $A$ e $B$, possuem raios diferentes, sendo $R_A = 2R$ e $R_B = 3R$. Inicialmente, a esfera $A$ está carregada com uma carga $Q_A = +20\ \mu\text{C}$ e a esfera $B$ está neutra ($Q_B = 0$). As duas esferas são interligadas por um fio condutor longo e fino até que o equilíbrio eletrostático seja alcançado.

Determine as cargas finais $Q'_A$ e $Q'_B$ de cada esfera após o equilíbrio.

---

##  Gabarito e Resoluções Passo a Passo

### Resolução da Questão 01

**Item a):** Há uma falta de elétrons. O sinal positivo da carga líquida ($Q > 0$) indica que o balanço de carga quebrou em favor dos prótons, o que significa que o corpo perdeu elétrons (as únicas cargas com mobilidade para deixar a malha atômica).

**Item b):** Convertendo a carga de microcoulomb para a unidade padrão:
$$Q = 4,8 \times 10^{-6}\text{ C}$$

Utilizando o princípio da quantização da carga ($Q = n \cdot e$):
$$n = \frac{4,8 \times 10^{-6}\text{ C}}{1,6 \times 10^{-19}\text{ C}}$$

$$n = 3,0 \times 10^{13}\text{ elétrons perdidos.}$$

### Resolução da Questão 02

**Item a):** Dados do problema: $n = 5,0 \times 10^{18}$ elétrons e $e = 1,6 \times 10^{-19}\text{ C}$. Aplicando o princípio da quantização para encontrar a carga total por segundo:
$$Q = n \cdot e$$
$$Q = (5,0 \times 10^{18}) \cdot (1,6 \times 10^{-19})$$
$$Q = 8,0 \times 10^{-1}\text{ C} = 0,8\text{ C}$$

**Item b):** Como a taxa de tempo fornecida é de $\Delta t = 1\text{ s}$, e a carga calculada foi de $\Delta Q = 0,8\text{ C}$:
$$I = \frac{\Delta Q}{\Delta t} = \frac{0,8\text{ C}}{1\text{ s}} = 0,8\text{ A}\ (800\text{ mA})$$


### Resolução da Questão 03

**Dados iniciais:** $Q_A = +12\ \mu\text{C}$, $Q_B = 0$ e $Q_C = 0$. Como as esferas são condutoras e idênticas, a carga se divide igualmente em cada contato.

1. **Primeiro contato ($A$ com $B$):**
   A carga total do sistema se conserva e se redistribui igualmente:
   $$Q'_A = Q'_B = \frac{Q_A + Q_B}{2} = \frac{12\ \mu\text{C} + 0}{2} = +6\ \mu\text{C}$$

2. **Segundo contato ($A$ com $C$):**
   Agora, a esfera $A$ (com sua nova carga de $+6\ \mu\text{C}$) toca em $C$ (que ainda está neutra):
   $$Q''_A = Q'_C = \frac{Q'_A + Q_C}{2} = \frac{6\ \mu\text{C} + 0}{2} = +3\ \mu\text{C}$$

**Resposta Final:**
* $Q_A = +3\ \mu\text{C} \text{ (ou } 3,0 \times 10^{-6}\text{ C)}$
* $Q_B = +6\ \mu\text{C} \text{ (ou } 6,0 \times 10^{-6}\text{ C)}$
* $Q_C = +3\ \mu\text{C} \text{ (ou } 3,0 \times 10^{-6}\text{ C)}$

### Resolução da Questão 04

**Dados iniciais:** $R_A = 2R$, $R_B = 3R$, $Q_A = +20\ \mu\text{C}$ e $Q_B = 0$. Como as esferas possuem raios diferentes, elas atingem o equilíbrio quando seus potenciais elétricos se igualam ($V_A = V_B$), gerando cargas finais proporcionais aos seus raios.

1. **Princípio da Conservação da Carga:**
   A soma das cargas após o contato deve ser igual à carga inicial total do sistema:
   $$Q'_A + Q'_B = Q_A + Q_B$$
   $$Q'_A + Q'_B = 20\ \mu\text{C} \quad \text{--- (Equação I)}$$

2. **Condição de Equilíbrio (Potenciais Iguais):**
   $$\frac{Q'_A}{R_A} = \frac{Q'_B}{R_B}$$
   
   Substituindo os valores dos raios:
   $$\frac{Q'_A}{2R} = \frac{Q'_B}{3R}$$
   
   Simplificando o termo $R$ e isolando $Q'_B$:
   $$Q'_B = \frac{3}{2}Q'_A \implies Q'_B = 1,5Q'_A \quad \text{--- (Equação II)}$$

3. **Resolvendo o Sistema de Equações:**
   Substituindo a Equação II na Equação I:
   $$Q'_A + 1,5Q'_A = 20$$
   $$2,5Q'_A = 20$$
   $$Q'_A = \frac{20}{2,5} = 8\ \mu\text{C}$$

   Agora, determinando o valor de $Q'_B$:
   $$Q'_B = 1,5 \cdot 8 = 12\ \mu\text{C}$$

**Resposta Final:**
Após o equilíbrio térmico e eletrostático, as esferas assumem os valores estáveis de **$Q'_A = 8\ \mu\text{C}$** e **$Q'_B = 12\ \mu\text{C}$**.