---
description: Run a Needs-Based Persona synthesis on transcripts in the current project phase
---

# Needs-Based Persona Synthesis

Run a persona synthesis on the transcripts in the current project phase.

## Before Starting

1. Read the project-level `CLAUDE.md` in the current project directory for client context.
2. Read the phase-level `CLAUDE.md` in the current phase directory to understand the Double Diamond phase.
3. Read the `scoping.md` in the current phase directory. If it does not exist, stop and ask the user to fill one in using `templates/project-scoping.md`.
4. Check the `analysis/` folder for existing JTBD and/or Pains & Gains analyses. **If they exist, they are mandatory input** — load them and use them as foundational data for clustering. If they do not exist, work from transcripts alone.

## Execution

Read and follow `protocols/persona-synthesis.md` step by step.

Ask the user which mode:
- **Guided** (default): Pause after each major stage for review.
- **Autopilot**: Run the full pipeline without pausing. Only use if the user explicitly requests it.

## Output

Write results to the current phase's `analysis/` folder following `templates/output-formats/persona-card.md`. Generate both `.md` and `.csv` outputs.
