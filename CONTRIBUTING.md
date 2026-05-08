
# 🌿 Contributing to Project Yggdrasil

Thank you for helping this tree grow! To maintain the bilingual structure and technical rigor, please follow these guidelines.

## 🏛️ Collaboration Workflow

We use the **Fork & Pull Request** model to keep the "main tree" stable.

- **Fork**: Create a copy of this repository in your GitHub account.
    
- **Clone**: Download your fork to your machine via terminal.
    
- **Branch**: Always create a new branch for your work: `git checkout -b feat/your-feature`.
    
- **Sync**: A Fork is a snapshot. It doesn't update automatically. Use `git fetch upstream` to keep your fork aligned with the original tree.
    

## 🛠️ Setup & Environment

- **Obsidian (Highly Recommended)**: This project is built as an **Obsidian Vault**. Obsidian is a powerful knowledge management tool that allows you to visualize the connections between notes (the "Graph View") and renders LaTeX formulas and Markdown links natively. While you can use any editor, Obsidian is essential for the full experience.
    

## 📐 Standards

- **Bilingualism**: Every new note should ideally have a mirrored version in both `/en` and `/pt` folders.
    
- **LaTeX (MathJax)**: Use standard syntax (e.g., `\begin{aligned}`) and avoid Obsidian-only shorthands to ensure GitHub rendering.
    
- **Markdown**: Use standard links `[Text](./path.md)` instead of Wikilinks, as GitHub is more restrictive.
    
- **Git CLI**: We value the terminal. Use clear messages following **Conventional Commits**.
    [check our commit guidelines here](./en/computation/git/commit_best_practices.md)

## 🖼️ Media & Assets Management

- **No Video Support**: GitHub does not support native video rendering in the repository structure. Do not upload video files.
    
- **Assets Folder**: All images must be placed inside the `/assets` folder.
    
- **Image Protocol**: Before linking an image to a note, check the **[assets/README.md](./assets/README.md)** for specific instructions on file naming conventions and compression.

> **Diagrams (Excalidraw):** We maintain a "Source vs. Export" policy for diagrams.

- **Source (.md):** Keep the original Excalidraw Markdown file in `assets/excalidraw/` to allow future edits.
    
- **Export (.png/.webp):** Always export a visual version to the `assets/` root for GitHub compatibility.
    
- **Tooling:** You can edit these files using the Excalidraw plugin in Obsidian or by dragging the `.md` file into [excalidraw.com](https://excalidraw.com).

## ⚖️ License & Ethical Conduct

This project is licensed under the **[MIT License](./LICENSE.md)**. By contributing to Project Yggdrasil, you agree to abide by our ethical standards.

### 🛡️ Ethical Usage & Image Rights

The following restrictions apply to all users and contributors:

- **Image Protection**: The use of authors' or contributors' names, handles, or profile images to promote commercial products or services is strictly prohibited.
    
- **No Hate Speech**: Associating this project with hate speech, discrimination, or extremist ideologies will result in immediate removal and blocking from the repository.
    

---

# 🌿 Contribuindo para o Projeto Yggdrasil

Antes de tudo, obrigado por ajudar esta árvore a crescer! Para manter a estrutura bilíngue e o rigor técnico, siga estas diretrizes.

## 🏛️ Fluxo de Colaboração

Utilizamos o modelo de **Fork & Pull Request** para manter a "árvore mestre" estável.

- **Fork**: Crie uma cópia deste repositório na sua conta do GitHub.
    
- **Clone**: Baixe o seu fork para sua máquina via terminal.
    
- **Branch**: Sempre crie uma branch nova para seu trabalho: `git checkout -b feat/sua-contribuicao`.
    
- **Sync (Sincronização)**: Um Fork é uma "foto" no tempo. Ele não atualiza sozinho. Use `git fetch upstream` para manter seu fork alinhado com a árvore original.
    

## 🛠️ Setup e Ferramentas

- **Obsidian (Altamente Recomendado)**: Este projeto é construído como um **Obsidian Vault**. O Obsidian é uma ferramenta de gestão de conhecimento que permite visualizar as conexões entre as notas (o "Graph View") e renderiza fórmulas LaTeX e links Markdown nativamente. Embora você possa usar qualquer editor, o Obsidian é essencial para a experiência completa.
    

## 📐 Padrões

- **Bilinguismo**: Toda nota nova deve idealmente ter uma versão espelhada nas pastas `/en` e `/pt`.
    
- **LaTeX (MathJax)**: Use a sintaxe padrão (ex: `\begin{aligned}`) e evite atalhos exclusivos do Obsidian para garantir a renderização no GitHub.
    
- **Markdown**: Use links padrão `[Texto](./caminho.md)` em vez de Wikilinks, pois o GitHub é mais restritivo.
    
- **Git CLI**: Valorizamos o uso do terminal. Use mensagens claras seguindo o padrão **Conventional Commits**.
    [Cofira nossa Diretrizes de Commit aqui](./pt/computacao/git/boas_praticas_commit.md)

## 🖼️ Gestão de Mídias e Assets

- **Sem Suporte a Vídeo**: O GitHub não suporta renderização nativa de vídeo na estrutura do repositório. Não faça upload de arquivos de vídeo.
    
- **Pasta de Assets**: Todas as imagens devem ser obrigatoriamente colocadas dentro da pasta `/assets`.
    
- **Protocolo de Imagem**: Antes de linkar uma imagem em uma nota, verifique o **[assets/README.md](./assets/README.md)** para instruções específicas sobre nomenclatura e compressão.

> **Diagramas (Excalidraw):** Mantemos uma política de "Fonte vs. Exportação".

- **Fonte (.md):** Mantenha o arquivo original do Excalidraw em `assets/excalidraw/` para permitir edições futuras.
    
- **Exportação (.png/.webp):** Sempre exporte uma versão visual para a raiz de `assets/` para garantir a visualização no GitHub.
    
- **Ferramental:** Você pode editar estes arquivos usando o plugin Excalidraw no Obsidian ou arrastando o arquivo `.md` para o site [excalidraw.com](https://excalidraw.com).
    

## ⚖️ Licença e Conduta Ética

Este projeto é licenciado sob a licença **[MIT License](./LICENSE.md)**. Ao contribuir para o Projeto Yggdrasil, você concorda em cumprir nossos padrões éticos.

### 🛡️ Ética e Direitos de Imagem

As seguintes restrições se aplicam a todos os usuários e colaboradores:

- **Proteção de Imagem**: É estritamente proibido o uso de nomes, handles ou imagens dos autores e colaboradores para promover produtos ou serviços comerciais.
    
- **Sem Discurso de Ódio**: Associar este projeto a discursos de ódio, discriminação ou ideologias extremistas resultará em remoção imediata e banimento do repositório.