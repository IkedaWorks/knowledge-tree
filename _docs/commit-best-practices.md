# Commit Guidelines (Conventional Commits)

This document defines the commit message standards to keep the repository history professional, readable, and auditable.

## Commit Anatomy
`type(scope): short description`

---

## Rules
* **Language:** English (e.g., `add`, `fix`, `update`, `remove`).
* **Verb:** Imperative present tense (e.g., `add` instead of `added`).
* **Limit:** Maximum 50 characters for the first line.
* **Scope:** Mandatory when changes impact a specific domain or module.

---

## Commit Types

| Type | When to Use | Practical Example |
| :--- | :--- | :--- |
| **`feat`** | Addition of **new academic content** (lessons, modules, study notes, exercises). | `feat(digital-electronics): add BCD code theory` |
| **`docs`** | Changes to **project governance and instructions** (`CONTRIBUTING.md`, guidelines, manuals). | `docs(governance): update commit guidelines` |
| **`refactor`** | Renaming, reorganizing, or restructuring files/folders without altering academic content. | `refactor(computation): rename theory files to kebab-case` |
| **`fix`** | Corrections to content errors (incorrect LaTeX formulas, broken links, typos). | `fix(chemistry): correct stoichiometry molar mass formula` |
| **`style`** | Formatting adjustments (Markdown tables, line breaks, whitespace) without altering text semantics. | `style(digital-electronics): align index tables` |
| **`chore`** | Infrastructure maintenance and cleanup (deleting unused files, `.gitignore`, license updates). | `chore(computation): remove empty networking module` |

---

## Scope Mapping

* **Academic Domains/Modules:** `computation`, `digital-electronics`, `chemistry`, `basic-chemistry`
* **Governance/Infrastructure:** `governance`, `repo`, `git`