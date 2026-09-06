# Diretrizes de Commit (Conventional Commits)

Este documento define o padrão de mensagens de commit para manter o histórico do repositório profissional, legível e auditável.

## Anatomia do Commit
`tipo(escopo): descrição curta`

---

## Regras

* **Idioma:** Inglês (ex: `add`, `fix`, `update`, `remove`).
* **Verbo:** Imperativo no presente (ex: `add` em vez de `added`).
* **Limite:** Máximo de 50 caracteres na primeira linha.
* **Escopo:** Obrigatório quando a mudança afeta um domínio ou módulo específico.

---

## Guia de Tipos (Sem Ambiguidade)

| Tipo | Quando usar | Exemplo Prático |
| :--- | :--- | :--- |
| **`feat`** | Adição de **novo conteúdo acadêmico** (aulas, módulos, notas de estudo, exercícios). | `feat(digital-electronics): add BCD code theory` |
| **`docs`** | Alterações em **governança e instruções do projeto** (`CONTRIBUTING.md`, diretrizes, manuais). | `docs(governance): update commit guidelines` |
| **`refactor`** | Renomear, reorganizar ou reestruturar arquivos e pastas sem alterar o conteúdo acadêmico. | `refactor(computation): rename theory files to kebab-case` |
| **`fix`** | Correção de erros no conteúdo (fórmulas LaTeX incorretas, links quebrados, digitação). | `fix(chemistry): correct stoichiometry molar mass formula` |
| **`style`** | Ajustes de formatação Markdown, tabelas ou espaçamentos sem alterar o texto em si. | `style(digital-electronics): align index tables` |
| **`chore`** | Manutenção de infraestrutura e limpeza (exclusão de arquivos mortos, `.gitignore`, licença). | `chore(computation): remove empty networking module` |

---

## Mapeamento de Escopos

* **Domínios/Módulos Acadêmicos:** `computation`, `digital-electronics`, `chemistry`, `basic-chemistry`
* **Governança/Infraestrutura:** `governance`, `repo`, `git`