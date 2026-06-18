# 🌳 Diretrizes de Commit (Conventional Commits)

Este documento define o padrão de mensagens de commit para manter o histórico do **Project Yggdrasil** profissional, legível e preparado para futuras automações.

## 🏗️ Anatomia de um Commit

Sintaxe: tipo(escopo): descrição curta

### 📋 Regras de Especificação

* **Idioma:** Use inglês. Como as ferramentas de Git e os tipos padrão são globais, as descrições devem acompanhar esse padrão (ex: `add`, `fix`, `update`).
* **Verbo no Imperativo:** Use o verbo no tempo imperativo e no presente (ex: `add` em vez de `added`).
* **Limite de Caracteres:** A primeira linha deve ter no máximo **50 caracteres**.
* **Foco no Escopo:** Sempre que possível, use parênteses para especificar a matéria ou ferramenta a que o commit se refere.

---

## 🏷️ Tipos Principais

| Tipo | Descrição | Exemplo |
| :--- | :--- | :--- |
| **`docs`** | 📚 Alterações em documentação, notas de estudo ou READMEs. | `docs(git): add commit guidelines` |
| **`feat`** | 🚀 Adição de novos conteúdos ou recursos funcionais (Scripts, matérias). | `feat(circuits): add Kirchhoff's laws` |
| **`refactor`**| 🔄 Reorganização de pastas ou arquivos sem alterar o sentido do conteúdo. | `refactor(physics): move statics assets` |
| **`fix`** | 🛠️ Correção de erros em fórmulas LaTeX, links quebrados ou bugs de script. | `fix(latex): correct Maxwell equation` |
| **`style`** | 🎨 Formatação e ajustes visuais (Markdown, espaçamento) sem alterar o sentido. | `style(md): fix indentation in intro` |
| **`chore`** | ⚙️ Manutenção de rotina (atualização de `.gitignore`, licenças ou metadados).| `chore: update license year` |

---

## ⚙️ Referência de Escopos

Sempre use um escopo preciso para isolar o impacto das alterações:
* **Matérias Principais:** `physics`, `calculus`, `circuits`, `electromagnetism`
* **Subtópicos e Ferramentas:** `statics`, `latex`, `git`, `python`

---

## 🚀 Por que usar isso?

1. **Histórico Profissional:** Demonstra domínio de fluxos de trabalho do padrão da indústria para recrutadores e colaboradores.
2. **Busca Facilitada:** Permite filtragem rápida na linha de comando via terminal usando git log --grep.
3. **Automação (Fase 2):** Facilita a execução de scripts em Python para varrer o histórico e gerar relatórios automatizados de progresso de estudo.