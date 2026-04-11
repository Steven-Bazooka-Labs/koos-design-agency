# Persona Synthesis Protocol

This protocol defines the complete execution pipeline for needs-based persona synthesis. It produces a deliverable following the template at `templates/output-formats/persona-card.md`. The pipeline uses 43 agent runs across 11 stages.

**Protocol dependency:** Persona synthesis works standalone but treats prior analyses as mandatory input when they exist. Before starting, check the `analysis/` folder. If JTBD and/or Pains & Gains analyses are present, they MUST be loaded and used as the primary data source for clustering. If no prior analyses exist, the protocol extracts needs, pains, and behaviors directly from transcripts.

---

## Stage 1: Preparation (1 orchestrator)

Read and internalize the following documents in order:

1. `CLAUDE.md` (project phase instructions, if present)
2. `templates/project-scoping.md` (filled-in version -- research questions, participant composition, known constraints)
3. All interview transcripts in the project's data directory
4. `methodologies/needs-based-personas.md` (methodology reference -- needs-based clustering, persona card structure, common pitfalls)
5. `knowledge-base/glossary.md` (especially Persona, Need, Convergence)
6. `knowledge-base/ethics/anonymization.md`
7. `knowledge-base/ethics/research-ethics.md`
8. `protocols/quality-criteria.md`
9. `protocols/bias-and-rigor.md` (run the Pre-Analysis Checks section)

**Check the `analysis/` folder for prior analyses:**

- **If JTBD analysis exists:** Load it. Each participant's set of jobs becomes part of their need profile for clustering. This is mandatory input, not optional context.
- **If Pains & Gains analysis exists:** Load it. Each participant's pains and gains become part of their need profile for clustering. This is mandatory input, not optional context.
- **If both exist:** Load both. The combination of jobs, pains, and gains per participant provides the richest clustering basis.
- **If neither exists:** Proceed with direct extraction from transcripts. Note in the deliverable that persona synthesis was performed without prior JTBD or Pains & Gains analysis, which typically produces less robust results.

Build a participant profile matrix: for each participant ID, compile their identified jobs (from JTBD analysis or transcripts), pains (from Pains & Gains analysis or transcripts), gains (from Pains & Gains analysis or transcripts), and notable behaviors from the transcripts.

Run Pre-Analysis Checks from `protocols/bias-and-rigor.md`.

**Guided mode:** Present preparation summary including:
- Number of participants and their data richness (how much material per participant)
- Prior analyses loaded and their scope
- Participant profile matrix overview
- Any sample gaps that may affect clustering
- Wait for confirmation

**Autopilot mode:** Log and proceed.

---

## Stage 2: Extraction (20 parallel agents -- 4 lenses x 5 agents each)

Launch all 20 extraction agents in parallel. Each agent receives: all transcripts, the participant profile matrix (with prior analysis data if available), the persona methodology reference, the glossary, and the quality criteria document.

### Stage 2a: Need Pattern Clustering (5 agents)

> "You are need-cluster-agent-[N] (where N is 1-5). You have transcripts and participant profiles (including any prior JTBD and Pains & Gains data).
>
> Your task: group participants into clusters based on shared need patterns. A need pattern is a combination of jobs, pains, and gains that recur across multiple participants and represent a distinct orientation toward the service or experience.
>
> Instructions:
> 1. Review each participant's need profile (jobs, pains, gains, and transcript evidence).
> 2. Identify which participants share similar combinations of needs. Look for participants who have the same core jobs, experience the same primary pains, and seek the same key gains.
> 3. Propose 3-5 clusters. For each cluster:
>    - Give it a descriptive archetype name that captures the core orientation (e.g., 'The Cautious First-Timer,' 'The Efficiency Optimizer,' 'The Reluctant Delegator').
>    - Write a one-sentence core orientation statement.
>    - List the participants in this cluster.
>    - List the 3-5 most important shared needs (jobs, pains, gains).
>    - Explain what makes this cluster distinct from the others.
> 4. Account for every participant. If a participant does not fit any cluster, note them as an outlier and explain why.
> 5. Note any participants who could belong to more than one cluster.
>
> Base your clustering on needs, not demographics. Two participants with different demographic profiles but similar need patterns belong in the same cluster. Two participants with identical demographics but different need patterns belong in different clusters.
>
> Tag all your output with your agent ID: need-cluster-agent-[N]."

### Stage 2b: Behavior Clustering (5 agents)

