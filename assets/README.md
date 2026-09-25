# Assets & Media Management

This directory centralizes binary files, vector diagrams, and media assets used throughout the project's knowledge base.

## Guidelines for Contributors

To maintain repository performance and compatibility between Obsidian and GitHub, follow these standards.

## File Formats

The repository strictly prioritizes modern and lightweight formats:

- **SVG:** Default format for technical diagrams, mathematical illustrations, coordinate systems, and plots generated via scripts or drawing tools.
    
- **WEBP:** Default format for compressed raster images, screenshots, and visual references where vectorization is not practical.
    
- **AVIF / PNG / JPG:** Fallback options used only when WEBP or SVG are not suitable or available.
    

## Asset Structure & Mapping

All shared media files are organized by **domain** and **module** following a 3-level depth structure:

$$\text{assets/} \rightarrow \text{<domain>/} \rightarrow \text{<module>/} \rightarrow \text{<filename>}$$

### Folder Flattening Rule

Internal content subfolders (such as `theory/`, `practice/`, `kinematics/`, `dynamics/`) **MUST NOT** be replicated inside `assets/`. All assets belonging to a module reside directly at the module root within `assets/<domain>/<module>/`.

Editable Excalidraw files are stored separately in `/assets/excalidraw/`.

## Technical Diagrams & Scripting

The project prioritizes reproducible, vector-based graphics.

- **Python (Matplotlib, Manim, SymPy):** Preferred method for precise scientific curves, function plots, and data visualizations.
    
- **Inkscape:** Preferred tool for advanced technical diagrams and illustrations.
    
- **Excalidraw:** Used for conceptual sketches and rapid diagrams. Export an SVG version for repository inclusion.
    

## Naming Convention

All filenames must strictly use **kebab-case** in **English**, ensuring clean and concise names.

Examples:

- vector-decomposition-2d.svg
    
- electric-flux-cube.svg
    
- analog-vs-digital.svg
    

## Linking Assets

Use standard Markdown syntax `![]()` with relative paths:

`![Vector Decomposition](../../../../../assets/physics/classical-mechanics/vector-decomposition-2d.svg)`

---
# Gestão de Ativos e Mídias

Este diretório centraliza arquivos binários, diagramas vetoriais e arquivos de mídia utilizados ao longo da base de conhecimento do projeto.

## Diretrizes para Colaboradores

Para manter o desempenho do repositório e a compatibilidade entre Obsidian e GitHub, siga estes padrões.

## Formatos de Arquivo

O repositório prioriza estritamente formatos modernos e leves:

- **SVG:** Formato padrão para diagramas técnicos, ilustrações matemáticas, sistemas de coordenadas e gráficos gerados por código ou ferramentas de desenho.
    
- **WEBP:** Formato padrão para imagens rasterizadas comprimidas, capturas de tela e referências visuais onde a vetorização não é viável.
    
- **AVIF / PNG / JPG:** Opções de suporte utilizadas apenas quando WEBP ou SVG não forem viáveis ou disponíveis.
    

## Estrutura e Mapeamento de Assets

Todos os arquivos de mídia são organizados por **domínio** e **módulo**, seguindo uma estrutura máxima de 3 níveis:

$$\text{assets/} \rightarrow \text{<domain>/} \rightarrow \text{<module>/} \rightarrow \text{<filename>}$$

### Regra de Achatamento de Subpastas

Subpastas internas de conteúdo (como `theory/`, `practice/`, `kinematics/`, `dynamics/`) **NÃO DEVEM** ser replicadas dentro de `assets/`. Todos os ativos de um módulo residem diretamente na raiz do módulo em `assets/<domain>/<module>/`.

Arquivos editáveis do Excalidraw são armazenados separadamente em `/assets/excalidraw/`.

## Diagramas Técnicos e Programação

O projeto prioriza gráficos reprodutíveis baseados em vetores.

- **Python (Matplotlib, Manim, SymPy):** Método preferencial para plotagem de funções, curvas científicas e visualização de dados com precisão.
    
- **Inkscape:** Ferramenta preferencial para diagramas técnicos e ilustrações avançadas.
    
- **Excalidraw:** Utilizado para esboços conceituais e diagramas rápidos. Exporte uma versão SVG para inclusão no repositório.
    

## Convenção de Nomenclatura

Todos os nomes de arquivo devem utilizar estritamente **kebab-case** em **inglês**, garantindo nomes limpos e diretos.

Exemplos:

- vector-decomposition-2d.svg
    
- electric-flux-cube.svg
    
- analog-vs-digital.svg
    

## Vinculando Assets

Utilize a sintaxe padrão do Markdown `![]()` com caminhos relativos:

`![Decomposição Vetorial](../../../../../assets/physics/classical-mechanics/vector-decomposition-2d.svg)`