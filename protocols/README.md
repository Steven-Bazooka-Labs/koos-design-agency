# Analysis Protocols

## What These Are

The files in this directory are execution protocols -- step-by-step instructions that Claude follows to run multi-agent analysis pipelines on qualitative research data. They are not methodology references (those live in `methodologies/`), not output templates (those live in `templates/output-formats/`), and not background knowledge (that lives in `knowledge-base/`). Protocols are operational playbooks. They tell Claude exactly what to do, in what order, with what inputs, and to what standard.

Each protocol encodes one of KOOS's core research analysis methods as a reproducible, auditable pipeline. The goal is consistent analytical rigor across projects, regardless of who initiates the analysis.

## Two Execution Modes

Every protocol supports two modes:

**Guided mode (default).** The pipeline pauses after each major stage and presents a summary to the user. The user reviews, asks questions, adjusts scope, or confirms before the pipeline continues. This is the recommended mode for most projects. It keeps a human analyst in the loop at every decision point.

**Autopilot mode.** The pipeline runs all stages without pausing. The user receives the final deliverable when complete. Use autopilot when the research context is well-understood, the data is clean, and speed matters more than stage-by-stage review.

To select a mode, specify it in the initial prompt when launching an analysis. If no mode is specified, guided mode is used.

## Common Pipeline Architecture

All four analysis protocols follow the same multi-agent pipeline structure:

| Stage | Description | Agents | Type |
|-------|-------------|--------|------|
| 1 | Preparation | 1 | Orchestrator |
| 2a | Extraction -- Lens A | 5 parallel | Extraction |
| 2b | Extraction -- Lens B | 5 parallel | Extraction |
| 2c | Extraction -- Lens C | 5 parallel | Extraction |
| 2d | Extraction -- Lens D | 5 parallel | Extraction |
| 3 | Convergence Analysis | 1 | Orchestrator |
| 4 | Disagreement Deep-Dive | 5 parallel | Analysis |
| 4.5a | Quote Verification | 5 parallel | Verification |
| 4.5b | Inference Verification | 5 parallel | Verification |
| 4.5c | Disagreement Audit | 5 parallel | Verification |
| 5 | Synthesis & Deliverable | 1 | Orchestrator |

Total: 43 agent runs per analysis. Four lenses with five independent agents each produce 20 extraction runs. Convergence, disagreement deep-dive, three verification stages, and final synthesis bring the total to 43.

The multi-agent design is intentional. Running the same analysis independently across multiple agents surfaces findings that a single pass would miss, quantifies confidence through convergence, and makes the analytical process auditable.

## Protocol Dependencies

**JTBD and Pains & Gains are fully independent.** They can be run in any order, in parallel, or alone. Neither requires prior analysis as input.

**Persona Synthesis and Journey Mapping work standalone but use prior analyses as mandatory input when available.** Before running either protocol, check the `analysis/` folder for existing JTBD and/or Pains & Gains outputs. If prior analyses exist, they must be loaded and used -- they are not optional context, they are required input. If no prior analyses exist, the protocol extracts needs, pains, and behaviors directly from transcripts.

## Confidence Tiers

Confidence tiers reflect how many of the 20 independent extraction runs surfaced a given finding:

| Tier | Run Count | Interpretation |
|------|-----------|----------------|
| High | 12+ of 20 | Strong, well-evidenced pattern. Multiple lenses and agents converge. Treat as validated finding. |
| Medium | 6-11 of 20 | Plausible pattern that merits attention. Requires human judgment to assess significance. |
| Low | 1-5 of 20 | Weak signal. May be an edge case, emerging pattern, or noise. Include for completeness but do not treat as validated. |

These thresholds apply across all four analysis protocols. Confidence tiers appear in every deliverable and drive prioritization decisions.

## Cross-Cutting Quality Layers

Three documents in this directory apply across all protocols as quality control mechanisms:

- **`quality-criteria.md`** -- Defines what makes a strong vs. weak insight, with worked examples for each analysis type. Use this to evaluate extraction quality during convergence and synthesis.
- **`bias-and-rigor.md`** -- Checklist of cognitive and methodological biases to guard against before, during, and after analysis. Run this checklist at Stage 5 before finalizing any deliverable.
- **`prioritization.md`** -- Three-axis framework (evidence strength, potential impact, frequency) for ranking findings. Apply during Stage 5 to produce the prioritization matrix in the final deliverable.

These are not optional supplements. Every protocol references them at specific stages. They are integral to the pipeline.
