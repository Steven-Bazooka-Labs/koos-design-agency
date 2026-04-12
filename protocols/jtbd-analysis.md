# JTBD Analysis Protocol

This protocol defines the complete execution pipeline for Jobs to Be Done analysis. It produces a deliverable following the template at `templates/output-formats/jtbd-output.md`. The pipeline uses 43 agent runs across 11 stages.

**Protocol dependency:** None. JTBD analysis is fully independent and requires no prior analyses as input.

---

## Stage 1: Preparation (1 orchestrator)

Read and internalize the following documents in order:

1. `CLAUDE.md` (project phase instructions, if present in the project root or phase directory)
2. `templates/project-scoping.md` (filled-in version in the project/phase directory -- research questions, hypotheses, participant composition, known constraints)
3. All interview transcripts in the project's data directory
4. `methodologies/jobs-to-be-done.md` (JTBD methodology reference)
5. `knowledge-base/glossary.md` (term definitions -- especially Job to Be Done, Insight, Finding, Observation)
6. `knowledge-base/ethics/anonymization.md` (anonymization requirements)
7. `knowledge-base/ethics/research-ethics.md` (contextual integrity, honest representation, disconfirming evidence)
8. `protocols/quality-criteria.md` (evidence bar, strong vs. weak finding definitions)
9. `protocols/bias-and-rigor.md` (run the Pre-Analysis Checks section)

Check the `analysis/` folder in the project directory for prior analyses. If JTBD has already been run, confirm with the user whether this is a re-analysis or an error. If Pains & Gains, Persona, or Journey Map analyses exist, note them as available context but do not treat them as input -- JTBD extraction is independent.

Run the Pre-Analysis Checks from `protocols/bias-and-rigor.md`. Record:
- Sample size and composition gaps
- Recruitment method and its likely bias
- Interview guide structure and any leading questions
- Pre-stated hypotheses (these will be passed to the adversarial lens)

**Guided mode:** Present the following summary to the user and wait for confirmation before proceeding:
- Number of transcripts and participants
- Research questions from the scoping document
- Any sample biases or constraints identified
- Pre-stated hypotheses that the adversarial lens will scrutinize
- Confirmation that the user wants to proceed with JTBD analysis

**Autopilot mode:** Log the preparation summary and proceed directly to Stage 2.

---

## Stage 2: Extraction (20 parallel agents -- 4 lenses x 5 agents each)

Launch all 20 extraction agents in parallel. Each agent receives the full set of transcripts, the JTBD methodology reference, the glossary, and the quality criteria document. Each agent works independently and does not see the output of any other agent.

### Stage 2a: Obvious/Explicit Lens (5 agents)

Dispatch each agent with the following instruction:

> "You are obvious-agent-[N] (where N is 1-5). Read all transcripts provided. Extract every job to be done that participants directly and explicitly articulate. These are jobs participants can name and describe themselves.
>
> For each job, use the Koos JTBD format: 'When [situation/trigger], I want to [motivation/desired progress], so I can [expected outcome/benefit].'
>
> For each job you extract:
> - Write the full job statement in the format above.
> - Classify the job type: Functional, Emotional, or Social.
> - Cite the exact supporting quote(s) from the transcript, with participant ID (e.g., P01, P02).
> - Note the transcript location (file name and line number or timestamp).
> - Assess whether this is a main job or a related job.
>
> Only extract jobs that the participant explicitly described. Do not infer jobs from behavior or read between the lines -- that is the task of other lenses. If a participant directly says what they are trying to achieve, in what situation, and why it matters, that is your target.
>
> Apply the evidence bar from quality-criteria.md: strong jobs are specific, evidenced, non-obvious, and actionable. Flag any job you extract that you suspect may be too vague or too obvious.
>
> Tag all your output with your agent ID: obvious-agent-[N]."

### Stage 2b: Implicit/Latent Lens (5 agents)

Dispatch each agent with the following instruction:

> "You are implicit-agent-[N] (where N is 1-5). Read all transcripts provided. Extract jobs to be done that participants did NOT directly state but that are implied by their behavior, workarounds, frustrations, and choices.
>
> Look for:
> - **Workarounds:** When a participant describes creating their own system, using a tool in an unintended way, or going outside the official process, ask: what job is this workaround trying to accomplish?
> - **Frustrations implying unmet goals:** When a participant expresses frustration, ask: what progress were they trying to make that was blocked?
> - **Behaviors revealing unstated objectives:** When a participant describes what they actually do (as opposed to what the system expects them to do), ask: what underlying job does this behavior serve?
> - **Repeated checking or monitoring:** When a participant describes checking something repeatedly, ask: what job is the monitoring serving? What uncertainty are they trying to resolve?
>
> For each job, use the Koos JTBD format: 'When [situation/trigger], I want to [motivation/desired progress], so I can [expected outcome/benefit].'
>
> For each job you extract:
> - Write the full job statement.
> - Classify the job type: Functional, Emotional, or Social.
> - Explain the inference: what behavior or statement led you to identify this job? What is the reasoning chain from observation to job?
> - Cite the exact supporting quote(s) with participant ID.
> - Note the transcript location.
>
> Be explicit about the gap between what the participant said and what you are inferring. Label your inferences clearly. The goal is to surface jobs that participants themselves might not articulate but that demonstrably drive their behavior.
>
> Tag all your output with your agent ID: implicit-agent-[N]."

### Stage 2c: Emotional & Social Lens (5 agents)

Dispatch each agent with the following instruction:

> "You are emotional-agent-[N] (where N is 1-5). Read all transcripts provided. Extract emotional jobs (how participants want to feel or avoid feeling) and social jobs (how participants want to be perceived or avoid being perceived).
>
> Look for:
> - **Emotional language:** Words describing feelings -- anxiety, relief, confidence, frustration, pride, embarrassment, calm, dread, hope. When a participant describes an emotion, ask: what emotional progress are they trying to make?
> - **Identity references:** Statements about who the participant is or wants to be -- 'I'm the kind of person who...', 'I don't want to be seen as...', 'As a parent/professional/caregiver, I need to...'
> - **Vulnerability:** Moments where participants reveal insecurity, fear of judgment, or loss of control. These often signal powerful emotional or social jobs.
> - **Pride and satisfaction:** Moments where participants describe feeling good about an interaction or outcome. What emotional or social job was fulfilled?
> - **Avoidance behaviors:** When participants describe going out of their way to avoid a situation, ask: what negative emotional or social outcome are they trying to prevent?
>
> For each job, use the Koos JTBD format: 'When [situation/trigger], I want to [motivation/desired progress], so I can [expected outcome/benefit].'
>
> For each job you extract:
> - Write the full job statement.
> - Classify the job type: Emotional or Social (not Functional -- that is covered by other lenses).
> - Cite the exact supporting quote(s) with participant ID.
> - Note the transcript location.
> - Describe the emotional or social dynamic at play.
>
> If a transcript contains no emotional or social jobs, say so explicitly rather than fabricating them. But in most qualitative research, emotional and social dimensions are present -- they simply require more attentive reading to surface.
>
> Tag all your output with your agent ID: emotional-agent-[N]."

### Stage 2d: Adversarial Lens (5 agents)

Dispatch each agent with the following instruction:

> "You are adversarial-agent-[N] (where N is 1-5). Read all transcripts provided. Your task is NOT to extract the most likely jobs to be done. Your task is to find jobs that COMPLICATE, CONTRADICT, or CHALLENGE the obvious interpretation of the data.
>
> Specifically, look for:
> - **Minority perspectives:** Jobs expressed by only 1-2 participants that contradict the majority pattern. These may be edge cases or they may reveal important segments.
> - **Tensions between jobs:** Cases where a participant (or different participants) holds jobs that conflict with each other. For example: wanting full control AND wanting someone else to handle everything. Wanting comprehensive information AND wanting simplicity.
> - **Contextual variations:** Cases where the same nominal job changes meaning in different contexts. The 'same' job at work vs. at home, for a first-timer vs. an experienced user, in a routine situation vs. a crisis.
> - **Over-interpreted data:** Passages in the transcripts where a straightforward statement might be read as a deeper job than the participant intended. Where are we at risk of over-reading?
> - **Hypothesis-confirming patterns:** Review the pre-stated hypotheses from the scoping document. Are there findings that seem to confirm them too neatly? What alternative explanations exist?
>
> For each finding:
> - State the tension, contradiction, or complication clearly.
> - Note what it tensions against (which obvious interpretation it challenges).
> - Cite the exact supporting quote(s) with participant ID.
> - Note the transcript location.
> - Recommend: is this a genuine tension worth reporting, a minority perspective worth preserving, or a potential over-interpretation to flag?
>
> You are the quality control layer. If the other 15 agents converge on a clean narrative, your job is to test whether that narrative survives scrutiny. Do not be contrarian for its own sake -- be contrarian where the evidence warrants it.
>
> Tag all your output with your agent ID: adversarial-agent-[N]."

