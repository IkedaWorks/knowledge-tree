# 🌳 Contributing to Project Yggdrasil

[English](#english) | [Português](#português)

## English

Thank you for helping this tree grow. This repository holds the educational content, UI components, and knowledge graph structures of Project Yggdrasil. The proprietary diagnostic engine lives in a separate private repository and is not covered here.

### 1. Ways to contribute

- Write a new document for an existing module.
    
- Translate a document, or review an existing translation.
    
- Fix errors in text, math, references or links.
    
- Add or improve figures.
    
- Report a problem or suggest a topic by opening an issue.
    

For anything larger than a single document (a new module, a new domain, a change to the structure), open an issue first so we can agree on the scope before you write.

### 2. Workflow

1. Fork the repository and clone your fork.
    
2. Add the original repository as upstream: git remote add upstream git@github.com:IkedaWorks/knowledge-tree.git
    
3. Create a branch from an up-to-date main: git checkout -b feat/your-contribution
    
4. Write commits in Conventional Commits form, with the domain as the scope when the change belongs to one. Types, scopes, and examples are in [_docs/commit-best-practices.md](./_docs/commit-best-practices.md).
    
5. Before opening the Pull Request, sync with the original repository: git fetch upstream && git rebase upstream/main
    
6. Open the Pull Request and go through the checklist. Keep it small: one document or one module per Pull Request.
    

### 3. Tools

Use whichever of these two fits the task. They are complementary.

- **Obsidian:** Best for reading the vault, following backlinks, and using Graph View. Open the repository root as a vault. It saves notes as `.md` and does not render `.mdx` unless you add a plugin. To keep front matter exactly as written, edit it as text, not through the Properties panel.

- **Cursor (or any code editor):** Best for writing, Git, YAML, and files that are not ordinary notes: `.mdx`, React in `src/components/`, and project config. It opens every file type in the repository as text.

### 4. Structure and file names

Paths ending in `/` are folders. Names with an extension are files. Angle brackets (`<...>`) are placeholders, not real names.

```text
📁 src/
│   📁 content/
│   │   📁 pt/                          ← Portuguese tree
│   │   📁 en/                          ← English tree (same layout as pt/)
│   │       📁 <domain>/
│   │           📄 README.md            ← domain index
│   │           📁 <module>/
│   │               📄 README.md        ← module index
│   │               📁 theory/          ← concept, method, proof, application
│   │               │   📄 <topic>.md
│   │               📁 practice/        ← assessment documents
│   │                   📄 <topic>-p1.md
│   📁 assets/                          ← figures and media (see that folder's README)
│   │   📁 <domain>/
│   │       📁 <module>/
│   │           📄 <figure-name>.svg
│   📁 components/                      ← interactive React components (code)
📁 _docs/                               ← project guides (not course content)
```

Language trees sit under `src/content/<lang>/`, where `<lang>` is an [ISO 639-1](https://en.wikipedia.org/wiki/ISO_639-1) code (`en`, `pt`, and any locale added later). Inside those trees, every folder and file name is **English-first**: the same English kebab-case path in every language. Do not translate folder or file names. The database and i18n tooling join translations by that shared path.

> **Note on module content:** Inside a module, content lives only in `theory/` and `practice/`. If a module is broad, split topics into separate documents inside `theory/`. Do not invent extra subfolders.

**File and folder names:**

- Always English kebab-case, regardless of the document's native language. `pt/<domain>/<module>/theory/<topic>.md` and `en/<domain>/<module>/theory/<topic>.md` share one path after the locale folder.
- Noun-centric: drop articles, prepositions, and stop words (`of`, `by`, `to`, `and`, `the`, `in`, `on`, `from`, `a`, `an`), unless removing them destroys the standard term.
- No numeric prefixes: `<module-name>/`, never `01-<module-name>/`.
- Proofs: `proof-<theorem-name>.md`.
- Assessments: `<document-id>-p<number>.md`.
    

### 5. Front matter

Every file starts with a YAML block between triple hyphens, as its very first lines. Use exactly the fields below, no more and no fewer.

#### Document (in `theory/` or `practice/`)

```yaml
id: "topic-name"
title: "Topic Title"
domain: "domain"
module: "module"
type: "concept"
schema_version: "2.0"
level: "intermediate"
language: "en"
prerequisites:
  - "prerequisite-id"
tags:
  - "tag-one"
  - "tag-two"
```

#### Module README

```yaml
id: "module"
title: "Module Title"
domain: "domain"
type: "module"
schema_version: "2.0"
level: "intermediate"
language: "en"
tags:
  - "tag-one"
  - "tag-two"
prerequisites: []
```

#### Domain README (no `domain`, `level`, or `prerequisites`)

```yaml
id: "domain"
title: "Domain Title"
type: "domain"
schema_version: "2.0"
language: "en"
tags:
  - "tag-one"
  - "tag-two"
```
    

**Rules:**

- **Quotes:** Every string value is in double quotes.
- **Empty list:** Write `[]`. Never leave a key blank.
- **English-first keys:** `id`, `domain`, `module`, `type`, `level`, `prerequisites`, and `tags` stay in English kebab-case in every locale. Two files that are the same document in different languages must use the **same** `id` (and the same values for those keys). That shared `id` is what the database and i18n tooling use to pair translations.
- **`title`:** Written in the document's native language. This is the field that is localized.
- **`language`:** The document's locale as an [ISO 639-1](https://en.wikipedia.org/wiki/ISO_639-1) two-letter code (`en`, `pt`, ...). It must match the `src/content/<lang>/` folder the file lives in.
- **`id`:** English kebab-case; unique for a given piece of content, reused only across its translations.
- **`type`:** One of `concept`, `method`, `proof`, `application`, `assessment`, `domain`, `module`. `application` and `assessment` are part of the knowledge-tree schema even if the repository does not yet contain files of those types. Use them when the content fits; do not substitute `concept` or `method`.

#### `application` vs `assessment`

- **`application`** (folder `theory/`): Expository theory. It presents case studies, engineering, and real-world systems: how an idea shows up in a working machine or process. The student reads to understand the practical use, not to be tested.
- **`assessment`** (folder `practice/`): Atomic exercises and practical problems. It holds statements, solution routes, and validation checkpoints. It measures mastery and produces telemetry (errors, time, and reasoning patterns) for the Neural Diagnostic Engine.
    

### 6. Document sections

Each document follows the project pedagogy: intuition, reasoning, formal theory, solved examples, real applications.

|**Kind**|**Headings**|
|---|---|
|`concept` (Exact Sciences)|Motivation and Context / Theoretical Formulation / Examples and Solved Problems / Applications and Advanced Connections|
|`concept` (Module Intro)|Purpose and Overview / Historical Context and Scientific Pioneers / Structural Pillars of the Module / Real-World Applications and Engineering Impact|
|`method`|Problem Statement and Conditions / Algorithmic Step-by-Step Procedure / Complete Solved Application / Common Pitfalls and Boundary Cases|
|`proof`|Statement and Hypotheses / Idea and Strategy / Formal Proof / Remarks and Boundary Cases|

### 7. Writing rules

- Open every document and section with the concrete problem or object.
    
- Write one idea per paragraph, define terms on first use, and explain formulas in prose.
    
- No exam tips and no phrases like "as mentioned above".
    
- Do not use the em dash (—) or en dash (–). Use commas, colons, or parentheses.
    
- LaTeX is plain MathJax: $...$ inline and
    
    $$...$$
    
    for display.
    
- Links must start with ./. No Wikilinks ([[...]]).
    

### 8. Figures and media

Formats, folder layout, naming, and how to link a figure from a document are in [src/assets/README.md](./src/assets/README.md). Put files in `src/assets/<domain>/<module>/`. Do not copy `theory/` or `practice/` into `assets/`.
    

### 9. Interactive content (MDX)

- Use .mdx only for documents with interactive React components from src/components/.
    
- The .mdx prose is educational content (CC BY-NC-SA 4.0). Components imported from src/components/ are code (MIT).
    

### 10. Use of AI

- Disclose AI usage in your Pull Request description.
    
- You are responsible for fact-checking, math validation, and reference verification.
    

### 11. Pull Request checklist

Copy this list into your Pull Request description:

- [ ] Front matter follows v2.0 schema with double-quoted strings.
    
- [ ] id is unique and matches the filename or folder name.
    
- [ ] File lives in theory/ or practice/.
    
- [ ] Symmetric pt and en versions exist.
    
- [ ] Section headings match the standard template.
    
- [ ] I read Section 13 and agree to the licensing terms.
    

### 12. Review process

A maintainer reviews every Pull Request for correctness, pedagogy, and graph consistency.

### 13. Licenses and your contribution

The legal text is in [LICENSE.md](./LICENSE.md). This section is the contributor agreement. By opening a Pull Request you agree to it.

**What applies where**

| Path | License |
| --- | --- |
| `src/content/` (Markdown/MDX, both `pt/` and `en/`) | CC BY-NC-SA 4.0 |
| `src/assets/` (figures and media) | CC BY-NC-SA 4.0 |
| `src/components/`, `src/layouts/`, root scripts | MIT |
| Anything else | MIT if it is code or configuration; CC BY-NC-SA 4.0 if it is prose |

The AI diagnostic engine, evaluation models, and student-state APIs are **not** in this repository and are **not** open source.

CC BY-NC-SA 4.0 means third parties may share and adapt the content with attribution, only for non-commercial use, and must keep the same license. MIT means the code may be used, modified, and sold, with the copyright notice preserved.

**By submitting a Pull Request you confirm that:**

1. You wrote the contribution, or you have explicit rights to submit it. Do not paste textbooks, paywalled papers, or media you do not own.
2. The contribution is licensed under the license of its path, as in the table above.
3. **Maintainer commercial grant:** You grant Fernando Ikeda / IkedaWorks a perpetual, worldwide, non-exclusive, royalty-free license to use, adapt, reproduce, and sublicense your contribution in commercial products and services (including the Yggdrasil diagnostic platform). This grant exists because CC BY-NC-SA 4.0 would otherwise block that use. You keep copyright and moral rights. Public reuse by everyone else stays under the path's license.
4. Third-party material you include is compatible with that path's license, and you name the source.

Original authors keep credit through Git history and attribution required by CC BY-NC-SA 4.0. Commercial use of the content by third parties needs authorization from the maintainer ([IkedaWorks](https://github.com/IkedaWorks)).
    

### 14. Names, images and conduct

- Contributors receive academic credit via Git history. Citing names for attribution is welcome.
- Do not use contributors' personal images, or their names or handles for advertising, commercial promotion, or product endorsement, without prior written consent.
- Hate speech, harassment, or extremism results in permanent exclusion. Report conduct issues to @IkedaWorks.
    

## Português

Obrigado por ajudar esta árvore a crescer. Este repositório guarda o conteúdo educacional e o grafo de conhecimento do Projeto Yggdrasil, em inglês e português. O motor de diagnóstico fica em outro repositório e não é tratado aqui.

### 1. Formas de contribuir

- Escrever um novo documento para um módulo existente.
    
- Traduzir um documento ou revisar uma tradução existente.
    
- Corrigir erros de texto, matemática, referências ou links.
    
- Adicionar ou melhorar figuras.
    
- Relatar um problema ou sugerir um tema abrindo uma issue.
    

Para qualquer mudança maior que um documento (um módulo novo, um domínio novo), abra uma issue primeiro para combinarmos o escopo.

### 2. Fluxo de trabalho

1. Faça um fork do repositório e clone o seu fork.
    
2. Adicione o repositório original como upstream: git remote add upstream git@github.com:IkedaWorks/knowledge-tree.git
    
3. Crie uma branch a partir de um main atualizado: git checkout -b feat/sua-contribuicao
    
4. Escreva os commits no padrão Conventional Commits, usando o domínio como escopo quando a mudança pertencer a um. Tipos, escopos e exemplos estão em [_docs/boas-praticas-commit.md](./_docs/boas-praticas-commit.md).
    
5. Antes de abrir o Pull Request, sincronize com o repositório original: git fetch upstream && git rebase upstream/main
    
6. Abra o Pull Request e percorra o checklist.
    

### 3. Ferramentas

Use a que servir melhor para a tarefa. As duas se complementam.

- **Obsidian:** Melhor para ler o vault, seguir backlinks e usar o Graph View. Abra a raiz do repositório como um Vault. Ele grava notas em `.md` e não renderiza `.mdx` sem um plugin. Para manter o front matter exatamente como está escrito, edite-o como texto, não pelo painel de Properties.

- **Cursor (ou outro editor de código):** Melhor para escrever, Git, YAML e arquivos que não são notas comuns: `.mdx`, React em `src/components/` e configuração do projeto. Abre qualquer tipo de arquivo do repositório como texto.

### 4. Estrutura e nomes de arquivo

Caminhos que terminam em `/` são pastas. Nomes com extensão são arquivos. Trechos entre `<...>` são placeholders, não nomes reais.

```text
📁 src/
│   📁 content/
│   │   📁 pt/                          ← árvore em português
│   │   📁 en/                          ← árvore em inglês (mesmo layout que pt/)
│   │       📁 <domain>/
│   │           📄 README.md            ← índice do domínio
│   │           📁 <module>/
│   │               📄 README.md        ← índice do módulo
│   │               📁 theory/          ← concept, method, proof, application
│   │               │   📄 <topic>.md
│   │               📁 practice/        ← documentos de avaliação
│   │                   📄 <topic>-p1.md
│   📁 assets/                          ← figuras e mídia (veja o README dessa pasta)
│   │   📁 <domain>/
│   │       📁 <module>/
│   │           📄 <figure-name>.svg
│   📁 components/                      ← componentes React interativos (código)
📁 _docs/                               ← guias do projeto (não é conteúdo de curso)
```

As árvores de idioma ficam em `src/content/<lang>/`, onde `<lang>` é um código [ISO 639-1](https://en.wikipedia.org/wiki/ISO_639-1) (`en`, `pt`, e qualquer locale adicionado depois). Dentro dessas árvores, todo nome de pasta e de arquivo é **English-first**: o mesmo caminho em kebab-case inglês em todos os idiomas. Não traduza nomes de pasta nem de arquivo. O banco de dados e as ferramentas de i18n ligam as traduções por esse caminho compartilhado.

> **Nota para conteúdo de módulos:** Dentro de um módulo, o conteúdo fica só em `theory/` e `practice/`. Se o módulo for amplo, separe os temas em documentos distintos dentro de `theory/`. Não invente subpastas extras.

**Nomes de arquivos e pastas:**

- Sempre kebab-case em inglês, independentemente da língua nativa do documento. `pt/<domain>/<module>/theory/<topic>.md` e `en/<domain>/<module>/theory/<topic>.md` compartilham o mesmo caminho depois da pasta de locale.
- Centrados em substantivos: elimine artigos e preposições (`de`, `com`, `para`, `of`, `to`).
- Sem prefixos numéricos: `<module-name>/`, nunca `01-<module-name>/`.
- Demonstrações: `proof-<theorem-name>.md`.
- Avaliações: `<document-id>-p<number>.md`.
    

### 5. Front matter

Todo arquivo começa com um bloco YAML entre três hifens.

#### Documento (em `theory/` ou `practice/`)

```yaml
id: "topic-name"
title: "Título do Tópico"
domain: "domain"
module: "module"
type: "concept"
schema_version: "2.0"
level: "intermediate"
language: "pt"
prerequisites:
  - "prerequisite-id"
tags:
  - "tag-one"
  - "tag-two"
```

#### README de Módulo

```yaml
id: "module"
title: "Título do Módulo"
domain: "domain"
type: "module"
schema_version: "2.0"
level: "intermediate"
language: "pt"
tags:
  - "tag-one"
  - "tag-two"
prerequisites: []
```

#### README de Domínio (sem `domain`, `level` nem `prerequisites`)

```yaml
id: "domain"
title: "Título do Domínio"
type: "domain"
schema_version: "2.0"
language: "pt"
tags:
  - "tag-one"
  - "tag-two"
```

**Regras:**

- **Aspas:** Todo valor string vai entre aspas duplas.
- **Lista vazia:** Escreva `[]`. Nunca deixe uma chave em branco.
- **Chaves English-first:** `id`, `domain`, `module`, `type`, `level`, `prerequisites` e `tags` ficam em kebab-case inglês em todos os locales. Dois arquivos que são o mesmo documento em línguas diferentes devem usar o **mesmo** `id` (e os mesmos valores nessas chaves). Esse `id` compartilhado é o que o banco de dados e as ferramentas de i18n usam para emparelhar traduções.
- **`title`:** Escrito na língua nativa do documento. Este é o campo localizado.
- **`language`:** O locale do documento como código de duas letras [ISO 639-1](https://en.wikipedia.org/wiki/ISO_639-1) (`en`, `pt`, ...). Deve coincidir com a pasta `src/content/<lang>/` em que o arquivo está.
- **`id`:** Kebab-case em inglês; único para um dado conteúdo, reutilizado só nas traduções dele.
- **`type`:** Um de `concept`, `method`, `proof`, `application`, `assessment`, `domain`, `module`. `application` e `assessment` fazem parte do schema da knowledge tree mesmo que o repositório ainda não tenha arquivos desses tipos. Use-os quando o conteúdo se encaixar; não substitua por `concept` ou `method`.

#### `application` vs `assessment`

- **`application`** (pasta `theory/`): Texto teórico expositivo. Apresenta estudos de caso, engenharia e sistemas do mundo real: como uma ideia aparece em uma máquina ou processo que funciona. O aluno lê para entender a aplicação prática, não para ser testado.
- **`assessment`** (pasta `practice/`): Exercícios e problemas práticos atômicos. Contém enunciados, rotas de resolução e *checkpoints* de validação. Avalia o domínio do aluno e gera telemetria (erros, tempo e padrão de raciocínio) para o Motor Neural de Diagnóstico.

### 6. Seções do documento

Cada documento segue a pedagogia do projeto: intuição, raciocínio, teoria formal, exemplos resolvidos e aplicações reais.

|**Tipo de documento**|**Títulos**|
|---|---|
|`concept` (Ciências Exatas)|Motivação e Contexto / Formulação Teórica / Exemplos e Problemas Resolvidos / Aplicações e Conexões Avançadas|
|`concept` (Introdução)|Propósito e Visão Geral / Contexto Histórico e Pioneiros Científicos / Pilares Estruturais do Módulo / Aplicações no Mundo Real e Impacto na Engenharia|
|`method`|Enunciado do Problema e Condições / Procedimento Algorítmico Passo a Passo / Aplicação Resolvida Completa / Armadilhas Comuns e Casos Limite|
|`proof`|Enunciado e Hipóteses / Ideia e Estratégia / Demonstração Formal / Observações e Casos Limite|

### 7. Regras de escrita

- Abra o documento sempre com o objeto ou problema concreto.
    
- Escreva uma ideia por parágrafo e defina cada termo no primeiro uso.
    
- Não use o travessão (—) nem a meia-risca (–). Use vírgula, dois-pontos ou parênteses.
    
- LaTeX é MathJax simples: $...$ em linha e
    
    $$...$$
    
    para equações destacadas.
    
- Links devem começar com ./. Sem Wikilinks ([[...]]).
    

### 8. Figuras e mídia

Formatos, layout das pastas, nomes e como ligar uma figura a partir de um documento estão em [src/assets/README.md](./src/assets/README.md). Coloque os arquivos em `src/assets/<domain>/<module>/`. Não copie `theory/` nem `practice/` para dentro de `assets/`.
    

### 9. Conteúdo interativo (MDX)

- Use .mdx apenas para documentos com componentes React de src/components/.
    
- O texto do .mdx é conteúdo educacional (CC BY-NC-SA 4.0). Os componentes em src/components/ são código (MIT).
    

### 10. Uso de IA

- Declare o uso de IA na descrição do Pull Request.
    
- Você é responsável por checar fatos, matemática e referências.
    

### 11. Checklist do Pull Request

- [ ] Front matter segue o schema v2.0 com aspas duplas.
    
- [ ] id é único e coincide com o nome do arquivo.
    
- [ ] O arquivo está em theory/ ou practice/.
    
- [ ] Versões pt e en existem e são simétricas.
    
- [ ] Li a Seção 13 e concordo com os termos de licenciamento.
    

### 12. Processo de revisão

Um mantenedor revisa todo PR para garantir correção técnica, clareza pedagógica e consistência no grafo.

### 13. Licenças e a sua contribuição

O texto legal está em [LICENSE.md](./LICENSE.md). Esta seção é o acordo de contribuição. Ao abrir um Pull Request, você concorda com ele.

**O que vale em cada caminho**

| Caminho | Licença |
| --- | --- |
| `src/content/` (Markdown/MDX, `pt/` e `en/`) | CC BY-NC-SA 4.0 |
| `src/assets/` (figuras e mídia) | CC BY-NC-SA 4.0 |
| `src/components/`, `src/layouts/` e scripts na raiz | MIT |
| Qualquer outro arquivo | MIT se for código ou configuração; CC BY-NC-SA 4.0 se for prosa |

O motor de diagnóstico, os modelos de avaliação e as APIs de estado do aluno **não** estão neste repositório e **não** são código aberto.

CC BY-NC-SA 4.0: terceiros podem compartilhar e adaptar o conteúdo com atribuição, só para uso não comercial, e devem manter a mesma licença. MIT: o código pode ser usado, modificado e vendido, desde que o aviso de copyright seja preservado.

**Ao enviar um Pull Request, você confirma que:**

1. Escreveu a contribuição, ou tem direitos explícitos para enviá-la. Não cole livros, artigos pagos ou mídia que você não possui.
2. A contribuição é licenciada pela licença do caminho, conforme a tabela.
3. **Licença comercial ao mantenedor:** Você concede a Fernando Ikeda / IkedaWorks uma licença perpétua, mundial, não exclusiva e gratuita para usar, adaptar, reproduzir e sublicenciar a sua contribuição em produtos e serviços comerciais (incluindo a plataforma de diagnóstico Yggdrasil). Essa concessão existe porque a CC BY-NC-SA 4.0 impediria esse uso. Você mantém o copyright e os direitos morais. O reúso público por qualquer outra pessoa continua sob a licença do caminho.
4. Material de terceiros que você incluir é compatível com a licença daquele caminho, e você indica a fonte.

Os autores originais recebem crédito pelo histórico do Git e pela atribuição exigida pela CC BY-NC-SA 4.0. Uso comercial do conteúdo por terceiros exige autorização do mantenedor ([IkedaWorks](https://github.com/IkedaWorks)).
    

### 14. Nomes, imagens e conduta

- Contribuidores são creditados no histórico do Git. Citar nomes para atribuição acadêmica é bem-vindo.
- Não use imagens pessoais de contribuidores, nem nomes ou handles para propaganda, promoção comercial ou endosso de produtos, sem consentimento prévio por escrito.
- Conteúdo discriminatório, de ódio ou de assédio leva ao banimento permanente. Denúncias podem ser feitas via issues de conduct ou para @IkedaWorks.