# Docs-as-Code Implementation: Migrating Complex Technical Content From LaTeX to Web-Ready Markdown

This case demonstrates the migration of a physics conference paper from LaTeX sources to web-optimized Markdown documentation using a Docs-as-Code approach. The original file was adapted via Pandoc for initial automated conversion and refined via thorough manual refactoring to ensure consistent rendering on web platforms, preserving complex formatting, mathematical equations, and visual assets.

## 🛠️ Tools & Technologies

* `LaTeX` `Overleaf`
* `Pandoc`
* `Markdown (GFM)` `YAML` `Inline HTML5` `MathJax`
* `VS Code` `Git` `GitHub` 


## 📁 Repository Structure

> **Quick Access:** Open [research-paper.md](./markdown-project/research-paper.md) to review the final web-ready Markdown document.

```text
📁 case-01-docs-as-code-latex-to-markdown/
│
├── 📁 latex-project/              # Original LaTeX source files
│   ├── 📁 images/                 # High-resolution figures for LaTeX
│   ├── main.tex                    # Primary LaTeX manuscript
│   └── style_in.sty                # Custom conference style template
│
├── 📁 markdown-project/           # Web-ready Markdown documentation
│   ├── 📁 images/                 # Visual assets linked in Markdown
│   └── research-paper.md           # Final Markdown document
│
├── research-paper.pdf              # Compiled PDF from LaTeX sources
└── README.md                       # Case overview
```

## 🔄 Workflow & Implementation Details

1. **Source Preparation & Compilation:** 
   - Authored and structured the technical paper in **Overleaf** using **LaTeX** and a custom conference template (`style_in.sty`).
   - Compiled `research-paper.pdf` to serve as a visual and structural benchmark for the migration.
2. **Automated Conversion:** Executed a **Pandoc** CLI conversion to transform `main.tex` into a raw GitHub-Flavored Markdown (GFM) draft, preserving core section headings and paragraph flow.
3. **Manual Refactoring & Web Adaptation:**
   - *Metadata & Front Matter:* Added a **YAML** front matter block (title, authors, abstract/tags) to align the file with Static Site Generator (SSG) standards.
   - *Visual Assets & Cross-References:* Replaced broken LaTeX figure blocks with standard Markdown image syntax, mapped relative paths to `./images/`, and restored in-text figure references.
   - *Mathematical Equations:* Reviewed and adjusted inline formulas to ensure clean **MathJax** rendering on web platforms.
   - *Bibliography & Interactive Citations:* Built the reference list using **HTML5** `<span>` anchors and manually linked all in-text citations to their sources.
   - *Markup Cleanup:* Removed leftover LaTeX macros and `style_in.sty` artifacts to keep the source code clean and maintainable.
4. **Quality Assurance & Version Control:** Previewed the rendered output locally in **VS Code** and verified all image paths, anchor links, and equations directly in the **GitHub** web interface.

## 🔗 External Links

   - **Original LaTeX Sources:** [View Project on Overleaf (Read-Only)](https://www.overleaf.com/read/dvkbfxrcbshd#e97f86)