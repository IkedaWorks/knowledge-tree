

# Crônica de uma "Descoberta" Extraordinária

Se você for um estudante atento — sem a intenção de me vangloriar, mas já o fazendo, tal como o grande Jô Soares utilizava desta preterição —, deve ter percebido que, ao final do processo de demonstração das derivadas trigonométricas, é possível atingir resultados distintos apenas manipulando a álgebra, em vez de realizar a substituição imediata pela relação fundamental da trigonometria. Curioso, não?

Ao atingir uma expressão derivada divergente do padrão, inicialmente supus tratar-se de um erro processual. Contudo, após análise, compreendi que não era um equívoco, mas sim uma "nova" descoberta. Nutri breves esperanças de ter realizado algo extraordinário, tornando-me um forte candidato à Medalha Fields... até descobrir que um matemático chamado **Riccati** já havia percorrido este caminho no século XVIII.

Pesquisando a fundo, entendi que essa "nova derivada" compõe o que se denomina **Equação Diferencial Ordinária (EDO)**. Como estudante de engenharia, este conceito é familiar em disciplinas como Circuitos Elétricos, mas fica o convite para que questionem seus professores sobre a relação profunda entre funções trigonométricas e as EDOs.

### A Relação Identificada

Na demonstração da derivada da tangente, $\frac{d}{dx}(\tan x)$, o estágio final apresenta a seguinte relação:

$$\frac{d}{dx}(\tan x) = \frac{\cos^2(x) + \sin^2(x)}{\cos^2(x)}$$

Em vez de substituir o numerador pela relação fundamental ($\sin^2 x + \cos^2 x = 1$), o que resultaria em $\sec^2(x)$, realizamos a decomposição das frações sob o denominador comum:

$$\frac{d}{dx}(\tan x) = \frac{\cos^2(x)}{\cos^2(x)} + \frac{\sin^2(x)}{\cos^2(x)}$$

Atingimos, assim, a elegante identidade:

$$\mathbf{\frac{d}{dx}(\tan x) = 1 + \tan^2(x)}$$

Neste cenário, se definirmos $\tan(x)$ como uma variável $y$, obtemos a EDO: $y' = 1 + y^2$.

### A Expansão para a Cotangente

A "toca do coelho" de Riccati não se limita à tangente. Como é sabido na engenharia, onde existe um seno, há um cosseno à espreita, e a cotangente segue a mesma lógica algébrica. Ao derivar $\frac{d}{dx}(\cot x)$, o processo conduz a um ponto similar:

$$\frac{d}{dx}(\cot x) = \frac{-\sin^2(x) - \cos^2(x)}{\sin^2(x)}$$

A aplicação da mesma "separação" fracionária revela uma simetria notável:

$$\frac{d}{dx}(\cot x) = \frac{-\sin^2(x)}{\sin^2(x)} + \frac{-\cos^2(x)}{\sin^2(x)}$$

O resultado apresenta uma estética matemática precisa:

$$\mathbf{\frac{d}{dx}(\cot x) = -(1 + \cot^2(x))}$$

Se definirmos a cotangente como $u$, temos a EDO de Riccati: $u' = -(1 + u^2)$. Trata-se de um espelho perfeito, com inversão de sinal, demonstrando que a taxa de variação da "co-função" é o negativo da unidade somada ao seu próprio quadrado.

### O Desfecho na Engenharia

O ponto crucial é que estas equações, que podem parecer meras curiosidades acadêmicas, são as mesmas que governam a carga e descarga de capacitores em circuitos não lineares ou a propagação de ondas em guias, temas centrais do Eletromagnetismo.

Riccati já descrevia o comportamento de sistemas complexos muito antes da invenção da iluminação elétrica. O que parecia um erro de percurso era, na verdade, a porta de entrada para a **Modelagem Matemática**.

Fica o aviso: se um resultado não parecer "padronizado" como o dos livros, analise-o detalhadamente. Você pode não receber a Medalha Fields hoje, mas estará mais próximo de compreender os mecanismos reais do mundo.