# Bias and Rigor Checklist

This checklist must be applied at three points in every analysis pipeline: before extraction begins (Stage 1), during convergence and synthesis (Stages 3-5), and as a final quality gate before the deliverable is finalized (Stage 5). Each item is a check to perform, not a rule to memorize. Work through them deliberately.

---

## Pre-Analysis Checks (Stage 1 -- Preparation)

Run these checks after reading the project scoping document and transcripts, before launching extraction agents.

- [ ] **Sample bias.** Review the participant composition in `templates/project-scoping.md`. Who is represented? Who is missing? Note any segments that are absent -- non-users, extreme users, specific demographics, geographies, or roles. Record these gaps explicitly so that findings are not overgeneralized to populations not represented in the sample.

- [ ] **Recruitment bias.** How were participants recruited? Self-selection (volunteers) tends to skew toward people with strong opinions. Client-recruited samples may over-represent satisfied customers. Referral chains may produce homogeneous perspectives. Note the recruitment method and its likely directional bias.

- [ ] **Interview bias.** Read the interview guide summary in the scoping document. Were questions leading? ("Don't you think the checkout is confusing?" vs. "Walk me through your checkout experience.") Were certain topics probed more deeply than others? Was the same moderator used for all sessions? Note any patterns that could systematically shape what participants said.

- [ ] **Hypothesis contamination.** If the scoping document lists hypotheses, note them. The adversarial lens (Stage 2d) should specifically scrutinize findings that conveniently confirm pre-stated hypotheses. Hypotheses are useful for calibrating scrutiny, not for guiding extraction.

- [ ] **Prior analysis influence.** If prior analyses (JTBD, Pains & Gains) are being used as input, note that extraction agents may anchor on prior findings rather than discovering new patterns. Instruct agents to treat prior analyses as context, not constraints, unless the protocol explicitly requires otherwise.

---

## During-Analysis Checks (Stages 3-5 -- Convergence, Deep-Dive, Synthesis)

Run these checks during convergence analysis and when reviewing agent outputs.

- [ ] **Confirmation bias.** Are you (or the agents) finding what you expected to find? Review the scoping document's hypotheses and check: are there findings that disconfirm them? If every finding aligns with prior expectations, the analysis may be confirming rather than discovering. Actively search for disconfirming evidence in the transcripts.

- [ ] **Anchoring bias.** Did the first few findings extracted set the frame for everything that followed? In multi-agent pipelines, check whether agents converge because they independently found the same pattern, or because early-identified themes dominated the conceptual space. Look for findings that only appeared in later agent runs or minority lenses.

- [ ] **Availability bias.** Are the most vivid, emotional, or dramatic participant stories disproportionately shaping findings? A participant who told a compelling story may be over-represented in the evidence index. Count how many findings rely on the same participant. If one participant's quotes appear in more than 30% of findings, investigate whether other participants' data was underweighted.

- [ ] **Groupthink in multi-agent context.** In a multi-agent pipeline, groupthink manifests as artificial convergence -- agents producing similar outputs not because the evidence demands it but because the prompt framing or shared context nudges them toward the same conclusions. Check whether high-convergence findings are genuinely supported by diverse transcript evidence or whether they reflect prompt-induced agreement. The adversarial lens exists specifically to counter this.

- [ ] **Premature closure.** Did the analysis stop too early? Are there transcript sections that were not explored? Themes that were mentioned once and then dropped? Contradictions that were noted but not investigated? Before finalizing convergence, scan transcripts for material that does not fit any current finding. Unclassified material may contain the most important insights.

- [ ] **Cultural and contextual flattening.** Are findings collapsing important differences between participant contexts? A finding that applies to Dutch participants may not apply to participants in Abu Dhabi. A pattern among experienced users may not hold for first-time users. Check whether the evidence base for each finding spans the relevant contextual variations in the sample.

- [ ] **Severity distortion.** Are minor annoyances being presented with the same weight as serious barriers? Check that the language and prominence of findings reflects their actual severity as expressed by participants, not the analyst's sense of importance.

---

## Post-Analysis Checks (Stage 5 -- Before Finalizing Deliverable)

Run these checks on the complete draft deliverable before it is finalized.

- [ ] **Evidence trail completeness.** For every finding in the deliverable, trace the chain: transcript quote -> agent extraction -> convergence count -> verification status -> final finding statement. If any link in the chain is missing, the finding is not ready for the deliverable.

- [ ] **Disconfirming evidence reported.** Check the Tensions & Conflicts section (or equivalent). Does it include findings where evidence was mixed or contradictory? A deliverable with no tensions is suspicious -- it may mean disagreements were suppressed rather than absent. Every deliverable should report at least the tensions identified by the adversarial lens.

- [ ] **Confidence calibration.** Review the distribution of High / Medium / Low confidence findings. A deliverable where every finding is High confidence is likely miscalibrated. Conversely, a deliverable where everything is Low confidence may indicate insufficient data or overly conservative scoring. The distribution should feel proportionate to the data quality and sample size.

- [ ] **Generalization scope.** Check every finding statement for scope creep. Does the finding say "users want" when it should say "the 8 participants in this study described"? Does it claim universality when the evidence comes from one segment? Ensure finding language matches the evidence scope. Refer to the language preferences in `knowledge-base/brand/tone-of-voice.md`.

- [ ] **Actionability check.** Review each finding and ask: can a design team do something with this? Findings that describe a state without implying a direction ("participants have varying levels of digital literacy") are context, not findings. Either reframe them as actionable insights or move them to background context.

- [ ] **Anonymization compliance.** Before the deliverable is finalized, verify that all participant references use IDs (P01, P02, etc.) and that no direct or indirect identifiers remain in quotes or descriptions. Follow the guidelines in `knowledge-base/ethics/anonymization.md`.

- [ ] **Ethical review.** Confirm that participant quotes are used in context, sensitive disclosures are handled with appropriate care, and no participant's words are used to support a claim they did not intend. Follow `knowledge-base/ethics/research-ethics.md`.

---

## How to Use This Checklist

This is not a form to fill out and file. It is a thinking tool. At each checkpoint in the pipeline, work through the relevant section item by item. When a check reveals an issue, act on it:

- If sample bias is significant, add a caveat to the executive summary and scope every finding appropriately.
- If confirmation bias is detected, return to the transcripts and specifically search for disconfirming evidence.
- If evidence trails are incomplete, do not publish the finding -- send it back for verification or remove it.

The checklist is referenced by name in every protocol at the stages where it applies. It is not optional.
