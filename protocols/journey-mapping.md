# Journey Mapping Protocol

This protocol defines the complete execution pipeline for customer journey mapping. It produces a deliverable following the template at `templates/output-formats/journey-map-output.md`. The pipeline uses 43 agent runs across 11 stages.

**Protocol dependency:** Journey mapping works standalone but treats ALL existing analyses as mandatory input when they are present. Check the `analysis/` folder before starting. If JTBD, Pains & Gains, and/or Persona analyses exist, they MUST be loaded and used. The journey map is the integrative deliverable -- it brings together jobs, pains, gains, and persona perspectives into a temporal, sequential view of the experience.

---

## Stage 1: Preparation (1 orchestrator)

Read and internalize the following documents in order:

1. `CLAUDE.md` (project phase instructions, if present)
2. `templates/project-scoping.md` (filled-in version -- research questions, participant composition, known constraints)
3. All interview transcripts in the project's data directory
4. `methodologies/customer-journey-mapping.md` (methodology reference -- touchpoints, emotional arc, moments of truth, gap analysis)
5. `knowledge-base/glossary.md` (especially Journey Map, Touchpoint, Moment of Truth, Pain Point, Gain)
6. `knowledge-base/ethics/anonymization.md`
7. `knowledge-base/ethics/research-ethics.md`
8. `protocols/quality-criteria.md`
9. `protocols/bias-and-rigor.md` (run the Pre-Analysis Checks section)

**Check the `analysis/` folder for prior analyses:**

- **If JTBD analysis exists:** Load it. Jobs provide the motivational context for the journey -- what progress are people trying to make at each stage? Map jobs to journey stages during synthesis.
- **If Pains & Gains analysis exists:** Load it. Pains map directly to specific touchpoints and stages. Gains indicate what value the experience does (or should) deliver at each point. This is mandatory input.
- **If Persona analysis exists:** Load it. The journey map should account for how different personas experience the journey differently. Per-persona journey variations are a required section when personas are available.
- **If all three exist:** Load all. The journey map becomes the comprehensive integrative view of the entire research synthesis.
- **If none exist:** Proceed with direct extraction from transcripts. Note in the deliverable that journey mapping was performed without prior analyses.

Run Pre-Analysis Checks from `protocols/bias-and-rigor.md`. For journey mapping, pay special attention to: do the transcripts cover the full journey or only specific stages? Were participants asked about their experience chronologically? Are early and late journey stages under-represented?

**Guided mode:** Present preparation summary including:
- Prior analyses loaded and their scope
- Estimated journey scope (where does the journey start and end based on transcript content?)
- Any gaps in journey coverage
- Wait for confirmation

**Autopilot mode:** Log and proceed.

---

## Stage 2: Extraction (20 parallel agents -- 4 lenses x 5 agents each)

Launch all 20 extraction agents in parallel. Each agent receives: all transcripts, any prior analysis outputs, the journey mapping methodology reference, the glossary, and the quality criteria document.

### Stage 2a: Touchpoint Mapping (5 agents)

> "You are touchpoint-agent-[N] (where N is 1-5). Read all transcripts provided. Map every interaction point between participants and the service, product, or experience being studied.
>
> For each touchpoint:
> - Name the touchpoint clearly (e.g., 'Initial phone call to reception,' 'Account creation on website,' 'Waiting room at clinic').
> - Identify the channel: digital (app, website, email, SMS), physical (office, letter, signage), or human (phone call, face-to-face, reception desk).
> - Place it in chronological sequence relative to other touchpoints. Identify which journey stage it belongs to.
> - Record participant actions at this touchpoint: what do they do? Use verbs.
> - Record participant thoughts at this touchpoint: what are they thinking? Use their own words from transcripts where possible.
> - Cite supporting quote(s) with participant ID and transcript location.
>
> Start the journey BEFORE first contact with the service -- include the awareness, need-recognition, and information-seeking stages. End AFTER the final transaction -- include follow-up, reflection, and consequences stages.
>
> If participants describe different sequences (some skip steps, some repeat steps, some take detours), map all variations and note which participants follow which path.
>
> Tag all your output with your agent ID: touchpoint-agent-[N]."

### Stage 2b: Emotional Arc (5 agents)

