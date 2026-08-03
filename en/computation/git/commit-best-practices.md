# Git Commit Guidelines (Conventional Commits)

This document defines the commit message standard to maintain the history of **Project Yggdrasil** professional, legible, and prepared for future automations.

## Anatomy of a Commit

Syntax: type(scope): short description

### Specification Rules
* **Language:** Use English. Since Git tools and types are global, descriptions must follow (e.g., `add`, `fix`, `update`).
* **Imperative Mood:** Use the imperative, present tense (e.g., `add` instead of `added`).
* **Length Limit:** The first line must have a maximum of **50 characters**.
* **Scope Focus:** Whenever possible, use parentheses to specify the subject or tool the commit refers to.

---

## Main Types

| Type           | Description                                                                        | Example                                  |
| :------------- | :--------------------------------------------------------------------------------- | :--------------------------------------- |
| **`docs`**     | Documentation changes, study notes, or READMEs.                                    | `docs(git): add commit guidelines`       |
| **`feat`**     | Addition of new content or functional features (Scripts, subjects).                | `feat(circuits): add Kirchhoff's laws`   |
| **`refactor`** | Reorganizing folders or files without changing content meaning.                    | `refactor(physics): move statics assets` |
| **`fix`**      | Correcting errors in LaTeX formulas, broken links, or script bugs.                 | `fix(latex): correct Maxwell equation`   |
| **`style`**    |  Formatting and visual adjustments (Markdown, spacing) without changing meaning. | `style(md): fix indentation in intro`    |
| **`chore`**    | Routine maintenance (updating `.gitignore`, licenses, or metadata).                | `chore: update license year`             |

---

##  Scopes Reference

Always use a precise scope to isolate the impact of the changes:
* **Core Subjects:** `physics`, `calculus`, `circuits`, `electromagnetism`
* **Sub-topics & Tools:** `statics`, `latex`, `git`, `python`

---

##  Why use this?

1. **Professional History:** Demonstrates mastery of industry-standard workflows to recruiters and collaborators.
2. **Easy Search:** Allows quick command-line filtering via terminal using git log --grep.
3. **Automation (Phase 2):** Facilitates the execution of Python scripts to parse history and generate automated progress reports.