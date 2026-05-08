
# 🌳 Commit Best Practices (Conventional Commits)

This guide defines the commit message standard to maintain the history of **Project Yggdrasil** professional, legible, and prepared for future automations.

## 🏗️ Message Structure

`type(scope): short description`

---

## 🏷️ Main Types

|**Type**|**Description**|**Example**|
|---|---|---|
|**docs**|Documentation changes, study notes, or READMEs.|`docs(git): add commit guidelines`|
|**feat**|Addition of new content or functional features (Scripts, new subjects).|`feat(circuits): add Kirchhoff's laws`|
|**refactor**|Reorganizing folders or files without changing the technical content.|`refactor(physics): move statics assets`|
|**fix**|Correcting errors in LaTeX formulas, broken links, or script bugs.|`fix(latex): correct Maxwell equation`|
|**style**|Formatting and visual adjustments (Markdown, spacing) without changing meaning.|`style(md): fix indentation in intro`|
|**chore**|Routine maintenance (updating .gitignore, licenses, or metadata).|`chore: update license year`|

## 💡 Golden Rules

1. **Use English:** Since Git is a global tool and types are in English, descriptions should also be (e.g., _add_, _fix_, _update_).
    
2. **Be Brief:** The first line of the commit should have a maximum of 50 characters.
    
3. **Scope Focus:** Whenever possible, use parentheses to specify the subject or tool the commit refers to.
    

## 🚀 Why use this?

1. **Professional History:** Demonstrates mastery of industry-standard tools to recruiters.
    
2. **Easy Search:** Allows for quick filtering via terminal using `git log --grep`.
    
3. **Automation:** Facilitates the creation of Python scripts (Phase 2 of the Roadmap) to generate automated progress reports.