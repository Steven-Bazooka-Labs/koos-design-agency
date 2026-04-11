# Jobs to Be Done -- Analysis Output

---

## Executive Summary

> Maximum 200 words. Summarize the most important jobs discovered, the confidence landscape, and any critical tensions. Write for a reader who will not read the full report.

[Executive summary text. State the number of jobs identified per confidence tier, highlight the 2-3 most significant findings, and flag any surprising or counter-intuitive results.]

---

## Research Context

| Field             | Value                                                                 |
| ----------------- | --------------------------------------------------------------------- |
| Client            | [Client organization name]                                            |
| Phase             | [e.g., Discovery / Concept / Validation]                              |
| Research Type     | [e.g., Generative / Evaluative / Mixed]                               |
| Participants      | [Number and brief composition, e.g., "12 participants: 8 end users, 4 administrators"] |
| Analysis Protocol | 4 lens stages (obvious, implicit, emotional, adversarial) x 5 parallel agents = 20 independent analysis runs, followed by convergence analysis |
| Verification      | Quote verification, inference verification, and disagreement audit each run by 5 independent agents |

---

## High Confidence Findings (12+ of 20 runs)

Findings in this tier were identified by 12 or more of the 20 independent analysis runs. These represent strong, well-evidenced patterns in the data.

### JOB-001: [Job statement in "When ___, I want to ___, so I can ___" format]

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | [X]/20 runs                                |
| Lens Breakdown    | Obvious [X]/5, Implicit [X]/5, Emotional [X]/5, Adversarial [X]/5 |
| Type              | [Functional / Emotional / Social]          |

**Supporting Evidence:**

> "[Exact participant quote]"
> -- Participant [ID], identified by agents [list agent IDs, e.g., O1, O3, I2, I4, E1, E2, E3, E5, A1, A2, A3, A4]

> "[Exact participant quote]"
> -- Participant [ID], identified by agents [list agent IDs]

> "[Exact participant quote]"
> -- Participant [ID], identified by agents [list agent IDs]

**Notes:** [Any additional context, caveats, or nuance about this job. Note if the adversarial lens raised any challenges that were resolved.]

---

### JOB-002: [Job statement]

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | [X]/20 runs                                |
| Lens Breakdown    | Obvious [X]/5, Implicit [X]/5, Emotional [X]/5, Adversarial [X]/5 |
| Type              | [Functional / Emotional / Social]          |

**Supporting Evidence:**

> "[Exact participant quote]"
> -- Participant [ID], identified by agents [list agent IDs]

> "[Exact participant quote]"
> -- Participant [ID], identified by agents [list agent IDs]

**Notes:** [Additional context]

---

[Continue for each High Confidence finding...]

---

## Medium Confidence Findings (6-11 of 20 runs)

Findings in this tier were identified by 6-11 of the 20 independent analysis runs. These are plausible patterns that merit attention but require human judgment to assess significance.

### JOB-[NNN]: [Job statement]

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | [X]/20 runs                                |
| Lens Breakdown    | Obvious [X]/5, Implicit [X]/5, Emotional [X]/5, Adversarial [X]/5 |
| Type              | [Functional / Emotional / Social]          |

**Supporting Evidence:**

> "[Exact participant quote]"
> -- Participant [ID], identified by agents [list agent IDs]

> "[Exact participant quote]"
> -- Participant [ID], identified by agents [list agent IDs]

**Human Review Note:** [Explain why this finding did not reach high confidence. Was it a split between lenses? Did the adversarial lens challenge it? Is the evidence ambiguous? Provide enough context for a human analyst to make a judgment call.]

**Notes:** [Additional context]

---

[Continue for each Medium Confidence finding...]

---

## Low Confidence Findings (1-5 of 20 runs)

Findings in this tier were identified by 5 or fewer of the 20 independent analysis runs. These are weak signals -- they may represent edge cases, emerging patterns, or noise. Include them for completeness but do not treat as validated findings.

### JOB-[NNN]: [Job statement]

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | [X]/20 runs                                |
| Lens Breakdown    | Obvious [X]/5, Implicit [X]/5, Emotional [X]/5, Adversarial [X]/5 |
| Type              | [Functional / Emotional / Social]          |

