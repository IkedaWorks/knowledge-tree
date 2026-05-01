
# 🏛️ Problemas Fundamentais: Estática

> [!IMPORTANT]
> 
> **Importante:**
> 
> Esta seção foca na aplicação prática do **Método do Paralelogramo** e da **Decomposição em Eixos Não Ortogonais**. Lembre-se: em problemas de engenharia, o desenho (DCL) é metade da solução.

### 📝 Lista de Problemas (Hibbeler)

![Exercises](physics-1-fundamental-exercises.webp)

#### F2.1. Resultante na Argola

- **Enunciado:** Determine a intensidade da força resultante que atua sobre a argola e sua direção, medida no sentido horário a partir do eixo $x$.
    
- **Gatilho de Resolução:** Decomposição $x/y$. Calcule $R_x = \sum F_x$ e $R_y = \sum F_y$. A direção final será $\theta = \arctan(|R_y|/|R_x|)$.
    

#### F2.2. Forças no Gancho

- **Enunciado:** Duas forças atuam sobre o gancho. Determine a intensidade da força resultante.
    
- **Gatilho de Resolução:** Lei dos Cossenos para a resultante de dois vetores: $R = \sqrt{F_1^2 + F_2^2 + 2F_1F_2\cos(\theta)}$.
    

#### F2.3. Resultante e Direção (Anti-horária)

- **Enunciado:** Determine a intensidade da força resultante e sua direção, medida no sentido anti-horário a partir do eixo $x$ positivo.
    
- **Dica:** Atente-se ao quadrante final do vetor resultante para ajustar o ângulo em relação ao semieixo $x$ positivo.
    

---

### ⚠️ Desafios de Decomposição (Eixos u, v)

#### F2.4. Decomposição nos eixos $u$ e $v$

- **Enunciado:** Decomponha a força de $30 \text{ N}$ nas componentes ao longo dos eixos $u$ e $v$, e determine a intensidade de cada uma delas.
    
- **Estratégia:** Como os eixos são oblíquos, monte o triângulo de forças e utilize a **Lei dos Senos**. As componentes são os lados do triângulo cujas direções são paralelas a $u$ e $v$.
    

#### F2.5. Componentes nos Membros $AB$ e $AC$

- **Enunciado:** A força $F = 450 \text{ N}$ atua sobre a estrutura. Decomponha essa força nas componentes que atuam ao longo dos membros $AB$ e $AC$.
    
- **Insight:** Aplique a mesma lógica de eixos não ortogonais. A força de $450 \text{ N}$ funciona como a resultante (diagonal) do paralelogramo formado pelos membros.
    

#### F2.6. Intensidade e Componente $F_v$

- **Enunciado:** Se a força $\mathbf{F}$ precisa ter uma componente ao longo do eixo $u$ com $F_u = 6 \text{ kN}$, determine a intensidade de $\mathbf{F}$ e de sua componente $\mathbf{F}_v$ ao longo do eixo $v$.
    
- **Cuidado:** O triângulo de forças deve ser construído a partir da componente conhecida para fechar a geometria da resultante.
    

---

> [!TIP]
> 
> **Tip**
> 
> **Engineer's Insight:** Em eixos oblíquos, a projeção ortogonal ($\cos/\text{sen}$ simples) falha. A **Lei dos Senos** é a ferramenta definitiva aqui:
> 
> $$\frac{F}{\text{sen}(\alpha)} = \frac{F_u}{\text{sen}(\beta)} = \frac{F_v}{\text{sen}(\gamma)}$$