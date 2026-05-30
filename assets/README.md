
# 📷 Assets & Media Management

This directory centralizes all binary files, vector diagrams, and media assets used across the engineering study notes.

## 🛠 Guidelines for Contributors

To ensure repository performance and cross-platform compatibility (Obsidian/GitHub), please follow these standards:

### 1. Preferred File Formats: 

* **Priority 1: `.svg` (Vector Graphics):** **Absolute priority** for technical diagrams, coordinate systems, and geometric shapes generated via Inkscape or Excalidraw. Infinite resolution with minimal file size.
* **Priority 2: `.webp` (Compressed Raster):** Use for realistic figures, intricate textbook screenshots, or complex visual textures where vectorization is impossible. Excellent compression-to-quality ratio.
* **Fallback: `.jpg / .jpeg`:** Use only for high-contrast photos of physical textbooks or handwritten paper notes.
* **Avoid: `.png`:** Do not use unless alpha transparency is explicitly required and the asset cannot be rendered as an `.svg`.

### 2. Naming Convention:

Use a hybrid approach to distinguish between content and assets, ensuring compatibility with GitHub and Unix-based systems:

* **Notes & Folders (snake_case):** Maintain for consistency with existing academic logs. *Example:* `phys1_statics_notes.md`
* **Images & Assets (kebab-case):** Standard for web assets and easy visual distinction in terminal trees. *Example:* `phys1-statics-hibbeler-f2-1.svg` or `calc1-integration-by-parts.webp`

> [!TIP]
>  
> **Tip:** This distinction helps in identifying file types at a glance in the terminal and prevents conflicts with Python/C variable naming conventions.

### 3. Workflow & Linking

* Save the optimized vector or compressed image directly into this `/assets` folder.
* Link it in your Markdown file using relative paths for maximum compatibility:
`![Brief Description](../assets/file-name.svg)`

---


# 📷 Gestão de Ativos e Mídias 

Este diretório centraliza todos os arquivos binários, diagramas vetoriais e ativos de mídia utilizados em todas as notas de estudo de engenharia.

## 🛠 Diretrizes para Colaboradores 

Para garantir o desempenho do repositório e a compatibilidade entre plataformas (Obsidian/GitHub), siga estes padrões:

### 1. Formatos de Arquivo Preferenciais:

- **Prioridade 1: `.svg` (Gráficos Vetoriais):** Prioridade absoluta para diagramas técnicos, sistemas de coordenadas e formas geométricas geradas via Inkscape ou Excalidraw. Resolução infinita com tamanho de arquivo minimalista.
    
- **Prioridade 2: `.webp` (Raster Comprimido):** Utilize para figuras realistas, capturas de tela complexas de livros didáticos ou texturas visuais onde a vetorização é inviável. Excelente taxa de compressão com alta qualidade visual.
    
- **Alternativa (Fallback): `.jpg / .jpeg`:** Utilize apenas para fotos de alto contraste de livros didáticos físicos ou esboços feitos à mão no papel.
    
- **Evite: `.png`:** Não utilize, a menos que a transparência de canal alfa seja estritamente necessária e o ativo não possa ser renderizado em `.svg`.
### 2. Convenção de Nomenclatura:

Utilize uma abordagem híbrida para distinguir entre conteúdo e ativos, garantindo compatibilidade com o GitHub e sistemas baseados em Unix:

- **Notas e Pastas (snake_case):** Mantenha para consistência com os logs acadêmicos existentes. Exemplo: `fis1_estatica_notas.md`
    
- **Imagens e Ativos (kebab-case):** Padrão para ativos web e fácil distinção visual no terminal. Exemplo: `fis1-estatica-hibbeler-f2-1.svg` ou `calc1-integracao-por-partes.webp`

  
 > [!TIP]
 > 
 > **Dica:** Esta distinção ajuda a identificar tipos de arquivo rapidamente no terminal e evita conflitos com convenções de nomenclatura de variáveis em Python/C.
### 3. Fluxo de Trabalho e Links:

Salve a imagem vetorial otimizada ou comprimida diretamente nesta pasta `/assets`
Vincule-a no seu arquivo Markdown usando caminhos relativos para máxima compatibilidade:
`![Breve Descrição](../assets/nome-do-arquivo.svg)`