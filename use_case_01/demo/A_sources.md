# Source register — Kabini AI Governance Pack, artefact A

**Artefact:** A. AI system inventory and use-case register — source notes
**Version:** 1.0.3 · **Issued:** 2026-09-07 · **Revised:** 2026-09-09 · **Owner:** Meera Krishnamurthy, General Counsel
**Applies to:** `A_ai_system_inventory_and_use_case_register.md`,
`A_annex_1_classification_rules.md`, `A_annex_2_worked_repair_matchscore.md`,
`A_annex_3_room_worksheet.md`

---

## 1. Why this file exists

Every figure, date and factual claim in artefact A carries a bracketed key. This file
says what each key is, where it was read, when it was read, and how far it can be
trusted. A number in a governance document with no source is the thing this course
teaches a board to refuse; the pack does not do it either.

## 2. The two kinds of fact in this artefact, and do not confuse them

**Facts about Kabini are facts about a teaching client.** Kabini Workforce Services
B.V., MatchScore, Nora, Cadence, Attestra Inc., Halcyon AI, Inc. and the five named
people do not exist. They were authored in `015_project/project.md` on 2026-09-07 and
are fixed for the whole course. Where the register states that Kabini places about
forty thousand contract workers a year, the source of that fact is `project.md` and
nothing else. It is not a market figure and must never be quoted as one.

**Facts about the Body of Knowledge, standards and law are facts about the world**, and
they are sourced to the dated research in `005_research/2026-09-07/`, which records its
own verification status including what it could not reach.

## 3. The keys

| Key | What it is | Where it was read | Date on it / date read | Trust |
|---|---|---|---|---|
| **[PRJ]** | *The project: the Kabini AI Governance Pack* — the fixed description of the teaching client, its four AI systems, its people, its existing systems and the stack | `015_project/project.md`, this repository | Written 2026-09-07; read 2026-09-07 | Authoritative **for the teaching client only**. It is fiction, and it is fixed: the names and systems do not change once the course has begun. |
| **[UCP]** | *Use case plan* — the backlog, and row 1's `Delivers` and `Teaches` lines, plus the detailed entry "1 — Take stock: what these four systems actually are" | `015_project/use_case_plan.md`, this repository | Written 2026-09-07; read 2026-09-07 | Authoritative for the scope of this artefact. |
| **[BRO]** | The course brochure — Module 1's promise and the pack's deliverable list, item 1 | `010_brochure/brochure.md`, this repository | Written 2026-09-07; read 2026-09-07 | Authoritative for what was sold. |
| **[BOK-2.1]** | IAPP AIGP **Body of Knowledge and Exam Blueprint v2.1** — approved by the AIGP EDB 9 September 2025, effective 2 February 2026, supersedes v2.0.1. The performance-indicator wording quoted in Annex 1 is taken verbatim from Domains I.A and IV.A | Text extract at `005_research/2026-09-07/extracts/aigp-bok-v2.1.txt` | Document effective 2026-02-02; extract captured and read 2026-09-07 | High. Extracted from the IAPP's own published PDF, which the IAPP publishes free. |
| **[DIFF]** | *BoK v2.0.1 → v2.1 diff* — the itemised change list, including the systematic replacement of "AI model" by "AI system" across Domains III and IV, and the addition of "agentic architectures" to the IV.A deployment-options indicator | `005_research/2026-09-07/bok-v2.0.1-to-v2.1-diff.md` | Dated 2026-09-07; read 2026-09-07 | High. Derived line by line from the two extracted blueprint texts, both in the same folder. |
| **[RR]** | *AIGP Certification Training — research report*, cited by section, e.g. **[RR §2.5]** | `005_research/2026-09-07/report.md` | Dated 2026-09-07; read 2026-09-07 | High for what it states first-hand; it marks its own second-hand and unreachable items, and those marks are carried through into this artefact. |
| **[ISO-22989]** | **ISO/IEC 22989:2022**, *Information technology — Artificial intelligence — Artificial intelligence concepts and terminology*, first edition 2022-07. Clause 3 carries the vocabulary the blueprint adopted: **3.1.4** AI system, **3.1.23** model, **3.3.7** machine learning model, **3.3.15** training, **3.1.17** inference, **3.1.1** AI agent, and the **3.1.5** autonomy / **3.1.16** heteronomy pair | Single-user copy purchased from the ISO Store, held at `005_research/2026-09-07/extracts/pdf/official/` | Document dated 2022-07; bought and read 2026-09-09 | Authoritative, and **not reproducible**. The licence is single-user and prohibits copying; this pack may cite a clause number and paraphrase, and may not quote. Before 2026-09-09 the standard was unreachable and this key did not exist. |
| **[HB-5.3.2]** | **IAPP Certification Candidate Handbook v5.3.2**, effective 1 June 2026, superseding 5.3.1 — the *general* handbook. The IAPP has folded the per-certification handbooks into it, so this is the only current one; there is no 2026 AIGP-specific handbook. §VI.A states that the number of scored and unscored questions is "listed on the designation's page on the IAPP website" | PDF at `005_research/2026-09-07/extracts/pdf/official/` | Effective 2026-06-01; downloaded and read 2026-09-09 | High, and current. Its significance to this artefact is what it **omits** — see the exam-mechanics row in §4. |