**Supporting Evidence:**

> "[Exact participant quote]"
> -- Participant [ID], identified by agents [list agent IDs]

**Review Recommendation:** [Specific guidance on what to do with this finding. e.g., "Explore in follow-up interviews with participants P03 and P07 who hinted at this need" or "Likely an artifact of the prototype's limited scope -- revisit after full-flow testing."]

**Notes:** [Additional context]

---

[Continue for each Low Confidence finding...]

---

## Tensions & Conflicts

Document cases where jobs contradict each other, where different participant segments have opposing needs, or where the adversarial lens identified fundamental tensions.

### Tension 1: [Short descriptive title]

| Jobs in Tension   | [JOB-NNN] vs. [JOB-NNN]                   |
| ----------------- | ------------------------------------------ |
| Nature            | [Describe the tension]                     |
| Affected Segments | [Which participants or segments]           |
| Implication       | [What this means for design decisions]     |

---

[Continue for each tension...]

---

## Verification Report

| Metric                          | Value       |
| ------------------------------- | ----------- |
| Total Quotes Referenced         | [Number]    |
| Verified Exact Match            | [X]%        |
| Verified Paraphrase (accurate)  | [X]%        |
| Out of Context                  | [X]%        |
| Not Found in Source Material    | [X]%        |

| Inference Metric                          | Value       |
| ----------------------------------------- | ----------- |
| Total Inferences Made                     | [Number]    |
| Supported by Evidence                     | [X]%        |
| Plausible but Unsupported                 | [X]%        |
| Contradicted by Evidence                  | [X]%        |

| Disagreement Audit                        | Value       |
| ----------------------------------------- | ----------- |
| Total Disagreements Identified            | [Number]    |
| Resolved (evidence favored one side)      | [Number]    |
| Unresolved (genuinely ambiguous)          | [Number]    |
| Escalated for Human Review                | [Number]    |

---

## Evidence Index

A complete mapping of every finding to its source evidence. Use this for traceability and audit.

| Finding ID | Quote / Evidence                          | Participant | Transcript Location  | Verification Status |
| ---------- | ----------------------------------------- | ----------- | -------------------- | ------------------- |
| JOB-001    | "[Quote excerpt...]"                      | [ID]        | [File:line or timestamp] | [Exact / Paraphrase / Out of Context / Not Found] |
| JOB-001    | "[Quote excerpt...]"                      | [ID]        | [File:line or timestamp] | [Status] |
| JOB-002    | "[Quote excerpt...]"                      | [ID]        | [File:line or timestamp] | [Status] |
| ...        | ...                                       | ...         | ...                  | ...                 |

---

## Methodology Note

This analysis was produced using KOOS's multi-agent analysis protocol. Each transcript was analyzed independently by 20 agents across 4 interpretive lenses:

- **Obvious lens (5 agents):** Surface-level, explicitly stated jobs
- **Implicit lens (5 agents):** Jobs inferred from behavior, workarounds, and context
- **Emotional lens (5 agents):** Jobs rooted in feelings, identity, and social dynamics
- **Adversarial lens (5 agents):** Challenges, stress-tests, and alternative interpretations of proposed jobs

Findings were then consolidated through convergence analysis. Confidence tiers reflect how many of the 20 independent runs surfaced each finding. All quotes were verified against source transcripts and all inferences were audited for evidentiary support.

Total agent runs for this analysis: 43 (20 lens runs + convergence + disagreement deep-dive + 15 verification runs).

---

## Recommended Next Steps

1. [Specific next step tied to findings, e.g., "Prioritize JOB-001 and JOB-003 for concept development -- both high confidence with strong emotional underpinning"]
2. [e.g., "Conduct follow-up interviews targeting the tension between JOB-002 and JOB-005"]
3. [e.g., "Review medium-confidence findings JOB-007 through JOB-009 with the project team before including in design requirements"]
4. [e.g., "Consider Pains & Gains analysis to deepen understanding of the functional barriers around JOB-004"]
5. [Additional next step]
