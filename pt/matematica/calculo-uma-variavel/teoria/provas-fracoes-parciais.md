

# Prova:

### A Intuição: O MMC Inverso

No ensino fundamental, aprendemos a juntar frações distintas em uma única expressão usando o MMC. No Cálculo, as **Frações Parciais** fazem o caminho oposto: elas "desmontam" um resultado final para encontrar as peças originais.

**A Analogia:** Imagine que a integral é uma máquina que não sabe processar "objetos colados" (frações com denominadores complexos). A DFP é a ferramenta que descola esses objetos em peças simples (frações de grau 1) que a máquina processa instantaneamente como **Logaritmos ($\ln$)**.

> [!IMPORTANT]
> 
> **A Garantia:** Se a álgebra permite somar duas frações e chegar em uma só, ela também garante que existe um caminho de volta único.

---

### A Prova Formal: Os Dois Pilares

A validade do método repousa sobre a combinação de um teorema algébrico e uma propriedade fundamental do cálculo.

#### Pilar A: Teorema Fundamental da Álgebra (Existência e Unicidade)

Dada uma função racional $f(x) = \frac{P(x)}{Q(x)}$, onde o $\text{grau de } P < \text{grau de } Q$:

1. **Fatoração:** O Teorema Fundamental da Álgebra garante que todo polinômio $Q(x)$ pode ser fatorado em termos lineares $(x - r)$ ou quadráticos irredutíveis.
    
2. **Identidade Algébrica:** O teorema das frações parciais afirma que existe um conjunto **único** de constantes ($A, B, C...$) tal que:
    
    $$\frac{P(x)}{(x-r_1)(x-r_2)} \equiv \frac{A}{x-r_1} + \frac{B}{x-r_2}$$
    
3. **Prova da Unicidade:** Ao multiplicar pelo denominador comum, caímos em um sistema de $n$ equações lineares com $n$ incógnitas. Como os termos $(x-r)$ são linearmente independentes, esse sistema sempre possui uma solução única.
    

#### Pilar B: Linearidade do Operador Integral

Uma vez provado por álgebra que a fração complexa é **identicamente igual** à soma das frações simples, aplicamos a propriedade da linearidade da integral:

$$\int \left( \sum_{i=1}^{n} \frac{A_i}{x-r_i} \right) dx = \sum_{i=1}^{n} \int \frac{A_i}{x-r_i} \, dx$$

Como a integral da soma é a soma das integrais, e a primitiva de $\frac{1}{x-r}$ é provadamente $\ln|x-r|$ (via substituição simples $u = x-r$), a técnica está formalmente validada.

---

### Conclusão: Por que esta prova é complexa?

Esta demonstração exige que você conecte três mundos diferentes:

- **Álgebra de Polinômios:** Para faturar e garantir a existência das raízes.
    
- **Álgebra Linear:** Para entender que os coeficientes $A, B, C$ vêm de um sistema que sempre tem solução.
    
- **Cálculo Integral:** Para aplicar a linearidade e o TFC.