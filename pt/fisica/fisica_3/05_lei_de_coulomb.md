# Lei de Coulomb (Força Elétrica)

A Lei de Coulomb trata da interação de cargas elétricas puntiformes (pontuais) em repouso. Como estamos falando da interação de um campo elétrico com uma carga elétrica, descrevemos esse fenômeno por meio de uma **força elétrica**, que serve como a fundação de toda a eletrostática.

---

## 📜 Contexto Histórico e a Balança de Torção

Formulada pelo físico francês Charles Augustin de Coulomb em 1785, esta lei quantifica a força de atração ou repulsão entre duas cargas. Como na época não existiam softwares de simulação ou multímetros, Coulomb desenvolveu um aparato mecânico extremamente sensível chamado **Balança de Torção**.

### O Processo Experimental: Medindo o Invisível Antes do Elétron

Coulomb publicou seus ensaios mais de **110 anos antes** de J.J. Thomson descobrir a existência do elétron (1897). Em vez de conhecer a quantidade absoluta de cargas elementares, Coulomb utilizou a **simetria geométrica e proporções** para isolar suas variáveis:

1. **Controle das Frações de Carga ($q_1 \cdot q_2$):**
   Para variar a carga sem ter um medidor absoluto, ele usou o princípio da condução por contato. Ele eletrizava uma esfera condutora polida com uma carga desconhecida $Q$ e a tocava em outra esfera idêntica e neutra. Por pura simetria geométrica, a carga líquida era obrigada a se dividir perfeitamente ao meio ($\frac{1}{2}Q$). Repetindo o processo, ele conseguia manipular frações precisas de carga ($\frac{1}{2}, \frac{1}{4}, \frac{1}{8}$) sem nem saber o que era um elétron.

2. **Dependência com a Distância ($1/r^2$):**
   Mantendo as cargas fixas e variando a distância ($r$) entre as esferas, ele mediu o ângulo de rotação do fio de suspensão. Ele observou que:
   * Dobrar a distância ($2r$) tornava a força eletrostática **4 vezes menor** ($\frac{1}{4}F$).
   * Triplicar a distância ($3r$) tornava a força **9 vezes menor** ($\frac{1}{9}F$).
   * *Conclusão:* A força é inversamente proporcional ao quadrado da distância: $F \propto \frac{1}{r^2}$.

> [!NOTE]
> 
> **Observe que o gráfico de força X distância é uma hipérbole de segundo grau, isso indica a proporção indireta.**
> 

### Funcionamento Mecânico do Aparato

A balança de torção consistia em um fino fio de prata ou seda que suspendia uma haste horizontal isolante:
* **Uma das extremidades** continha uma pequena esfera condutora (a carga a ser testada).
* **A extremidade oposta** continha um contrapeso feito de material isolante neutro (como papel ou cera), servindo puramente para manter o equilíbrio mecânico horizontal, sem sofrer interferência elétrica.

Ao introduzir no sistema uma segunda esfera condutora fixa e carregada, a repulsão eletrostática empurrava a esfera móvel, torcendo o fio de suspensão. O fio exercia um torque restaurador mecânico proporcional ao ângulo de torção (Lei de Hooke para torção). Lendo o deslocamento angular estável em uma escala graduada de vidro, Coulomb calculava a força eletrostática exata.

Unindo essas observações empíricas, chegou-se à famosa relação escalar:
$$F = k \frac{|q_1 \cdot q_2|}{r^2}$$

---

## 🔬 O Conceito Matemático Vetorial

Embora Coulomb tenha deduzido a relação de forma escalar, a engenharia e o Cálculo III exigem a abordagem vetorial para modelar sistemas tridimensionais complexos. 

A magnitude da força é ditada por:

* **Constante Eletrostática ($k$):** $k = \frac{1}{4\pi\epsilon_0} \approx 8,99 \times 10^9 \text{ N}\cdot\text{m}^2/\text{C}^2$

* **Permissividade do Vácuo ($\epsilon_0$):** $\epsilon_0 \approx 8,85 \times 10^{-12} \text{ C}^2/\text{N}\cdot\text{m}^2$

### 🎯 Notação Vetorial (Cálculo Vetorial)

A força vetorial que a carga de origem ($1$) exerce sobre a carga de destino ($2$) é escrita como:

$$\vec{F}_{1\to2} = k \frac{q_1 \cdot q_2}{r^2} \hat{r}_{1\to2}$$

Onde $\hat{r}_{1 \to 2} = \frac{\vec{r}_{1 \to 2}}{r}$ é o versor (vetor unitário) que aponta na linha reta da carga 1 para a carga 2. Se o produto $q_1 \cdot q_2$ for positivo, a força assume o mesmo sentido do versor (repulsão), se for negativo, assume o sentido oposto (atração).

---

## 🧩 Princípio da Superposição

Quando um sistema possui múltiplas cargas atuando no espaço, a força resultante sobre uma carga específica é a **soma vetorial** de todas as forças exercidas sobre ela individualmente pelas outras cargas:

$$\vec{F}_{res} = \vec{F}_{1} + \vec{F}_{2} + \vec{F}_{3} + \dots = \sum_{i=1}^{n} \vec{F}_{i}$$

> [!CAUTION]
> 
> **Erro Clássico de Engenharia:** Nunca some os módulos das forças diretamente, a menos que todas as cargas estejam na mesma linha reta (colineares). Sempre decomponha as forças em suas componentes cartesianas ($\hat{i}, \hat{j}, \hat{k}$) antes de efetuar a soma.