> "You are behavior-cluster-agent-[N] (where N is 1-5). You have transcripts and participant profiles.
>
> Your task: group participants into clusters based on shared behavioral patterns. Look at what participants actually DO, not what they need or want.
>
> Focus on:
> - **Actions and workarounds:** How do participants approach the service? Do they read everything first or dive in? Do they create their own systems? Do they ask for help or figure it out alone?
> - **Channel preferences:** Which channels do participants gravitate toward? Phone, digital, in-person? Why?
> - **Decision-making patterns:** How do participants make decisions? Quickly or slowly? Independently or with consultation? Based on information or intuition?
> - **Habits and routines:** What recurring behaviors appear in the transcripts?
>
> Propose 3-5 behavioral clusters:
> 1. Give each cluster a descriptive name.
> 2. List the participants in each cluster.
> 3. Describe the defining behavioral patterns.
> 4. Note whether these behavioral clusters align with the need patterns you might expect, or whether they diverge.
>
> Account for every participant. Note overlaps and ambiguous cases.
>
> Tag all your output with your agent ID: behavior-cluster-agent-[N]."

### Stage 2c: Barrier Clustering (5 agents)

> "You are barrier-cluster-agent-[N] (where N is 1-5). You have transcripts and participant profiles.
>
> Your task: group participants by the obstacles, fears, and constraints that shape their experience. Where need clustering looks at what participants want to achieve, barrier clustering looks at what prevents them from getting there.
>
> Focus on:
> - **Knowledge barriers:** Lack of information, jargon confusion, not knowing what is expected.
> - **Emotional barriers:** Anxiety, fear of making mistakes, feeling overwhelmed, dread of interaction.
> - **Structural barriers:** Process complexity, time constraints, cost, accessibility issues.
> - **Trust barriers:** Distrust of the system, skepticism about outcomes, past negative experiences.
>
> Propose 3-5 barrier clusters:
> 1. Give each cluster a descriptive name.
> 2. List the participants in each cluster.
> 3. Describe the primary barriers that define this cluster.
> 4. Note how these barriers relate to the needs and behaviors you observe in transcripts.
>
> Account for every participant.
>
> Tag all your output with your agent ID: barrier-cluster-agent-[N]."

### Stage 2d: Adversarial Clustering Review (5 agents)

> "You are adversarial-cluster-agent-[N] (where N is 1-5). You have transcripts and participant profiles.
>
> Your task is NOT to create clusters. Your task is to challenge the clustering process itself.
>
> Consider:
> - **Forcing people into groups:** Are we creating artificial segments? Would the data be better served by fewer clusters or more? Are some clusters actually just sub-segments of a larger group?
> - **Real segments or artifacts?** Do the clusters reflect genuine differences in need patterns, or are they artifacts of the sample (e.g., the clusters mirror the recruitment channels rather than real need differences)?
> - **Demographic contamination:** Are clusters secretly organized around demographics rather than needs? If every participant in a cluster happens to be the same age or role, the clustering may be demographic in disguise.
> - **Missing clusters:** Is there a participant group that current clustering approaches would miss? A minority pattern that does not fit the main clusters but represents a real, distinct need set?
> - **Cluster boundary challenges:** Pick the two clusters that seem most similar and argue that they should be merged. Pick the largest cluster and argue that it should be split. What evidence supports each argument?
> - **Over-fitting to prior analysis:** If JTBD or Pains & Gains data was used, are the clusters just reflecting the categories from those analyses rather than revealing new patterns in how needs combine across participants?
>
> For each challenge, cite specific transcript evidence. Propose an alternative clustering if your challenges are strong enough to warrant one.
>
> Tag all your output with your agent ID: adversarial-cluster-agent-[N]."

**Guided mode:** After all 20 agents complete, present:
- Clustering proposals from each lens (need, behavior, barrier)
- Where the three lenses agree and disagree on cluster composition
- Adversarial challenges and their implications
- Wait for user input on cluster count and composition

**Autopilot mode:** Log and proceed.

---

## Stage 3: Convergence Analysis (1 orchestrator)

Convergence for persona synthesis focuses on cluster consistency rather than individual finding counts.

1. **Compare cluster proposals across agents.** Count how many of the 20 agents placed each pair of participants in the same cluster. Build a participant co-occurrence matrix: for each pair of participants, record how many agents grouped them together.
2. **Identify stable clusters.** Participants who are grouped together by 12+ agents are stably clustered. Participants who are grouped together by 6-11 agents are in ambiguous territory. Participants grouped together by fewer than 6 agents are unlikely to belong to the same persona.
3. **Determine optimal cluster count.** Review the range of cluster counts proposed by agents. If most agents propose 3-4, that is the likely range. If there is strong disagreement (some say 3, some say 5), the adversarial analysis should inform the decision.
4. **Reconcile lens perspectives.** Check whether need clusters, behavior clusters, and barrier clusters align. Where they diverge (e.g., two participants share needs but have very different behaviors), this is important information for the persona description.
5. **Assign confidence scores.** Each persona cluster receives a confidence score based on the co-occurrence matrix: how consistently did agents group these participants together?

