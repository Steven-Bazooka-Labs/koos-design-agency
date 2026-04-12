# Koos AI-Augmented Research Analysis Framework — Design Spec

## Context

**Client:** Koos design agency (koos.agency) — ~40 person service design, UX, and human-centered AI agency. Offices in Amsterdam and Abu Dhabi. B Corp certified. 15-year track record. Clients include Careem, Siemens, VW, NS, Philips, OLX, ING, Amsterdam Municipality, VGZ, KLM, Randstad, Rijkswaterstaat.

**Builder:** Bazooka Labs (bazookalabs.nl) — custom software house specializing in AI.

**Purpose:** A proof-of-concept demo repo that shows Koos how AI can standardize their research analysis workflows. The demo should sell a full engagement where Bazooka Labs builds the production version.

**The problem:** Koos's designers are all using AI in their own ways — different tools, different prompts, different quality bars. Research analysis (transcript analysis, insight extraction, persona building) is time-intensive, inconsistent across team members, and hard to quality-control. There is no standardized methodology encoded anywhere.

**The solution:** A git repo that encodes Koos's methodologies, quality standards, tone of voice, and analysis protocols. Designers connect it to Claude Desktop as a knowledge base. When they need to analyze research, Claude follows Koos's own protocols — running multi-agent pipelines with built-in evidence verification and quality control.

**Demo audience:** The CEO + 2-3 senior designers/researchers. They'll receive the repo in advance and walk through it together with Bazooka Labs. The CEO needs to see business value; the senior designers need to feel the methodology is rigorous.

**Timeline:** Not yet scheduled. Repo should be solid, not rushed.

**Target aha moments:**
1. Speed — "It analyzed 10 transcripts in minutes, not days"
2. The meta-analysis — "It ran the analysis 20 times, showed convergence and disagreement, verified its own evidence, and flagged what needs human review"
3. The system — "This isn't a prompt trick — it's infrastructure we could own and extend"

---

## Approach

Pure markdown + CLAUDE.md files (Approach A). Everything lives in `.md` files. No MCP servers, no external tooling, no dependencies. Works immediately when connected to Claude Desktop. The repo IS the product — transparent, auditable, versionable, and extensible by Koos.

Stretch goal: add Claude Code slash commands (`.claude/commands/`) for the most polished pipelines.

---

## Repository Structure

