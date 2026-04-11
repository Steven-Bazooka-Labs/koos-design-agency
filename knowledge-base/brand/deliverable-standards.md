# KOOS Deliverable Standards

This document defines the structure, formatting, and quality requirements for every research deliverable produced at KOOS. All outputs — whether written by a researcher or generated with AI assistance — must meet these standards before reaching a client.

## Required Structure

Every research deliverable follows a six-part structure. Sections may vary in length depending on the project, but none may be omitted.

### 1. Executive Summary (max 200 words)

The executive summary gives a busy stakeholder everything they need in under a minute. It states the research objective, the most significant findings (with confidence levels), and the top recommendations. No jargon. No preamble. If the reader stops here, they should still walk away informed.

### 2. Research Context

A brief section covering: who commissioned the research, the business question it addresses, the participant profile, and the timeframe. This section grounds the findings for anyone who was not involved in scoping the project.

### 3. Findings (Main Body)

Findings form the core of the deliverable. They are organised by theme or by confidence level, whichever structure best serves the reader. Each finding must include four elements:

- **Finding statement** — a clear, one-sentence summary (e.g., "Participants do not trust automated claim decisions")
- **Confidence level** — High, Medium, or Low, based on evidence volume and consistency
- **Supporting evidence** — direct quotes, behavioural observations, or quantitative data, each with participant IDs and transcript references
- **Implications** — what this finding means for the client's product, service, or strategy

Findings are numbered using a consistent scheme: `JOB-001`, `PAIN-003`, `PERSONA-A`, `OPP-012`, and so on. This numbering enables cross-referencing across deliverables and makes it easy to track individual findings through to recommendations.

### 4. Evidence Index

Every finding must be traceable to its source. The evidence index is a reference table listing:

| Finding ID | Supporting Quote / Observation | Participant ID | Transcript Reference | Agent Run (if applicable) |
|---|---|---|---|---|
| PAIN-003 | "I called three times and got three different answers." | P07 | T07, lines 142-148 | analysis-run-2024-03-12 |

This index serves two purposes: it allows clients to verify findings against raw data, and it provides an audit trail for quality review.

### 5. Methodology Note

A concise account of how the research was conducted and analysed. This section should specify:

- Which research protocol was used (and link to it if available)
- Number of analysis passes and who or what conducted them
- Any AI-assisted analysis steps, including which models and prompts were used
- Verification steps taken (peer review, member checking, triangulation)
- Known limitations of the methodology

This section is not a formality. It is how we demonstrate rigour.

### 6. Recommended Next Steps

Recommendations are split into two categories, clearly labelled:

- **Evidence strongly supports** — actions backed by high-confidence findings with consistent evidence across multiple participants
- **Recommend exploring** — directions suggested by the evidence but not yet confirmed, requiring further research or validation

Each recommendation links back to one or more finding IDs from the main body.

---

## Formatting Standards

Consistent formatting makes deliverables scannable, professional, and accessible across teams.

- **Headings:** Use H2 (`##`) for major sections and H3 (`###`) for subsections. Never skip heading levels.
- **Tables:** Use tables for any comparative or structured data. Side-by-side comparisons are always clearer in table form than in prose.
- **Participant quotes:** Use blockquote formatting (`>`) with the participant ID appended.
  > "I didn't know which letter to believe." — P03
- **Caveats and review flags:** Use a clearly labelled callout block for any caveat, limitation, or item requiring human review.
  > **[Human Review Required]** This pattern was identified by automated analysis and has not yet been verified against the full transcript.
- **Bold key terms** on first use to help readers build a mental glossary.
- **Short paragraphs:** 3-5 sentences maximum. If a paragraph exceeds five sentences, break it up or convert part of it to a list.
- **Finding IDs:** Use the standard scheme (`JOB-001`, `PAIN-003`, `PERSONA-A`) consistently throughout.

---

## Quality Bar

These are non-negotiable requirements. A deliverable that fails any of these checks is not ready for client review.

| Requirement | Standard |
|---|---|
| No finding without evidence | Every finding must cite a minimum of 2 supporting quotes from different participants |
| No evidence without source | Every quote includes a participant ID and transcript reference |
| No recommendation without a finding | Every recommendation links to at least one finding ID |
| Confidence levels on everything | Every finding carries a High / Medium / Low confidence label |
| Export-ready formats | A CSV export accompanies every markdown deliverable, containing structured finding data (ID, statement, confidence, evidence references, recommendations) |

### Pre-Delivery Checklist

Before any deliverable is shared with a client, confirm:

1. All six sections are present and complete.
2. The executive summary is 200 words or fewer.
3. Every finding has a unique ID, a confidence level, and at least two supporting quotes from different participants.
4. The evidence index accounts for every finding in the main body.
5. The methodology note accurately describes the analysis process, including any AI-assisted steps.
6. Recommendations are categorised as "evidence strongly supports" or "recommend exploring."
7. The CSV export is generated and consistent with the markdown content.
8. A second team member has reviewed the deliverable against this checklist.
