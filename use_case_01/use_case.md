# Use case 1 — Take stock: what these four systems actually are

*AIGP Certification Training · Rathinam Trainers & Consultants · The AI Engineering Series*
*Written 2026-09-07 and revised 2026-09-09 from the material actually produced in
[`use_case_01/demo/`](./demo/), against `015_project/project.md`,
`015_project/use_case_plan.md`, `010_brochure/brochure.md` and
`005_research/2026-09-07/`. The 2026-09-09 revisions track the register's correction
releases 1.0.1, 1.0.2 and 1.0.3 and change no finding; §7 of the register lists what each
corrected.*

**Section produced:** A — AI system inventory and use-case register, version **1.0.3**
(first baseline 1.0, issued 2026-09-07; corrected 2026-09-09)
**Module carried:** M1 Foundations
**Live time:** 60 minutes
**Position:** first use case of thirty. Nothing is carried in; everything after this is
carried forward from it.

---

## 1. The client scenario, and why it matters

**Kabini Workforce Services B.V.** places about **forty thousand contract workers a
year** across the European Union, South Korea and the United States, and employs
**eleven thousand permanent staff**. Its legal team is **six people** who already carry
GDPR, employment law in nine countries and the commercial contract book
[`project.md` §1].

Kabini has **no AI governance function at all** — no inventory, no policy, no impact
assessment, no named owner for any AI system. What it has is four AI systems already
running or in pilot, and two deadlines it did not set for itself: the board has
committed to publishing an **EU AI Act readiness statement** to bid for a public-sector
staffing framework, and its largest client, a Korean electronics manufacturer, has begun
putting **AI Basic Act questions into procurement questionnaires** that Vikram Nair in
Seoul cannot answer [`project.md` §1].

Meera Krishnamurthy, the General Counsel, asked for *"a governance programme I can put in
front of a board, an auditor and a procurement officer. Not a strategy deck. The actual
documents, with owners and dates on them"* [`project.md` §1].

**Why this is the first hour of the course, and not a lecture.** Neither of Kabini's
two deadlines can be started from a list nobody has written. A readiness statement needs
a list of what is being declared ready. A procurement questionnaire asks about named
systems. Every artefact in the pack — the impact assessment, the risk register, the data
dossier, the vendor redline, the kill switch, the applicability memo — hangs off a row
in this register, and the architecture makes that explicit: **the register is written
first and edited last** [`project.md` §3].

There is a second reason, and it is about the exam rather than the client. The blueprint
opens at sub-domain **I.A — "Know the generally accepted definitions and types of AI"**
[BoK v2.1, Domain I]. The fastest way to teach the difference between a *model* and a
*system* is not to define it. It is to make somebody write down which one they have four
of [`use_case_plan.md` §1].

---

## 2. What this use case delivers

**The `Delivers` line, quoted from row 1 of `015_project/use_case_plan.md`:**

> An AI system inventory and use-case register with a row for MatchScore, Nora, the
> right-to-work check and Cadence, each classified as classic, generative or agentic,
> each described as a *system* rather than a model, and each naming whether it is used
> as-is, fine-tuned, retrieval-augmented or agentic.

**What was actually built, expanding that line.** Five Markdown files in
[`use_case_01/demo/`](./demo/), all of them committed material rather than templates:

| File | What it is |
|---|---|
| `A_ai_system_inventory_and_use_case_register.md` | **The section.** Artefact A, version 1.0.3, issued 2026-09-07 and corrected 2026-09-09, owned by Meera Krishnamurthy. A summary table of four rows and a **full record for each of the four systems** carrying around twenty fields, plus eight findings drawn from reading the rows together, twelve open items with named owners and due dates, an explicit statement of what version 1.0 does not say and which use case adds it, change control, and sign-off by the five named people |
| `A_annex_1_classification_rules.md` | The nine rules **R1–R9** the register applied, each with the question it makes you ask and where it bites in these four rows |
| `A_annex_2_worked_repair_matchscore.md` | AIS-001 written first as a model description and then repaired into a system description, seven fields at a time, with the source of each and what it unlocks later |
| `A_annex_3_room_worksheet.md` | The blank record, the three rows the room fills, the four arguments to let it have, and the two-minute close |
| `A_sources.md` | Six citation keys with what each is, where read, date read, trust level, and a claim-by-claim table |

**Beyond the `Delivers` line, and worth saying out loud:** each row also names a business
owner who is a **person**, separates what happens at **training** time from what happens
at **inference** time and says who performs each, and records what is **not documented**
as a numbered open item with an owner and a date. Only one of the four systems —
MatchScore — had a business owner recorded in `project.md`; the register appoints
interim owners for the other three and marks each of them as interim.