## 4. What each key was used for in artefact A

| Claim in artefact A | Key | Note |
|---|---|---|
| Kabini places ~40,000 contract workers a year and employs 11,000 permanent staff; the legal team is six people | [PRJ] §1 | Teaching-client figure. Used in the register only to size the systems' reach. |
| Kabini has no AI inventory, no AI policy, no impact assessment and no named owner for any AI system | [PRJ] §1 | This is the "before" state the register closes. |
| The four systems, what each does, who built or sells each, and the named people | [PRJ] §1 | MatchScore, Nora, the right-to-work check, Cadence; Attestra Inc. (Delaware, United States); Halcyon AI, Inc.; Meera Krishnamurthy, Arjun Sundaram, Kavitha Rajagopal, Vikram Nair, Deepa Sridharan. |
| Kavitha Rajagopal is MatchScore's business owner | [PRJ] §1 people table | The only system-to-owner link `project.md` fixes. Every other owner in the register is appointed **by** the register and marked interim. |
| Talent Cloud, Kabini People, the placement warehouse (eight years of outcomes, Amazon-hosted, `eu-west-1`), the Bengaluru replica in `ap-south-1`, Attestra's API, Halcyon AI's hosted API, the existing policy set | [PRJ] §1 "Kabini's existing systems and data" | Also the source of "nobody has ever written down where all of it came from" and of the replica sitting in no transfer record. |
| The Halcyon AI agreement was signed by Deepa Sridharan without legal review | [PRJ] §1 | Recorded in the register as a contract-status fact; the redline itself is use case 19. |
| The register is written first and edited last, and every other artefact hangs off a row in it | [PRJ] §3 | The architecture rule this artefact obeys. |
| Every document in the pack carries a version, a date and a named owner | [PRJ] §5 item 14 | Why every file here has a header block. |
| Row 1 of the backlog: what this use case delivers and teaches, and the 60-minute estimate | [UCP] §2 table, row 1; §3 entry 1 | Quoted in `use_case.md`. |
| Module 1's scope — classic vs generative vs agentic, model vs system, training vs inference, as-is vs fine-tuning vs RAG vs agentic, ISO/IEC 22989 as the source of the model/system distinction | [BRO] §3 Module 1; [BRO] coverage map row M1 | |
| "Know the generally accepted definitions and types of AI" is the first performance indicator of sub-domain **I.A**, weighted 4–6 questions | [BOK-2.1] Domain I page | Verbatim indicator text. The blueprint prints the 4–6 without saying 4–6 *of what*; the denominator comes from [RR] §2.4, next row. |
| The exam is **100 questions, of which 85 are scored** and 15 are unscored pilot items | [RR] §2.4 | **Two caveats, and both belong on any slide that carries the figure.** *First, the source:* [RR] §2.4 takes it from the IAPP AIGP Candidate Handbook copy bearing effective date **2 April 2024** — a document two structural revisions old, which still refers to "seven domains" and which [RR] §2.4 explicitly says to distrust on structure. Where this artefact needs the exam's *structure*, it uses [BOK-2.1] and not the handbook. *Second, the denominator is a reading, not a reading-off:* the blueprint prints per-domain counts of 16–20, 19–23, 21–25 and 21–25, which **sum to 77–93**. That brackets 85 and not 100, so the counts are **best read as counts of the scored set** — but that is **an inference this artefact draws from two published figures, and not a statement the IAPP makes anywhere either source reproduces.** It is written as an inference wherever it is used. *Third, added 2026-09-09 — the source is now known to be superseded, and its successor does not repeat the figure:* the IAPP has folded the AIGP-specific handbook into the general **[HB-5.3.2]**, whose §VI.A says only that the counts are "listed on the designation's page on the IAPP website", and the AIGP designation page states no count. So the 85-of-100 split rests on a 2024 document that is stale on structure, with **no current IAPP publication confirming it**, and the denominator inference has gained no support. Nothing about how the figure is written changes; what changes is that its weakness is now established rather than suspected. |
| Domain I overall is weighted 16–20 questions; Domains III and IV 21–25 each, so **42–50 together** | [BOK-2.1] Domain I, III and IV pages; [RR] §3.3 "Disagreement 2" | The 42–50 figure is read off the two domain pages. [RR] §3.3 states it as "42–50 of 85 scored questions"; the *denominator* in that phrasing is the inference recorded in the row above, not a published IAPP statement. |
| The IV.A deployment-options indicator reads "cloud vs. on-premise vs. edge, and using the AI model as is or with fine-tuning, retrieval augmented generation, agentic architectures, or other techniques to improve performance and fit" | [BOK-2.1] Domain IV page | Verbatim. This is the wording the register's *realisation* column follows. |
| The IV.A model-type indicator reads "classic vs. generative, proprietary vs. open source, small vs. large, and language vs. multimodal capabilities" | [BOK-2.1] Domain IV page | Verbatim. |
| "AI model" was replaced by "AI system" throughout Domains III and IV in v2.1 | [DIFF] §5; [RR] §2.3 item 4 | Six specific indicator rewrites are listed in [DIFF] §5. |
| "Agentic architectures" was added to the IV.A deployment options in v2.1 | [DIFF] §5, "Other III/IV changes" table; [RR] §2.3 closing paragraph | |
| ISO/IEC 22989 is AI concepts and terminology, is named in the Body of Knowledge, and is where the model-versus-system distinction the v2.1 blueprint adopted comes from | [RR] §2.5 "Standards"; [BRO] §3 Module 1; confirmed against [ISO-22989] clauses 3.1.4 and 3.1.23 | **Caveat, revised 2026-09-09 and still on the face of Annex 1.** The standard was originally unreachable — `iso.org` returned HTTP 403 [RR §2.5] — and the attribution rested on the research report alone. A single-user copy was bought and read on 2026-09-09, and it confirms the attribution: 3.1.4 defines an AI system as an engineered system that generates outputs, 3.1.23 defines a model as a representation. **The licence prohibits reproduction**, so the rule tightens rather than relaxes: a clause number may be cited, and no verbatim 22989 wording appears anywhere in this artefact or may be added to it. |
| The core ISO list in the blueprint is now 22989, 42001 and 42005; ISO/IEC 42005:2025 was published May 2025 and added in v2.1 | [RR] §2.5, §5.9; [DIFF] | Named in the register only as a forward pointer to use cases 8 and 10. |
| A candidate who thinks in weights answers the wrong question; the model/system point is worth roughly 46 questions' worth of material | [RR] §4 item 2 | Used in `use_case.md` and Annex 2 to justify why this use case opens the course. |
| Learners want to classify their employer as one thing; the exam wants them to classify an activity | [RR] §4 item 3 | The reason the register carries no developer/provider/deployer/user column in v1.0 — that is use case 3. |
| Enough technology to make the governance vocabulary land, then stop | [RR] §3.3 "Disagreement 1" | The reason Annex 1 is nine rules on a page and not a lecture on machine learning. |

