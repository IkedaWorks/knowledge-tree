
# Dominando Integrais Trigonométricas

### 1. A Ontologia do Método: Por que funciona?

A integração trigonométrica não é um conjunto de truques isolados; é a aplicação da **Simetria** e da **Periodicidade**.

- **Identidades de Pitágoras:** Permitem transitar entre funções e suas derivadas (Seno $\leftrightarrow$ Cosseno).
    
- **Identidades de Redução (Euler):** Permitem transformar potências (energia acumulada) em frequências múltiplas, que são linearmente fáceis de integrar.
    

---

### 2. Tipologias e Gatilhos Mentais

Para não perder tempo em prova, você precisa de **gatilhos de reconhecimento imediato**:

#### A. O "Roubo" do Diferencial ($\int \sin^m x \cos^n x \, dx$)

- **Gatilho:** Existe algum expoente **ímpar**?
    
- **Ação:** Separe uma unidade desse expoente para ser o seu $du$. Se $\cos x$ é o ímpar, seu $u$ será $\sin x$.
    
- **Demonstração:** Baseia-se em $\sin^2 x + \cos^2 x = 1$. Ao isolar um termo, o restante torna-se um polinômio simples em relação à outra função.
    

#### B. A Barreira dos Pares ($\int \sin^m x \cos^n x \, dx$ com $m, n$ pares)

- **Gatilho:** Todos os expoentes são **pares**. Não há "sobra" para o $du$.
    
- **Ação:** Expansão via **Ângulo Metade**. Você "paga o pedágio" algébrico para baixar o grau.
    
- **Fórmulas:** $\sin^2 x = \frac{1 - \cos(2x)}{2} \quad | \quad \cos^2 x = \frac{1 + \cos(2x)}{2}$.
    

#### C. O Binômio Tangente-Secante ($\int \tan^m x \sec^n x \, dx$)

- **Gatilho 1:** Secante é **par**? Reserve $\sec^2 x$ para o $du$ e use $\sec^2 x = 1 + \tan^2 x$.
    
- **Gatilho 2:** Tangente é **ímpar**? Reserve $\sec x \tan x$ para o $du$ e use $\tan^2 x = \sec^2 x - 1$.
    

#### D. Substituição Trigonométrica (A Geometria Oculta)

- **Gatilho:** Raízes do tipo $\sqrt{\pm x^2 \pm a^2}$.
    
- **Ação:** Mapeie os termos no **Teorema de Pitágoras**.
    
    - $\sqrt{a^2 - x^2} \to x = a \sin \theta$ (Cateto oposto).
        
    - $\sqrt{a^2 + x^2} \to x = a \tan \theta$ (Cateto oposto, hipotenusa é a raiz).
        
    - $\sqrt{x^2 - a^2} \to x = a \sec \theta$ (Hipotenusa).
        

---

### 3. Seção de Exercícios: Prática Deliberada

1. **Ímpar Puro:** $\int \cos^3 x \, dx$
    
2. **Par Cruel:** $\int \sin^2 x \cos^2 x \, dx$
    
3. **Tangente/Secante:** $\int \tan^3 x \sec^4 x \, dx$
    
4. **Tangente Ímpar:** $\int \tan^5 x \sec^3 x \, dx$
    
5. **Substituição Clássica:** $\int \frac{1}{x^2\sqrt{x^2+9}} \, dx$
    
6. **Substituição Seno:** $\int \sqrt{1-4x^2} \, dx$
    
7. **Frequências Diferentes:** $\int \sin(5x) \sin(2x) \, dx$
    
8. **Secante ao Cubo (Cíclica):** $\int \sec^3 x \, dx$
    
9. **Completando Quadrado + Subst.:** $\int \frac{1}{\sqrt{x^2-4x+13}} \, dx$
    
10. **O Desafio Final (Nível JEE Advanced):** Abaixo.
    

---

### 4. O Desafio Supremo: JEE Advanced Style

**Problema:** Calcule a integral definida:

$$I = \int_{0}^{\pi/2} \frac{\sin^2 x}{\sin x + \cos x} \, dx$$

**Por que é difícil?** Não cai em uma tipologia simples de imediato. Exige manipulação de propriedades de simetria (Propriedade de King) combinada com técnicas trigonométricas.

**Passo a Passo (The God Run):**

1. **Propriedade de Simetria:** $\int_{a}^{b} f(x) dx = \int_{a}^{b} f(a+b-x) dx$.
    
    Logo, $I = \int_{0}^{\pi/2} \frac{\cos^2 x}{\cos x + \sin x} \, dx$.
    
2. **Soma das Integrais:** $2I = \int_{0}^{\pi/2} \frac{\sin^2 x + \cos^2 x}{\sin x + \cos x} \, dx = \int_{0}^{\pi/2} \frac{1}{\sin x + \cos x} \, dx$.
    
3. **Transformação do Denominador:** Use a identidade $\sin x + \cos x = \sqrt{2} \sin(x + \pi/4)$.
    
    $2I = \frac{1}{\sqrt{2}} \int_{0}^{\pi/2} \csc(x + \pi/4) \, dx$.
    
4. **Integral da Cossecante:** $\int \csc u \, du = \ln|\csc u - \cot u|$.
    
    $2I = \frac{1}{\sqrt{2}} \left[ \ln|\csc(x + \pi/4) - \cot(x + \pi/4)| \right]_{0}^{\pi/2}$.
    
5. **Avaliação:**
    
    No limite $\pi/2$: $\ln|\csc(3\pi/4) - \cot(3\pi/4)| = \ln|\sqrt{2} - (-1)| = \ln(\sqrt{2} + 1)$.
    
    No limite $0$: $\ln|\csc(\pi/4) - \cot(\pi/4)| = \ln|\sqrt{2} - 1|$.
    
6. **Resultado Final:**
    
    $2I = \frac{1}{\sqrt{2}} \ln\left(\frac{\sqrt{2}+1}{\sqrt{2}-1}\right)$. Racionalizando: $\frac{\sqrt{2}+1}{\sqrt{2}-1} = (\sqrt{2}+1)^2$.
    
    $2I = \frac{1}{\sqrt{2}} \ln(\sqrt{2}+1)^2 = \frac{2}{\sqrt{2}} \ln(\sqrt{2}+1)$.
    
    **$I = \frac{1}{\sqrt{2}} \ln(\sqrt{2} + 1)$**