---

## 3. What the section covers, and the question it answers

**The question:** *What, exactly, do we have?*

Not "is it legal", not "is it risky", not "who is the provider". Those are use cases 26,
2 and 3. This section answers the prior question that all three of them assume has been
answered, and it answers it in the vocabulary the exam and the regulator both use.

**Course coverage, from row 1's `Teaches` line:** **M1 Foundations** — generally accepted
definitions and types of AI; classic vs generative vs agentic; model vs system; training
vs inference; fine-tuning vs RAG vs agentic; ISO/IEC 22989 vocabulary. That maps to
blueprint sub-domain **I.A**, weighted **4 to 6 questions** [BoK v2.1, Domain I], and —
through the model/system distinction — to the **42 to 50 questions** of Domains III and
IV that were rewritten in v2.1 to govern the system rather than the model.

**Say the denominator carefully, because the room will ask.** The paper is 100 questions
of which **85 are scored** and 15 are unscored pilot items [research report §2.4]. The
blueprint's four domain counts sum to **77–93**, which brackets 85 and not 100, so the
counts are best read as counts of the scored set — and the research report states the
III + IV figure that way, as "42–50 of 85 scored questions" [research report §3.3,
"Disagreement 2"].
**That reading is an inference from two published figures, not a sentence the IAPP
writes**, and `demo/A_sources.md` marks it as one on the row where the figure is used.
The 85-of-100 split itself comes from an IAPP candidate handbook copy dated **2 April
2024**, which is stale on the exam's structure — it still says "seven domains" — so it is
used only as a denominator and never for structure, and the structure comes from the
blueprint [research report §2.4].

**And that source is now known to be superseded by one that drops the figure.** Checked
2026-09-09: the IAPP has discontinued the AIGP-specific handbook and folded it into the
general Certification Candidate Handbook v5.3.2, effective 1 June 2026. That handbook
does **not** repeat the split; its §VI.A says the number of scored and unscored questions
is "listed on the designation's page on the IAPP website", and the AIGP designation page
carries no count. So the figure has no current publication behind it, and the inference
about the denominator gained no support. Nothing about how either is written changes —
both were already marked. What changes is that the weakness is established rather than
suspected, and a trainer asked "where does 85 come from?" should say **a 2024 handbook
the IAPP has since replaced with one that is silent on it**.

---

## 4. The argument the section makes, in order

Six moves. Each rests on something nameable, and the names are on the real document, not
only here.

**Move 1 — Govern the system, not the model.** Rule **R1**. Every record names the model
*plus* the data in, the data out, the interfaces, the human oversight and the deployment
context. **Rests on:** the systematic replacement of "AI model" by "AI system" across
Domains III and IV in Body of Knowledge **v2.1** — six specific indicator rewrites, listed
in `005_research/2026-09-07/bok-v2.0.1-to-v2.1-diff.md` §5 — which the research
attributes to the **ISO/IEC 22989** vocabulary the blueprint names. *The standard has
since been read and is still never quoted.* It was unreachable when the pack was written
— `iso.org` returned HTTP 403 — and a licensed single-user copy was bought and read on
2026-09-09. It confirms the attribution: clause **3.1.4** defines an AI system as an
engineered system that generates outputs, clause **3.1.23** defines a model as a
representation, which is exactly what R1 enforces. The licence forbids reproduction, so
the rule tightened rather than relaxed — **a clause number may be cited, a clause may
not be quoted** — and Annex 1 carries that on its face.

**Move 2 — Test the type in the order agentic, generative, classic.** Rule **R2**, with
the tests at **R3** and **R4**. Testing "does it generate text?" first gets Cadence
wrong. **Rests on:** the blueprint's IV.A indicators, which treat classic-versus-
generative as a **model** distinction and "agentic architectures" as a **deployment
option** — the latter added in v2.1 [BoK v2.1 IV.A; diff §5]. Agency is built around a
model, so it is tested at the system level first.

**Move 3 — One model, two systems, two classifications.** Nora and Cadence run on the
same Halcyon AI hosted model [`project.md` §1]. Nora is generative; Cadence is agentic,
because it books interviews and issues offers **without a human in the loop**. Identical
weights, different system, different class, different controls. This is Move 1 arriving
as a concrete argument, and it is the one the plan says the room argues about
[`use_case_plan.md` §3 entry 1].

**Move 4 — Training and inference are different facts with different parties.** Rule
**R5**. Kabini trains MatchScore itself and sends nothing to a third party to do it —
but it trains it **in Bengaluru, against a replica of the warehouse in `ap-south-1`**,
so the data leaves the Union without any vendor being involved [`project.md` §1]. For
Nora it is the other way round: Kabini cannot see Halcyon's pre-training at all,
fine-tunes on top of it, and sends every prompt to Halcyon's API. It performs no training for the right-to-work check and only causes
inference — by making an API call that sends **biometric data out of the EU**
[`project.md` §1]. Half of what the pack asks later resolves differently depending on
which of the two is being discussed.

