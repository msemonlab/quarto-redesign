# Architectural & Design Changes

This document outlines the design, UX, and technical architecture in the `quarto-redesign` repository, built directly upon the custom "Research Instrument" design language of `quarto-test` with targeted enhancements.

---

## Executive Summary of Design & Technical Architecture

| Category | Source (`quarto-test`) | Enhanced Architecture (`quarto-redesign`) | Status |
|---|---|---|---|
| **Design Language** | "Research Instrument" & "Immersive Cinematic Layer" | Preserved 100% of atmospheric gradients, grid drift, and glassmorphism styling | [PASS] Verified |
| **Layout System** | Two-column desktop layout (816px main + 270px sidebar) | Exact two-column layout with sidebar widget and domain navigation | [PASS] Verified |
| **Header Shell** | Custom sticky header with title, label, search, and Sun/Moon toggle | Enhanced zero-flicker Sun/Moon toggle, rotating SVGs, and responsive drawer | [PASS] Verified |
| **Theme Toggle** | Client-side `data-theme` switch with `localStorage` | Enhanced with early pre-render head script to eliminate dark mode flash | [PASS] Verified |
| **Search Engine** | Form sending query to `search.html` with static placeholder | Fully functional client-side search engine indexing repository records | [PASS] Verified |
| **Operational Telemetry** | Status card with initialization notes | Status card preserved in full, plus live pulsating emerald beacon | [PASS] Verified |
| **Publication Showcase** | Single static initialization line | Enhanced publication card with year/status badges and BibTeX modal | [PASS] Verified |
| **Footer & Branding** | Hero-gradient footer with signature and transmission note | Retained 100%, added SVG vector favicon and clean responsive spacing | [PASS] Verified |
| **Deployment CI/CD** | Actions workflow | Verified GitHub Actions workflow with `enablement: true` on GitHub Pages | [PASS] Verified |

---

## Key Enhancements over Original `quarto-test`

1. **Pre-Render Zero-Flicker Theme Detection**:
   In `_includes/head.html`, an early inline script queries `localStorage` and `prefers-color-scheme` to set `data-theme` before the first paint, eliminating any flash of light theme for dark-mode visitors.
2. **Interactive Search**:
   On `search.html`, incoming search queries (`?q=...`) are parsed and matched in real-time against an in-browser repository index, rendering highlighted card results.
3. **Publication Cards & BibTeX Citations**:
   MS Emon's foundational working paper is structured into an academic card with clean badges (`2025`, `In Progress`, `Working Paper`), ResearchGate link, and a collapsible BibTeX citation drawer.
4. **Active Instrument Telemetry**:
   An emerald pulse beacon dot was integrated into the `PRIMARY OBSERVATION FIELD` status card, reinforcing the scientific telemetry aesthetic.
5. **Clean Quarto Pipeline**:
   The project builds with 0 errors and 0 warnings using `quarto render`, outputting clean static HTML directly deployable to GitHub Pages.
6. **Precision Logo Lockup Alignment**:
   Calibrated `.header-repository-label` (`RESEARCH REPOSITORY`) using horizontal condensation (`transform: scaleX(...)`) and tracked uppercase lettering to visually and geometrically match the exact rendered length of `MS Emon` across both desktop and mobile viewports.