```
koos-design-agency/
├── README.md
├── CLAUDE.md
│
├── docs/
│   └── architecture.md
│
├── knowledge-base/
│   ├── company/
│   │   ├── about-koos.md
│   │   └── sectors.md
│   ├── brand/
│   │   ├── tone-of-voice.md
│   │   └── deliverable-standards.md
│   ├── ethics/
│   │   ├── research-ethics.md
│   │   └── anonymization.md
│   └── glossary.md
│
├── methodologies/
│   ├── jobs-to-be-done.md
│   ├── pains-and-gains.md
│   ├── needs-based-personas.md
│   └── customer-journey-mapping.md
│
├── protocols/
│   ├── README.md
│   ├── jtbd-analysis.md
│   ├── pains-gains-analysis.md
│   ├── persona-synthesis.md
│   ├── journey-mapping.md
│   ├── quality-criteria.md
│   ├── bias-and-rigor.md
│   └── prioritization.md
│
├── templates/
│   ├── project-scoping.md
│   └── output-formats/
│       ├── jtbd-output.md
│       ├── pains-gains-output.md
│       ├── persona-card.md
│       └── journey-map-output.md
│
├── projects/
│   ├── amsterdam-municipality/
│   │   ├── CLAUDE.md
│   │   ├── context/
│   │   │   ├── client-brief.md
│   │   │   ├── stakeholder-notes.md
│   │   │   └── desk-research.md
│   │   ├── 1-discover/
│   │   │   ├── CLAUDE.md
│   │   │   ├── scoping.md
│   │   │   ├── transcripts/
│   │   │   │   ├── participant-01.md
│   │   │   │   ├── participant-02.md
│   │   │   │   ├── participant-03.md
│   │   │   │   ├── participant-04.md
│   │   │   │   ├── participant-05.md
│   │   │   │   ├── participant-06.md
│   │   │   │   ├── participant-07.md
│   │   │   │   ├── participant-08.md
│   │   │   │   ├── participant-09.md
│   │   │   │   └── participant-10.md
│   │   │   └── analysis/
│   │   │       └── .gitkeep
│   │   ├── 2-define/
│   │   │   ├── CLAUDE.md
│   │   │   ├── inputs/
│   │   │   │   └── .gitkeep
│   │   │   └── outputs/
│   │   │       └── .gitkeep
│   │   ├── 3-develop/
│   │   │   ├── CLAUDE.md
│   │   │   └── ...
│   │   └── 4-deliver/
│   │       ├── CLAUDE.md
│   │       └── ...
│   │
│   ├── vgz-healthcare/
│   │   ├── CLAUDE.md
│   │   ├── context/
│   │   │   ├── client-brief.md
│   │   │   ├── stakeholder-notes.md
│   │   │   └── desk-research.md
│   │   ├── 1-discover/
│   │   │   ├── CLAUDE.md
│   │   │   └── ...
│   │   ├── 2-define/
│   │   │   ├── CLAUDE.md
│   │   │   └── ...
│   │   ├── 3-develop/
│   │   │   ├── CLAUDE.md
│   │   │   ├── scoping.md
│   │   │   ├── transcripts/
│   │   │   │   ├── participant-01.md
│   │   │   │   └── ... (10 transcripts)
│   │   │   └── analysis/
│   │   │       └── .gitkeep
│   │   └── 4-deliver/
│   │       ├── CLAUDE.md
│   │       └── ...
│   │
│   └── ns-railways/
│       ├── CLAUDE.md
│       ├── context/
│       │   ├── client-brief.md
│       │   ├── stakeholder-notes.md
│       │   └── desk-research.md
│       ├── 1-discover/
│       │   ├── CLAUDE.md
│       │   └── ...
│       ├── 2-define/
│       │   ├── CLAUDE.md
│       │   └── ...
│       ├── 3-develop/
│       │   ├── CLAUDE.md
│       │   └── ...
│       └── 4-deliver/
│           ├── CLAUDE.md
│           ├── scoping.md
│           ├── transcripts/
│           │   ├── participant-01.md
│           │   └── ... (10 transcripts)
│           └── analysis/
│               └── .gitkeep
│
└── examples/
    └── vgz-sample-analysis/
        ├── jtbd-analysis.md
        ├── pains-gains-analysis.md
        ├── persona-cards.md
        ├── journey-map.md
        ├── verification-report.md
        ├── meta-analysis-log.md
        └── exports/
            ├── personas.csv
            ├── jtbd-matrix.csv
            └── pains-gains-matrix.csv
```

---

## README.md

The front door to the repo. Structured to persuade, not just inform.

### Section 1: The Why — The Problem You're Living With

Frame the pain Koos is experiencing:
- Designers are talented researchers, but every one of them analyzes transcripts differently
- Two designers analyzing the same interviews produce different insights — not because one is wrong, but because humans anchor on different things, get fatigued, and can't systematically cross-reference 10 transcripts
- Analysis takes days. Quality is inconsistent. Knowledge leaves when people leave. There's no institutional methodology ensuring the same rigor every time.
- AI is already being used — but everyone uses their own prompts, tools, and approach. The inconsistency problem is getting worse, not better.

### Section 2: The Painkiller

- What if your best researcher's methodology was encoded, standardized, and available to everyone — running at machine speed with built-in quality control no human has the patience to do manually?
- Not replacing researchers. Giving them a system that handles the systematic work at inhuman rigor, so they can focus on the interpretive, creative, strategic work that requires human judgment.

### Section 3: What It Is and How It Works

- Architecture overview with pipeline diagram
- Repo structure at a glance
- How the CLAUDE.md layering works

### Section 4: What It Produces

- Four analysis types
- Structured deliverables with confidence levels and evidence trails
- Export formats for design tools

### Section 5: How to Use It

- Step-by-step getting started guide

### Section 6: What's Inside

- Quick directory guide

---

## Root CLAUDE.md

The file that shapes all of Claude's behavior when connected to this repo.

### 1. Identity & Orientation

- "You are a research analyst working within Koos's methodology framework. You follow Koos's established protocols, use Koos's terminology, and produce deliverables that match Koos's quality standards and tone of voice."
- Points to `knowledge-base/` for company context, brand, glossary, ethics
- Instructs Claude to always use glossary terms consistently

