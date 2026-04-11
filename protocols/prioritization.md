# Prioritization Framework

This framework is applied during Stage 5 (Synthesis) of every analysis protocol to rank findings and produce the prioritization matrix in the final deliverable. It uses three axes, each scored independently, to produce a priority classification.

---

## Axis 1: Evidence Strength

Evidence strength reflects how well-supported a finding is by the multi-agent pipeline and the underlying participant data.

| Level | Definition |
|-------|-----------|
| **High** | 12+ of 20 agent runs surfaced this finding (High confidence tier). Supported by quotes from 3+ different participants. Verified quotes, supported inferences. Cross-lens presence (appeared in 2+ of the 4 extraction lenses). |
| **Medium** | 6-11 of 20 agent runs surfaced this finding (Medium confidence tier). Supported by quotes from 2+ different participants. At least some quotes verified. May be concentrated in 1-2 lenses. |
| **Low** | 1-5 of 20 agent runs surfaced this finding (Low confidence tier). May rely on a single participant's quote. Verification may be incomplete or mixed. May appear in only one lens. |

Evidence strength is the most objective of the three axes. It is derived directly from the pipeline's convergence and verification data.

---

## Axis 2: Potential Impact

Potential impact assesses how much this finding matters to the people it affects and how much design leverage it offers.

| Level | Definition |
|-------|-----------|
| **High** | Relates to a core job to be done, a severe pain, or a critical moment of truth. Affects the person's ability to achieve their primary goal. Failure here causes abandonment, significant distress, or systemic failure. Design intervention would transform the experience. |
| **Medium** | Relates to an important touchpoint, a moderate pain, or a desired gain. Affects satisfaction and efficiency but does not block the person's primary goal. Design intervention would meaningfully improve the experience. |
| **Low** | Relates to a minor interaction, a cosmetic issue, or an unexpected gain. The person can achieve their goal without this being addressed. Design intervention would polish the experience but not change its fundamental quality. |

Potential impact requires judgment. Use participant language and behavioral evidence to calibrate: did participants describe this as a deal-breaker, an annoyance, or a nice-to-have? Did it cause abandonment, workarounds, or a shrug?

---

## Axis 3: Frequency

Frequency reflects how many participants in the sample exhibited or described this finding.

| Level | Definition |
|-------|-----------|
| **High** | 7+ of 10 participants (or 70%+ of the sample, adjusted for sample size). This is a widespread pattern. |
| **Medium** | 4-6 of 10 participants (or 40-60% of the sample). This affects a significant segment but is not universal. |
| **Low** | 1-3 of 10 participants (or under 40% of the sample). This may be a niche concern or an emerging pattern. |

Frequency counts are based on unique participants who exhibited the behavior or expressed the sentiment, not on the number of agent runs that identified it. A finding can have high agent convergence but low participant frequency if multiple agents all identified the same pattern from the same small set of participants.

---

## Priority Classifications

Combine the three axes to determine the priority classification for each finding.

| Classification | Criteria | Action |
|---------------|----------|--------|
| **Immediate** | All three axes are High | Address first. These are well-evidenced, high-impact, widespread patterns. They are the foundation of the design brief. |
| **Strong opportunity** | Two or more axes are High | Address with high priority. These are either well-evidenced and impactful, well-evidenced and widespread, or impactful and widespread. Strong candidates for the next design sprint. |
| **Worth exploring** | Mixed levels across axes | Include in the design conversation. May require additional research to confirm, or may represent opportunities for specific segments rather than the full population. |
| **Monitor** | Multiple axes are Low | Track but do not prioritize. These are weak signals that may become important in future research or as the product evolves. |
| **Human review** | Low evidence but High impact | Escalate for human judgment. These findings could be significant but the evidence is too thin to act on with confidence. Flag them explicitly in the deliverable and recommend targeted follow-up research. |

The "Human review" classification deserves special attention. A finding with Low evidence strength but High potential impact is dangerous to ignore and dangerous to act on. The correct response is neither to dismiss it nor to treat it as validated, but to flag it as a priority for further investigation.

---

## Example Prioritization Matrix

| ID | Finding | Evidence Strength | Potential Impact | Frequency | Priority |
|----|---------|------------------|-----------------|-----------|----------|
| JOB-001 | When receiving an unexpected school notification during work, parents need to immediately assess urgency to manage anxiety | High (16/20 runs, 4 participants, cross-lens) | High (core emotional job, drives behavior) | High (8/10 participants) | Immediate |
| PAIN-003 | 48-hour silence after claim submission causes anxiety and duplicate submissions | High (14/20 runs, verified quotes) | High (moment of truth, causes abandonment) | Medium (5/10 participants) | Strong opportunity |
| GAIN-007 | Participants value a single point of contact who knows their full history | Medium (9/20 runs) | Medium (desired gain, not blocking) | High (7/10 participants) | Strong opportunity |
| JOB-009 | Some participants want to delegate the entire process to a trusted person | Low (4/20 runs) | Medium (alternative coping strategy) | Low (2/10 participants) | Monitor |
| PAIN-011 | One participant described a safety concern with the physical waiting area | Low (2/20 runs) | High (safety-related, potential serious harm) | Low (1/10 participants) | Human review |

---

## Applying This Framework

During Stage 5 synthesis, score every finding on all three axes and assign a priority classification. Include the completed matrix in the deliverable. The matrix serves two purposes: it helps the client focus design effort where it will have the greatest impact, and it makes the prioritization reasoning transparent and auditable.

Do not use this framework to suppress findings. Every finding that survives verification appears in the deliverable regardless of its priority classification. Low-priority findings are reported in the Low Confidence section. The prioritization matrix ranks them; it does not filter them.
