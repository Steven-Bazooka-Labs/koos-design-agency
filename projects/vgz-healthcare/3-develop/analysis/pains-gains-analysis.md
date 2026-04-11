# Pains & Gains Analysis — VGZ Digital Self-Service Portal

---

## Executive Summary

This analysis identified 17 pains and 16 gains from concept testing of VGZ's digital self-service portal with 10 policyholders. The strongest finding is a structural mismatch: the portal provides transparency without agency. Participants valued the claims timeline universally (7/10), but the absence of action capability — appeals, messaging, medication feedback — was the most consistent critique (4 participants, 16/20 agent runs). Medication switch communication failure was the highest-frequency pain (9/10 participants, 18/20 runs), spanning functional confusion and genuine clinical anxiety. Two population-level risks emerged: the portal deepens digital exclusion for isolated elderly users, and the absence of granular privacy controls blocks adoption by a growing GGZ segment. The top recommendation is to launch claims tracking first, add two-way communication capability as a fast follow, and redesign medication change notifications in plain language with clinical reassurance before the medication feature goes live.

---

## Research Context

| Field             | Value                                                                 |
| ----------------- | --------------------------------------------------------------------- |
| Client            | Cooperatie VGZ                                                        |
| Phase             | Develop (Concept Testing)                                             |
| Research Type     | Evaluative — testing a clickable Figma prototype of a digital self-service portal |
| Participants      | 10 VGZ policyholders: 3 chronic condition, 2 parents, 2 elderly (65+), 1 occasional/healthy user, 1 mental health, 1 retired willing-learner. Ages 28–71. |
| Analysis Protocol | 4 extraction lenses (functional pains, emotional/social pains, functional gains, emotional/social gains) × 5 parallel agents = 20 independent extraction runs, followed by convergence analysis |
| Verification      | Quote verification (35 quotes, 0 fabricated), inference verification (12 inferences audited), and disagreement audit each run by independent agents |

---

## Pains

### High Confidence Pains (12+ of 20 runs)

#### PAIN-001: Medication changes communicated with jargon ("preferentiebeleid") rather than plain language — no clinical context, no confirmation that the prescribing doctor is aware

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 18/20 runs                                |
| Lens Breakdown    | Functional 5/5, Emotional 5/5, Func. Gain 4/5, Emot. Gain 4/5 |
| Category          | Functional + Emotional                     |
| Severity          | High                                       |
| Touchpoint        | Medication management — wijzigingshistorie screen; pharmacy counter (current state) |
| Participants      | 9/10 (P01, P02, P03, P04, P06, P07, P08, P09, P10) |

**Supporting Evidence:**

> "Wacht, hier staat een uitleg bij de wijziging. Er staat: 'gewijzigd vanwege preferentiebeleid.' Wat is preferentiebeleid? Dat is weer zo'n woord."
> — P02, identified by all 4 lenses

> "Hier staat niet: uw arts is akkoord. Hier staat niet: maakt u zich geen zorgen. Hier staat alleen een moeilijk woord en een datum."
> — P06, identified by all 4 lenses

> "Preferentiebeleid, ik ken het systeem inmiddels. Het is kostenbeheersing, dat is logisch, ik snap het rationeel. Maar de communicatie is onder de maat."
> — P07, identified by functional and emotional lenses

**Notes:** The verification audit nuanced this finding: digitally confident participants (P01, P04, P05, P07) understand the term but still find it insufficient. The shared pain across all segments is not incomprehension of the word itself but the absence of clinical context, reassurance, and next-step guidance. For lower-literacy participants (P02, P06), the term is genuinely incomprehensible and anxiety-inducing. P02 proposed the exact plain-language formulation needed: "Uw medicijn is van merk veranderd. Het werkzame bestanddeel is precies hetzelfde. Uw arts is hiervan op de hoogte."

---

#### PAIN-002: Claims submission is a "black hole" — no confirmation of receipt, no intermediate status, no expected processing timeline

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 17/20 runs                                |
| Lens Breakdown    | Functional 5/5, Emotional 3/5, Func. Gain 5/5, Emot. Gain 4/5 |
| Category          | Functional                                 |
| Severity          | High                                       |
| Touchpoint        | Declaratiestatus — post-submission waiting period (current Mijn VGZ) |
| Participants      | 7/10 (P01, P02, P03, P04, P07, P09, P10) |

**Supporting Evidence:**

> "Nu moet ik bellen om te vragen waar mijn declaratie is. Of ik zoek in Mijn VGZ maar daar staat alleen 'in behandeling' of 'afgehandeld.' Geen tussenliggende stappen, geen verwachte doorlooptijd, niets."
> — P01, identified by all 4 lenses

> "Ik dien ze in, digitaal via Mijn VGZ of soms per post als het digitaal niet lukt, en dan verdwijnen ze in een zwart gat."
> — P10, identified by functional and emotional lenses

> "Heb ik het goed gedaan? Heb ik de juiste bonnetjes meegestuurd? Is het geweigerd en heb ik de brief gemist?"
> — P03, identified by functional and emotional lenses

**Notes:** This is the pain with the clearest resolution path: the prototype's claims timeline received universally positive feedback. The current "in behandeling" / "afgehandeld" binary provides no useful information. P10 calls VGZ 2–3 times per month purely for status checks, at 30 minutes per call.

---

#### PAIN-003: Portal is view-only — participants cannot appeal claims, report medication problems, send messages, or initiate machtigingen

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 16/20 runs                                |
| Lens Breakdown    | Functional 5/5, Emotional 4/5, Func. Gain 4/5, Emot. Gain 3/5 |
| Category          | Functional                                 |
| Severity          | High                                       |
| Touchpoint        | Portal-wide — medication overview, claims status, all outcome screens |
| Participants      | 4/10 (P01, P03, P04, P10) |

**Supporting Evidence:**

> "Het is een vitrinekast, als ik eerlijk ben. Ik mag kijken, maar niet aanraken. En als patiënt met een chronische aandoening wil ik niet alleen geïnformeerd worden, ik wil gehoord worden."
> — P01, identified by all 4 lenses

> "Het is een etalage. Ik mag kijken, maar niet aanraken."
> — P04, identified by functional and emotional lenses

> "Informatie zonder de mogelijkheid om te handelen is als een recept zonder keuken. Je weet wat er zou moeten gebeuren, maar je kunt het niet doen."
> — P10, identified by functional and emotional lenses

**Notes:** The inference verification clarified that this critique does not make the portal net-negative. All participants who raised it (P01, P04, P10) confirmed they would still use the portal in its current form. P04 framed it as "een zes in plaats van een vier" — an improvement, but not the solution. The risk is that patients who encounter a negative event (rejected claim, unexplained medication switch) are redirected back to the telephone channel, replicating the frustration the portal is meant to reduce.

---

#### PAIN-004: No family or caregiver profile switching — must log out and re-authenticate with each family member's DigiD to access their data

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 14/20 runs                                |
| Lens Breakdown    | Functional 5/5, Emotional 3/5, Func. Gain 4/5, Emot. Gain 2/5 |
| Category          | Functional                                 |
| Severity          | High                                       |
| Touchpoint        | Portal access — profile/account management |
| Participants      | 3/10 (P01, P03, P07) |

**Supporting Evidence:**

> "Mijn eerste reactie is: kan ik hierin switchen tussen mijn eigen gegevens en die van Fenna? Want dat is mijn dagelijkse realiteit. [...] Als ik hier moet uitloggen en opnieuw inloggen om Fenna's spullen te zien, dan is het al niet meer handig. Dan is het twee keer de helft, in plaats van een keer het geheel."
> — P03, identified by functional and emotional lenses

