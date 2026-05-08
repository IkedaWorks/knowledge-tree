
# 🌳 Boas Práticas de Commit 

Este guia define o padrão de mensagens de commit para manter o histórico do **Project Yggdrasil** profissional, legível e preparado para automações futuras.

## 🏗️ Estrutura da Mensagem
`tipo(escopo): descrição curta em inglês`

---

## 🏷️ Tipos Principais 

| Tipo         | Descrição                                                             | Exemplo                                  |
| :----------- | :-------------------------------------------------------------------- | :--------------------------------------- |
| **docs**     | Alterações em documentação, notas de estudo ou READMEs.               | `docs(git): add commit guidelines`       |
| **feat**     | Adição de novo conteúdo ou funcionalidade (Scripts, novas matérias).  | `feat(circuits): add Kirchhoff's laws`   |
| **refactor** | Reorganização de pastas ou arquivos sem mudar o conteúdo técnico.     | `refactor(physics): move statics assets` |
| **fix**      | Correção de erros em fórmulas LaTeX, links ou bugs em scripts.        | `fix(latex): correct Maxwell equation`   |
| **style**    | Formatação e ajustes visuais (Markdown, espaços) sem mudar o sentido. | `style(md): fix indentation in intro`    |
| **chore**    | Manutenções de rotina (atualizar .gitignore, licenças).               | `chore: update license year`             |

## 💡 Regras de Ouro

1. **Use o Inglês:** Como o Git é uma ferramenta global e os tipos são em inglês, a descrição também deve ser (ex: *add*, *fix*, *update*).
2. **Seja Breve:** A primeira linha do commit deve ter no máximo 50 caracteres.
3. **Foco no Escopo:** Sempre que possível, use os parênteses para dizer a qual matéria ou ferramenta o commit se refere.

## 🚀 Por que usar isso?

1. **Histórico Profissional:** Demonstra domínio de ferramentas de mercado para recrutadores.
2. **Busca Facilitada:** Permite filtrar mudanças rapidamente via terminal com `git log --grep`.
3. **Automação:** Facilita a criação de scripts Python (Fase 2 do Roadmap) para gerar relatórios de progresso.