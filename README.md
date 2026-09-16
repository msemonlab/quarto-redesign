# MS Emon's Personal Log - Quarto Redesign

This repository contains my personal log, research notes, and the source code for my Quarto-based website. Now that the repository is private, this README serves as my internal notebook, task tracker, and development reference.

## Quick Links

- **Live Production Site:** [https://msemonlab.github.io/quarto-redesign/](https://msemonlab.github.io/quarto-redesign/)  
- **ResearchGate Profile:** [Md. Salauddin Emon](https://www.researchgate.net/profile/Md-Salauddin-Emon)  
- **GitHub Organization / User:** [@msemonlab](https://github.com/msemonlab)

---

## Research Logs & Notes

*(Use this space to track ongoing thoughts, research progress, and private notes)*

- **[2026-09-16]** Transitioned repository to private. Refocused the README to be a personal log and tracker instead of a public-facing description.

---

## Site Architecture & Structure Reference

```text
quarto-redesign/
├── .github/workflows/pages.yml       # Automated CI/CD pipeline for GitHub Pages
├── _includes/                        # Custom HTML templates (head, header, footer)
├── assets/                           # CSS, images, and logos
├── _quarto.yml                       # Central Quarto project configuration
├── index.qmd                         # Homepage
├── research.qmd                      # Research archive
├── analytics.qmd                     # Analytics archive
├── about.qmd                         # Profile and methodology
└── search.qmd                        # Search page
```

---

## Local Development Reminders

### Prerequisites
1. [Quarto CLI](https://quarto.org/docs/get-started/)
2. `git`

### Useful Commands

- **Live Preview Server:** 
  ```bash
  quarto preview
  ```
- **Production Build:**
  ```bash
  quarto render
  ```
  *(Compiles the static website into the `_site/` directory)*