**Guided mode:** After all 20 agents complete, present a summary to the user:
- Total jobs extracted across all agents (before deduplication)
- Breakdown by lens: how many jobs from obvious, implicit, emotional, adversarial
- Any notable tensions or contradictions flagged by the adversarial lens
- Wait for user confirmation before proceeding to convergence

**Autopilot mode:** Log the summary and proceed to Stage 3.

---

## Stage 3: Convergence Analysis (1 orchestrator)

Collect all output from the 20 extraction agents. Perform the following steps:

1. **Deduplicate.** Group semantically equivalent jobs. Two job statements are equivalent if they describe the same situation, motivation, and outcome, even if they use different words. Do not merge jobs that share a motivation but differ in situation or outcome -- those are distinct jobs.

2. **Count runs.** For each unique job, count how many of the 20 agents independently identified it (or a semantically equivalent version). Record which specific agents identified it (e.g., obvious-agent-1, implicit-agent-3, emotional-agent-5).

3. **Assign confidence tiers.**
   - High: 12+ of 20 runs
   - Medium: 6-11 of 20 runs
   - Low: 1-5 of 20 runs

4. **Track cross-lens presence.** For each job, note which lenses identified it. A job found across 3-4 lenses is more robust than one found only within a single lens, even at the same run count. Record the lens breakdown: Obvious [X]/5, Implicit [X]/5, Emotional [X]/5, Adversarial [X]/5.

5. **Build the convergence matrix.** Create a table listing every unique job with: job statement, job type, confidence tier, total run count, lens breakdown, and all supporting participant IDs.

6. **Identify tensions.** Review adversarial agent output. Map tensions and contradictions to the convergence matrix. Note which high-confidence findings have adversarial challenges and what those challenges are.

7. **Count participant coverage.** For each job, count how many unique participants provided supporting evidence. A job with 15/20 run agreement but evidence from only 2 participants is less robust than it appears.

**Guided mode:** Present the convergence matrix to the user, highlighting:
- High confidence findings and their cross-lens profiles
- Medium confidence findings that are close to the High threshold
- Tensions and contradictions from the adversarial lens
- Any findings with high run counts but low participant coverage
- Wait for user input before proceeding

**Autopilot mode:** Log the matrix and proceed to Stage 4.

---

## Stage 4: Disagreement Deep-Dive (5 parallel agents)

Launch 5 agents to review findings that are in the Medium or Low confidence tier, or that have adversarial challenges. Each agent receives the convergence matrix, all original agent outputs, and the full transcripts.

Dispatch each agent with the following instruction:

> "You are disagreement-agent-[N] (where N is 1-5). You are reviewing findings where the 20 extraction agents did not reach consensus. For each Medium and Low confidence finding, and for each adversarial challenge to a High confidence finding:
>
> 1. Re-read the relevant transcript passages.
> 2. Argue the case FOR this being a valid finding. What evidence supports it?
> 3. Argue the case AGAINST this being a valid finding. What evidence contradicts it or suggests it is noise?
> 4. Map any tensions: does this finding conflict with other findings? Is the conflict real (participants genuinely disagree) or artificial (different ways of saying the same thing)?
> 5. Recommend one of three classifications:
>    - **Likely valid:** The evidence, while not overwhelming, supports this finding. Retain it with appropriate confidence labeling.
>    - **Likely noise:** The evidence is too thin, too ambiguous, or too dependent on a single data point. Remove or downgrade.
>    - **Needs human judgment:** The evidence is genuinely ambiguous. Present both sides to the human analyst and let them decide.
>
> Support every recommendation with specific transcript evidence. Do not decide based on gut feeling -- show the evidence trail.
>
> Tag all your output with your agent ID: disagreement-agent-[N]."

**Guided mode:** Present the disagreement analysis to the user:
- Findings classified as "likely valid" by majority of disagreement agents
- Findings classified as "likely noise" by majority
- Findings classified as "needs human judgment"
- Specific tensions and conflicts with evidence from both sides
- Wait for user decisions on ambiguous findings

