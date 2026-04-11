# KOOS Research Analysis System

## The Problem You Already Know

Your designers are talented researchers. They conduct thoughtful interviews, build genuine rapport with participants, and care deeply about getting it right. But when ten transcripts land on someone's desk, what happens next is different every time.

Two designers analyzing the same set of interviews will produce different insights -- not because one is wrong, but because humans naturally anchor on different things. We get fatigued. We latch onto vivid quotes and underweight the quiet patterns. We cannot systematically cross-reference what Participant 3 said against what Participants 1, 5, and 8 said about the same underlying need. Not across ten transcripts. Not with the rigor the work deserves.

Analysis takes days. Quality varies by who does it and how much time they had. When someone leaves, their way of seeing the data leaves with them. There is no institutional methodology that guarantees the same depth and rigor every time, regardless of who runs the analysis or how tight the deadline is.

And here is the uncomfortable part: you are already using AI. Everyone is. But everyone is using their own prompts, their own tools, their own approach. The inconsistency problem is not getting better. It is getting worse -- now with the added risk that no one can explain or reproduce how a particular insight was generated.

## What If Your Best Researcher's Method Was Available to Everyone

Imagine your most rigorous researcher's methodology -- their systematic approach, their instinct for triangulation, their discipline around evidence -- encoded into a system that anyone on the team can run. At machine speed. With built-in quality controls that no human has the patience to perform manually.

This is not about replacing your researchers. It is about giving them a system that handles the systematic grunt work at a level of thoroughness they would never have time for. Twenty independent analysis passes over the same data. Automatic cross-referencing of every finding against every transcript. Confidence levels on every insight. Quote verification on every claim.

Your researchers get freed up for the work that actually requires human judgment: interpretation, creative synthesis, strategic framing, and the kind of empathetic pattern recognition that makes KOOS's research valuable in the first place.

## How It Works

This repository encodes KOOS's research methodologies, quality standards, tone of voice, and ethical guidelines into a structured knowledge base. When connected to Claude Desktop or Claude Code, Claude becomes a KOOS research analyst -- one that follows your methodology, speaks in your voice, and applies your standards consistently.

Four analysis types are available as slash commands:

- `/analyze-jtbd` -- Jobs to Be Done analysis
- `/analyze-pains-gains` -- Pains and Gains mapping
- `/analyze-personas` -- Needs-based Persona synthesis
- `/analyze-journey` -- Customer Journey Mapping

Each command triggers a multi-agent pipeline designed for rigor through redundancy: 4 analytical lens stages, each run by 5 parallel agents working independently, producing 20 separate analysis passes. These feed into convergence analysis, disagreement resolution, and evidence verification -- 43 total agent runs before a final deliverable is produced.

Two execution modes are available:

- **Guided mode** (default) -- pauses at each stage for human review and steering
- **Autopilot mode** -- runs the full pipeline end to end at machine speed

See `docs/architecture.md` for the complete pipeline diagram and detailed system design.

## What It Produces

Every analysis run generates structured, evidence-backed deliverables:

- **Findings with confidence levels** -- each insight rated by the strength of supporting evidence across transcripts
- **Traceable evidence** -- every finding linked to specific transcript quotes and participant IDs
- **Verification report** -- automated check of quote accuracy and inference validity
- **Export-ready formats** -- CSV outputs for Miro, spreadsheets, and other design tools

See `examples/vgz-sample-analysis/` for a complete output example showing what the pipeline produces from real transcript data.

## Getting Started

1. **Open this repo** in Claude Desktop or Claude Code
2. **Navigate to a project folder** -- for example, `projects/vgz-healthcare/3-develop/`
3. **Run a slash command** -- type `/analyze-jtbd` or describe what you want in natural language
4. **Choose your mode** -- guided mode pauses at each stage for review; autopilot runs the full pipeline
5. **Review the outputs** in the `analysis/` folder created within the project directory
6. **Reference the example** in `examples/vgz-sample-analysis/` to see what finished output looks like

## What's Inside

| Folder | What's Inside |
|---|---|
| `knowledge-base/` | Company context, brand guidelines, ethics framework, and research glossary |
| `methodologies/` | Framework references for JTBD, Pains & Gains, Personas, and Journey Mapping |
| `protocols/` | Step-by-step analysis pipeline instructions -- the engine that drives each analysis |
| `templates/` | Project scoping template and output format definitions |
| `projects/` | Three demo projects with client context, scoping documents, and interview transcripts |
| `examples/` | Pre-run analysis output showing what the pipeline produces |
| `.claude/` | Slash commands, path-scoped rules, and Claude configuration |
| `docs/` | Architecture documentation and pipeline diagrams |

## The Three Demo Projects

The repo includes three complete project setups with transcripts ready for analysis:

- **VGZ Healthcare** (`projects/vgz-healthcare/`) -- health insurance customer experience research
- **NS Railways** (`projects/ns-railways/`) -- rail travel passenger experience research
- **Amsterdam Municipality** (`projects/amsterdam-municipality/`) -- municipal services resident experience research

Each project contains client briefs, desk research, stakeholder notes, and ten interview transcripts. Pick any project and any analysis type to see the system in action.

---

This system does not change how KOOS thinks about research. It encodes how KOOS already thinks -- and makes that thinking consistent, traceable, and available to everyone on the team, every time.
