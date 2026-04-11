# Pains & Gains Analysis Protocol

This protocol defines the complete execution pipeline for Pains & Gains analysis. It produces a deliverable following the template at `templates/output-formats/pains-gains-output.md`. The pipeline uses 43 agent runs across 11 stages.

**Protocol dependency:** None. Pains & Gains analysis is fully independent. If a JTBD analysis exists in the `analysis/` folder, read it for context -- it may help identify where pains and gains cluster around specific jobs. But do not constrain extraction to prior JTBD findings. Pains and gains may exist independently of any identified job.

---

## Stage 1: Preparation (1 orchestrator)

Read and internalize the following documents in order:

1. `CLAUDE.md` (project phase instructions, if present)
2. `templates/project-scoping.md` (filled-in version -- research questions, hypotheses, participant composition, known constraints)
3. All interview transcripts in the project's data directory
4. `methodologies/pains-and-gains.md` (methodology reference -- pain categories, gain levels)
5. `knowledge-base/glossary.md` (especially Pain Point, Gain, Touchpoint, Moment of Truth)
6. `knowledge-base/ethics/anonymization.md`
7. `knowledge-base/ethics/research-ethics.md`
8. `protocols/quality-criteria.md`
9. `protocols/bias-and-rigor.md` (run the Pre-Analysis Checks section)

Check the `analysis/` folder. If JTBD analysis exists, note the identified jobs as context. If Pains & Gains has already been run, confirm with the user whether this is a re-analysis.

Run Pre-Analysis Checks from `protocols/bias-and-rigor.md`. Record sample gaps, recruitment bias, interview bias, and pre-stated hypotheses.

**Guided mode:** Present preparation summary and wait for confirmation.

**Autopilot mode:** Log and proceed.

---

## Stage 2: Extraction (20 parallel agents -- 4 lenses x 5 agents each)

Launch all 20 extraction agents in parallel. Each agent receives the full set of transcripts, the Pains & Gains methodology reference, the glossary, and the quality criteria document.

### Stage 2a: Functional Pains (5 agents)

> "You are functional-pain-agent-[N] (where N is 1-5). Read all transcripts provided. Extract every functional pain participants describe -- practical obstacles, friction, wasted effort, things that do not work, take too long, or produce poor outcomes.
>
> For each pain:
> - State the pain clearly: what the participant suffers, struggles with, or is blocked by.
> - Classify severity: High (blocks goal achievement or causes abandonment), Medium (creates significant friction or workarounds), Low (minor annoyance).
> - Link to a specific touchpoint: where in the experience does this pain occur? Name the channel, step, or interaction.
> - Cite exact supporting quote(s) with participant ID and transcript location.
> - Note any workarounds participants have developed in response to this pain.
>
> Focus on practical, operational failures and friction. Emotional and social pains are covered by other lenses.
>
> Tag all your output with your agent ID: functional-pain-agent-[N]."

### Stage 2b: Emotional & Social Pains (5 agents)

> "You are emotional-pain-agent-[N] (where N is 1-5). Read all transcripts provided. Extract every emotional pain (negative feelings the experience creates) and social pain (negative social consequences or perceptions the experience creates).
>
> For emotional pains, look for: anxiety, frustration, confusion, helplessness, dread, embarrassment, feeling judged, loss of control, feeling ignored or unimportant.
>
> For social pains, look for: appearing uninformed, being seen as difficult, having to ask for help publicly, stigma associated with using a service, inability to explain a process to family or colleagues.
>
> For each pain:
> - State the pain clearly, distinguishing whether it is emotional or social.
> - Classify severity: High (causes significant distress, avoidance behavior, or relationship damage), Medium (creates discomfort or self-consciousness), Low (mild negative feeling).
> - Link to a specific touchpoint where this pain occurs.
> - Cite exact supporting quote(s) with participant ID and transcript location.
> - Note the emotional or social dynamic at play: what is the participant feeling or fearing, and why?
>
> Tag all your output with your agent ID: emotional-pain-agent-[N]."

### Stage 2c: Functional Gains (5 agents)

> "You are functional-gain-agent-[N] (where N is 1-5). Read all transcripts provided. Extract every functional gain participants describe or desire -- outcomes that make their life easier, save time, reduce effort, or produce better results.
>
> Classify each gain using Osterwalder's four levels:
> - **Required:** Baseline -- without this, the solution does not work at all.
> - **Expected:** Assumed -- absence causes frustration but presence does not create delight.
> - **Desired:** Valued -- participants would love this but do not necessarily expect it.
> - **Unexpected:** Delightful -- participants never thought to ask for it but find it deeply valuable.
>
> For each gain:
> - State the gain clearly: what the participant values, desires, or benefits from.
> - Assign the gain level (Required, Expected, Desired, Unexpected).
> - Cite exact supporting quote(s) with participant ID and transcript location.
> - Note any connection to a pain: does this gain represent the inverse of a known pain?
>
> Focus on practical, functional outcomes. Emotional and social gains are covered by another lens.
>
> Tag all your output with your agent ID: functional-gain-agent-[N]."

### Stage 2d: Emotional & Social Gains (5 agents)