> "You are emotional-arc-agent-[N] (where N is 1-5). Read all transcripts provided. Map how participants felt at each stage and touchpoint of their journey.
>
> For each stage or touchpoint where emotional evidence exists:
> - Identify the dominant emotion (use specific emotion words: anxious, relieved, frustrated, hopeful, confused, angry, satisfied, indifferent, overwhelmed, proud, embarrassed).
> - Rate the emotional valence: Positive, Neutral, or Negative.
> - Identify emotional triggers: what specifically caused this emotional shift? Was it a piece of information, a person's behavior, a wait time, a design element?
> - Identify emotional highs (moments of relief, delight, confidence) and emotional lows (moments of frustration, anxiety, abandonment).
> - Cite supporting quote(s) with participant ID and transcript location.
>
> The goal is to construct a continuous emotional arc across the journey. Where does emotion rise? Where does it drop? Where does it plateau? What triggers the transitions?
>
> Do not invent emotions where the transcript provides no evidence. If a stage has no emotional data, note the gap rather than filling it with assumptions.
>
> Tag all your output with your agent ID: emotional-arc-agent-[N]."

### Stage 2c: Moments of Truth (5 agents)

> "You are moment-of-truth-agent-[N] (where N is 1-5). Read all transcripts provided. Identify the make-or-break interactions -- the touchpoints where participants' overall perception of the experience was disproportionately shaped.
>
> A moment of truth is identified by:
> - **Disproportionate emotional impact:** The participant's emotional language at this touchpoint is significantly more intense than at routine touchpoints.
> - **Decision point:** This is where participants decided to continue, abandon, recommend, or complain.
> - **Perception formation:** Multiple participants describe this touchpoint as the point where they formed their overall judgment of the service.
> - **Behavioral consequence:** This touchpoint triggered a significant action (abandonment, workaround, complaint, advocacy, repeat use).
>
> For each moment of truth:
> - Identify the stage and touchpoint.
> - Explain WHY it is a moment of truth: what makes this interaction disproportionately important?
> - Describe the positive outcome when this moment goes well.
> - Describe the negative outcome when this moment goes poorly.
> - Cite supporting quote(s) with participant ID and transcript location.
> - Count how many participants identified this as a pivotal interaction.
>
> Not every touchpoint is a moment of truth. Be selective. Reserve this classification for interactions that genuinely carry outsized weight. Refer to the definition in `knowledge-base/glossary.md`.
>
> Tag all your output with your agent ID: moment-of-truth-agent-[N]."

### Stage 2d: Gap Analysis (5 agents)

> "You are gap-agent-[N] (where N is 1-5). Read all transcripts provided. Identify gaps in the current journey -- things that should exist but do not, places where the journey breaks, and missing touchpoints.
>
> Look for:
> - **Missing touchpoints:** Interactions that participants expected or needed but that do not exist. Did participants expect a confirmation and not get one? Did they look for information that was not available? Did they want to contact someone and could not?
> - **Broken handoffs:** Points where the journey transfers between channels, departments, or stages and the transition fails. Information lost, context not carried over, participant forced to repeat themselves.
> - **Timing gaps:** Periods of silence or inaction where participants are left waiting without communication. What happens in these gaps? What do participants feel and do?
> - **Missing feedback loops:** Places where participants did something (submitted, applied, requested) but received no acknowledgment or status update.
> - **Desired but absent features:** Things participants explicitly wished for that do not currently exist in the journey.
>
> For each gap:
> - Describe what is missing and where in the journey it is missing.
> - Describe the impact on participant experience: what does the gap cause? Anxiety, repeated contact, abandonment, workarounds?
> - Cite supporting quote(s) with participant ID and transcript location.
> - Suggest what the desired experience would look like (based on participant language, not your own design assumptions).
>
> Tag all your output with your agent ID: gap-agent-[N]."

**Guided mode:** After all 20 agents complete, present:
- Proposed journey stages and touchpoint inventory
- Emotional arc overview (highs and lows)
- Identified moments of truth
- Key gaps
- Wait for user input on journey structure

**Autopilot mode:** Log and proceed.

---

## Stage 3: Convergence Analysis (1 orchestrator)

Convergence for journey mapping focuses on agreement about journey structure, touchpoint identification, emotional arc direction, and moment of truth classification.

1. **Consolidate journey stages.** Compare the stage structures proposed by touchpoint agents. Identify the consensus stage sequence. Note any stages that only some agents identified -- are they real stages with less evidence, or artifacts of different framing?

2. **Consolidate touchpoints.** Build a master touchpoint inventory. Count how many agents independently identified each touchpoint. Touchpoints identified by 12+ agents are high confidence. Those identified by 6-11 are medium. Those by 1-5 are low.

3. **Consolidate emotional arc.** For each stage, aggregate the emotional ratings across agents. Where agents agree on the direction (positive/negative/neutral), assign that direction with the specific emotion word most frequently used. Where agents disagree on direction, note the disagreement.