**Move 5 — The realisation axis only applies to a model you did not train.** Rules **R6**
and **R8**. The blueprint's wording is *"using the AI model **as is** or with
**fine-tuning**, **retrieval augmented generation**, **agentic architectures**, or other
techniques to improve performance and fit"* [BoK v2.1 IV.A, verbatim] — a list of things
a deployer does to somebody else's pre-trained model. MatchScore was trained in-house, so
the correct entry is **"not applicable"**, not "as-is". Writing "as-is" quietly implies
somebody else made the training decisions, and the data-provenance, quality and bias
obligations follow that implication to the wrong door.

**Move 6 — Say what you do not know, and mark what you guessed.** Rules **R9** and the
open-item discipline. The right-to-work check is classified **classic from the outside**,
marked *asserted by the deployer, unconfirmed by the provider*, because Kabini did not
build it and cannot inspect it [`project.md` §1] and Attestra has never been asked.
Twelve open items carry a named owner and a date. **Rests on:** the pack rule that every
document carries a version, a date and a named owner and that no two documents contradict
each other about a fact [`project.md` §5 item 14].

**And one restraint, which is part of the argument.** Version 1.0 makes **no legal claim
about any system** — no risk tier, no Article 50, no high-impact AI, no transfer
conclusion. It records the facts those conclusions will be drawn from and stops. That is
the course's whole sequencing decision in miniature: teach the lifecycle first and map
law onto it afterwards, because the blueprint itself de-emphasised law-first framing in
v2.1 [research report §3.3]. It is also plain prudence — the research records that
EUR-Lex was unreachable and the EU timeline is corroborated rather than read from the
Official Journal [research report §2.5], so those dates get written once, carefully, in
the applicability memo, not scattered through the register.

---

## 5. What a reader can decide afterwards that they could not before

**For Kabini.**

- Which four things the readiness statement is about, by name and reference.
- Who to send a procurement questionnaire back to, per system — including the three
  systems whose owner is interim and marked as interim.
- That **two of the four systems have no real business owner**, and that they are the two
  whose output bears hardest on an individual: the check that decides whether someone may
  work at all, and the agent that issues offers.
- That the two systems Kabini understands least — one it cannot inspect, one whose
  intermediate steps nobody reads — are the two that decide most about a person.
- That personal data reaches two external endpoints, and that in one case it is biometric
  and crosses out of the EU. Recorded as a data-flow fact, ready for use cases 23 and 24
  to reason about.
- That **nobody measures how often any of them runs** (OI-01, against all four).

**For a participant.**

- Describe any AI system in their own organisation as a system rather than a model, and
  classify it as classic, generative or agentic without guessing — the "By the end, a
  participant can" line from `use_case_plan.md` §3 entry 1.
- Answer the two scenario traps the research names: the same model in two systems, and
  the model the company trained itself.
- Recognise, in an exam question or a meeting, that "we use it as-is" is an answer about
  provenance and not about safety.
- Write "not documented" in a governance document and have it be a control rather than an
  embarrassment, because it carries an owner and a date.

**What they still cannot do, and should know they cannot.** Say what harms any of these
systems can do (use case 2), who is developer or provider for which activity (use case
3), what risk tier any of them is in (use case 26), or which obligation bites from what
date (use cases 27 and 28). §6 of the register lists each of those and names the use case
that closes it.

---

## 6. Where every figure in it was read

Full detail, claim by claim, in [`demo/A_sources.md`](./demo/A_sources.md). The two
kinds of fact, and do not confuse them:

**Facts about Kabini are facts about a teaching client.** Kabini, MatchScore, Nora,
Cadence, Attestra Inc., Halcyon AI, Inc. and the five named people were authored in
`015_project/project.md` on **2026-09-07** and are fixed for the course. Forty thousand
contract workers a year, eleven thousand permanent staff, a legal team of six, the two
thousand three hundred in Bengaluru, eight years of placement outcomes, `eu-west-1`,
`ap-south-1`, Delaware — every one of those resolves to
`project.md` §1 and to nothing else. **None of them is a market figure and none may be
quoted as one.**

**Facts about the world are sourced to the dated research** in
`005_research/2026-09-07/`, read 2026-09-07:

| Claim | Read in |
|---|---|
| Body of Knowledge **v2.1**, approved 9 September 2025, effective 2 February 2026, superseding v2.0.1; Domain I weighted 16–20 questions, sub-domain I.A 4–6; Domain IV weighted 21–25; the verbatim I.A and IV.A indicator wording | `005_research/2026-09-07/extracts/aigp-bok-v2.1.txt` |
| "AI model" → "AI system" across Domains III and IV, six indicator rewrites; "agentic architectures" added to IV.A | `005_research/2026-09-07/bok-v2.0.1-to-v2.1-diff.md` §5 — both are in §5, the second in its "Other III/IV changes" table. §6 of that file is front-matter and framing, and nothing here rests on it |
| The exam is 100 questions of which **85 are scored** | `005_research/2026-09-07/report.md` §2.4 — **which reads it from the IAPP candidate handbook dated 2 April 2024, stale on structure.** Used only as a denominator, never for structure. That the blueprint's domain counts (summing to 77–93) are counts of the 85 is **this pack's inference**, marked as one in `demo/A_sources.md`, and is not a published IAPP statement. **Re-checked 2026-09-09:** the successor handbook, the general v5.3.2 effective 1 June 2026, **omits the figure** and points at the designation page, which carries none — so no current IAPP publication confirms it |
| ISO/IEC 22989 is the source of the model/system distinction the blueprint adopted; the standard **has been read, and may not be quoted** | Originally unreachable — `iso.org` returned HTTP 403, `005_research/2026-09-07/report.md` §2.5. A single-user licensed copy was bought and read 2026-09-09 and is held at `005_research/2026-09-07/extracts/pdf/official/`; it confirms the attribution at clauses **3.1.4** and **3.1.23**. The licence prohibits reproduction, so the pack cites clause numbers and paraphrases and quotes nothing |
| A candidate who thinks in weights answers the wrong question, across ~46 questions' worth of material | `005_research/2026-09-07/report.md` §4 item 2 |
| Developer / provider / deployer / user are task labels applied per activity, not company labels — the reason this register carries no role column | `005_research/2026-09-07/report.md` §4 item 3 |
| Teach enough technology to make the governance vocabulary land, then stop — the reason Annex 1 is nine rules on a page | `005_research/2026-09-07/report.md` §3.3 |
| EUR-Lex unreachable; EU AI Act dates corroborated rather than official — the reason version 1.0 states none of them | `005_research/2026-09-07/report.md` §2.5 |

**Verify before delivery:** that the IAPP has not issued a Body of Knowledge revision
after v2.1. Annex 1 quotes v2.1 indicator wording verbatim, and it is the main external
text this section depends on. The old second check — whether a handbook newer than April
2024 exists — was **closed on 2026-09-09**: one does, it is the general handbook v5.3.2,
and it drops the question counts rather than confirming them. What replaces it is
narrower: check whether the **AIGP designation page** has since published a question
count, because v5.3.2 §VI.A says that is where the count lives and on 2026-09-09 it
carried none.

---

## 7. How it runs in the room

Sixty minutes [`use_case_plan.md` §2 row 1]. Nothing to install, no account, no key, no
network. Markdown on a projector.

| Minutes | What happens | File |
|---|---|---|
| ~15 | The trainer builds AIS-001 **on screen and gets it wrong on purpose**, describing MatchScore as a model, then repairs it field by field into a system | `demo/A_annex_2_worked_repair_matchscore.md` |
| ~30 | The room splits three ways and fills AIS-002, AIS-003 and AIS-004 from the blank record. It argues about Cadence | `demo/A_annex_3_room_worksheet.md` |
| ~15 | The finished register is read back: the four rows, the eight findings, the twelve open items, and what version 1.0 deliberately does not say | `demo/A_ai_system_inventory_and_use_case_register.md` |

**The close.** Kabini walked into the hour with four AI systems and no inventory, no
policy, no impact assessment and no named owner. It walks out with four rows, four
owners — three of them interim and marked as such — and twelve things it now knows it does
not know. Nothing was built and nothing was fixed. Every other artefact in the pack hangs
off one of these rows, and none of them could have been started an hour ago.

---

## 8. A decision this use case had to make, and made

`015_project/use_case_plan.md` §6 item 8 left one thing open: whether participants write
the pack in Word or Google Docs, or whether it is version-controlled in this repository
as Markdown — and it says the decision **has to be made before use case 1, not after**.

**Decided: Markdown, in the repository.** Every artefact carries a version, a date and a
named owner in a header block; a fact lives in one place and changes there; a change to a
row raises the version and re-issues the artefacts that quoted it. Participants may still
draft in whatever editor they own — `project.md` §4 requires no more than a browser, Teams
and a document editor — but the trainer's issued copy of every artefact is the Markdown in
this repository, and it is what use case 30 signs off against.