> "Ik moet uitloggen en weer inloggen met haar DigiD. Elke keer. En haar DigiD werkt met haar telefoon, en die telefoon ligt bij haar thuis in Ede, en ik zit in Rotterdam."
> — P07, identified by all 4 lenses

**Notes:** For P07 (mantelzorger), this is not a convenience issue but a safety concern: her mother has dementia and cannot reliably relay DigiD codes. P03 previously filed a claim on the wrong policy because she confused family member accounts. P07 explicitly described the Netflix-style profile switch as the solution pattern.

---

#### PAIN-005: No advance notification before medication switch — participants discover the change at the pharmacy counter

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 14/20 runs                                |
| Lens Breakdown    | Functional 4/5, Emotional 4/5, Func. Gain 3/5, Emot. Gain 3/5 |
| Category          | Functional + Emotional                     |
| Severity          | High                                       |
| Touchpoint        | Medication management — pre-pharmacy notification gap |
| Participants      | 6/10 (P02, P04, P06, P07, P08, P09) |

**Supporting Evidence:**

> "Ik schrok me een hoedje. Ik dacht: dit is verkeerd, dit is niet van mij, er is een fout gemaakt."
> — P02, identified by functional and emotional lenses

> "Er was geen waarschuwing, geen uitleg, alleen een ander doosje bij de apotheek. Dat vond ik onverantwoord."
> — P08, identified by emotional lens

> "Er kwam een brief, naar haar adres in Ede, maar zij opent haar post niet meer consequent. [...] Die brief lag twee weken in de gang, tussen de reclamefolders."
> — P07, identified by all 4 lenses

**Notes:** The verification audit nuanced this: in some cases letters were sent but failed — wrong timing, wrong addressee (patient instead of caregiver), jargon. The pain is notification failure across every current channel, not the complete absence of notification. For P07's mother with dementia, the notification gap created a clinical safety risk: she took the wrong medication for a week because she did not recognise the new packaging.

---

#### PAIN-006: DigiD authentication is a functional blocker for elderly and digitally less confident users

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 13/20 runs (High analytical confidence, 2/10 participants) |
| Lens Breakdown    | Functional 4/5, Emotional 4/5, Func. Gain 2/5, Emot. Gain 3/5 |
| Category          | Functional                                 |
| Severity          | High                                       |
| Touchpoint        | Portal login — DigiD two-factor authentication |
| Participants      | 2/10 (P02, P06) |

**Supporting Evidence:**

> "Dan komt er een code op mijn telefoon, en dan moet ik die invoeren op de computer, maar dan is die code al verlopen, want ik was niet snel genoeg. En dan moet ik opnieuw beginnen. Annelies doet dat in twee minuten, maar ik zit er een halfuur mee. En dan geef ik het op."
> — P02, identified by functional and emotional lenses

> "Na drie keer proberen stond mijn account geblokkeerd. Peter heeft dat opgelost, over de telefoon, vanuit Groningen, en dat duurde een uur. En daarna voelde ik me zo, zo nutteloos."
> — P06, identified by emotional lens

**Notes:** High analytical confidence (13/20 runs extracted this independently) despite only 2 participants. The evidence is deeply detailed and specific. Both P02 and P06 describe DigiD not as difficult but as impossible without help. P06's account resulted in a blocked account. This finding should be read alongside the broader populations both participants reference: P02's buurvrouw (74, no internet) and P06's bridgeclub (four widowed women, all struggling with digital tools).

---

#### PAIN-007: Dependency on family members for basic insurance tasks — elderly participants cannot use digital systems independently and experience this as a loss of identity

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 13/20 runs (High analytical confidence, 2/10 participants) |
| Lens Breakdown    | Functional 3/5, Emotional 5/5, Emot. Gain 4/5 |
| Category          | Functional + Social                        |
| Severity          | High                                       |
| Touchpoint        | All digital interactions — delegated to daughters/sons |
| Participants      | 2/10 (P02, P06) |

**Supporting Evidence:**

> "Ik voel me dan een beetje... ja, een last. Dat klinkt misschien overdreven, maar het is wel zo. Ik heb altijd alles zelf gedaan, weet u."
> — P02, identified by all emotional lenses

> "Ik wil niet die moeder zijn die elke dag belt met een probleem."
> — P06, identified by emotional lens

> "Ik was niet hulpeloos, ik was de helft van een team. En nu moet ik het hele team zijn, en dat lukt niet altijd, maar ik wil het wel proberen."
> — P02, identified by emotional gain lens

**Notes:** This pain is deeply interwoven with bereavement (both P02 and P06 lost their husbands) and with identity ("ik was een zelfstandige vrouw"). The dependency is not merely practical — it threatens their sense of self as capable adults. P02 times her calls to Annelies for Tuesday evenings after the children's bedtime to minimise the burden she perceives herself to be.

---

#### PAIN-008: Patient forced to be the sole coordinator between GP, pharmacy, and insurer during medication disputes

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 12/20 runs                                |
| Lens Breakdown    | Functional 4/5, Emotional 3/5, Func. Gain 3/5 |
| Category          | Functional                                 |
| Severity          | High                                       |
| Touchpoint        | Medication management — cross-party coordination during machtiging process |
| Participants      | 4/10 (P01, P04, P09, P10) |

**Supporting Evidence:**

> "Iedereen wijst naar iemand anders. Dat is toch niet normaal? Ik ben de enige in dit verhaal die elke dag die pillen slikt, en ik ben de enige die niet gehoord wordt."
> — P04, identified by functional and emotional lenses

> "Dat had ik zelf moeten uitzoeken. De verzekeraar had me niet gewaarschuwd. De apotheek bagatelliseerde het. Als patiënt moet je zelf opletten."
> — P09, identified by functional lens

**Notes:** P04's experience is the most detailed: three months of stomach complaints while navigating between GP, pharmacy, and VGZ, involving five phone calls, two extra GP visits, and three pharmacy visits (~10 hours total). The system failure is not any single party but the absence of process ownership. The portal concept does not address this coordination gap.

---

#### PAIN-009: Elderly and isolated participants experience the portal as deepening their exclusion from a digital-first society

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 12/20 runs (High analytical confidence, 2/10 participants) |
| Lens Breakdown    | Functional 2/5, Emotional 5/5, Emot. Gain 4/5 |
| Category          | Social + Emotional                         |
| Severity          | High                                       |
| Touchpoint        | Portal concept — overall encounter with the prototype |
| Participants      | 2/10 (P02, P06) |

**Supporting Evidence:**

> "Overal word ik een beetje meer buitengesloten. En dit portaal, hoe goed bedoeld ook, voelt als nog een deur die dichtgaat."
> — P06, identified by emotional lens

> "Wij zijn niet lui. Wij zijn niet dom. Wij zijn opgegroeid in een andere wereld, en die wereld is veranderd, en wij proberen bij te houden. Maar het gaat te snel soms."
> — P02, identified by emotional lens

**Notes:** This finding applies to a specific sub-segment: older users who combine low digital confidence with limited social support networks. It is not a blanket characterisation of older adults. P09 (age 62) responded positively to the portal and positioned herself as a "willing learner," demonstrating that age alone is not a proxy for exclusion. The risk is highest for users like P02 and P06 — widowed, isolated, without a tech-savvy family member nearby. P06 references her bridgeclub: four widowed women, all struggling with the same digital barriers.

