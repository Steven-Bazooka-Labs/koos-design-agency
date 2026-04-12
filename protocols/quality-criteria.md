# Quality Criteria for Analysis Findings

This document defines the evidence bar for every finding produced by the multi-agent analysis pipeline. Use it during convergence analysis (Stage 3) and synthesis (Stage 5) to evaluate whether extracted findings meet Koos's standard of rigor.

---

## What Makes a Strong Finding

A strong finding has four properties:

1. **Specific.** It identifies a concrete situation, behavior, emotion, or interaction -- not a vague category. You can picture the moment it describes.
2. **Evidenced.** It is supported by direct quotes from at least 2 different participants. Three or more quotes from different participants is ideal.
3. **Non-obvious.** It reveals something that was not already assumed or known before the research. It changes how you think about the problem.
4. **Actionable.** A design team can act on it. It points toward something that can be changed, created, removed, or amplified.

All four properties must be present. A finding that is specific and evidenced but obvious adds no value. A finding that is non-obvious and actionable but unsupported by evidence is speculation.

---

## What Makes a Weak Finding

A weak finding fails one or more of the four criteria above. Common failure modes:

- **Too broad.** The finding describes a general category rather than a specific pattern.
- **Single quote.** Only one participant's words support it. With one quote, you have an observation, not a finding.
- **Obvious.** The finding restates what the client already knew or what anyone would expect without research.
- **Not actionable.** The finding describes a state but suggests no direction for design intervention.

---

## Worked Examples by Analysis Type

### JTBD

**Weak:** "Users want a better experience."
This fails all four criteria. It is vague (what experience? better how?), likely supported by generic sentiment rather than specific quotes, obvious (of course they do), and too broad to act on.

**Strong:** "When parents receive an unexpected notification from their child's school during the workday (situation), they want to immediately assess whether it requires action or is informational (motivation), so they can decide whether to interrupt their current task without the anxiety of not knowing (outcome). Supported by P02, P05, P08, P11 -- all described the same pattern of checking their phone with a spike of worry, then needing 2-3 sentences to determine urgency."
This is specific (school notification during work), evidenced (4 participants), non-obvious (the job is not "read the notification" but "triage urgency to manage anxiety"), and actionable (design the notification to signal urgency level within the first line).

### Pains and Gains

**Weak pain:** "The website is confusing."
Too broad (which part?), likely a paraphrase rather than a direct finding, obvious, and not actionable without knowing what specifically confuses people.

**Strong pain:** "At the insurance claim submission step, participants could not determine which supporting documents were required versus optional. P03 uploaded everything she had 'just in case,' P07 abandoned the process to call the helpdesk, and P09 submitted without attachments and received a rejection 5 days later. The form labels 'Supporting documents' and 'Additional information' were interpreted as interchangeable by 6 of 10 participants."
Specific (claim submission, document upload step), evidenced (3 participants with distinct behavioral responses, 6/10 quantified), non-obvious (the problem is not complexity but ambiguity between two field labels), actionable (clarify the distinction between required and optional uploads).

**Weak gain:** "Participants want faster service."
Generic, predictable, and too vague to design for.

**Strong gain:** "Participants described a moment of genuine relief when they received a proactive status update before they had to ask. P01: 'I was about to call them and then the text came in -- it felt like someone was actually paying attention.' P06: 'That one message saved me 20 minutes of sitting on hold.' This gain was most pronounced among participants who had previously experienced the 48-hour silence after claim submission (PAIN-003)."
Specific (proactive status update), evidenced (2 participants with quotes, linked to a specific pain), non-obvious (the value is not speed but the feeling of being attended to), actionable (implement proactive notifications at the post-submission stage).

### Personas

**Weak:** "Young, tech-savvy users."
This is a demographic label, not a needs-based persona. It tells you nothing about what these people need, fear, or value. Two "young, tech-savvy" people can have completely different needs from the same service.

**Strong:** "The Cautious First-Timer -- participants who have never navigated this process before and approach it with significant uncertainty about requirements, timelines, and consequences of mistakes. Their primary job is not to complete the process efficiently but to avoid making an error that creates downstream problems. They read every instruction fully, hesitate before submitting, and seek external validation (asking a friend, calling the helpdesk) before committing. Cluster includes P01, P04, P07, P10. Distinguished from 'The Experienced Optimizer' cluster by anxiety level, information-seeking behavior, and willingness to use workarounds."
Specific (describes a stance toward the service, not a demographic), evidenced (4 participants), non-obvious (the primary driver is error avoidance, not task completion), actionable (design for confidence-building: clear progress indicators, explicit confirmation of requirements, easy undo).

### Journey Mapping

**Weak:** "Onboarding could be improved."
Vague, obvious, and gives no direction.

**Strong:** "The emotional low point of the journey occurs between Stage 3 (document submission) and Stage 4 (first response), a gap that averages 6 business days. During this period, participants described growing anxiety, repeated checking of their email and portal, and a loss of confidence that their submission was received correctly. P03: 'After day 3 with no response I started to think I did something wrong.' P08: 'I actually submitted it again because I wasn't sure the first one went through.' This gap is the primary moment of truth -- 4 of 10 participants described it as the point where they formed their overall judgment of the service."
Specific (identifies the exact gap and its duration), evidenced (2 quotes, 4/10 quantified for moment-of-truth status), non-obvious (the problem is not the response time itself but the silence during the gap), actionable (add an acknowledgment notification at submission and a progress update at day 3).

---

## The Evidence Bar

The minimum evidence bar for a finding to appear in the final deliverable:

| Classification | Minimum Evidence | Note |
|---------------|-----------------|------|
| Finding | 2 quotes from different participants | Below this threshold, it is an observation, not a finding |
| Insight | 3+ quotes from different participants, plus a non-obvious interpretation | Insights require both evidence volume and analytical depth |
| Observation | 1 quote | Include in the evidence index but do not present as a validated finding |

When evaluating quotes during verification (Stage 4.5a), apply these statuses:

- **Verified:** The quote matches the source transcript exactly or with trivial variation.
- **Paraphrased:** The quote captures the participant's meaning accurately but uses different words. Acceptable if flagged.
- **Out of context:** The quote is real but is being used to support a claim the participant did not intend. Remove the finding or find alternative evidence.
- **Not found:** The quote cannot be located in any source transcript. Remove the finding unless alternative evidence exists.

A finding that loses all its verified or accurately paraphrased quotes during verification must be removed from the deliverable, regardless of its convergence score.