### 2. Available Capabilities

- Lists the four analysis types (JTBD, Pains & Gains, Personas, Journey Mapping)
- Points to their protocol files in `protocols/`
- One-sentence description of each

### 3. Two Modes

- **Autopilot mode**: User requests a full analysis. Claude reads the protocol, executes all stages including 20 parallel agent runs, convergence, verification, and produces the final deliverable without pausing. Outputs to the project's `analysis/` folder.
- **Guided mode** (default): Same protocol, but Claude pauses after each major stage — shows intermediate results, asks for input, lets the user steer before proceeding.
- Default is guided mode. User explicitly requests autopilot.

### 4. Project Context Awareness

- Always check for a project-level CLAUDE.md and phase-level CLAUDE.md
- Always check for a scoping.md before starting analysis
- If no scoping doc exists, ask the user to fill one in using the template

### 5. Output Standards

- All outputs go to the project phase's `analysis/` folder
- Follow templates in `templates/output-formats/`
- Always include evidence quotes with participant IDs
- Always include confidence levels
- Generate CSV exports alongside markdown
- Respect anonymization guidelines

### 6. Quality Guardrails

- Run bias checks from `protocols/bias-and-rigor.md` before finalizing
- Apply quality criteria from `protocols/quality-criteria.md`
- Apply prioritization from `protocols/prioritization.md`
- Flag findings with fewer than 2 supporting quotes

---

## Knowledge Base (10 documents)

### 1. `knowledge-base/company/about-koos.md`

Who Koos is: ~40 people, B Corp certified, Amsterdam + Abu Dhabi, 15-year track record. Three pillars: Service Design, UX/UI Design, Human-Centered AI. Mission: "Your catalyst for change." Key client stats demonstrating scale and impact. Not a sales document — gives Claude context to calibrate tone and understand who it's working for.

### 2. `knowledge-base/company/sectors.md`

The six sectors Koos works in: Public Sector, Big Tech, Healthcare, Mobility, Finance, Energy. For each: typical problems Koos solves, who the stakeholders are, domain sensitivities (healthcare = patient privacy, public sector = inclusivity and accessibility, finance = regulatory constraints). Helps Claude contextualize findings appropriately per domain.

### 3. `knowledge-base/brand/tone-of-voice.md`

How Koos writes and speaks:
- Professional but warm, not corporate
- Evidence-driven, never speculative without flagging it
- Clear and visual — structured layouts and concrete examples over walls of text
- Empathetic toward research participants — they're people, not data points
- Dutch directness — concise, no fluff, never cold
- 3-4 before/after examples: "Don't write it like this / Write it like this"

### 4. `knowledge-base/brand/deliverable-standards.md`

What a Koos deliverable looks like:
- Executive summary, structured findings, evidence base, recommended next steps
- Visual hierarchy: headings, tables, callout boxes over long paragraphs
- Always include participant quotes
- Confidence levels on every finding
- Export-ready formats alongside the primary document

### 5. `knowledge-base/ethics/research-ethics.md`

- Participants gave their time and trust — respect their words
- Never take quotes out of context to support a predetermined conclusion
- Flag when sample size is too small to generalize
- Extra care with sensitive topics (health, finances, personal struggles)
- Distinguish between what participants said and what we interpret

### 6. `knowledge-base/ethics/anonymization.md`

- Participants referred to by ID (P01, P02...), never by name
- Remove identifying details: employers, neighborhoods, family members, medical specifics
- Identifying information in quotes gets paraphrased and marked [anonymized]
- Special care for small samples where context clues could identify someone

### 7. `knowledge-base/glossary.md`

15-20 terms with definitions and usage examples:
- Insight, Observation, Finding, Need, Pain point, Gain, Job to be done, Moment of truth, Touchpoint, Persona, Journey, Service blueprint, etc.
- Each with: definition, example of correct usage, common misuse to avoid

### 8. `protocols/quality-criteria.md`

What makes a strong insight:
- Specific (not vague), supported by 2+ participants, actionable, non-obvious
What makes a weak insight:
- Too broad, single-quote evidence, obvious, not actionable
- 3-4 worked examples of strong vs. weak for each analysis type
- The bar: no specific transcript evidence = not an insight, it's a guess

