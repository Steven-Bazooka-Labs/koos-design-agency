---
description: Run a Pains and Gains analysis on transcripts in the current project phase
---

# Pains & Gains Analysis

Run a Pains & Gains analysis on the transcripts in the current project phase.

## Before Starting

1. Read the project-level `CLAUDE.md` in the current project directory for client context.
2. Read the phase-level `CLAUDE.md` in the current phase directory to understand the Double Diamond phase.
3. Read the `scoping.md` in the current phase directory. If it does not exist, stop and ask the user to fill one in using `templates/project-scoping.md`.
4. Check the `analysis/` folder for existing analyses. If a JTBD analysis exists, read it for context (but do not let it constrain extraction).

## Execution

Read and follow `protocols/pains-gains-analysis.md` step by step.

Ask the user which mode:
- **Guided** (default): Pause after each major stage for review.
- **Autopilot**: Run the full pipeline without pausing. Only use if the user explicitly requests it.

## Output

Write results to the current phase's `analysis/` folder following `templates/output-formats/pains-gains-output.md`. Generate both `.md` and `.csv` outputs.
