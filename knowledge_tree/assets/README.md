
# 📷 Assets & Media Management

This directory centralizes all binary files, diagrams, and media assets used across the engineering study notes.

## 🛠 Guidelines for Contributors 

To ensure repository performance and cross-platform compatibility (Obsidian/GitHub), please follow these standards:

### 1. Preferred File Formats
* **Priority:** `.webp` - Excellent compression ratio with high visual quality.
* **Fallback:** `.jpg` / `.jpeg` - Use for high-contrast photos of textbooks or handwritten sketches.
* **Avoid:** `.png` - Unless transparency is strictly required, as file sizes tend to be unnecessarily large for static diagrams.

### 2. Naming Convention
Use **snake_case** with descriptive prefixes to keep files searchable and prevent broken links in Unix-based systems:
* `phys1_statics_hibbeler_f2_1.webp`
* `calc1_integration_by_parts.webp`

### 3. Workflow & Linking
1. Save the optimized image directly into this `/assets` folder.
2. Link it in your Markdown file using **relative paths** for maximum compatibility:
   `![Brief Description](../assets/file_name.webp)`

---
**Maintained under the First Principles learning framework.**