**Autopilot mode:** Apply majority rule (3+ of 5 agents agree) for "likely valid" and "likely noise." Retain "needs human judgment" findings in the deliverable with explicit flags.

---

## Stage 4.5a: Quote Verification (5 parallel agents)

Launch 5 agents to verify every quote cited in the current finding set against the original transcripts.

Dispatch each agent with the following instruction:

> "You are quote-verifier-[N] (where N is 1-5). You have the complete set of findings with their cited quotes AND the original interview transcripts.
>
> For every quote cited in support of a finding:
> 1. Locate the quote in the original transcript.
> 2. Compare the cited version with the original.
> 3. Assign one of four statuses:
>    - **Verified:** The quote matches the transcript exactly or with trivial variation (punctuation, filler words).
>    - **Paraphrased:** The quote captures the participant's meaning accurately but uses different words. Note the original wording.
>    - **Out of context:** The quote exists in the transcript but is being used to support a claim the participant did not intend. Explain the original context.
>    - **Not found:** The quote cannot be located in any transcript. It may be fabricated or severely misremembered.
>
> Report your verification results for every quote. Do not skip any.
>
> Tag all your output with your agent ID: quote-verifier-[N]."

After all 5 verifiers complete, consolidate results using majority rule (3+ of 5 must agree on a status). For any finding whose supporting quotes are ALL classified as "out of context" or "not found" by majority, remove the finding from the deliverable.

---

## Stage 4.5b: Inference Verification (5 parallel agents)

Launch 5 agents to verify whether the evidence actually supports each inference made in the findings.

Dispatch each agent with the following instruction:

> "You are inference-verifier-[N] (where N is 1-5). You have the complete set of findings and the original transcripts.
>
> For each finding that involves an inference (particularly findings from the implicit and emotional lenses), evaluate whether the cited evidence logically supports the stated conclusion.
>
> Assign one of three statuses:
> - **Well-supported:** The evidence clearly supports the inference. The reasoning chain from quote to conclusion is sound.
> - **Plausible but thin:** The inference is reasonable but relies on a single data point, a generous reading of the quote, or a logical leap that is not fully justified. Flag what additional evidence would be needed.
> - **Unsupported:** The inference does not follow from the evidence. The quote does not say what the finding claims it says, or the reasoning chain has a gap.
>
> For each inference, explain your reasoning. Show why the evidence does or does not support the conclusion.
>
> Tag all your output with your agent ID: inference-verifier-[N]."

After all 5 verifiers complete, consolidate results using majority rule (3+ of 5). Findings classified as "unsupported" by majority are removed from the deliverable. Findings classified as "plausible but thin" by majority are retained but downgraded one confidence tier (High becomes Medium, Medium becomes Low, Low is flagged for human review).

---

## Stage 4.5c: Disagreement Audit (5 parallel agents)

Launch 5 agents to audit the disputed findings from Stage 4, checking whether the disagreements are based on verified evidence.

Dispatch each agent with the following instruction:

> "You are disagreement-auditor-[N] (where N is 1-5). You have the Stage 4 disagreement analysis results, the Stage 4.5a quote verification results, and the Stage 4.5b inference verification results.
>
> For each finding that was disputed in Stage 4:
> 1. Check whether the evidence cited by BOTH sides of the disagreement passed quote verification.
> 2. Check whether the inferences on BOTH sides passed inference verification.
> 3. If one side's evidence was verified and the other's was not, the disagreement is resolved in favor of verified evidence.
> 4. If both sides have verified evidence, the disagreement is genuine and should be reported as a tension in the deliverable.
> 5. If neither side has verified evidence, the finding should be removed.
>
> For each disputed finding, state your conclusion:
> - **Resolved -- evidence favors [side]:** One side has verified evidence; the other does not.
> - **Genuine tension:** Both sides have verified evidence. Report in the Tensions section.
> - **Removed -- insufficient evidence:** Neither side has verified evidence.
>
> Tag all your output with your agent ID: disagreement-auditor-[N]."

After all 5 auditors complete, consolidate using majority rule.

**Guided mode:** Present the complete verification report to the user:
- Quote verification summary (% verified, paraphrased, out of context, not found)
- Inference verification summary (% well-supported, plausible but thin, unsupported)
- Disagreement audit results (resolved, genuine tensions, removed)
- List of findings removed or downgraded as a result of verification
- Wait for user review before proceeding to synthesis

