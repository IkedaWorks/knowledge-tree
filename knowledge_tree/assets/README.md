
# 📷 Assets & Media Management

This directory centralizes all binary files, diagrams, and media assets used across the engineering study notes.

## 🛠 Guidelines for Contributors 

To ensure repository performance and cross-platform compatibility (Obsidian/GitHub), please follow these standards:

### 1. Preferred File Formats
* **Priority:** `.webp` - Excellent compression ratio with high visual quality.
* **Fallback:** `.jpg` / `.jpeg` - Use for high-contrast photos of textbooks or handwritten sketches.
* **Avoid:** `.png` - Unless transparency is strictly required, as file sizes tend to be unnecessarily large for static diagrams.

### 2. Naming Convention 

Use a hybrid approach to distinguish between content and assets, ensuring compatibility with GitHub and Unix-based systems:

- **Notes & Folders (`snake_case`):** Maintain for consistency with existing academic logs.
    
    - `phys1_statics_notes.md`
        
- **Images & Assets (`kebab-case`):** Standard for web assets and easy visual distinction.
    
    - `phys1-statics-hibbeler-f2-1.webp`
        
    - `calc1-integration-by-parts.webp`
        

> [!TIP] 
> 
> This distinction helps in identifying file types at a glance in the terminal and prevents conflicts with Python/C variable naming conventions.

### 3. Workflow & Linking
1. Save the optimized image directly into this `/assets` folder.
2. Link it in your Markdown file using **relative paths** for maximum compatibility:
   `![Brief Description](../assets/file_name.webp)`

---