**Guided mode:** Present the co-occurrence matrix and proposed cluster structure. Wait for confirmation of cluster count and composition.

**Autopilot mode:** Use the clustering supported by the strongest co-occurrence data.

---

## Stage 4: Disagreement Deep-Dive (5 parallel agents)

Launch 5 agents to review clustering disagreements.

> "You are disagreement-agent-[N]. Review cases where agents disagreed about cluster assignment. For each ambiguous participant or contested cluster boundary:
> 1. Re-read the participant's transcript and profile.
> 2. Argue the case for placing them in Cluster A.
> 3. Argue the case for placing them in Cluster B.
> 4. Recommend: belongs in A / belongs in B / genuinely straddles both (document as overlap) / may represent a distinct cluster.
>
> Also review the adversarial challenges to the overall clustering structure. Are any challenges strong enough to change the cluster count?
>
> Tag all your output with your agent ID: disagreement-agent-[N]."

**Guided mode:** Present boundary decisions and overlap cases. Wait for user input.

**Autopilot mode:** Apply majority rule.

---

## Stage 4.5a: Quote Verification (5 parallel agents)

Verify all quotes that will be used in persona cards against original transcripts. Same procedure as JTBD protocol: Verified, Paraphrased, Out of context, Not found.

---

## Stage 4.5b: Inference Verification (5 parallel agents)

Verify whether the clustering inferences are supported by evidence. Specifically: does the evidence support that these participants genuinely share a need pattern, or has the clustering forced unrelated participants together? Statuses: Well-supported, Plausible but thin, Unsupported.

---

## Stage 4.5c: Disagreement Audit (5 parallel agents)

Audit disputed clustering decisions against verified evidence. Resolve where possible, retain genuine ambiguities as documented overlaps.

**Guided mode:** Present verification report. Wait for review.

**Autopilot mode:** Apply results and proceed.

---

## Stage 5: Synthesis & Deliverable (1 orchestrator)

Produce the final deliverable following `templates/output-formats/persona-card.md`.

### Synthesis steps:

1. **Build persona cards.** For each cluster, construct the persona card:
   - Archetype name (from the need clustering agents, refined by convergence)
   - Core orientation (one sentence)
   - Key jobs (3-5, from JTBD analysis if available, otherwise from extraction)
   - Primary pains (3-5, from Pains & Gains analysis if available, otherwise from extraction)
   - Primary gains (3-5, from Pains & Gains analysis if available, otherwise from extraction)
   - Representative quotes (2-3 per persona, verified)
   - Behavioral indicators (from behavior clustering)
   - Participant IDs in cluster
   - Confidence score

2. **Document persona overlaps.** For each pair of personas that share characteristics or have ambiguous participants, describe the shared elements, the key differentiator, and the ambiguous participants.

3. **Document clustering methodology.** Record: clustering basis, number of clusters, agent agreement statistics, merge decisions, split decisions, confidence assessment.

4. **Apply bias checks.** Run `protocols/bias-and-rigor.md`. Pay special attention to stereotype checks and demographic contamination.

5. **Apply prioritization.** Use `protocols/prioritization.md` to recommend which personas should be prioritized for design work, based on cluster size, evidence strength, and potential design impact.

6. **Build Verification Report.** Compile verification statistics.

7. **Write Executive Summary.** Maximum 200 words.

8. **Write Recommended Next Steps.** Tie recommendations to persona IDs and finding IDs from prior analyses.

9. **Generate Meta-Analysis Log.** Pipeline execution metadata.

10. **Generate CSV Export.** Columns: Persona ID, Archetype Name, Participant IDs, Confidence Score, Key Jobs, Primary Pains, Primary Gains.

**Guided mode:** Present complete deliverable for final review.

**Autopilot mode:** Save to `analysis/` directory.

---

## Output Files

| File | Description |
|------|-------------|
| `persona-synthesis.md` | Main deliverable following `templates/output-formats/persona-card.md` |
| `persona-meta-log.md` | Pipeline execution metadata |
| `persona-export.csv` | Structured data export |