### 9. `protocols/bias-and-rigor.md`

Checklist format:
- Confirmation bias: only finding what we expected?
- Anchoring: first transcripts over-shaping conclusions?
- Selection bias: who wasn't interviewed?
- Leading questions: any interview questions that prompted answers?
- Recency bias: dramatic quotes overweighted vs. frequency?
- Claude runs through this before finalizing any analysis

### 10. `protocols/prioritization.md`

Three-axis prioritization:
- Evidence strength (how many participants, how consistent)
- Potential impact (how much would addressing this change the experience)
- Frequency (how often does this come up in the journey)
- Each finding rated on all three axes
- Output as a prioritization matrix

---

## Methodologies (4 documents)

These describe the frameworks themselves — what they are, when to use them, how Koos applies them. They are reference material, not execution instructions (that's what protocols are for).

### 1. `methodologies/jobs-to-be-done.md`

Based on Christensen's JTBD framework, adapted for Koos:
- What a JTBD is: the underlying progress a person is trying to make in a given circumstance
- Three types: functional, emotional, social
- The standard format: "When [situation], I want to [motivation], so I can [expected outcome]"
- When to use: exploratory research, understanding unmet needs, reframing problems
- Koos-specific: emphasis on evidence-backed jobs, always tied to transcript quotes, always considering context

### 2. `methodologies/pains-and-gains.md`

Based on Osterwalder's Value Proposition Canvas, adapted:
- Pains: frustrations, obstacles, risks, undesired outcomes (functional, emotional, social)
- Gains: desired outcomes, benefits, aspirations (required, expected, desired, unexpected)
- When to use: concept testing, value proposition development, understanding current experience
- Koos-specific: always linked to specific touchpoints in the journey, always evidenced

### 3. `methodologies/needs-based-personas.md`

Koos's approach to personas — built from needs, not demographics:
- Why needs-based: two 35-year-old women can have completely different needs; two people of different ages can share the same need pattern
- Built by clustering participants by need patterns, jobs, and pain/gain profiles
- Each persona: archetype name, need pattern description, key jobs, pains, gains, representative quotes, behavioral indicators
- When to use: after JTBD and pains/gains analysis, to synthesize and communicate findings

### 4. `methodologies/customer-journey-mapping.md`

- What a journey map captures: touchpoints, actions, emotional arc, pain points, moments of truth, opportunities
- Multi-stakeholder awareness: the customer's journey intersects with organizational processes
- When to use: visualizing the full experience, identifying improvement opportunities, aligning stakeholders
- Koos-specific: evidence-based (every touchpoint and emotion backed by transcript data), moments of truth as focal points

---

## Analysis Protocols (4 documents)

These are the execution instructions — the step-by-step pipelines Claude follows. All four share the same multi-agent architecture.

### Common Pipeline Architecture

Every protocol follows this structure:

| Stage | Description | Agents |
|-------|-------------|--------|
| 1 | Preparation | 1 (orchestrator) |
| 2a | Extraction — Lens A | 5 parallel |
| 2b | Extraction — Lens B | 5 parallel |
| 2c | Extraction — Lens C | 5 parallel |
| 2d | Extraction — Lens D | 5 parallel |
| 3 | Convergence Analysis | 1 (orchestrator) |
| 4 | Disagreement Deep-Dive | 5 parallel |
| 4.5a | Quote Verification | 5 parallel |
| 4.5b | Inference Verification | 5 parallel |
| 4.5c | Disagreement Audit | 5 parallel |
| 5 | Synthesis & Deliverable | 1 (orchestrator) |

**Total: 43 agent runs per analysis type.**

### Stage 1: Preparation (1 orchestrator)

- Read the project's phase-level CLAUDE.md — understand the Double Diamond phase
- Read the scoping.md — research questions, hypotheses, target audience
- Read all transcripts in the phase's `transcripts/` folder
- Read the relevant methodology doc from `methodologies/`
- Read `knowledge-base/glossary.md` for consistent terminology
- Read `knowledge-base/ethics/anonymization.md` for data handling

### Stage 2: Parallel Extraction (4 lens stages x 5 agents = 20 runs)

Each stage launches 5 independent agents. Same lens instructions per stage, but independent execution produces natural variation in interpretation, prioritization, and phrasing.

Each agent produces: a list of findings in the protocol's standard format, each with supporting transcript quotes and participant IDs, tagged with lens stage and agent run number (e.g., `implicit-agent-3`).

**The four lenses vary by protocol — see protocol-specific sections below.**

### Stage 3: Convergence Analysis (1 orchestrator)

Analyzes all 20 extraction runs for agreement and disagreement:
- **Cross-agent agreement within a lens**: Did all 5 agents in a lens find the same thing? Strong signal.
- **Cross-lens agreement**: Did a finding appear in multiple lens stages? Rich, multi-dimensional finding.
- **Frequency mapping**: Each unique finding scored by how many of the 20 runs identified it or something semantically equivalent.

Confidence tiers:
- **High confidence (12+ of 20 runs)**: Core finding, consistently identified
- **Medium confidence (6-11 runs)**: Real but nuanced, may depend on lens or interpretation
- **Low confidence (1-5 runs)**: May be noise or a subtle insight — flag for review

### Stage 4: Disagreement Deep-Dive (5 parallel agents)

Each agent independently reviews all medium and low confidence findings:
- Takes opposing positions and argues for/against the validity of each finding, citing specific transcript evidence
- Maps tensions between conflicting findings
- Documents: the two positions, evidence for each, recommendation (likely valid / likely noise / needs human judgment)
- Everything tagged with evidence trail

### Stage 4.5: Evidence Verification

**Step 4.5a: Quote Verification (5 parallel agents)**

All cited evidence quotes distributed across 5 agents. Each independently verifies against original transcripts:
- **Verified**: Quote exists and is accurately reproduced
- **Paraphrased**: Real but not exact — flag the original wording
- **Out of context**: Real quote but meaning shifts when read with surrounding text
- **Not found**: Hallucinated — remove from analysis

**Step 4.5b: Inference Verification (5 parallel agents)**

Each agent independently reviews all findings and checks whether cited evidence supports the inference:
- **Well-supported**: Evidence clearly supports the conclusion
- **Plausible but thin**: Evidence exists but the inferential leap is large
- **Unsupported**: Evidence doesn't actually say what the finding claims

5 agents means clear majority signal: 4/5 saying well-supported is definitive. 3/5 saying thin is a meaningful flag.

**Step 4.5c: Disagreement Audit (5 parallel agents)**

Each agent independently reviews medium and low confidence findings from Stage 4:
- Checks whether each side of a disagreement is built on verified, properly contextualized evidence
- If a disagreement collapses because one side's evidence doesn't hold up, the finding gets reclassified
- 5 agents auditing the same disagreements shows whether the disagreement is genuinely ambiguous (3-2 split) or collapses under scrutiny (5-0)

**What happens to flagged items:**
- Hallucinated quotes: removed. Findings losing all evidence get demoted or removed.
- Paraphrased quotes: replaced with exact original. Finding stands.
- Out of context quotes: full surrounding passage included. Finding may be reclassified.
- Unsupported inferences: demoted in confidence.

### Stage 5: Synthesis & Deliverable (1 orchestrator)

Produces the final analysis following the output template:
- Findings organized by confidence tier (high/medium/low)
- Each finding includes: statement, confidence score, which lens stages found it, which agent runs found it, all supporting quotes with participant IDs
- Evidence index: queryable reference section tracing every finding back to transcript passages and agent runs
- Verification report: quote accuracy rates, inference validation results, audit outcomes
- Meta-analysis log: readable account of how the pipeline worked
- CSV/export files
- Final bias and rigor check pass

### Protocol-Specific Lenses

**JTBD Analysis — `protocols/jtbd-analysis.md`:**
- Lens A (Obvious/Explicit): Directly articulated jobs — what participants said they want or need
- Lens B (Implicit/Latent): Jobs talked around — workarounds, frustrations implying unmet needs, behaviors revealing unstated goals
- Lens C (Emotional & Social): How participants want to feel, be perceived; identity, relationships, trust, confidence
- Lens D (Adversarial): Jobs that complicate, contradict, or create tension with earlier findings; edge cases, minority perspectives, contextual variations

Output format per finding:
```
### JOB-014: [When switching medications, I want to understand why, so I can trust the change is safe]

**Confidence:** High (16/20 runs)
**Lenses:** obvious (5/5), implicit (4/5), emotional (5/5), adversarial (2/5)
**Supporting evidence:**
  - P03: "I just want someone to explain why they're changing my pills" (obvious-agent-1, obvious-agent-2, obvious-agent-4, emotional-agent-3)
  - P07: "My neighbor had a bad reaction when they switched, so now I always worry" (emotional-agent-1, emotional-agent-2, emotional-agent-5, implicit-agent-2)
  - P01: [describes calling pharmacy three times before filling prescription] (implicit-agent-1, implicit-agent-3, implicit-agent-5)
**Adversarial note:** agent-4 argued this is actually two separate jobs (understanding rationale vs. feeling safe) — merged here because evidence suggests they're inseparable for patients. Flag for human review if disaggregation matters for the design response.
```

**Pains & Gains Analysis — `protocols/pains-gains-analysis.md`:**
- Lens A (Functional Pains): Practical obstacles, process friction, things that don't work, wasted time/effort
- Lens B (Emotional & Social Pains): Frustration, anxiety, embarrassment, feeling judged, loss of control
- Lens C (Functional Gains): Desired outcomes, efficiency improvements, things that would make life easier
- Lens D (Emotional & Social Gains): Desired feelings, confidence, status, belonging, peace of mind

**Persona Synthesis — `protocols/persona-synthesis.md`:**
- **No hard dependencies — works standalone on transcripts alone.** But when prior analyses exist in the project's `analysis/` folder (JTBD, pains/gains), they are **mandatory input** — the protocol must incorporate them as foundational data, not optional enrichment. When they don't exist, the protocol runs its own lightweight extraction internally as part of preparation.
- Lens A (Need Pattern Clustering): Group participants by shared need patterns — who wants the same things?
- Lens B (Behavior Clustering): Group by how they currently act — similar workarounds, similar habits
- Lens C (Barrier Clustering): Group by what holds them back — similar obstacles, similar fears
- Lens D (Adversarial): Challenge the clusters — are we forcing people into groups? Who doesn't fit? Are we seeing real segments or artifacts?

**Journey Mapping — `protocols/journey-mapping.md`:**
- **No hard dependencies — works standalone on transcripts alone.** But when prior analyses exist in the project's `analysis/` folder (JTBD, pains/gains, personas), they are **mandatory input** — the protocol must build on them, using identified jobs, pains, gains, and persona segments to enrich the journey map. When they don't exist, the protocol works directly from transcript evidence.
- Lens A (Touchpoint Mapping): Identify every interaction point from the transcripts — what happened, in what order
- Lens B (Emotional Arc): Map how participants felt at each touchpoint — satisfaction, frustration, anxiety, delight
- Lens C (Moments of Truth): Identify the make-or-break moments where the experience either earned or destroyed trust
- Lens D (Gap Analysis): Where are the missing touchpoints? What should exist but doesn't? Where does the journey break down?

### Protocol Dependency Rule

All four protocols can run independently on any project at any time — there are no hard prerequisites. However, when prior analysis outputs exist in the project's `analysis/` folder, later protocols **must** use them as foundational input:

- **JTBD and Pains & Gains**: Fully independent. Can run in parallel. No prior analysis needed.
- **Persona Synthesis**: If JTBD and/or pains/gains analyses exist → mandatory input. If not → works from transcripts alone.
- **Journey Mapping**: If any prior analyses exist (JTBD, pains/gains, personas) → all are mandatory input. If not → works from transcripts alone.

The rule is: **use it if it's there (non-negotiable), work without it if it's not.** The protocol's preparation stage checks the `analysis/` folder and adapts accordingly.

---

## Two Execution Modes

### Autopilot Mode

User triggers with something like: "Run a full JTBD analysis on these transcripts. Autopilot."

Claude:
1. Reads all relevant context (CLAUDE.md hierarchy, scoping, methodology, protocol)
2. Executes all stages sequentially, launching parallel agents at each stage
3. Produces the final deliverable in the `analysis/` folder
4. Presents a summary to the user with key findings and the verification report

### Guided Mode (Default)

User triggers with something like: "Walk me through a JTBD analysis on these transcripts."

Claude pauses after each major stage:
- After Stage 2 (Extraction): "Here's what the 20 agents found across all four lenses. [summary]. Do you want to proceed to convergence analysis, or dig into any specific findings first?"
- After Stage 3 (Convergence): "Here's the convergence matrix. [high/medium/low breakdown]. Do you want to proceed to the disagreement deep-dive, or discuss any findings?"
- After Stage 4 (Disagreement): "Here are the unresolved disagreements. [summary]. Do you want to proceed to evidence verification, or weigh in on any of these?"
- After Stage 4.5 (Verification): "Here's the verification report. [stats]. X quotes were corrected, Y findings were reclassified. Ready for final synthesis?"
- After Stage 5: "Here's the final deliverable. [summary]. Want me to adjust anything before I generate the exports?"

---

## Project Structure (Double Diamond)

Each project has a client-level context and four phases following the Double Diamond.

### Client-Level Context

**`projects/<project>/CLAUDE.md`:**
- Who the client is, the relationship, key stakeholders
- The strategic challenge driving the engagement
- Overview of project phases and current status

**`projects/<project>/context/`:**
- `client-brief.md` — the original problem statement from the client
- `stakeholder-notes.md` — notes from kickoff meetings, email summaries, key decisions
- `desk-research.md` — background research, market data, competitor analysis, prior work

### Phase-Level Structure

Each phase gets a CLAUDE.md that tells Claude where it sits in the Double Diamond and how to calibrate analysis behavior:

**`1-discover/CLAUDE.md`:** Divergent. Explore the problem space. Don't jump to solutions. Look for patterns, unmet needs, surprises. Cast a wide net.

**`2-define/CLAUDE.md`:** Convergent. Synthesize Discover findings into problem statements, personas, journey maps, opportunity areas. Prioritize and frame.

**`3-develop/CLAUDE.md`:** Divergent. Generate and test solutions. Concept testing transcripts live here. Evaluate concepts against needs from Discover/Define.

**`4-deliver/CLAUDE.md`:** Convergent. Validate the refined solution. Evaluative research. What works, what doesn't, what needs iteration.

Phases without active research contain only the CLAUDE.md (and placeholder directories). Phases with transcripts contain: CLAUDE.md, scoping.md, transcripts/, analysis/.

---

## Three Demo Projects

### 1. Amsterdam Municipality — Exploratory Research (Discover Phase)

**Client context:** Municipality of Amsterdam, 850,000 citizens, committed to inclusive digital services.

**Research scenario:** Exploratory research into how citizens experience municipal services — permits, reporting issues, social services, digital channels. Looking for unmet needs and improvement opportunities.

**Transcripts (10, in Dutch):**
- Citizens of different ages (22-74), backgrounds, digital literacy levels, neighborhoods
- Topics: permits, reporting, social services, municipal website, service desk
- Mix of frustrated, satisfied, and workaround-developing participants
- Some participants contradict each other
- Embedded patterns for the pipeline to discover:
  - 6/10 describe the same workaround independently (implicit pattern)
  - Strong emotional jobs around feeling heard and taken seriously by the municipality
  - One minority perspective that challenges the main narrative

**Active phase:** `1-discover/` — contains scoping.md and 10 transcripts

### 2. VGZ Healthcare — Concept Testing (Develop Phase)

**Client context:** VGZ, largest health insurer in the Netherlands, transforming toward customer-centric digital services.

**Research scenario:** Testing a concept for a digital self-service portal where patients manage health insurance matters (claims, referrals, medication approvals, finding care providers).

**Transcripts (10, in Dutch):**
- Patients of varying ages (28-71), health situations, digital confidence
- Being shown and reacting to the portal concept
- Mix: enthusiasm, skepticism, confusion, "why doesn't this exist already"
- Some surface needs the concept doesn't address
- Embedded patterns:
  - Concept works for digitally confident patients but fails for those who need it most (key tension)
  - Unanimous pain around medication switching process
  - Social job: patients want to feel competent managing their own health admin

**Active phase:** `3-develop/` — contains scoping.md and 10 transcripts

### 3. NS Railways — Evaluative Research (Deliver Phase)

**Client context:** NS (Nederlandse Spoorwegen), 10.1 million passengers annually, modernizing into customer-centric mobility provider.

**Research scenario:** Evaluating passenger experience with a recently launched real-time multimodal journey planner in the NS app.

**Transcripts (10, in Dutch):**
- 5 daily commuters, 3 occasional travelers, 2 tourists
- Mix: love it, haven't noticed it, tried it and went back to Google Maps
- Embedded patterns:
  - Feature works for simple journeys but breaks down for multimodal trips (train + bus + walk)
  - Commuters don't need it (they know their route) — but they want disruption recovery
  - Tourists have the highest unmet need but the worst discoverability

**Active phase:** `4-deliver/` — contains scoping.md and 10 transcripts

---

## Synthetic Transcript Specifications

Each transcript:
- ~2,000-3,000 words
- In Dutch (VGZ and Amsterdam projects are Dutch participants; NS includes mix but primary language is Dutch)
- Interview metadata header: date, duration (~45-60 min), interviewer name (fictional Koos employee), participant ID, location, research context
- Verbatim conversational style: interviewer questions and participant responses
- Realistic verbal patterns: hesitation ("eh," "nou ja..."), self-correction, tangents steered back by interviewer, emotional moments, contradictions within same participant
- Mix of articulate and less articulate participants
- Each set of 10 has intentional analytical properties:
  - 2-3 "loud" insights any analysis will find
  - 3-4 implicit patterns requiring cross-transcript synthesis
  - 1-2 contradictions or tensions for the adversarial lens
  - 1-2 emotional/social findings surfacing only with the right lens
  - Enough variation that 5 parallel agents will genuinely find different things

---

## Pre-Run Example Output

**`examples/vgz-sample-analysis/`** contains a fully completed analysis of the VGZ concept testing transcripts, showing what the pipeline produces.

Files:
- `jtbd-analysis.md` — Full JTBD deliverable with confidence tiers, evidence, lens tracking, adversarial notes
- `pains-gains-analysis.md` — Pains and gains organized by functional/emotional/social, same evidence structure
- `persona-cards.md` — 3-4 needs-based personas with archetype names, need patterns, key jobs, pains, gains, representative quotes
- `journey-map.md` — Patient concept testing journey with touchpoints, emotional arc, moments of truth, opportunities
- `verification-report.md` — Full evidence verification summary with quote accuracy rates, inference validation, audit results
- `meta-analysis-log.md` — Readable log of pipeline execution: agent counts, convergence patterns, disagreement resolution, verification outcomes
- `exports/personas.csv` — Persona data for Miro import
- `exports/jtbd-matrix.csv` — All jobs with confidence scores
- `exports/pains-gains-matrix.csv` — All pains and gains with scores

---

## Output Templates

### `templates/project-scoping.md`

Intake template filled in before starting analysis:
- Project name, client, phase (Discover/Define/Develop/Deliver)
- Research type (exploratory/concept testing/evaluative/other)
- Research questions (what are we trying to learn?)
- Hypotheses (if any — what do we expect to find?)
- Target audience (who was interviewed and why?)
- Sample size and composition
- Interview guide summary (key topics covered)
- Known constraints or biases in the sample

### `templates/output-formats/jtbd-output.md`

Template for JTBD deliverables — sections, formatting, required fields per finding.

### `templates/output-formats/pains-gains-output.md`

Template for pains & gains deliverables.

### `templates/output-formats/persona-card.md`

Template for persona cards — archetype name, description, jobs, pains, gains, quotes, behavioral indicators.

### `templates/output-formats/journey-map-output.md`

Template for journey map deliverables — touchpoint structure, emotional arc notation, moment of truth format.

---

## Architecture Documentation

**`docs/architecture.md`:**

- Full pipeline diagram (Mermaid or ASCII) showing all stages, agent counts, data flow
- Why multi-agent: the intellectual argument for 20 agents > 1 agent (diversity of interpretation, statistical convergence, systematic rigor)
- How evidence verification works and why it matters (anti-hallucination, trust)
- How the Double Diamond phase context shapes analysis behavior
- How the system is designed to be extended: adding new protocols, new analysis types, new projects
- How CLAUDE.md layering works: root → project → phase

---

## What's Out of Scope

- MCP servers or external tooling (future engagement territory)
- Real client data (all synthetic)
- Production deployment (this is a proof of concept)
- Front-end UI (Claude Desktop IS the interface)
- Integration with design tools beyond CSV exports (future territory)
- Slash commands (stretch goal, not core)