---

### Medium Confidence Pains (6-11 of 20 runs)

#### PAIN-010: No eigen risico or coverage limit visibility during the year — participants cannot plan care or finances

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 11/20 runs                                |
| Lens Breakdown    | Functional 4/5, Func. Gain 4/5, Emot. Gain 2/5 |
| Category          | Functional                                 |
| Severity          | Medium                                     |
| Touchpoint        | Dashboard — absent feature |
| Participants      | 5/10 (P01, P04, P06, P09, P10) |

**Supporting Evidence:**

> "Ik wil in januari al weten: als ik dit tempo doorzet, hoeveel moet ik zelf bijbetalen in december? Een soort voorspelling, gebaseerd op mijn verbruikspatroon."
> — P01, identified by functional lens

> "Een eigen-risicomameter. Hoe ver ben ik met mijn eigen risico dit jaar? [...] Dan weet ik in een oogopslag: ik heb nog 180 euro over, dus die fysiotherapie kan er nog bij."
> — P09, identified by functional lens

**Human Review Note:** Five participants across diverse profiles identified this independently. The disagreement audit rated it "likely valid." P06's mention is softer (a literacy issue as much as a visibility issue), but P01, P04, P09, and P10 each articulated the need with specificity. Upgrade candidate if chronic patient segment is weighted in prioritisation.

---

#### PAIN-011: GGZ and sensitive health data visible by default on dashboard — no granular privacy controls, creating an adoption barrier for the mental health segment

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 9/20 runs (downgraded from Medium toward Low after verification) |
| Lens Breakdown    | Functional 2/5, Emotional 2/5, Func. Gain 2/5, Emot. Gain 3/5 |
| Category          | Functional + Social                        |
| Severity          | High (potential impact)                    |
| Touchpoint        | Dashboard — GGZ declarations and medication visible at first login |
| Participants      | 1/10 (P08); P05 corroborates indirectly |

**Supporting Evidence:**

> "Mijn GGZ-sessies? Die wil ik niet op het dashboard. Niet als eerste ding dat ik zie als ik inlog. En al helemaal niet als iemand over mijn schouder meekijkt. Een collega, een familielid, een partner."
> — P08, identified by functional and emotional lenses

> "Ik snap dat iemand die in behandeling is voor iets gevoeligs, depressie, een verslaving, een SOA, daar totaal anders over denkt. En voor die mensen moet je extra waarborgen inbouwen."
> — P05, identified by functional gain lens

**Human Review Note:** This finding rests primarily on one participant (P08), with indirect corroboration from P05. The disagreement audit rated it "needs human judgment." P08's evidence is specific and credible — she describes concrete scenarios (ex-partner accessing account, colleague seeing lock screen, HR stumbling on data). The "growing segment" claim draws on P08's citation of GGZ as the fastest-growing care category. **Recommend dedicated GGZ-segment research before treating this as a confirmed adoption barrier at population level.** However, implementing granular privacy controls is independently justified as a healthcare data handling best practice under AVG/GDPR.

---

#### PAIN-012: Medication switches cause physiological effects beyond administrative inconvenience — distinct from nocebo, particularly for thyroid and psychiatric medications

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 9/20 runs                                |
| Lens Breakdown    | Functional 3/5, Emotional 3/5, Emot. Gain 2/5 |
| Category          | Functional + Emotional                     |
| Severity          | High                                       |
| Touchpoint        | Medication management — post-switch period |
| Participants      | 3/10 (P04, P08, P09) |

**Supporting Evidence:**

> "Mijn TSH was iets verschoven. Niet dramatisch, van 2.1 naar 2.8, nog binnen de norm, maar het bevestigde dat zo'n wisseling niet niets is."
> — P09, identified by functional lens

> "De eerste twee weken na de switch had ik meer last van trillingen, slaapproblemen, en een soort wazig gevoel. En er was geen waarschuwing, geen uitleg."
> — P08, identified by emotional lens

**Human Review Note:** Evidence varies by medication class. P09 provides objective clinical data (TSH shift confirmed by blood test) for levothyroxine. P08 describes symptoms consistent with known pharmacokinetic variation in antidepressants. P04 explicitly acknowledges the nocebo possibility for omeprazol/pantoprazol. **[Human Review Required]** Clinical accuracy of this characterisation should be verified by a medical advisor before this finding informs portal design decisions about medication switch warnings.

---

#### PAIN-013: Chronic patients have normalised spending 1.5–3 hours per month on administrative phone calls as "just how it works"

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 8/20 runs                                |
| Lens Breakdown    | Functional 3/5, Emotional 2/5, Func. Gain 2/5 |
| Category          | Functional                                 |
| Severity          | Medium                                     |
| Touchpoint        | Helpdesk — calling for claim status, medication queries |
| Participants      | 3/10 (P01, P07, P10) |

**Supporting Evidence:**

> "Nu bel ik misschien twee keer per kwartaal met de klantenservice alleen voor declaratievragen. Dat zijn gesprekken van minimaal een kwartier, met wachttijd erbij."
> — P01, identified by functional lens

> "Twee, drie keer per maand. Soms vaker. [...] Dat is anderhalf uur per maand dat ik aan de telefoon zit met mijn verzekeraar. Tijd die ik niet heb, want op slechte dagen kan ik nauwelijks mijn bed uitkomen vanwege de pijn."
> — P10, identified by functional and emotional lenses

**Notes:** The pains methodology explicitly supports identifying normalised pains — friction that participants have stopped complaining about because they have accepted it as inevitable. P10 connects calling time directly to physical suffering; P07 describes avoiding calls entirely because 20 minutes on hold is time she cannot spare. The verification audit confirmed this as well-supported.

---

#### PAIN-014: Helpdesk jargon and speed cause elderly participants to self-censor — they stop asking questions to avoid appearing incompetent

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 8/20 runs (Medium analytical confidence, 2/10 participants) |
| Lens Breakdown    | Emotional 4/5, Emot. Gain 2/5 |
| Category          | Social + Emotional                         |
| Severity          | High                                       |
| Touchpoint        | Helpdesk — phone calls with VGZ agents |
| Participants      | 2/10 (P02, P06) |

**Supporting Evidence:**

> "Die mensen aan de telefoon praten zo snel, en ze gebruiken woorden die ik niet altijd begrijp, 'preferentiebeleid,' 'therapeutisch equivalent,' dat soort dingen. En dan durf ik niet te vragen of ze het nog een keer willen uitleggen, want dan denken ze: die snapt het niet."
> — P02, identified by emotional lens

**Notes:** The consequence of this self-censoring is behavioural: P02 stops calling VGZ entirely and delegates to her daughter. The fear is not imagined — it is a response to a real interaction dynamic where speed and jargon signal that slower callers are unwelcome. This is a social pain with a functional consequence: participants lose access to the primary support channel.

---

#### PAIN-015: Referral letters require manual patient handoff — faxing, posting, or photographing paper documents

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 7/20 runs                                |
| Lens Breakdown    | Functional 4/5, Func. Gain 3/5 |
| Category          | Functional                                 |
| Severity          | Medium                                     |
| Touchpoint        | Verwijsbrieven — document submission process |
| Participants      | 5/10 (P01, P03, P06, P07, P09) |

**Supporting Evidence:**

> "Ik heb twee keer een verwijsbrief moeten faxen. Faxen! In 2025!"
> — P01, identified by functional lens

