# Architectural & Design Changes

This document outlines the design, UX, and technical improvements introduced in the `quarto-redesign` repository compared to the source `quarto-test` repository.

---

## Executive Summary of Improvements

| Category | Original Source (`quarto-test`) | Redesigned System (`quarto-redesign`) | Rationale / Benefit |
|---|---|---|---|
| **Quarto Integration** | `navbar: false`, `search: false`, `theme: none`, `page-layout: custom` | Fully native Quarto website architecture with Bootstrap 5 SCSS integration | Enables Quarto's native navigation, search indexing, responsive mobile drawer, and future computational features. |
| **Header / Shell** | Hardcoded raw HTML include (`_includes/header.html`) | Clean declarative Quarto navbar in `_quarto.yml` with vector logo and research pill | Eliminates brittle template duplication and fixes double-header / missing tag bugs. |
| **Theme & Styling** | Monolithic 53KB legacy CSS file (`assets/styles.css`) | Modular SCSS design system (`custom.scss`) utilizing Quarto's Sass compilation pipeline | Significantly faster load time, clean maintainability, and tight integration with Bootstrap variables. |
| **Dark Mode** | Custom ad-hoc JavaScript toggle injected into the footer | Seamless native Quarto light/dark mode switch (`cosmo` + `darkly` with custom SCSS) | Built-in preference persistence (`localStorage`), system color-scheme detection, zero flicker. |
| **Typography & Scale** | Inconsistent heading sizes with duplicated `h1` titles | Refined typography scale using `Inter` and `JetBrains Mono` with WCAG AA compliance | Resolves duplicate headings (e.g. `<h1>Research</h1>` appearing twice) and improves reading ergonomics. |
| **Operational Status** | Static HTML card with fixed formatting | Enhanced **Live Telemetry Observation Card** with active pulsing status beacon | Preserves the "research instrument" identity while elevating UX and visual polish. |
| **Publications & Citations** | Single static text line noting initialization | Rich publication cards with year/status/type badges, links, and collapsible BibTeX citation modals | Professional academic scannability; supports standalone `references.bib`. |
| **Search Functionality** | Placeholder static HTML form without indexing | Native instant Quarto search overlay (keyboard shortcut `/` or `s`) + dedicated `/search.html` permalink | Instant search across all page contents, headings, and publications. |
| **Deployment CI/CD** | Basic build script | Robust GitHub Actions workflow (`.github/workflows/pages.yml`) deploying to GitHub Pages | Automated zero-touch build & deploy on push to `main`. |
| **Assets & Branding** | No custom vector assets | Custom SVG vector brand logo and browser favicon in `assets/images/` | Professional visual branding across browser tabs and mobile home screens. |

---

## Detailed Audit of Enhancements

### 1. 100% Content Preservation
Every item of content, data, and context from the original repository was meticulously preserved:
- **Identity & Tagline:** `"Strategy Analyst | Systems, Neuroscience & E-commerce | Data-Driven & Customer-Centric"`
- **Live Status & Telemetry:**
  - Eyebrow: `"PRIMARY OBSERVATION FIELD"`
  - Title: `"Operational Status"`
  - Card: `"Strategic Research Synthesis"`
  - Status: `"The Repository is currently in initialization stage."`
  - Focus: `"Foundational ResearchGate Publication — In Progress"`
  - Note: `"System status: Calibrating for data-driven and customer-centric frameworks."`
- **Research Archive:** Preserved the original research description, archive initialization note, and ResearchGate author links.
- **Analytics Archive:** Preserved the analytical archive description, list of planned themes (customer-centric systems, e-commerce scalability, human cognition & decision quality), and computational notebook readiness.
- **About the Repository:** Preserved the exact repository description, systems thinking focus, working notes purpose, and ResearchGate connection.

### 2. Information Architecture & Navigation
- Replaced the brittle raw HTML header and mobile drawer script with Quarto's responsive navbar.
- Configured a comprehensive global footer featuring MS Emon's academic signature, section links, GitHub, and ResearchGate icons.
- Added a smooth "Back to Top" navigation button for enhanced reading flow on long documents.

### 3. Academic Publication Framework
- Structured MS Emon's upcoming publication into an academic card format with:
  - Year badge (`2025`)
  - Status badge (`In Progress`)
  - Type badge (`Working Paper` / `ResearchGate`)
  - Direct links to ResearchGate
  - Collapsible BibTeX citation block for easy referencing
- Added `references.bib` at root to allow native Quarto citations in future `.qmd` working notes.

### 4. Accessibility & Performance
- Ensured semantic HTML hierarchy (`h1` &rarr; `h2` &rarr; `h3`) with no skipped or duplicated levels.
- Strictly maintained WCAG AA color contrast standards across both light and dark modes.
- Added full keyboard accessibility for navigation links, theme toggle, and search dialog.
- Responsive breakpoints tested across mobile, tablet, and desktop viewports.
