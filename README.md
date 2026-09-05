# MS Emon &mdash; Research Repository (Quarto Redesign)

A modern, accessible, and responsive personal research and strategy website built with [Quarto](https://quarto.org/).

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
├── assets/
│   └── images/
│       ├── logo.svg          # Brand vector logo (systems & neural nodes)
│       └── favicon.svg       # Vector browser favicon
├── _quarto.yml               # Central Quarto project & layout configuration
├── custom.scss               # Custom design system, typography, & light/dark mode styling
├── references.bib            # BibTeX bibliography database for publications & citations
├── index.qmd                 # Homepage with live telemetry banner & research pillars
├── research.qmd              # Research archive with working papers & BibTeX citations
├── analytics.qmd             # Analytics archive with planned computational frameworks
├── about.qmd                 # Researcher profile, methodology, & collaboration links
├── search.qmd                # Dedicated search landing page & index integration
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

By default, the server runs at `http://localhost:4200/`. Any changes saved to `.qmd`, `custom.scss`, or `_quarto.yml` will automatically refresh in your browser.

### Production Build / Render

To compile the full static website:

```bash
quarto render
```

The rendered production-ready files are generated into the `_site/` directory.

### Checking the Installation

To verify your Quarto installation and ensure all dependencies are clean:

```bash
quarto check
```

---

## Deployment to GitHub Pages

The repository uses automated deployment via GitHub Actions:

1. **Automatic Build:** Every push to the `main` branch triggers `.github/workflows/pages.yml`.
2. **Build Process:** GitHub Actions sets up Quarto, compiles all `.qmd` files, bundles assets and search indexes, and uploads the artifact.
3. **Publishing:** GitHub Pages deploys the output directly.

### Enabling GitHub Pages on the Repository:

1. Go to repository **Settings** &rarr; **Pages**.
2. Under **Build and deployment** &rarr; **Source**, select **GitHub Actions**.
3. Any subsequent commit pushed to `main` will automatically build and publish the live site.

---

## License & Copyright

&copy; 2026 MS Emon. All rights reserved.
