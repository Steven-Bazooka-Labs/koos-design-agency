# koos-ai Rollout Plan — from proven concept to working capability

*Bazooka Labs for Koos · July 2026 · Companion to the "Second Brain" memo (June 2026). A one-page summary exists separately; this is the full plan, including costs, data handling, risks, and everything we still need from Koos.*

---

## 1. Where we stand

The June proof-of-concept did its job. What exists and is verified today:

| Asset | Status |
|---|---|
| **`koos-ai` repo** — the **canon** (the single Koos-owned source of truth for tools and knowledge) and the **plugin marketplace** (the mechanism Claude Code uses to install and update from it), in one | Built, private on GitHub (v0.3.1) |
| **Three priority tools** as agreed: Contract Checker, Survey Builder, Design Token Generator | Complete — including the companion rule files (survey quality rules, survey structure guide, token naming standards), carried over intact from the Build Week originals |
| **Knowledge base** | Real Koos content: company profile, brand voice; plus a core guardrails draft (Koos review pending — see §4, Phase 0) |
| **Feedback loop** | Live in the repo, seeded with RJ's real Build Week feedback — including two open actions for Koos legal (§7) |
| **Operational guides** | Four docs shipped in the repo: setup, designer onboarding, steward guide, how-updates-work |
| **Install + update mechanics** | Verified end-to-end, including in the desktop app: install, namespaced tools (`/koos:contract-checker`), and the release→update loop (version bump → push → update). Automatic update pickup at startup is documented behaviour, **to be confirmed** on the first pilot machines in Week 1 (the 30-second manual path is verified) |
| **Demo environment** | Synthetic "Stadslijn" client project folder incl. a test contract with planted issues — used in the June demo, reusable for onboarding |

What is deliberately **not** in scope yet: the other Build Week tools (promoted later, one by one), integrations (HubSpot, Google Slides), the lead-gen and search-visibility workstreams (§10).

---

## 2. The approach: one pilot, two tracks, production-real

We start narrow and real, not broad and theoretical. Two tracks, because the tools serve two different workflows:

**Track A — Contracts (the depth test).** The Contract Checker runs where contracts actually live: with the new-business side (it was built by RJ for exactly that context). During the pilot, every incoming contract goes through the checker there. **Nothing tool-drafted leaves the building unreviewed:** amendments and emails go out only after sign-off by the commercial owner — and legal, where Koos's normal process requires it. Naming that reviewer is part of the Phase-0 confirmation.

**Track B — Design & research tools (the breadth test).** 2–3 designers use the Survey Builder and/or the Design Token Generator on live project work, as their projects actually need them. This is what tests the "shared toolkit for designers" story: install, use in a real project folder, feedback, updates.

Everything runs the production way from the first day: installed plugin, real project folders, feedback loop, versioned updates. Build Week's per-team setups did exactly their job — proving the tools were worth building. The pilot proves the shared way of running them.

---

## 3. Roles — and what they cost internally

| Role | Who | Time | Responsibility |
|---|---|---|---|
| **Sponsor** | Koos (e.g. Saskia/RJ) | ~1 h/wk | Decisions, unblocking, pilot selection, judging the success criteria |
| **Steward** (recommend naming **two**) | Koos — git-comfortable | 2–4 h/wk each in pilot | Owns the canon: releases, feedback triage, promotion, anonymisation gate. Full role description: `docs/steward-guide.md` in the repo |
| **Track A owner** | Koos — new business (e.g. RJ) | within existing contract work | Runs live contracts through the checker; reviews anything tool-drafted before it goes out |
| **Pilot designers** | Koos, 2–3 people | their normal work + ~1–2 h total each | Use the tools on real work; log feedback (2 sentences in Slack) |
| **Bazooka** | Steven | per phase, see §6 | Setup, coaching the steward, tool fixes, pilot support, review |

**Internal time, added up:** two stewards at 2–4 h/wk over Phase 0 plus the pilot (~4 weeks elapsed) is 16–32 h; sponsor ~4 h; designers ~3–6 h combined. **Roughly 25–40 internal hours total** — that's the real internal cost to put next to the external one (§6).

