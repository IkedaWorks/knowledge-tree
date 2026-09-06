# 🌳 Contributing to Project Yggdrasil

Thank you for helping this tree grow! To maintain the bilingual structure and technical rigor of the project, please follow these guidelines.

## Collaboration Workflow

We use the **Fork & Pull Request** model to keep the main tree stable.

- **Fork:** Create a copy of this repository in your GitHub account.
- **Clone:** Download your fork to your local machine.
- **Branch:** Always create a dedicated branch for your work: `git checkout -b feat/your-feature`.
- **Commit:** Use clear commit messages following the **Conventional Commits** specification.
- **Sync:** Keep your fork up to date with `git fetch upstream` before opening a Pull Request.

For commit conventions, see:
[Commit Best Practices](_docs/commit-best-practices.md)

## Setup & Environment

- **Obsidian (Highly Recommended):** This repository is built as an **Obsidian Vault**. Obsidian provides native support for Markdown, MathJax, backlinks, and Graph View. Although any Markdown editor can be used, Obsidian offers the intended editing experience.
- **Git CLI:** We recommend using Git from the command line whenever possible.

## Repository Structure

The repository follows a bilingual structure:

- `/en` — English notes.
- `/pt` — Portuguese notes.
- `/assets` — Shared media files and technical diagrams.

Whenever possible, new notes should have equivalent versions in both `/en` and `/pt`.

## Front Matter

Every Markdown note should begin with a front matter block.

Required fields:

```yaml
---
title:
id:
---
```

- **title:** Human-readable document title.
- **id:** Canonical document identifier.

## Naming Convention

Use **kebab-case** throughout the repository.

Examples:

```
free-body-diagram.md
gauss-law.md
electric-field.svg
```

Apply the same convention to folders whenever possible.

## Markdown & LaTeX

- Use standard Markdown links (`[Text](./path.md)`) instead of Wikilinks to maximize GitHub compatibility.
- Use standard MathJax syntax (e.g. `\begin{aligned}`) and avoid Obsidian-exclusive shorthands whenever possible.

## Media & Assets

- GitHub does not support native video rendering inside repositories. Do not upload video files.
- Store all shared images and diagrams inside `/assets`.
- Before adding media, read **[assets/README.md](./assets/README.md)** for file format, optimization and organization guidelines.

## Technical Diagrams

We prioritize editable vector graphics and lightweight documentation.

- **Professional Diagrams (Inkscape):** Prefer SVG for engineering, mathematics and physics diagrams. Always commit the editable `.svg` file.
- **Conceptual Sketches (Excalidraw):** Keep editable files inside `assets/excalidraw/` and export an `.svg` copy into `/assets` for GitHub rendering.
- Avoid raster formats unless vector graphics are not feasible.

## License & Ethical Conduct

This project is licensed under the [MIT License](./LICENSE.md). By contributing to Project Yggdrasil, you agree to follow these community standards.

### Ethical Usage & Image Rights

- **Image & Name Protection:** Authors and contributors may be cited for academic attribution and open-source credit. Using names, usernames or profile images for advertising, commercial promotion or to imply endorsement of third-party products or services is strictly prohibited.
- **Inclusive Environment:** This repository is an educational space. Hate speech, discrimination, harassment or extremist content are incompatible with this project and may result in removal of contributions and permanent exclusion.

---

# 🌳 Contribuindo para o Projeto Yggdrasil

Obrigado por ajudar esta árvore a crescer! Para manter a estrutura bilíngue e o rigor técnico do projeto, siga estas diretrizes.

## Fluxo de Colaboração

Utilizamos o modelo **Fork & Pull Request** para manter a árvore principal estável.

- **Fork:** Crie uma cópia deste repositório na sua conta do GitHub.
- **Clone:** Baixe o seu fork para sua máquina.
- **Branch:** Sempre crie uma branch dedicada para o seu trabalho: `git checkout -b feat/sua-contribuicao`.
- **Commit:** Utilize mensagens claras seguindo o padrão **Conventional Commits**.
- **Sync:** Mantenha seu fork sincronizado com `git fetch upstream` antes de abrir um Pull Request.

Para as convenções de commit, consulte:
[Boas Práticas de Commit](_docs/boas-praticas-commit.md)

## Ambiente e Ferramentas

- **Obsidian (Altamente Recomendado):** Este repositório é construído como um **Obsidian Vault**. O Obsidian oferece suporte nativo a Markdown, MathJax, backlinks e Graph View. Embora qualquer editor Markdown funcione, o Obsidian proporciona a experiência de edição pretendida.
- **Git CLI:** Recomendamos utilizar o Git pela linha de comando sempre que possível.

## Estrutura do Repositório

O repositório segue uma estrutura bilíngue:

- `/en` — Conteúdo em inglês.
- `/pt` — Conteúdo em português.
- `/assets` — Arquivos de mídia e diagramas compartilhados.

Sempre que possível, novas notas devem possuir versões equivalentes em `/en` e `/pt`.

## Front Matter

Toda nota Markdown deve iniciar com um bloco de front matter.

Campos obrigatórios:

```yaml
---
title:
id:
---
```

- **title:** Título legível do documento.
- **id:** Identificador canônico do documento.
## Convenção de Nomenclatura

Utilize **kebab-case** em todo o repositório.

Exemplos:

```
diagrama-de-corpo-livre.md
lei-de-gauss.md
campo-eletrico.svg
```

Sempre que possível, utilize a mesma convenção para as pastas.

## Markdown e LaTeX

- Utilize links Markdown padrão (`[Texto](./caminho.md)`) em vez de Wikilinks para garantir compatibilidade com o GitHub.
- Utilize a sintaxe padrão do MathJax (ex.: `\begin{aligned}`) e evite recursos exclusivos do Obsidian sempre que possível.

## Mídias e Assets

- O GitHub não suporta renderização nativa de vídeos dentro do repositório. Não envie arquivos de vídeo.
- Armazene todas as imagens e diagramas compartilhados na pasta `/assets`.
- Antes de adicionar qualquer mídia, leia **[assets/README.md](./assets/README.md)** para conhecer as diretrizes de formatos, otimização e organização.

## Diagramas Técnicos

Priorizamos gráficos vetoriais editáveis e documentação leve.

- **Diagramas Profissionais (Inkscape):** Prefira SVG para diagramas de engenharia, matemática e física. Sempre faça commit do arquivo `.svg` editável.
- **Esboços Conceituais (Excalidraw):** Mantenha os arquivos editáveis em `assets/excalidraw/` e exporte uma cópia em `.svg` para `/assets` destinada à visualização no GitHub.
- Evite formatos rasterizados sempre que gráficos vetoriais forem viáveis.

## Licença e Conduta Ética

Este projeto é licenciado sob a [Licença MIT](./LICENSE.md). Ao contribuir para o Projeto Yggdrasil, você concorda em seguir estas diretrizes da comunidade.

### Uso Ético e Direitos de Imagem

- **Proteção de Imagem e Nome:** A citação de autores e colaboradores é permitida e incentivada para fins de atribuição acadêmica e créditos em projetos open source. É estritamente proibido utilizar nomes, usuários ou imagens de perfil para publicidade, promoção comercial ou para sugerir o endosso de produtos e serviços de terceiros.
- **Ambiente Inclusivo:** Este repositório é um espaço educacional. Discursos de ódio, discriminação, assédio ou ideologias extremistas são incompatíveis com este projeto e poderão resultar na remoção das contribuições e no banimento permanente do colaborador.