> "Waarom moet ik als mantelzorger een papieren brief ophalen bij de huisarts in Ede, mee naar huis nemen in Rotterdam, fotograferen, uploaden, en hopen dat de foto leesbaar is?"
> — P07, identified by functional lens

**Notes:** Multiple participants (P01, P05, P07) independently pointed out that the real solution is automatic transfer via Zorgdomein or LSP, not a patient-operated upload function. P05 characterised the upload button as "een pleister op een gebroken been." The portal's upload feature is an improvement over faxing/posting but does not address the systemic integration gap.

---

#### PAIN-016: Fear of making irreversible mistakes in the portal prevents elderly participants from even beginning to explore

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 7/20 runs (Medium analytical confidence, 2/10 participants) |
| Lens Breakdown    | Emotional 3/5, Func. Gain 2/5 |
| Category          | Emotional                                  |
| Severity          | Medium                                     |
| Touchpoint        | Portal interface — initial encounter |
| Participants      | 2/10 (P02, P06) |

**Supporting Evidence:**

> "Ik ben bang dat ik iets verkeerd doe. Dat ik ergens op klik en dat er iets verandert. Stel dat ik ergens op klik en ik verander iets aan mijn polis?"
> — P06, identified by emotional lens

> "Er moet bij staan: 'U kunt niets kapotmaken. Als u ergens op klikt, kunt u altijd terug.' Want dat is mijn grootste angst, dat ik iets doe wat niet meer ongedaan gemaakt kan worden."
> — P02, identified by emotional lens

**Notes:** P06 grounds this fear in a real prior experience: she once accidentally deleted a tax email and her son had to retrieve it. The fear is evidence-based, not abstract technophobia. Both participants independently proposed the same solution: a visible, persistent "u kunt niets kapotmaken" reassurance message.

---

### Low Confidence Pains (1-5 of 20 runs) — Observations

#### PAIN-017: Medication change for a child creates heightened parental anxiety — changes feel more threatening when the patient is your child

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 5/20 runs                                |
| Category          | Emotional                                  |
| Severity          | Medium                                     |
| Participants      | 1/10 (P03) |

> "Maar is het hetzelfde? Het is voor een kind van twee! Ik wil dan weten: is dit getest op kleine kinderen? Zitten er andere hulpstoffen in?"
> — P03

**Review Recommendation:** Observation — single participant. Flag for follow-up research with a parent cohort. The parental-anxiety dimension of medication switches is distinct from the adult-patient dimension and may warrant its own analysis.

---

#### PAIN-018: Lock-screen push notifications could expose GGZ medication status in social or workplace contexts

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 5/20 runs                                |
| Category          | Social                                     |
| Severity          | High (potential impact)                    |
| Participants      | 1/10 (P08) |

> "Een pushbericht met 'GGZ-medicatie gewijzigd' op je lockscreen, terwijl je telefoon op tafel ligt bij een werkoverleg: dat is een nachtmerrie."
> — P08

**Review Recommendation:** Observation — single participant. However, the design implication (privacy-aware notifications for sensitive categories) is valid regardless of participant count as a healthcare data handling best practice. P08's proposed solution: "Alleen 'U heeft een bericht in uw gezondheidsportaal.' Punt. Niet wat het bericht is."

---

#### PAIN-019: Portal centralises health data in a human-readable UI, creating a new privacy exposure that did not exist in the fragmented current system

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 4/20 runs                                |
| Category          | Functional                                 |
| Severity          | Medium                                     |
| Participants      | 1/10 (P08) |

> "Met dit portaal wordt het een overzichtelijk scherm. Het wordt visueel, het wordt leesbaar, het wordt menselijk interpreteerbaar. En dat maakt het kwetsbaarder. Toegankelijker is niet altijd beter."
> — P08

**Review Recommendation:** Observation — single participant. The underlying principle (centralisation increases exposure surface) is a valid security consideration for the development team.

---

## Gains

### High Confidence Gains (12+ of 20 runs)

#### GAIN-001: Real-time claims status timeline (ingediend → in beoordeling → goedgekeurd → uitbetaald) eliminates need to call for status

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 18/20 runs                                |
| Lens Breakdown    | Functional 5/5, Emotional 5/5, Func. Gain 5/5, Emot. Gain 4/5 (note: counted via pain-inverse) |
| Category          | Expected                                   |
| Type              | Functional                                 |
| Participants      | 7/10 (P01, P02, P03, P04, P07, P09, P10) |

**Supporting Evidence:**

> "Dit is precies wat ik mis. [...] Net als bij een pakketje volgen bij PostNL. Dat snap ik meteen. Ik hoef niemand uitleg te vragen. Dit zou mij echt helpen."
> — P01, identified by all 4 lenses

> "Oh. Oh, dit is goed. Een tijdlijn per declaratie. [...] Als dit er was geweest vorig jaar, dan had ik niet drie keer hoeven bellen."
> — P10, identified by functional and emotional lenses

> "Met dit overzicht zou ik in een oogopslag zien: oké, het is in beoordeling, het duurt nog even, maar het is er. Ik hoef niet te bellen. Ik hoef niet te twijfelen. Dat scheelt mij stress. Echt waar."
> — P03, identified by functional and emotional lenses

**Notes:** The most universally valued feature in the prototype. Every participant who commented rated it positively. P05 (UX designer) characterised it as "hygiëne" — table stakes, not a differentiator. Multiple participants compared it to package tracking (PostNL) and banking apps.

---

#### GAIN-002: Plain-language explanation of medication changes with explicit doctor-awareness confirmation

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 18/20 runs                                |
| Lens Breakdown    | All 4 lenses |
| Category          | Desired (downgraded from Required after verification) |
| Type              | Functional + Emotional                     |
| Participants      | 9/10 implicit; P02, P05, P06, P09 explicit |

**Supporting Evidence:**

> "Kunt u dat er niet bij zetten, in gewone mensentaal? Zoiets als: 'Uw medicijn is van merk veranderd. Het werkzame bestanddeel is precies hetzelfde. Uw arts is hiervan op de hoogte en heeft goedkeuring gegeven.' Dan snap ik het. Dan ben ik gerustgesteld. Nu word ik juist ongeruster."
> — P02, identified by all 4 lenses

> "Dat geeft rust. En rust is wat ik nodig heb. Mijn hart heeft rust nodig, letterlijk."
> — P06, identified by emotional lens

**Notes:** Downgraded from Required to Desired after verification: no participant said they would reject the portal without this. However, its absence causes anxiety specifically in the medication feature, and for vulnerable participants (P02, P06) the emotional impact is severe. The gain is high-priority Desired, not baseline Required.

---

#### GAIN-003: Two-way action capability — appeals, messaging, feedback, and machtiging requests from within the portal

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 17/20 runs                                |
| Lens Breakdown    | All 4 lenses |
| Category          | Desired                                    |
| Type              | Functional                                 |
| Participants      | 4/10 (P01, P03, P04, P10) |

**Supporting Evidence:**

> "Het moet tweerichtingsverkeer worden. Ik wil niet alleen kijken, ik wil ook communiceren. Ik wil een dialoog, geen monoloog."
> — P04, identified by all 4 lenses

> "Als ik vanuit dit scherm een bezwaar kan indienen, met een formulier dat al mijn gegevens heeft, en ik alleen hoef te schrijven waarom ik het er niet mee eens ben, dan is het een gamechanger."
> — P10, identified by functional lens

