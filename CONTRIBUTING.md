
# 🌳 Contributing to Project Yggdrasil

Thank you for helping this tree grow! To maintain the bilingual structure and technical rigor, please follow these guidelines.

##  Collaboration Workflow

We use the **Fork & Pull Request** model to keep the "main tree" stable.

- **Fork**: Create a copy of this repository in your GitHub account.
    
- **Clone**: Download your fork to your machine via terminal.
    
- **Branch**: Always create a new branch for your work: `git checkout -b feat/your-feature`.
    
- **Sync**: A Fork is a snapshot. It doesn't update automatically. Use `git fetch upstream` to keep your fork aligned with the original tree.
    

##  Setup & Environment

- **Obsidian (Highly Recommended)**: This project is built as an **Obsidian Vault**. Obsidian is a powerful knowledge management tool that allows you to visualize the connections between notes (the "Graph View") and renders LaTeX formulas and Markdown links natively. While you can use any editor, Obsidian is essential for the full experience.
    

##  Standards

- **Bilingualism**: Every new note should ideally have a mirrored version in both `/en` and `/pt` folders.
    
- **LaTeX (MathJax)**: Use standard syntax (e.g., `\begin{aligned}`) and avoid Obsidian-only shorthands to ensure GitHub rendering.
    
- **Markdown**: Use standard links `[Text](./path.md)` instead of Wikilinks, as GitHub is more restrictive.
    
- **Git CLI**: We value the terminal. Use clear messages following **Conventional Commits**.
    [check our commit guidelines here](./en/computation/git/commit_best_practices.md)

##  Media & Assets Management

- **No Video Support**: GitHub does not support native video rendering in the repository structure. Do not upload video files.
    
- **Assets Folder**: All images must be placed inside the `/assets` folder.
    
- **Image Protocol**: Before linking an image to a note, check the **[assets/README.md](./assets/README.md)** for specific instructions on file naming conventions and compression.

##  Technical Diagrams & Vector Graphics
We follow an architecture that prioritizes vector clarity and lightweight documentation:

* **Professional Diagrams (Inkscape & SVG):** For complex physics, calculus, or electromagnetism diagrams, prefer using **Inkscape**. Always save and commit the diagram directly in native **.svg** format into the `assets/` folder. Do not convert to raster unless strictly necessary.
* **Handdrawn Sketches (Excalidraw):** Useful for quick, conceptual drafts. Keep the original editable file in `assets/excalidraw/` (as `.md` or export as `.excalidraw`) and export a high-resolution `.svg` (instead of `.png`) to the `assets/` root for GitHub preview rendering.

##  License & Ethical Conduct 

This project is licensed under the [MIT License](./LICENSE.md). By contributing to Project Yggdrasil, you agree to abide by our ethical standards. 

##  Ethical Usage & Image Rights 

The following restrictions apply to all users and contributors: 
 - Image & Name Protection: Citing the names and handles of authors and contributors is permitted and encouraged strictly for academic attribution and open-source crediting purposes. However, using profile images (photos, avatars), names, or handles for advertising, marketing, commercial promotion, or to falsely imply endorsement of third-party products and services is strictly prohibited. 
 - Inclusive Environment (No Hate Speech): This repository is a strictly educational space. Associating this project, its forks, or its contributors with hate speech, discrimination, harassment, or extremist ideologies will result in an immediate ban of the contributor and the permanent removal of their contributions.

---

#  Contribuindo para o Projeto Yggdrasil

Antes de tudo, obrigado por ajudar esta árvore a crescer! Para manter a estrutura bilíngue e o rigor técnico, siga estas diretrizes.

##  Fluxo de Colaboração

Utilizamos o modelo de **Fork & Pull Request** para manter a "árvore mestre" estável.

- **Fork**: Crie uma cópia deste repositório na sua conta do GitHub.
    
- **Clone**: Baixe o seu fork para sua máquina via terminal.
    
- **Branch**: Sempre crie uma branch nova para seu trabalho: `git checkout -b feat/sua-contribuicao`.
    
- **Sync (Sincronização)**: Um Fork é uma "foto" no tempo. Ele não atualiza sozinho. Use `git fetch upstream` para manter seu fork alinhado com a árvore original.
    

##  Setup e Ferramentas

- **Obsidian (Altamente Recomendado)**: Este projeto é construído como um **Obsidian Vault**. O Obsidian é uma ferramenta de gestão de conhecimento que permite visualizar as conexões entre as notas (o "Graph View") e renderiza fórmulas LaTeX e links Markdown nativamente. Embora você possa usar qualquer editor, o Obsidian é essencial para a experiência completa.
    

##  Padrões

- **Bilinguismo**: Toda nota nova deve idealmente ter uma versão espelhada nas pastas `/en` e `/pt`.
    
- **LaTeX (MathJax)**: Use a sintaxe padrão (ex: `\begin{aligned}`) e evite atalhos exclusivos do Obsidian para garantir a renderização no GitHub.
    
- **Markdown**: Use links padrão `[Texto](./caminho.md)` em vez de Wikilinks, pois o GitHub é mais restritivo.
    
- **Git CLI**: Valorizamos o uso do terminal. Use mensagens claras seguindo o padrão **Conventional Commits**.
    [Cofira nossa Diretrizes de Commit aqui](./pt/computacao/git/boas_praticas_commit.md)

##  Gestão de Mídias e Assets

- **Sem Suporte a Vídeo**: O GitHub não suporta renderização nativa de vídeo na estrutura do repositório. Não faça upload de arquivos de vídeo.
    
- **Pasta de Assets**: Todas as imagens devem ser obrigatoriamente colocadas dentro da pasta `/assets`.
    
- **Protocolo de Imagem**: Antes de linkar uma imagem em uma nota, verifique o **[assets/README.md](./assets/README.md)** para instruções específicas sobre nomenclatura e compressão.

###  Diagramas Técnicos (Excalidraw)

Mantemos uma arquitetura de **"Fonte vs. Exportação"** para garantir que a árvore seja editável e visível:

1. **Fonte (`.md`):** Mantenha o arquivo original do Excalidraw em `assets/excalidraw/`.
    
2. **Exportação (`.png` / `.webp`):** Sempre exporte uma versão visual para a raiz de `assets/` para compatibilidade com o GitHub.
    
3. **Ferramental:** Use o plugin Excalidraw no Obsidian ou edite via web em <a href="https://excalidraw.com" target="_blank" rel="noopener noreferrer">Excalidraw</a> e arrastar o arquivo `.md`  para dentro da tela.

##  Licença e Conduta Ética

 Este projeto é licenciado sob a licença [MIT](./LICENSE.md). Ao contribuir para o Projeto Yggdrasil, você concorda em cumprir nossos padrões éticos. 
 
##  Diretrizes Éticas e Direitos de Imagem

 As seguintes restrições aplicam-se a todos os usuários e colaboradores: 
 - Proteção de Imagem e Nome: A citação de nomes e handles dos autores e colaboradores é permitida e incentivada exclusivamente para fins de atribuição de créditos acadêmicos e open-source. No entanto, o uso de imagens de perfil (fotos, avatares), nomes ou handles para fins de publicidade, marketing, promoção comercial ou para sugerir falsamente o endosso de produtos e serviços de terceiros é estritamente proibido.
 - Ambiente Inclusivo (Sem Discurso de Ódio): Este repositório é um espaço estritamente educacional. Qualquer associação deste projeto, de seus forks ou de seus colaboradores com discursos de ódio, discriminação, assédio ou ideologias extremistas resultará no banimento imediato do colaborador e na remoção permanente de suas contribuições.