## 5. What this artefact deliberately does not source, because it does not claim it

Version 1.0 of the register makes **no legal claim about any system**. It does not say
that MatchScore is high-risk, that Article 50 reaches Nora, that Attestra's service
involves a restricted transfer, or that Cadence is high-impact AI under Korea's AI Basic
Act. Those are use cases 26, 27 and 28, and the research report is explicit that the EU
timeline is corroborated rather than read from the Official Journal — EUR-Lex was
unreachable from the research environment [RR §2.5] — so those dates will be written
once, with their compilation date on their face, in the applicability memo.

The register does record the **facts** those conclusions will be drawn from: what each
system decides, on whose data, from where to where. Recording the facts is not the same
as stating the conclusion, and keeping them apart is why the register can be re-used
when the law moves.

## 6. Re-verification before delivery

| What | Why | Who |
|---|---|---|
| That the IAPP has not issued a Body of Knowledge revision after v2.1 | The register's classification rules quote v2.1 indicator wording verbatim | Trainer, before the first sitting |
| ~~That the candidate handbook still says 100 questions with 85 scored, and whether a handbook revision later than 2 April 2024 exists~~ **Closed 2026-09-09.** A newer handbook exists — the general **[HB-5.3.2]** — and it **drops the figure** rather than confirming it; the AIGP-specific handbook has been discontinued. The 85-of-100 split therefore stays sourced to the 2024 handbook with its staleness marked, and the denominator stays an inference. Nothing in Annex 1 or Annex 2 changes | [RR] §2.4 had marked the existence of a newer handbook as **unverified**. It is now verified, and the answer weakens rather than strengthens the figure | Closed by the AI governance workstream |
| Whether the IAPP has since published a question count on the AIGP designation page | It is the only place [HB-5.3.2] §VI.A says the count lives, and it carried none on 2026-09-09. If a count appears there, it supersedes the 2024 handbook as the source | Trainer, before the first sitting |
| Nothing else in this artefact | Version 1.0 asserts no legal date and no external figure other than blueprint wording and the exam-mechanics split above | — |