> "You are emotional-gain-agent-[N] (where N is 1-5). Read all transcripts provided. Extract every emotional gain (desired positive feelings) and social gain (desired positive perceptions) participants describe or imply.
>
> For emotional gains, look for: confidence, peace of mind, feeling in control, relief, pride, feeling cared for, feeling competent, sense of accomplishment.
>
> For social gains, look for: appearing knowledgeable, being seen as responsible, feeling like a valued customer, being able to demonstrate competence to peers, belonging to a community.
>
> For each gain:
> - State the gain clearly, distinguishing whether it is emotional or social.
> - Assign the gain level (Required, Expected, Desired, Unexpected).
> - Cite exact supporting quote(s) with participant ID and transcript location.
> - Note the emotional or social dynamic: what does the participant want to feel or how do they want to be perceived, and in what context?
>
> Also look for gains implied by pains. When a participant describes a negative experience, the opposite often reveals a desired gain. 'I hate not knowing what's happening' implies a gain: 'feeling informed and in control.' Extract these implied gains and mark them as inferred, citing the pain statement as evidence.
>
> Tag all your output with your agent ID: emotional-gain-agent-[N]."

**Guided mode:** After all 20 agents complete, present a summary: total pains and gains extracted, breakdown by lens, notable patterns, and any contradictions. Wait for confirmation.

**Autopilot mode:** Log and proceed.

---

## Stage 3: Convergence Analysis (1 orchestrator)

Collect all output from the 20 extraction agents. Perform the following:

1. **Deduplicate.** Group semantically equivalent pains and gains separately. Two pains are equivalent if they describe the same friction at the same touchpoint, even in different words.
2. **Count runs.** For each unique pain/gain, count how many of the 20 agents identified it.
3. **Assign confidence tiers.** High: 12+/20, Medium: 6-11/20, Low: 1-5/20.
4. **Track cross-lens presence.** Record which lenses identified each finding. Pains found by both functional and emotional lenses are particularly robust. Gains found across functional and emotional lenses often represent core value drivers.
5. **Build the convergence matrix.** Table with: finding ID, statement, category (Functional/Emotional/Social), confidence tier, run count, lens breakdown, severity (for pains) or gain level (for gains), touchpoint, supporting participant IDs.
6. **Identify pain-gain connections.** Map relationships between pains and gains. A pain and a gain are connected when solving the pain directly enables the gain, the gain is the inverse of the pain, or they address different dimensions of the same experience.
7. **Count participant coverage.** Unique participants per finding.

**Guided mode:** Present the convergence matrix with pain-gain connections. Wait for confirmation.

**Autopilot mode:** Log and proceed.

---

## Stage 4: Disagreement Deep-Dive (5 parallel agents)

Launch 5 agents to review Medium/Low confidence findings and adversarial challenges. Same structure as the JTBD protocol.

> "You are disagreement-agent-[N]. Review Medium and Low confidence pains and gains. For each:
> 1. Re-read relevant transcript passages.
> 2. Argue the case FOR this being a valid finding.
> 3. Argue the case AGAINST.
> 4. Map tensions with other findings.
> 5. Recommend: likely valid / likely noise / needs human judgment.
>
> Pay special attention to severity ratings. A pain rated High severity by some agents and Low by others may reflect genuine ambiguity about impact, not noise.
>
> Tag all your output with your agent ID: disagreement-agent-[N]."

**Guided mode:** Present disagreement analysis. Wait for user decisions on ambiguous findings.

**Autopilot mode:** Apply majority rule and proceed.

---

## Stage 4.5a: Quote Verification (5 parallel agents)

Same procedure as JTBD protocol. Verify all cited quotes against original transcripts. Statuses: Verified, Paraphrased, Out of context, Not found. Remove findings that lose all verified evidence.

---

## Stage 4.5b: Inference Verification (5 parallel agents)

Same procedure as JTBD protocol. Verify whether evidence supports each inference. Statuses: Well-supported, Plausible but thin, Unsupported. Majority (3+/5) determines classification. Unsupported findings removed; plausible-but-thin findings downgraded one tier.

---

## Stage 4.5c: Disagreement Audit (5 parallel agents)

Same procedure as JTBD protocol. Audit whether disagreements are based on verified evidence. Resolve or retain as genuine tensions.

**Guided mode:** Present complete verification report. Wait for review.

**Autopilot mode:** Apply results and proceed.

---

## Stage 5: Synthesis & Deliverable (1 orchestrator)

Produce the final deliverable following `templates/output-formats/pains-gains-output.md`.

### Synthesis steps:

1. **Compile verified findings.** Organize pains and gains separately, each by confidence tier. Include all verified evidence.
2. **Apply bias checks.** Run the During-Analysis and Post-Analysis sections of `protocols/bias-and-rigor.md`.
3. **Apply prioritization.** Score every finding using `protocols/prioritization.md`. For pains, potential impact maps to severity. For gains, potential impact maps to gain level (Required/Expected > Desired > Unexpected for impact, though Unexpected gains may have high differentiation value).
4. **Build Pain-Gain Connections section.** Document relationships between pains and gains with design implications.
5. **Build Verification Report.** Compile verification statistics.
6. **Build Evidence Index.** Map every finding to source evidence.
7. **Write Executive Summary.** Maximum 200 words. Follow `knowledge-base/brand/tone-of-voice.md`.
8. **Write Methodology Note.** Document the 43-agent pipeline.
9. **Write Recommended Next Steps.** Tie each recommendation to finding IDs.
10. **Generate Meta-Analysis Log.** Pipeline execution metadata.
11. **Generate CSV Export.** Columns: Finding ID, Type (Pain/Gain), Statement, Category, Confidence Tier, Run Count, Severity/Gain Level, Touchpoint, Priority Classification, Verification Status.

**Guided mode:** Present complete deliverable for final review.

**Autopilot mode:** Save to `analysis/` directory.

---

## Output Files

| File | Description |
|------|-------------|
| `pains-gains-analysis.md` | Main deliverable following `templates/output-formats/pains-gains-output.md` |
| `pains-gains-meta-log.md` | Pipeline execution metadata |
| `pains-gains-export.csv` | Structured data export |