**Notes:** The single most cross-cutting functional gap across all participant segments. P01's "vitrinekast" and P04's "etalage" metaphors both point to this absence. The portal concept generates genuine excitement — which makes the absence of action capability a sharper disappointment.

---

#### GAIN-004: Profile switching for family members and caregivers without re-authentication (Netflix-style)

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 15/20 runs                                |
| Lens Breakdown    | Functional 5/5, Emotional 3/5, Func. Gain 4/5, Emot. Gain 2/5 |
| Category          | Required (for caregiver/family segment)    |
| Type              | Functional                                 |
| Participants      | 3/10 (P01, P03, P07) |

**Supporting Evidence:**

> "Een soort profielswitch, zoals je bij Netflix hebt: klik op het profielfoto, wissel naar 'Moeder,' en ik zie al haar declaraties. Dat moet erin."
> — P07, identified by all 4 lenses

> "Een gezinsoverzicht. Ik wil niet switchen tussen profielen, ik wil een dashboard waar ik in een oogopslag zie: mijn declaraties, Fenna's declaraties, openstaande taken, komende afspraken."
> — P03, identified by functional lens

**Notes:** For the caregiver and parent segments, this is a baseline requirement — without it, the portal has "niet meer waarde dan wat ik nu al doe met mijn Notion-bord" (P07). P07 estimated the portal with proper caregiver features would save her 60+ hours per year.

---

#### GAIN-005: Feeling independent and self-sufficient — not a burden on adult children for basic insurance tasks

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 14/20 runs (High analytical confidence, 2/10 participants) |
| Lens Breakdown    | Emotional 5/5, Func. Gain 2/5, Emot. Gain 5/5 |
| Category          | Required (emotional baseline)              |
| Type              | Emotional                                  |
| Participants      | 2/10 (P02, P06) |

**Supporting Evidence:**

> "Als ik het zelf zou kunnen gebruiken, makkelijk, zonder gedoe met inloggen en codes en wachtwoorden, en als het in gewone taal geschreven was, niet in verzekeraarstaal, dan zou ik het fijn vinden. Want dan hoef ik Annelies niet meer te bellen. Dan kan ik het zelf. En dat wil ik eigenlijk het liefste."
> — P02, identified by emotional lens

> "Ik was niet hulpeloos, ik was de helft van een team. En nu moet ik het hele team zijn, en dat lukt niet altijd, maar ik wil het wel proberen."
> — P02, identified by emotional gain lens

**Notes:** Deeply evidenced from two participants whose accounts carry significant emotional weight. The gain is not about convenience — it is about identity restoration after bereavement and the reclamation of autonomy.

---

#### GAIN-006: Proactive advance notification of medication change (2+ weeks before pharmacy dispensing)

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 13/20 runs                                |
| Lens Breakdown    | All 4 lenses |
| Category          | Desired                                    |
| Type              | Functional                                 |
| Participants      | 2/10 explicit (P07, P09); 6/10 implicit via pain accounts |

**Supporting Evidence:**

> "Een bericht, twee weken van tevoren: 'Let op: uw medicijn levothyroxine wordt volgende maand gewijzigd naar een ander merk. Dit is waarom. Dit kunt u verwachten. Dit is wat u kunt doen als u vragen heeft. Klik hier om uw huisarts te informeren.'"
> — P09, identified by functional and emotional lenses

**Notes:** P09 provided the most detailed notification template of any participant. For P07's mother with dementia, advance notification to the caregiver (not the patient) is a safety requirement: the near-miss of a week on the wrong medication could have been prevented by a timely notification to P07 in Rotterdam.

---

#### GAIN-007: Feeling in control of health administration — "het gevoel dat het op orde is"

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 12/20 runs                                |
| Lens Breakdown    | Func. Gain 2/5, Emot. Gain 5/5, Emotional 3/5 |
| Category          | Required (emotional baseline)              |
| Type              | Emotional                                  |
| Participants      | 5/10 (P01, P03, P04, P09, P10) |

**Supporting Evidence:**

> "Het gevoel dat het op orde is. Dat ik het onder controle heb. Dat ik een goede moeder ben die ook de administratie aankan."
> — P03, identified by emotional gain lens

> "Dit portaal zou ramen in die wachtruimte maken. Ik kan zien wat er gebeurt, wanneer het gebeurt, en waarom. [...] Frustratie komt grotendeels van onzekerheid."
> — P04, identified by functional and emotional lenses

---

### Medium Confidence Gains (6-11 of 20 runs)

#### GAIN-008: Real-time eigen risico (deductible) meter visible on dashboard

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 11/20 runs                                |
| Category          | Desired                                    |
| Type              | Functional                                 |
| Participants      | 4/10 (P01, P04, P09, P10) |

> "Een eigen-risicomameter. Hoe ver ben ik met mijn eigen risico dit jaar? Hoeveel is er al verbruikt? Hoeveel heb ik nog over? Dat zou bovenin het dashboard moeten staan, altijd zichtbaar, als een soort thermometer."
> — P09

---

#### GAIN-009: Push notifications for status changes coming to the user rather than requiring login

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 10/20 runs                                |
| Category          | Desired                                    |
| Type              | Functional                                 |
| Participants      | 5/10 (P01, P03, P05, P07, P09) |

> "Als mijn declaratie van status verandert, wil ik een push-notificatie. Als mijn medicatie wijzigt, wil ik direct een bericht met uitleg, niet een brief die drie weken later op de mat valt."
> — P01

> "De informatie moet naar mij komen, niet andersom."
> — P03

---

#### GAIN-010: Granular privacy controls — ability to hide GGZ and sensitive health categories behind extra authentication

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 10/20 runs                                |
| Category          | Required (for GGZ-sensitive feature adoption, not for baseline portal adoption) |
| Type              | Functional + Emotional                     |
| Participants      | 1/10 (P08); P05 corroborates indirectly |

> "Privacyinstellingen als first-class feature. Niet als afterthought, niet als een pagina in de instellingen die niemand vindt, maar als een prominent onderdeel van het portaal."
> — P08

**Human Review Note:** Required specifically for adoption of the sensitive-data features (medication history, care provider search, referral letters indicating diagnosis) by the GGZ segment. P08 confirmed she would use the declaratiestatus for non-sensitive items regardless. Without privacy controls, users like P08 will adopt the portal partially, bypassing the features with the highest potential value for their care needs.

---

#### GAIN-011: Medication overview replaces personal spreadsheets and manual tracking systems

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 8/20 runs                                |
| Category          | Desired                                    |
| Type              | Functional                                 |
| Participants      | 2/10 (P01, P07) |

> "Het verschil is overzicht. Alles op een plek. Ik hoef niet meer drie systemen te checken en de resultaten handmatig samen te voegen in mijn spreadsheet."
> — P01

---

#### GAIN-012: Co-browsing helpdesk — a human who can see the user's screen in real time ("mensenknop")

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Confidence Score  | 7/20 runs                                |
| Category          | Desired                                    |
| Type              | Functional + Emotional                     |
| Participants      | 3/10 (P01, P02, P06) |

> "Een grote knop, onderin, waarmee ik iemand aan de telefoon krijg die meteen ziet wat ik zie. Niet dat ik eerst tien minuten moet uitleggen op welk scherm ik zit."
> — P02

> "Als iemand naast me zit en het me laat zien. [...] Of iemand die meekijkt, die zegt: 'Ik zie uw scherm, mevrouw, u bent op de medicatiepagina, klik nu op het groene vakje.' Dan voelt het alsof er iemand naast me zit. Zoals Jan deed."
> — P02