4. **Consolidate moments of truth.** Count how many agents independently identified each moment of truth. Apply confidence tiers. A moment of truth is most robust when it is identified by multiple agents across the moment-of-truth lens AND confirmed by emotional arc agents as an emotional extreme.

5. **Consolidate gaps.** Deduplicate and count gap identifications. Map gaps to specific journey stages.

6. **Integrate prior analyses.** Map JTBD findings to relevant journey stages (which jobs are active at which stage?). Map pains and gains to specific touchpoints. Map persona variations onto the journey.

7. **Count participant coverage.** For each touchpoint, stage, and moment of truth, count unique participants.

**Guided mode:** Present consolidated journey structure. Wait for confirmation.

**Autopilot mode:** Log and proceed.

---

## Stage 4: Disagreement Deep-Dive (5 parallel agents)

Launch 5 agents to review journey mapping disagreements.

> "You are disagreement-agent-[N]. Review disagreements about:
> 1. Journey stage boundaries: where one stage ends and another begins.
> 2. Emotional direction at contested stages: agents disagree on whether the emotion is positive or negative.
> 3. Moment of truth classification: some agents flagged a touchpoint as a moment of truth, others did not.
> 4. Gap severity: agents disagree on how significant a gap is.
>
> For each disagreement, re-read the relevant transcript passages. Argue both sides. Recommend: one side is more supported / genuine ambiguity (present both views) / insufficient evidence (remove or downgrade).
>
> Tag all your output with your agent ID: disagreement-agent-[N]."

**Guided mode:** Present disagreement analysis. Wait for user decisions.

**Autopilot mode:** Apply majority rule.

---

## Stage 4.5a: Quote Verification (5 parallel agents)

Verify all cited quotes against original transcripts. Same procedure as JTBD protocol.

---

## Stage 4.5b: Inference Verification (5 parallel agents)

Verify whether evidence supports each inference. Particularly important for emotional arc ratings (did the participant actually express this emotion, or is it inferred?) and moment of truth classifications (does the evidence support that this touchpoint is disproportionately important?).

---

## Stage 4.5c: Disagreement Audit (5 parallel agents)

Audit disputed findings against verified evidence. Resolve or retain as genuine ambiguities.

**Guided mode:** Present verification report. Wait for review.

**Autopilot mode:** Apply results and proceed.

---

## Stage 5: Synthesis & Deliverable (1 orchestrator)

Produce the final deliverable following `templates/output-formats/journey-map-output.md`.

### Synthesis steps:

1. **Build the Journey Overview table.** Stages, key touchpoints, overall emotion, and moment of truth count per stage.

2. **Build the Detailed Journey.** For each stage and touchpoint: actions, thoughts, emotion, pain points (linked to PAIN-NNN IDs if available), and opportunities. Mark moments of truth with the `***MOMENT OF TRUTH***` designation.

3. **Build the Moments of Truth Summary.** Consolidated table of all moments of truth with confidence scores.

4. **Build the Emotional Arc Visualization.** Text-based representation of the emotional trajectory. Include the arc narrative (2-3 sentences describing the overall emotional shape).

5. **Build the Gap Analysis table.** Current experience, desired experience, gap severity, and opportunity for each gap.

6. **Build Per-Persona Journey Variations.** If persona analysis exists, document how each persona's journey differs from the aggregate. Include persona-specific moments of truth.

7. **Apply bias checks.** Run `protocols/bias-and-rigor.md`. Pay special attention to: are some journey stages over-represented because the interview guide focused on them? Are early/late stages under-evidenced?

8. **Apply prioritization.** Use `protocols/prioritization.md` to rank moments of truth and gaps by evidence strength, potential impact, and frequency.

9. **Build Verification Report.**

10. **Write Executive Summary.** Maximum 200 words. Summarize: journey scope, number of stages, key moments of truth, overall emotional arc, most critical gaps.

11. **Write Methodology Note.** Document the 43-agent pipeline.

12. **Write Recommended Next Steps.** Tie recommendations to specific stages, touchpoints, moments of truth, and gap IDs. Cross-reference with prior analysis finding IDs.

13. **Generate Meta-Analysis Log.**

14. **Generate CSV Export.** Columns: Stage, Touchpoint, Channel, Emotion, Valence, Moment of Truth (Y/N), Confidence Score, Pain IDs, Gain IDs, Gap Description, Participant IDs.

**Guided mode:** Present complete deliverable for final review.

**Autopilot mode:** Save to `analysis/` directory.

---

## Output Files

| File | Description |
|------|-------------|
| `journey-map-analysis.md` | Main deliverable following `templates/output-formats/journey-map-output.md` |
| `journey-map-meta-log.md` | Pipeline execution metadata |
| `journey-map-export.csv` | Structured data export |
