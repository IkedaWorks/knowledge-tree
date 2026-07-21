
## A Construção Axiomática dos Conjuntos (ZFC)

### Visão Geral

A Teoria dos Conjuntos moderna não busca refletir a realidade física, mas sim estabelecer um sistema formal e não contraditório. Os axiomas apresentados são convenções formais deliberadas para construir todos os objetos matemáticos a partir de um único conceito primitivo: o **Conjunto**.

### Formalização dos Axiomas

#### 1. Axioma do Conjunto Vazio

Garante a existência de ao menos um conjunto que não possui elementos.

- **Definição Formal**
    
    $$\exists x \forall y (y \notin x)$$
    
- **Notação:** Denotado por $\emptyset$ ou $\{\}$.
    
- **Propriedade:** Único conjunto com cardinalidade igual a zero ($\vert{}\emptyset\vert{} = 0$).
    

#### 2. Axioma do Par e os Ordinais de Von Neumann

Permite a criação de um novo conjunto contendo exatamente dois elementos dados.

- **Definição Formal**
    
    $$\forall a \forall b \exists c \forall x (x \in c \iff (x = a \lor x = b))$$
    
- **Construção dos Números Naturais ($\mathbb{N}$)**
    
    - $0 \equiv \emptyset$
        
    - $1 \equiv \{0\} = \{\emptyset\}$
        
    - $2 \equiv \{0, 1\} = \{\emptyset, \{\emptyset\}\}$
        
    - $3 \equiv \{0, 1, 2\} = \{\emptyset, \{\emptyset\}, \{\emptyset, \{\emptyset\}\}\}$
        
    - $n + 1 \equiv n \cup \{n\}$
        

#### 3. Definição Formal do Par Ordenado (Kuratowski)

Conjuntos comuns são não ordenados ($\{a, b\} = \{b, a\}$). Para formalizar ordem e precedência sem introduzir novos conceitos primitivos, utiliza-se a definição de Kazimierz Kuratowski.

- **Definição Formal**
    
    $$(a, b) \equiv \{\{a\}, \{a, b\}\}$$
    
- **Teorema da Igualdade de Pares**
    
    $$(a, b) = (c, d) \iff (a = c \land b = d)$$
    
- **Mecanismo:** A assimetria da estrutura permite extrair o primeiro elemento $a$ (a interseção dos elementos de $(a,b)$) e o segundo elemento $b$.
    

#### 4. Axioma da Fundação (Regularidade)

Garante que a relação de pertinência $\in$ seja bem-fundada, impedindo cadeias infinitas descendentes e auto-pertinência.

- **Definição Formal**
    
    $$\forall x (x \neq \emptyset \implies \exists y (y \in x \land y \cap x = \emptyset))$$
    
- **Consequência Teórica:** Proíbe expressamente que $A \in A$. Todo conjunto possui uma profundidade finita cuja base é o conjunto vazio $\emptyset$.
    

#### 5. Axioma da União

Permite extrair elementos de uma coleção de conjuntos e agrupá-los em um único nível.

- **Definição Formal**
    
    $$\forall A \exists U \forall x (x \in U \iff \exists B (x \in B \land B \in A))$$
    
- **Notação:** $U = \bigcup A$
    
- **Exemplo:** Se $A = \{\{1, 2\}, \{3, 4\}\}$, então $\bigcup A = \{1, 2, 3, 4\}$.
    

### Resumo Técnico

A escolha destes axiomas visa estritamente o rigor operacional. A partir destas definições formais, constroem-se as relações, as funções, o Produto Cartesiano $A \times B$ e toda a aritmética dos números reais.