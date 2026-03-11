# CLAUDE.md — Project Instructions for Claude Code

## Project Overview

This is the **AI + Spec-Driven Development (SDD) Operating Model** for Qcells software engineering teams. It defines how teams transition to AI-augmented, specification-driven development.

**Core concept:** The specification is the atomic unit of planning, execution, and reporting. Architects write specs, senior developers implement them using Claude Code agent teams, TPMs track delivery, and dev managers oversee people and process.

## Repository Structure

```
sdd-operating-model/
├── index.html              # Full operating model (GitHub Pages site)
├── README.md               # Project overview
├── CONTRIBUTING.md          # Feedback & contribution guide
├── CLAUDE.md               # This file — Claude Code project instructions
├── specs/
│   └── SPEC_TEMPLATE.md    # Spec template for architects
├── docs/
│   └── adr/
│       └── 001-adopt-sdd.md  # ADR: Adopt SDD with AI
└── .github/
    └── ISSUE_TEMPLATE/
        └── feedback.md     # Issue template for feedback
```

## Key Files

- **`index.html`** — The primary deliverable. Contains the full operating model as a single-page HTML document for GitHub Pages.
- **`specs/SPEC_TEMPLATE.md`** — The template that architects use to write implementation specs.
- **`docs/adr/`** — Architecture Decision Records documenting key decisions.

## Conventions

- This is a documentation/specification project, not a traditional codebase.
- `index.html` is a self-contained single-page site (HTML + inline CSS/JS). Keep it self-contained.
- Use Markdown for all docs, specs, and ADRs.
- Status: DRAFT — this is an internal Qcells document under active review.
- Owner: Chief Architect, Qcells.

## When Editing

- Preserve the existing structure and tone of documents.
- Keep `index.html` as a single self-contained file (no external dependencies).
- Follow the spec template format in `specs/SPEC_TEMPLATE.md` when creating new specs.
- Follow ADR format conventions when adding new architecture decision records.
