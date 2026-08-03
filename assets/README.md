# Assets & Media Management

This directory centralizes binary files, vector diagrams, and media assets used throughout the project's knowledge base.

## Guidelines for Contributors

To maintain repository performance and compatibility between Obsidian and GitHub, follow these standards.

## File Formats

Preferred formats:

- **SVG:** Default format for technical diagrams, mathematical illustrations, coordinate systems, and geometric shapes created with Inkscape or Excalidraw.
- **WEBP:** Preferred format for compressed raster images, screenshots, and visual references where vectorization is not practical.
- **JPG/JPEG:** Use only for photographs or scanned physical materials when necessary.
- **PNG:** Avoid unless transparency is required and SVG or WEBP are not suitable.

## Asset Organization

All shared media files must be stored inside:

```
/assets
```

Editable Excalidraw files should be stored in:

```
/assets/excalidraw
```

## Technical Diagrams

The project prioritizes editable and lightweight graphics.

- Use **Inkscape** for professional technical diagrams.
- Commit diagrams in native **SVG** format whenever possible.
- Use **Excalidraw** for conceptual sketches.
- Export an SVG version for GitHub rendering.

Avoid raster formats when a vector solution is available.

## Naming Convention

All assets should follow **kebab-case**.

Examples:

```
free-body-diagram.svg
gauss-law-example.webp
electric-field-lines.svg
```

## Linking Assets

Use relative Markdown paths when referencing assets:

```md
![Brief Description](../assets/file-name.svg)
```

---

# Gestão de Ativos e Mídias

Este diretório centraliza arquivos binários, diagramas vetoriais e arquivos de mídia utilizados ao longo da base de conhecimento do projeto.

## Diretrizes para Colaboradores

Para manter o desempenho do repositório e a compatibilidade entre Obsidian e GitHub, siga estes padrões.

## Formatos de Arquivo

Formatos preferenciais:

- **SVG:** Formato padrão para diagramas técnicos, ilustrações matemáticas, sistemas de coordenadas e formas geométricas criadas com Inkscape ou Excalidraw.
- **WEBP:** Formato preferencial para imagens rasterizadas comprimidas, capturas de tela e referências visuais onde a vetorização não é viável.
- **JPG/JPEG:** Utilize apenas para fotografias ou materiais físicos digitalizados quando necessário.
- **PNG:** Evite, a menos que transparência seja necessária e SVG ou WEBP não sejam adequados.

## Organização dos Assets

Todos os arquivos de mídia compartilhados devem ser armazenados em:

```
/assets
```

Arquivos editáveis do Excalidraw devem ser armazenados em:

```
/assets/excalidraw
```

## Diagramas Técnicos

O projeto prioriza gráficos editáveis e leves.

- Utilize **Inkscape** para diagramas técnicos profissionais.
- Faça commit dos diagramas no formato nativo **SVG** sempre que possível.
- Utilize **Excalidraw** para esboços conceituais.
- Exporte uma versão SVG para renderização no GitHub.

Evite formatos rasterizados quando uma solução vetorial estiver disponível.

## Convenção de Nomenclatura

Todos os assets devem seguir **kebab-case**.

Exemplos:

```
diagrama-corpo-livre.svg
lei-de-gauss-exemplo.webp
linhas-campo-eletrico.svg
```

## Vinculando Assets

Utilize caminhos relativos em Markdown ao referenciar assets:

```md
![Breve Descrição](../assets/nome-do-arquivo.svg)
```