# MS Emon &mdash; Research Repository (Quarto Redesign)

A modern, accessible, and responsive personal research and strategy website built with [Quarto](https://quarto.org/), inspired by the "Research Instrument" design language of `quarto-test`.

**Live Production Site:** [https://msemonlab.github.io/quarto-redesign/](https://msemonlab.github.io/quarto-redesign/)  
**ResearchGate Profile:** [Md. Salauddin Emon](https://www.researchgate.net/profile/Md-Salauddin-Emon)  
**GitHub Organization / User:** [@msemonlab](https://github.com/msemonlab)

---

## Site Architecture & Structure

```text
quarto-redesign/
├── .github/
│   └── workflows/
│       └── pages.yml         # Automated CI/CD pipeline for GitHub Pages deployment
├── _includes/
│   ├── head.html             # Google Fonts, vector favicon, & pre-render theme detection
│   ├── header.html           # Custom sticky header with search, Sun/Moon toggle, & drawer
│   └── footer.html           # Two-column layout closing, sidebar widgets, & hero-gradient footer
├── assets/
│   ├── images/
│   │   ├── logo.svg          # Brand vector logo (systems & neural nodes)
│   │   └── favicon.svg       # Vector browser favicon
│   └── styles.css            # Custom CSS system: atmospheric gradients, grid drift, & cards
├── _quarto.yml               # Central Quarto project configuration
├── index.qmd                 # Homepage with live observation field & publication spotlight
├── research.qmd              # Research archive with working papers & BibTeX citations
├── analytics.qmd             # Analytics archive with planned computational frameworks
├── about.qmd                 # Researcher profile, methodology, & collaboration links
├── search.qmd                # Dedicated search page with client-side indexing engine
├── README.md                 # Project setup and development guide
└── CHANGES.md                # Comprehensive audit of improvements vs. original
```

---

## Local Development & Rendering

### Prerequisites

1. Install the latest [Quarto CLI](https://quarto.org/docs/get-started/) (v1.4+ recommended).
2. Ensure `git` is installed.

### Live Preview Server

To start an interactive local development server with instant hot-reloading:

```bash
quarto preview
```

### Production Build / Render

To compile the full static website:

```bash
quarto render
```

Generated outputs will be compiled into the `_site/` directory ready for deployment.
