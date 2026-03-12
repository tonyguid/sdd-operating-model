# CLAUDE.md — Project Instructions for Claude Code

## Project Overview

This is the **AI + Spec-Driven Development (SDD) Operating Model** for Qcells software engineering teams. It defines how teams transition to AI-augmented, specification-driven development.

**Core concept:** The specification is the atomic unit of planning, execution, and reporting. Architects write specs, senior developers implement them using Claude Code agent teams, TPMs track delivery, and dev managers oversee people and process.

## Repository Structure

```
sdd-operating-model/
├── index.html              # Overview/landing page (GitHub Pages)
├── styles.css              # Shared CSS for all pages
├── architect.html          # Architect role detail page
├── senior-developer.html   # Senior Developer role detail page
├── tpm.html                # TPM role detail page
├── dev-manager.html        # Dev Manager role detail page
├── work-management.html    # Work Management process page (ADO + Scrum mapping)
├── README.md               # Project overview
├── CONTRIBUTING.md          # Feedback & contribution guide
├── CLAUDE.md               # This file — Claude Code project instructions
├── specs/
│   └── SPEC_TEMPLATE.md    # Spec template for architects
├── docs/
│   └── adr/
│       └── 001-adopt-sdd.md  # ADR: Adopt SDD with AI
└── .github/
    ├── ISSUE_TEMPLATE/
    │   └── feedback.md     # Issue template for feedback
    └── workflows/
        └── pages.yml       # GitHub Pages deployment workflow
```

## Key Files

- **`index.html`** — Overview landing page with role summary cards, spec lifecycle, executive reporting, and transformation sections.
- **`styles.css`** — Shared stylesheet used by all HTML pages. All styling lives here.
- **`architect.html`, `senior-developer.html`, `tpm.html`, `dev-manager.html`, `product-owner.html`** — Dedicated role detail pages with full responsibilities, artifacts, KPIs, and insights.
- **`work-management.html`** — Work management page covering Scrum-to-SDD mapping, Azure DevOps board setup, ceremonies, estimation, and spec flow.
- **`specs/SPEC_TEMPLATE.md`** — The template that architects use to write implementation specs.
- **`docs/adr/`** — Architecture Decision Records documenting key decisions.

## Conventions

- This is a documentation/specification project, not a traditional codebase.
- Multi-page static site with shared `styles.css` — no build tools, no frameworks, no external CDN dependencies.
- All HTML pages share a common header, nav bar, and footer. The nav `active` class is hardcoded per page (no JavaScript).
- Use Markdown for all docs, specs, and ADRs.
- Status: DRAFT — this is an internal Qcells document under active review.
- Owner: Chief Architect, Qcells.

## Agent Team Configuration

Use a **team of 3 agents** for all implementation tasks on this project. When executing work, launch 3 parallel sub-agents to maximize throughput. Typical decomposition:

- **Agent 1:** HTML content creation or modification (new pages, new sections, content updates)
- **Agent 2:** CSS styling and cross-file nav updates (styles.css changes, nav bar updates across all HTML files)
- **Agent 3:** Documentation and verification (CLAUDE.md, README.md updates, browser preview verification)

Adjust the split based on the task — the key principle is 3 agents running in parallel whenever possible.

## When Editing

- Preserve the existing structure and tone of documents.
- All CSS changes go in `styles.css` — no inline `<style>` blocks in HTML files.
- When adding/renaming pages, update the `<nav class="site-nav">` in all HTML files.
- Follow the spec template format in `specs/SPEC_TEMPLATE.md` when creating new specs.
- Follow ADR format conventions when adding new architecture decision records.