**Notes:** One of the strongest independently convergent feature requests — P02 and P06 described the identical concept without hearing each other's responses. The verification audit confirmed this as well-supported. For the digitally excluded segment, this feature bridges the gap between self-service and human support.

---

### Low Confidence Gains (1-5 of 20 runs) — Observations

#### GAIN-013: Familiar banking-app dashboard layout reduces learning curve

| Participants | 3/10 (P01, P07, P09) |
| Confidence Score | 5/20 runs |

> "Het lijkt op mijn bankapp, de ING-app. En die kan ik goed gebruiken. [...] Als dit portaal op dezelfde manier werkt, dan denk ik dat ik dit ook kan leren."
> — P09

**Review Recommendation:** Design validation finding. The banking-app convention reduces onboarding friction for digitally capable users.

---

#### GAIN-014: Medication information linked to trusted sources (Farmacotherapeutisch Kompas, patient associations) rather than unfiltered Google results

| Participants | 2/10 (P01, P09) |
| Confidence Score | 5/20 runs |

> "Een officiele bron, geselecteerd door VGZ of door een arts, betrouwbaar en begrijpelijk, dat zou ik vertrouwen."
> — P09

---

#### GAIN-015: Privacy-aware notifications — no content on lock screen, only "u heeft een bericht"

| Participants | 1/10 (P08) |
| Confidence Score | 4/20 |

**Review Recommendation:** Observation — but the design implication is valid as a healthcare data handling best practice.

---

#### GAIN-016: Access audit log — who viewed my data, when, and why

| Participants | 1/10 (P08) |
| Confidence Score | 3/20 |

> "Een inzagelogboek. Wie heeft mijn data ingezien, wanneer, en waarom. [...] Dat is niet alleen een privacy-feature, het is een vertrouwensfeature."
> — P08

**Review Recommendation:** Observation. The underlying principle (transparency over data access) has regulatory relevance.

---

#### GAIN-017: Tax year overview exportable for belastingaangifte

| Participants | 1/10 (P09) |
| Confidence Score | 3/20 |

**Review Recommendation:** Observation. Unexpected use case outside the portal's primary scope.

---

#### GAIN-018: Practice/sandbox mode for exploring without consequences

| Participants | 1/10 (P02) |
| Confidence Score | 2/20 |

> "Een soort oefenomgeving. Waar ik kan rondklikken zonder dat het echt is. Zodat ik kan oefenen. Net als die vluchtsimulator voor piloten, maar dan voor mij en mijn verzekeringszaken."
> — P02

**Review Recommendation:** Observation. The underlying need (reducing irreversibility fear) can be addressed through standard UX patterns: confirmation dialogs, visible undo, and the "u kunt niets kapotmaken" reassurance message.

---

## Pain-Gain Connections

### Connection 1: Black Hole → Timeline

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Pain              | PAIN-002: Claims submission is a black hole |
| Related Gain      | GAIN-001: Real-time claims status timeline |
| Relationship      | Direct inverse — solving this pain directly enables this gain |
| Design Implication | The claims timeline is the highest-value, lowest-risk feature to launch first. Every participant validated it. It addresses the most widespread pain (7/10) with the most universally positive response. |

### Connection 2: Jargon → Plain Language

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Pain              | PAIN-001: Medication communicated with jargon |
| Related Gain      | GAIN-002: Plain-language explanation with doctor confirmation |
| Relationship      | Direct inverse — plain language eliminates the jargon pain |
| Design Implication | Every medication change screen needs a 3-sentence plain Dutch explanation. P02 wrote the template: "Uw medicijn is van merk veranderd. Het werkzame bestanddeel is precies hetzelfde. Uw arts is hiervan op de hoogte." |

### Connection 3: Display Case → Two-Way Communication

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Pain              | PAIN-003: Portal is view-only |
| Related Gain      | GAIN-003: Two-way action capability |
| Relationship      | Direct inverse — interactivity transforms the portal from information display to care tool |
| Design Implication | Without action capability, the portal surfaces problems without enabling resolution — redirecting patients back to the phone. Priority actions: appeals on rejected claims, medication feedback, messaging. |

### Connection 4: No Profile Switch → Netflix-Style Switching

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Pain              | PAIN-004: No family/caregiver profile switching |
| Related Gain      | GAIN-004: Profile switching without re-authentication |
| Relationship      | Direct inverse |
| Design Implication | Non-negotiable for parents and mantelzorgers. Without it, the portal serves individuals but not families — missing the actual unit of healthcare administration. |

### Connection 5: Pharmacy Surprise → Advance Notification

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Pain              | PAIN-005: No advance notification before medication switch |
| Related Gain      | GAIN-006: Proactive notification 2+ weeks ahead |
| Relationship      | Direct inverse — advance notification prevents the pharmacy-counter shock |
| Design Implication | Proactive notification 2 weeks before switch takes effect, sent to the managing person (patient or caregiver), in plain language. For P07's mother with dementia, this is a clinical safety measure. |

### Connection 6: Dependency → Independence

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Pain              | PAIN-007: Dependency on children creates shame |
| Related Gain      | GAIN-005: Feeling independent and self-sufficient |
| Relationship      | Emotional inverse — portal accessibility determines whether elderly users regain or lose independence |
| Design Implication | Accessibility is not an afterthought — it is the difference between identity restoration and identity loss for this segment. Co-browsing helpdesk (GAIN-012) is the bridge. |