**Autopilot mode:** Apply majority-rule results and proceed to Stage 5.

---

## Stage 5: Synthesis & Deliverable (1 orchestrator)

Produce the final deliverable following the template at `templates/output-formats/jtbd-output.md`. This stage integrates all prior outputs into a polished, client-ready document.

### Step 5.1: Compile verified findings

Assemble the final list of findings from the verified, post-audit convergence matrix. Organize by confidence tier (High, Medium, Low). For each finding, include:
- Job statement in Koos format
- Job type (Functional, Emotional, Social)
- Confidence score (X/20 runs)
- Lens breakdown
- All verified supporting quotes with participant IDs
- Notes from adversarial and disagreement analysis

### Step 5.2: Apply bias checks

Run the During-Analysis and Post-Analysis sections of `protocols/bias-and-rigor.md` on the compiled findings. Specifically:
- Check for confirmation bias against the scoping document hypotheses
- Check for availability bias (is one participant over-represented?)
- Verify evidence trail completeness for every finding
- Confirm disconfirming evidence is reported
- Check confidence calibration
- Check generalization scope in finding language
- Verify anonymization compliance

### Step 5.3: Apply prioritization

Score every finding on the three axes defined in `protocols/prioritization.md`:
- Evidence strength (derived from convergence data)
- Potential impact (assessed from participant language and behavioral evidence)
- Frequency (counted from unique participant coverage)

Assign priority classifications: Immediate, Strong opportunity, Worth exploring, Monitor, Human review. Build the prioritization matrix table.

### Step 5.4: Build the Tensions & Conflicts section

Document all genuine tensions identified through the adversarial lens, disagreement deep-dive, and disagreement audit. For each tension:
- Which jobs are in conflict
- The nature of the conflict
- Which participants or segments are affected
- The design implication

### Step 5.5: Build the Verification Report

Compile the verification statistics from Stages 4.5a, 4.5b, and 4.5c into the verification report table, covering quote verification rates, inference verification rates, and disagreement audit outcomes.

### Step 5.6: Build the Evidence Index

Create the complete evidence index mapping every finding to its source evidence: finding ID, quote, participant ID, transcript location, verification status.

### Step 5.7: Write the Executive Summary

Write the executive summary last, after all other sections are complete. Maximum 200 words. Summarize: number of jobs by confidence tier, the 2-3 most significant findings, any critical tensions, and the overall confidence landscape. Follow the writing standards in `knowledge-base/brand/tone-of-voice.md` and `knowledge-base/brand/deliverable-standards.md`.

### Step 5.8: Write the Methodology Note

Document the analysis process: 4 lenses x 5 agents = 20 extraction runs, convergence analysis, 5-agent disagreement deep-dive, 15 verification agent runs, synthesis. Total: 43 agent runs.

### Step 5.9: Write Recommended Next Steps

Tie each recommendation to specific finding IDs. Categorize as "evidence strongly supports" or "recommend exploring" per `knowledge-base/brand/deliverable-standards.md`.

### Step 5.10: Generate the Meta-Analysis Log

Record the pipeline execution metadata: which agents ran, when, what they found, how convergence was determined, what was removed during verification, and any adjustments made during synthesis.

### Step 5.11: Generate the CSV Export

Produce a structured CSV with columns: Finding ID, Job Statement, Job Type, Confidence Tier, Run Count, Lens Breakdown, Participant IDs, Priority Classification, Verification Status.

**Guided mode:** Present the complete deliverable to the user for final review. Highlight:
- Executive summary
- High confidence findings with their priority classifications
- Tensions and conflicts
- Verification report statistics
- Any findings flagged for human review
- Wait for final approval or revision requests

**Autopilot mode:** Save the deliverable to the `analysis/` directory in the project folder. Log completion.

---

## Output Files

The protocol produces the following outputs in the project's `analysis/` directory:

| File | Description |
|------|-------------|
| `jtbd-analysis.md` | Main deliverable following `templates/output-formats/jtbd-output.md` |
| `jtbd-evidence-index.md` | Complete evidence index (may be inline in the main deliverable) |
| `jtbd-verification-report.md` | Verification statistics (may be inline in the main deliverable) |
| `jtbd-meta-log.md` | Pipeline execution metadata |
| `jtbd-export.csv` | Structured data export |
