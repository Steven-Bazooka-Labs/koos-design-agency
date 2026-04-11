---
description: Run a Customer Journey Mapping analysis on transcripts in the current project phase
---

# Customer Journey Mapping

Run a journey mapping analysis on the transcripts in the current project phase.

## Before Starting

1. Read the project-level `CLAUDE.md` in the current project directory for client context.
2. Read the phase-level `CLAUDE.md` in the current phase directory to understand the Double Diamond phase.
3. Read the `scoping.md` in the current phase directory. If it does not exist, stop and ask the user to fill one in using `templates/project-scoping.md`.
4. Check the `analysis/` folder for existing JTBD, Pains & Gains, and/or Persona analyses. **All that exist are mandatory input** — load them and use their findings to enrich the journey map. If none exist, work from transcripts alone.

## Execution

Read and follow `protocols/journey-mapping.md` step by step.

Ask the user which mode:
- **Guided** (default): Pause after each major stage for review.
- **Autopilot**: Run the full pipeline without pausing. Only use if the user explicitly requests it.

## Output

Write results to the current phase's `analysis/` folder following `templates/output-formats/journey-map-output.md`. Generate both `.md` and `.csv` outputs.