### Connection 7: Digital Exclusion → Co-Browsing Support

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Pain              | PAIN-009: Portal deepens digital exclusion |
| Related Gain      | GAIN-012: Co-browsing helpdesk ("mensenknop") |
| Relationship      | Partial resolution — co-browsing bridges the gap for users who cannot self-serve |
| Design Implication | A visible "bel ons" button that initiates co-browsing (agent sees user's screen) was independently proposed by P01, P02, and P06. This is not a nice-to-have — for the excluded segment, it determines whether the portal is accessible at all. |

### Connection 8: GGZ Exposure → Granular Privacy

| Attribute         | Value                                      |
| ----------------- | ------------------------------------------ |
| Pain              | PAIN-011: GGZ data visible by default |
| Related Gain      | GAIN-010: Granular privacy controls |
| Relationship      | Direct inverse |
| Design Implication | Privacy controls as a first-class onboarding feature. At first login: "Wilt u bepaalde categorieën zorg verbergen op uw dashboard?" Without this, a significant and growing user segment will partially bypass the portal. |

---

## Prioritization Matrix

| ID | Finding | Evidence Strength | Potential Impact | Frequency | Priority |
|---|---|---|---|---|---|
| PAIN-001 | Medication changes communicated with jargon, no clinical context | High (18/20, cross-lens) | High (causes anxiety, clinical risk) | High (9/10) | **Immediate** |
| PAIN-002 | Claims submission is a black hole | High (17/20, cross-lens) | High (drives majority of phone calls) | High (7/10) | **Immediate** |
| PAIN-003 | Portal is view-only — no action capability | High (16/20, cross-lens) | High (redirects to phone, frustrates chronic patients) | Medium (4/10) | **Strong opportunity** |
| PAIN-004 | No family/caregiver profile switching | High (14/20) | High (safety risk for dementia patients) | Low (3/10) | **Strong opportunity** |
| PAIN-005 | No advance notification before medication switch | High (14/20) | High (clinical safety, pharmacy shock) | Medium (6/10) | **Immediate** |
| PAIN-006 | DigiD is a functional blocker for elderly | High analytical (13/20) | High (total access barrier) | Low (2/10) | **Human review** |
| PAIN-007 | Dependency on children creates shame and identity loss | High analytical (13/20) | High (identity, wellbeing) | Low (2/10) | **Human review** |
| PAIN-008 | Patient as sole coordinator between GP, pharmacy, insurer | High (12/20) | High (months of suffering) | Medium (4/10) | **Strong opportunity** |
| PAIN-009 | Portal deepens digital exclusion for isolated elderly | High analytical (12/20) | High (systemic exclusion) | Low (2/10) | **Human review** |
| PAIN-010 | No eigen risico / coverage limit visibility | Medium (11/20) | Medium (financial planning) | Medium (5/10) | **Worth exploring** |
| PAIN-011 | GGZ data visible by default, no privacy controls | Medium (9/20) | High (adoption barrier for GGZ segment) | Low (1/10) | **Human review** |
| PAIN-012 | Medication switches cause physiological effects | Medium (9/20) | High (clinical) | Low (3/10) | **Human review** |
| PAIN-013 | Normalised administrative calling time (1.5-3 hrs/month) | Medium (8/20) | Medium (time, physical cost) | Low (3/10) | **Worth exploring** |
| PAIN-014 | Helpdesk jargon causes self-censoring in elderly | Medium (8/20) | High (access barrier) | Low (2/10) | **Human review** |
| GAIN-001 | Real-time claims status timeline | High (18/20) | High (eliminates primary call reason) | High (7/10) | **Immediate** |
| GAIN-002 | Plain-language medication explanation with doctor confirmation | High (18/20) | High (reduces anxiety for vulnerable patients) | High (9/10 implicit) | **Immediate** |
| GAIN-003 | Two-way action capability (appeals, messaging, feedback) | High (17/20) | High (transforms portal from display to tool) | Medium (4/10) | **Strong opportunity** |
| GAIN-004 | Profile switching for family/caregivers | High (15/20) | High (safety, time savings) | Low (3/10) | **Strong opportunity** |
| GAIN-005 | Feeling independent, not a burden | High analytical (14/20) | High (identity, wellbeing) | Low (2/10) | **Human review** |
| GAIN-006 | Proactive advance notification 2+ weeks before switch | High (13/20) | High (clinical safety) | Medium (6/10 implicit) | **Strong opportunity** |
| GAIN-007 | Feeling in control of health administration | High (12/20) | High (emotional baseline) | Medium (5/10) | **Strong opportunity** |
| GAIN-008 | Eigen risico meter on dashboard | Medium (11/20) | Medium (financial planning) | Medium (4/10) | **Worth exploring** |
| GAIN-009 | Push notifications for status changes | Medium (10/20) | Medium (convenience) | Medium (5/10) | **Worth exploring** |
| GAIN-010 | Granular privacy controls for GGZ | Medium (10/20) | High (GGZ segment adoption) | Low (1/10) | **Human review** |
| GAIN-012 | Co-browsing helpdesk ("mensenknop") | Medium (7/20) | High (bridges digital gap) | Low (3/10) | **Human review** |

---

## Verification Report

| Metric                          | Value       |
| ------------------------------- | ----------- |
| Total Quotes Referenced         | 35          |
| Verified Exact Match            | 71%         |
| Verified Paraphrase (accurate)  | 29%         |
| Out of Context                  | 0%          |
| Not Found in Source Material    | 0%          |

| Inference Metric                          | Value       |
| ----------------------------------------- | ----------- |
| Total Inferences Audited                  | 12          |
| Well-supported                            | 2 (17%)     |
| Plausible but thin (nuanced in deliverable) | 8 (67%)   |
| Unsupported (corrected in deliverable)    | 2 (17%)     |

| Disagreement Audit                        | Value       |
| ----------------------------------------- | ----------- |
| Total Findings Reviewed                   | 22 (13 Medium, 9 Low) |
| Likely Valid                              | 12          |
| Likely Valid with Reframing               | 4           |
| Needs Human Judgment                      | 1           |
| Observations (single participant)         | 5           |

**Corrections applied during verification:**
1. GAIN-002 downgraded from Required to Desired — no participant would reject the portal without it
2. PAIN-001 nuanced from "universally incomprehensible" to "universally insufficient" — literate participants understand the term but still find it inadequate
3. PAIN-003 "worse than no solution" inference removed — all participants would still use the portal
4. PAIN-009 scoped to sub-segment — P09 contradicts blanket older-user exclusion claim
5. PAIN-011 flagged for dedicated GGZ validation — primarily one participant's evidence
6. PAIN-013 (provider search) reclassified from pain to feature misalignment observation (removed from deliverable pains; noted below)
7. Confidence labels augmented with participant counts where analytical confidence and frequency diverge

**Feature Misalignment Note (formerly PAIN-013):** Provider search generated consistently low utility assessments across 7 participants, but all mentions were prompted by the prototype walkthrough, not spontaneous. No participant raised provider search as a problem unprompted. P03: "Dit voelt als een soort Thuisbezorgd voor artsen." P05: "Wie zoekt een arts via zijn verzekeraar?" P07: "Sterretjes zonder context zijn decoratie, geen informatie." This is not a pain — it is a feature with low expected adoption. Recommend deprioritising in the current build.

---

## Evidence Index

| Finding ID | Quote / Evidence | Participant | Transcript Location | Verification Status |
|---|---|---|---|---|
| PAIN-001 | "gewijzigd vanwege preferentiebeleid. Wat is preferentiebeleid?" | P02 | participant-02.md, line 54 | Verified |
| PAIN-001 | "Hier staat niet: uw arts is akkoord." | P06 | participant-06.md, line 62 | Verified |
| PAIN-001 | "preferentiebeleid, ik ken het systeem inmiddels... de communicatie is onder de maat." | P07 | participant-07.md, line 34 | Verified |
| PAIN-001 | "therapeutische gelijkwaardigheid en formularium" | P05 | participant-05.md, line 26 | Verified |
| PAIN-002 | "daar staat alleen 'in behandeling' of 'afgehandeld.' Geen tussenliggende stappen" | P01 | participant-01.md, line 34 | Verified |
| PAIN-002 | "dan verdwijnen ze in een zwart gat" | P10 | participant-10.md, line 22 | Paraphrased |
| PAIN-002 | "Heb ik het goed gedaan? Heb ik de juiste bonnetjes meegestuurd?" | P03 | participant-03.md, line 42 | Verified |
| PAIN-003 | "Het is een vitrinekast. Ik mag kijken, maar niet aanraken." | P01 | participant-01.md, line 48 | Verified |
| PAIN-003 | "Het is een etalage. Ik mag kijken, maar niet aanraken." | P04 | participant-04.md, line 46 | Verified |
| PAIN-003 | "informatie zonder de mogelijkheid om te handelen is als een recept zonder keuken" | P10 | participant-10.md, line 44 | Paraphrased |
| PAIN-003 | "Ik wil een dialoog, geen monoloog." | P04 | participant-04.md, line 82 | Verified |
| PAIN-004 | "kan ik hierin switchen tussen mijn eigen gegevens en die van Fenna?" | P03 | participant-03.md, line 38 | Verified |
| PAIN-004 | "Ik moet uitloggen en weer inloggen met haar DigiD. Elke keer." | P07 | participant-07.md, line 28 | Verified |
| PAIN-005 | "Ik schrok me een hoedje. Ik dacht: dit is verkeerd" | P02 | participant-02.md, line 26 | Verified |
| PAIN-005 | "Er was geen waarschuwing, geen uitleg, alleen een ander doosje" | P08 | participant-08.md, line 32 | Verified |
| PAIN-005 | "Die brief lag twee weken in de gang, tussen de reclamefolders" | P07 | participant-07.md, line 34 | Verified |
| PAIN-006 | "Annelies doet dat in twee minuten, maar ik zit er een halfuur mee" | P02 | participant-02.md, line 18 | Verified |
| PAIN-006 | "Na drie keer proberen stond mijn account geblokkeerd" | P06 | participant-06.md, line 56 | Verified |
| PAIN-007 | "Ik voel me dan een beetje... ja, een last." | P02 | participant-02.md, line 22 | Verified |
| PAIN-007 | "Ik wil niet die moeder zijn die elke dag belt met een probleem." | P06 | participant-06.md, line 18 | Verified |
| PAIN-008 | "Iedereen wijst naar iemand anders. Ik ben de enige die niet gehoord wordt." | P04 | participant-04.md, line 30 | Verified |
| PAIN-009 | "Overal word ik een beetje meer buitengesloten... nog een deur die dichtgaat." | P06 | participant-06.md, line 104 | Verified |
| PAIN-009 | "Wij zijn niet lui. Wij zijn niet dom." | P02 | participant-02.md, line 106 | Verified |
| PAIN-010 | "Ik wil in januari al weten: hoeveel moet ik zelf bijbetalen in december?" | P01 | participant-01.md, line 84 | Verified |
| PAIN-010 | "Een eigen-risicomameter" | P09 | participant-09.md, line 90 | Verified |
| PAIN-011 | "Mijn GGZ-sessies? Die wil ik niet op het dashboard." | P08 | participant-08.md, line 46 | Paraphrased |
| PAIN-011 | "Privacyinstellingen als first-class feature." | P08 | participant-08.md, line 100 | Verified |
| GAIN-001 | "Net als bij een pakketje volgen bij PostNL. Dat snap ik meteen." | P01 | participant-01.md, line 34 | Verified |
| GAIN-001 | "Oh. Oh, dit is goed. Een tijdlijn per declaratie." | P10 | participant-10.md, line 40 | Verified |
| GAIN-002 | "Kunt u dat er niet bij zetten, in gewone mensentaal?" | P02 | participant-02.md, line 60 | Verified |
| GAIN-002 | "Dat geeft rust. Mijn hart heeft rust nodig, letterlijk." | P06 | participant-06.md, line 66 | Verified |
| GAIN-003 | "Het moet tweerichtingsverkeer worden." | P04 | participant-04.md, line 82 | Verified |
| GAIN-004 | "Een soort profielswitch, zoals je bij Netflix hebt" | P07 | participant-07.md, line 48 | Verified |
| GAIN-006 | "Een bericht, twee weken van tevoren" (full template provided by P09) | P09 | participant-09.md, line 96 | Paraphrased |
| GAIN-012 | "Een grote knop waarmee ik iemand aan de telefoon krijg die meteen ziet wat ik zie" | P02 | participant-02.md, line 92 | Verified |

---

## Methodology Note

This analysis was produced using KOOS's multi-agent analysis protocol. Each transcript was analyzed independently by 20 agents across 4 extraction lenses:

- **Functional pains (5 agents):** Practical obstacles, friction, wasted effort, operational failures
- **Emotional & social pains (5 agents):** Anxiety, frustration, shame, exclusion, loss of control, stigma
- **Functional gains (5 agents):** Outcomes that save time, reduce effort, produce better results
- **Emotional & social gains (5 agents):** Confidence, independence, feeling cared for, being seen as competent

Findings were consolidated through convergence analysis (Stage 3). Confidence tiers reflect how many of the 20 independent runs surfaced each finding: High (12+), Medium (6-11), Low (1-5).

All quotes were verified against source transcripts (35 quotes, 0 fabricated, 0 out of context). 12 analytical inferences were audited: 2 confirmed, 8 nuanced, 2 corrected. 22 Medium/Low confidence findings were reviewed through a disagreement deep-dive: 12 confirmed, 4 reframed, 1 escalated for human judgment, 5 classified as observations.

Total agent runs: 43 (20 extraction + 1 convergence + 5 disagreement + 5 quote verification + 5 inference verification + 5 disagreement audit + 1 synthesis).

---

## Recommended Next Steps

### Evidence strongly supports

1. **Launch claims tracking first** (PAIN-002 → GAIN-001). This is the highest-value, lowest-risk feature. Universal positive response, addresses the most widespread pain (7/10 participants), and delivers the most requested gain. P05 (UX designer): "Launch small, iterate fast. Lanceer de declaratiestatus als eerste."

2. **Redesign all medication change notifications in plain language before the medication feature goes live** (PAIN-001 → GAIN-002). The current "preferentiebeleid" label is insufficient for all segments and incomprehensible for the most vulnerable. P02's template should be the starting point: what changed, why, and that the doctor is aware. This is a content change, not a technology change.

3. **Add advance medication change notifications sent 2+ weeks before pharmacy dispensing** (PAIN-005 → GAIN-006). Send to the managing person (patient or caregiver), not only the policyholder address. For dementia patients, this is a clinical safety measure.

4. **Build two-way action capability as a fast follow** (PAIN-003 → GAIN-003). Priority actions: appeal a rejected claim, report a medication problem, send a message to VGZ. Without this, every negative event in the portal redirects the user to the telephone channel.

### Recommend exploring

5. **Conduct dedicated research with mantelzorgers and the GGZ segment** — PAIN-004 (caregiver profiles) and PAIN-011 (GGZ privacy) are strongly evidenced within this study but rest on 1-3 participants each. Both have high potential impact. Validate with targeted samples before committing development investment.

6. **Prototype a co-browsing helpdesk** (GAIN-012) — independently proposed by P01, P02, and P06. For the digitally excluded segment, this is the feature that determines whether the portal is accessible at all. Test with elderly users in a realistic setting (home, alone, with their own devices).

7. **Add an eigen risico meter to the dashboard** (GAIN-008) — 5 participants, practical use case for chronic patients and frequent users.

8. **Implement privacy-aware notifications** (GAIN-015) — no content on lock screen for any health-related notification. This is a best practice regardless of whether the GGZ segment concern is validated at population level.

9. **Reassess the provider search feature** — lowest-utility feature in the concept. No participant would use it in preference to their GP's recommendation. Consider deprioritising or fundamentally redesigning before launch.

---

## Meta-Analysis Log

| Metric | Value |
|---|---|
| Total parallel extraction runs | 20 (4 lenses × 5 agents) |
| Convergence analysis | 1 orchestrator pass |
| Disagreement deep-dive agents | 5 |
| Quote verification agents | 5 (35 quotes verified) |
| Inference verification agents | 5 (12 inferences audited) |
| Disagreement audit agents | 5 (22 findings reviewed) |
| Synthesis | 1 orchestrator pass |
| **Total processing stages** | **43 agent runs across 7 stages** |
| High confidence findings | 9 pains, 7 gains |
| Medium confidence findings | 7 pains, 5 gains |
| Low confidence (observations) | 3 pains, 6 gains |
| Findings removed during verification | 1 (PAIN-013 reclassified as feature misalignment) |
| Findings corrected during verification | 5 (gain levels, scope claims, universality claims) |
| Findings flagged for human review | 7 |