**Making the steward role stick** (this choice matters more than any technical decision in the plan): give it an internal booking code, a named place in the review cycle ("this is part of your development", not invisible glue work), and a **6-month horizon with an explicit re-decision point**. The profile: a Build Week standout, pragmatic, respected enough that "not in the canon yet" sticks. After Phase 2 mechanisms land, the target is ≤2 h/wk.

---

## 4. Phased plan

### Phase 0 — Foundation (the week after Koos confirms the §11 items; ~half a day of sessions)

1. Koos creates (or names) its **GitHub organisation**; Bazooka stands up the private `koos-ai` repo there; the interim Bazooka-hosted copy retires. From then on the repo — and everything in it — is Koos property (§9).
2. Koos names the **steward(s)**, the **Track A owner**, and the **pilot designers**; everyone gets repo access; the **#koos-ai** Slack channel is created.
3. **Data & compliance gate** — the four checks in §5, resolved before any live client document goes through a tool.
4. **Guardrails working session (60–90 min, Bazooka + Koos research/practice leads).** The current core-guardrails file is a Bazooka draft and is labeled as such. This is *not* a sign-off meeting: Koos's own research-ethics and anonymisation practice gets worked in, and Koos's edits become v1. (Context: Koos's real research-ethics framework has been a known gap since Build Week — the starter pack shipped a placeholder. This session closes that gap for the toolkit; the full framework is ask #4 in §8.)
5. **Steward setup session (~2 h):** walk the repo, do the steward's first release together (a real small fix), verify install + GitHub auth on their machine.

*Exit condition: the steward has shipped a version bump that another machine received via update — and the data gate is green.*

### Phase 1 — Pilot (3 working weeks)

**Week 1 — Onboard.** Bazooka + steward onboard the pilot group (~45 min each: the 15-minute guide, then a ~30-minute session — install, auth and update-token check, auto-update setup, and a supervised sample run against the setup guide's per-machine checklist). **Baselines are captured before first tool use** (Track A: time spent on the last few contract reviews, per the owner). First live contract goes through the checker this week.

**Week 2 — Use.** Both tracks run on real work. Feedback flows to `#koos-ai`. The steward runs the weekly triage-fix-release rhythm; **at least one release ships mid-pilot**, proving the update loop on Koos machines.

**Week 3 — Verify & decide.** Steward + Bazooka compile the evidence: usage (from the feedback log and self-reports — **nothing is measured on anyone's machine**), time-vs-baseline, feedback→fix cycle times, the Drive-folder verdict, auth/update reliability. Pilot review session: **the sponsor judges the criteria (§12) and decides** — expand, adjust, or stop.

*(Calendar note: three **working** weeks — with summer holidays, let the elapsed time stretch rather than pilot with half the group away.)*

### Phase 2 — Expand (after the pilot review)

- Onboard the next wave with the same guides (repeatable without Bazooka in the room); pick the scale-out mechanism — onboarding script, shared project settings, or settings IT deploys centrally to every Mac ("managed settings") — options in `docs/setup-guide.md`, Step 5.
- **Brief the employee representation before this phase** (see §5).
- Promote the next tools from the Build Week set, one release at a time. Candidates by evidence and readiness: **transcript-analyser**, **figma-token-checker** (its rules file already exists), **email-proposal**, **case-builder**. Integration-dependent tools (**pitch-builder**/Google Slides, **am-assistant**/HubSpot) only after their integrations are decided.
- Add **sector guardrail modules** (healthcare first, given VGZ/Santeon-type work), loaded per client sector.

### Phase 3 — Steady state

Steward rhythm on a fixed weekly slot; quarterly tool review (usage, staleness, retirement). Bazooka steps back to a support role. Any further build work (new tools, integrations, the parked workstreams in §10) happens as **separately scoped, capped sprints that Koos triggers** — there is no open-ended engagement tail baked into this plan.

---

## 5. Data & compliance — the Phase-0 gate

The honest mechanics: **running a tool sends the working files' content to Anthropic's Claude API for processing** — that's how Claude Code works. Installing the toolkit uploads nothing; nothing ever enters the shared repo un-anonymised. But "we put your contract through an AI" is a sentence Koos must be able to complete confidently for clients like VGZ or Rijkswaterstaat. Four checks, all before live client documents go through:

1. **Account setup.** Pilot runs on a **Koos-owned Claude workspace under Anthropic's commercial terms** (business data not used for training; admin control) — not on personal accounts. Decide tier and seats; budget note in §6.
2. **DPA & processing.** Review Anthropic's data-processing addendum (it's incorporated into the commercial terms); confirm retention settings and processing location as part of that review. *(Bazooka prepares the summary; Koos legal confirms.)*
3. **Client permission check.** A legal sweep of the pilot clients' MSAs/NDAs for AI/subprocessor clauses **before** their documents go through a tool. Where a contract doesn't permit it: that client's documents stay out of the pilot (or go through in redacted form).
4. **The client-facing answer**, drafted for legal review, so every Koos person says the same thing when asked. Working draft: *"We use Claude (Anthropic) as a drafting assistant under a commercial agreement — client data is not used for model training and is handled per our data-processing agreement. A Koos professional reviews everything before it reaches you, and on request we exclude your project from AI-assisted work."* **[To be reviewed and owned by Koos legal.]**

**Employee representation / AVG note.** Pilot metrics are aggregated and self-reported only — no per-person dashboards, nothing measured on machines; pilot participation is voluntary. That design keeps the pilot outside "monitoring" territory on purpose: tooling capable of tracking behaviour or performance triggers a works-council **consent** right at 50+ employees (WOR art. 27); at Koos's ~40 people the lighter PVT/staff-meeting regime applies (WOR arts. 35b/35c), with narrower formal rights. We still **brief the PVT — or the staff meeting, or the OR if Koos has voluntarily instituted one — before the Phase-2 scale-out**. Cheaper to raise in week 0 than to discover in week 6.

---

## 6. Costs — external, internal, and what stopping costs

| | Effort | Cost |
|---|---|---|
| **Bazooka, Phase 0** — repo handover, data-gate prep, guardrails session, steward setup | [est. 10–14 h] | [rate × hours — per engagement note] |
| **Bazooka, Phase 1** — onboarding, weekly support, fixes-as-releases, audit + review session | [est. 16–22 h] | [idem] |
| **Koos internal, Phases 0–1** | ~25–40 h (per §3) | opportunity cost, mostly steward |
| **Claude licensing** | — | Koos's own Anthropic workspace seats for pilot participants (tier decision in the §5 data gate) |

*Bracketed effort figures are Bazooka's estimates; rates and totals are in the engagement note that accompanies this plan.*

**If the Week-3 verdict is "stop":** total exposure is the Phase 0–1 hours above, the internal time, and the pilot's Claude seats — and Koos keeps a working, documented toolkit: the repo, all three tools, the guides and the feedback loop are Koos property in working order (§9). Phase 2 and 3 are only entered by decision, never by momentum.

---

## 7. Found work: two open actions for Koos legal

Surfaced by the Contract Checker work during Build Week (tracked in the repo's feedback log):

1. **The Koos T&C still lists Lisbon, Berlin and Oslo as Koos Group offices** — current reality is Amsterdam + Abu Dhabi.
2. **The T&C doesn't make methodology/deliverable use rights conditional on full payment** — the Contract Checker flags client contracts for exactly this, so Koos's own paper should match.

Both are small, both predate this project, and fixing them makes tool and contract consistent. Three further researched gaps (participant consent ownership, change-request process, freelancer carve-outs) are logged as candidates for the tool's risk framework.

---

## 8. Context files: what we have vs. what we need from Koos

The toolkit is only as good as the Koos knowledge under it.

### Already in the canon (real content)

| File | Source | Note |
|---|---|---|
| `company.md` — who Koos is | Build Week knowledge base | ✔ |
| `brand-voice.md` — how Koos writes | Build Week knowledge base | ✔ |
| Koos contract baseline (liability, IP/CC-BY-SA, payment ladder, jurisdiction, GDPR…) | Embedded in Contract Checker, from RJ's tool | ✔ — two legal updates pending (§7) |
| `survey-quality-rules.md`, `survey-structure-guide.md` | Noor & Ruben's originals | ✔ bundled, unchanged |
| `rules.md` — token naming conventions & standards | Jasper & Carmel's original | ✔ bundled, unchanged |
| `guardrails/core.md` | Bazooka draft | ⚠ explicitly labeled "Koos review pending" until the Phase-0 working session |

### Needed from Koos (the ask list)

| # | What | Feeds | Owner at Koos | When |
|---|---|---|---|---|
| 1 | **Phase-0 confirmations** — GitHub org, steward(s), Track A owner, pilot designers + project, Slack channel | Everything | Sponsor | Phase 0 |
| 2 | **Data gate inputs** — workspace/tier decision, DPA review, pilot-client contract sweep, sign-off on the client answer | §5 | Sponsor + legal | Phase 0 |
| 3 | **Guardrails working session** — Koos's research-ethics and anonymisation practice, worked into the core guardrails | Every tool run | Research leads | Phase 0 |
| 4 | **The real research-ethics framework** as a document (known gap since Build Week) | Knowledge base | Research leads | Phase 1 |
| 5 | **T&C updates** — the two legal actions in §7 | Contract Checker accuracy | Legal | Phase 1 |
| 6 | **Sector sensitivities** — existing notes/policies for healthcare, finance, public sector | `guardrails/<sector>.md` | Practice leads | Phase 2 |
| 7 | **Terminology / glossary** — the terms Koos insists on (and the misuses it bans) | Consistent tool output | Practice leads | Phase 2 |
| 8 | **Services & offering descriptions** | Tools that write client-facing text | Sponsor/marketing | Phase 2 |
| 9 | **Deliverable formats** — the report/proposal structures worth templating | `templates/` | Practice leads | Phase 2 |
| 10 | *(Per-tool, later)* rate card (email-proposal), HubSpot access (am-assistant), Slides template (pitch-builder) | Next promotions | Various | When promoted |

Items 6–9 usually already exist as decks, wikis, and habits — the steward + Bazooka turn what exists into canon files; Koos reviews. Nothing needs writing from scratch.

---

## 9. Ownership & exit — in writing

- **The repo and everything in it is Koos property** from the Phase-0 handover: tools, guides, guardrails, feedback logs. We recommend stating this explicitly in the engagement terms. (Bazooka stays free to reuse the *generic* operating model — canon/marketplace/steward pattern — elsewhere; never Koos's content.)
- **No key-person dependency by design.** Everything is markdown and git. Any steward — or any future vendor — can maintain, extend, or fork it without Bazooka. The guides exist precisely so the operating knowledge doesn't live in one head.
- **Platform dependency:** distribution rides Claude Code's plugin mechanism, which Anthropic may evolve. The content doesn't care — it's portable markdown; worst case, the same tool folders drop into Claude Code's plain skills locations (`~/.claude/skills/` or a project's `.claude/skills/`) and keep working — invocations just lose the `koos:` prefix — while distribution is re-plumbed. The update mechanics in the guides are the part most exposed to change, and the steward guide flags exactly that.
- **If the pilot says stop:** see §6. The toolkit remains usable as-is for as long as it's useful.

---

## 10. Explicitly parked (so nothing is silently dropped)

- **Lead-generation tooling** — parked pending a design that answers deliverability, GDPR and B-Corp reputation questions (the "multiple sending addresses" idea from June needs scrutiny before any build).
- **"GEO"** (generative-engine optimisation — making Koos show up in AI-generated answers) — separate workstream, unrelated to this rollout.
- **Deeper integration layers** (an MCP bridge — a technical connection layer between systems — and promotion automation) — trigger-gated: revisit only when manual promotion becomes the bottleneck.
- **Remaining Build Week tools** — in the team folders, promoted deliberately in Phase 2+.

---

## 11. What we need confirmed to start (the Phase-0 list)

1. GitHub organisation (or green light for Bazooka to create one in Koos's name).
2. Steward name(s) — ideally two — plus their booking arrangement (§3) and a slot for the 2-hour setup session.
3. Track A owner (contracts) and 2–3 Track B designers, plus the pilot project(s).
4. A slot for the 60–90 min guardrails working session with research/practice leads.
5. Legal capacity for the §5 data gate (DPA review + pilot-client contract sweep), and a `#koos-ai` Slack channel.

---

## 12. Pilot success criteria — agreed up front, judged by Koos

Assessed in the Week-3 session **by the sponsor, not by Bazooka**. Baselines captured before first tool use.

1. **Track A:** ≥ 3 live contracts through the checker; ≥ 1 tool-drafted amendment sent after the commercial owner's review; time-per-review vs. the pre-pilot baseline, with the target set by the sponsor at kickoff.
2. **Track B:** ≥ 2 real runs of the design/research tools whose outputs were actually used in project work — as judged by the designers.
3. **The loop lives:** ≥ 5 feedback entries from ≥ 2 Koos users (Bazooka's own entries don't count); ≥ 2 releases shipped in response; ≥ 1 release picked up on every pilot machine mid-pilot.
4. **Operational verdicts, documented:** Google Drive workflow (works / workaround / avoid) and update+auth reliability per machine.
5. **A decision** — expand / adjust / stop — made on this evidence.

These are criteria the pilot can *fail*. That's deliberate: if the value case is real, it survives being measured.

---

## 13. Risks & mitigations

| Risk | Status | Mitigation |
|---|---|---|
| **Google Drive project folders**: Claude Code reading Drive-for-Desktop files has known rough edges (online-only/streamed files; open bug reports) | Partially verified; the pilot settles it | "Make available offline" as standard practice (in the onboarding guide). **Plan B if the Week-3 verdict is "avoid":** (a) local working folder per project with a defined move-to-Drive step at project close (disk encryption — standard on modern Macs — to be confirmed across Koos's fleet or enforced centrally; governance implications named, not shrugged at), or (b) Drive stays the archive and active work happens in an offline-marked subset. The call is the sponsor's + steward's, with Week-3 evidence — it's an architecture decision, and it stays Koos's |
| **Tools quietly go stale on a machine** — background updates on a private repo need a one-time access token per machine, separate from normal GitHub login (documented behaviour; silent when missing) | Known, documented, designed around | Token setup + auth check are hard steps in onboarding; symptom + fix in the troubleshooting table; steward re-checks on any "stale tools" report |
| **Auto-update at startup** — documented, not yet observed on Koos machines | Doc-confirmed; manual path verified | To be confirmed on the first pilot laptops in Week 1; 30-second manual fallback; the mid-pilot release explicitly rehearses it |
| **Steward bottleneck / single point of failure** | Structural | Two stewards; booking code + re-decision point (§3); guides make the role transferable |
| **Feedback loop goes quiet** | The classic failure of shared libraries | Two-sentence bar; steward closes the loop visibly (what shipped, who flagged it); explicit success criterion (§12.3) |
| **Client data enters the canon** | Prevented by design | Only the steward writes to the canon; anonymisation gate on promotion; Build Week folders (which contain real client documents) are never copied wholesale |
| **A tool output reaches a client unreviewed** | Process | Track A has a named reviewer before anything goes out; designer-in-the-lead is in the guardrails and the onboarding framing |
| **Compliance surprise (client contracts, OR)** | Addressed up front | The §5 gate runs before live documents; OR informed before scale-out |

---

## 14. What Bazooka delivers per phase

| Phase | Deliverables | Effort |
|---|---|---|
| 0 | Repo handover to the Koos org; data-gate preparation (DPA summary, client-answer draft); guardrails working session; steward setup session; onboarding materials (done — in the repo) | [est. 10–14 h] |
| 1 | Designer + Track A onboarding; weekly support; fixes shipped as releases; pilot audit + review session | [est. 16–22 h] |
| 2 | Next-tool promotions (per tool: harden, package, release); sector guardrail modules with practice leads; scale-out mechanism; OR-briefing support | scoped after the pilot decision |
| 3 | Support + separately scoped, capped build sprints on Koos's trigger | per sprint |

---

## Appendix — claim verification status

Because this plan makes operational promises, the honest ledger. **Verified by doing** (multiple machines, June–July 2026): the install commands; the desktop-app GUI path with a private repo; namespaced skill invocation; the full release→marketplace-refresh→plugin-update loop; the settings blocks Claude Code writes on install; the bundled rule files byte-identical to the Build Week originals. **Documented, pilot-verifies:** automatic update pickup at startup on designer machines; team pre-provisioning (Claude Code prompting to add the marketplace when a shared project declares it). **Known behaviours and issues, designed around** (documented by Anthropic or on the public Claude Code issue tracker): marketplace remove/re-add doesn't refresh; `enabledPlugins` doesn't auto-install; background updates on private repos need an environment token (missing token fails silently); Google Drive online-only files. Details and sources live in the repo's `docs/`.
