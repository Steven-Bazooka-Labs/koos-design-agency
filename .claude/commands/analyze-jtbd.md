---
description: Run a Jobs to Be Done analysis on transcripts in the current project phase
---

# Jobs to Be Done Analysis

Run a JTBD analysis on the transcripts in the current project phase.

## Before Starting

1. Read the project-level `CLAUDE.md` in the current project directory for client context.
2. Read the phase-level `CLAUDE.md` in the current phase directory to understand the Double Diamond phase.
3. Read the `scoping.md` in the current phase directory. If it does not exist, stop and ask the user to fill one in using `templates/project-scoping.md`.
4. Check the `analysis/` folder for existing analyses. Read any that exist for context.

## Execution

Read and follow `protocols/jtbd-analysis.md` step by step.

Ask the user which mode:
- **Guided** (default): Pause after each major stage for review.
- **Autopilot**: Run the full pipeline without pausing. Only use if the user explicitly requests it.

## Output

Write results to the current phase's `analysis/` folder following `templates/output-formats/jtbd-output.md`. Generate both `.md` and `.csv` outputs.
