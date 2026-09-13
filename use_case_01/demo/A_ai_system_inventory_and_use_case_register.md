# A. AI system inventory and use-case register

**Kabini Workforce Services B.V. — Kabini AI Governance Pack, artefact A**

| | |
|---|---|
| **Artefact** | A — AI system inventory and use-case register. The spine of the pack: every other artefact hangs off a row in this one [PRJ §3] |
| **Version** | **1.0.3** — a correction release. See change control at §7 |
| **Issued** | **2026-09-07**, revised **2026-09-09** |
| **Document owner** | **Meera Krishnamurthy, General Counsel** — the board's sponsor for this work [PRJ §1] |
| **Prepared by** | AI governance workstream |
| **Status** | Issued. Baseline for the pack. |
| **Next review** | On any change to a recorded system, or **2027-03-07**, whichever is sooner |
| **Scope of version 1.0** | What each system **is**: its description as a system, its classification as classic / generative / agentic, how the model behind it is realised, where training happens and where inference happens, who owns it, and what data it touches |
| **Sources** | Every bracketed key resolves in `A_sources.md`. Every classification decision resolves to a numbered rule in `A_annex_1_classification_rules.md` |
| **A note on the version number** | Prose in this artefact and its annexes says **"version 1.0"** where it means *this first baseline*. **1.0.1**, **1.0.2** and **1.0.3** are correction releases against that baseline; none changes a finding, a classification, an owner, an open item or a due date, and §7 lists exactly what each corrected. Use case 2 raises the register to **1.1** when it appends the risk-and-harm profile |

> **This is a teaching client.** Kabini Workforce Services B.V. and its four systems,
> vendors and named people were authored in `015_project/project.md` on 2026-09-07 and
> are fixed for the course. Every fact about Kabini in this register is sourced to
> that document, marked **[PRJ]**, and to nothing else. It is not a market figure, a
> real company or advice about anybody's organisation. The vocabulary and the
> classification rules the register applies **are** real, and they are sourced to the
> IAPP Body of Knowledge v2.1 and to the dated research under `005_research/2026-09-07/`.

---

## 1. Why this register exists, and what it settles

Before this document, Kabini had four AI systems running or in pilot and **no AI
inventory, no AI policy, no impact assessment and no named owner for any AI system**
[PRJ §1]. Meera Krishnamurthy could say there were "some AI things". Nobody could list
them.

The board has committed to publishing an EU AI Act readiness statement in order to bid
for a public-sector staffing framework, and Kabini's largest client — a Korean
electronics manufacturer — has begun putting AI Basic Act questions into procurement
questionnaires that Vikram Nair cannot answer [PRJ §1]. Neither of those can be started,
let alone finished, from a list nobody has written.

**This register settles four things, and only four.** It is version 1.0 on purpose.

1. **What exists.** Four entries, AIS-001 to AIS-004, each with a reference that every
   later artefact in the pack quotes.
2. **What each one is, described as a *system* and not as a model** — the model plus
   the data going in, the interfaces, the human oversight around it and the deployment
   context it sits in. This is the distinction the blueprint adopted in v2.1 when it
   replaced "AI model" with "AI system" across both lifecycle domains [DIFF §5], and it
   is why the register governs four systems rather than the three models underneath
   them.
3. **What type each one is** — classic, generative or agentic — with the rule that
   produced the answer named beside it, so that a reader can disagree with the rule
   rather than with a bare assertion.
4. **How the model behind each one is realised** — trained in-house, used as-is,
   fine-tuned, retrieval-augmented, or wrapped in an agentic architecture — in the
   blueprint's own words [BOK-2.1 IV.A].

**What version 1.0 deliberately does not say** is set out in §6. Read it before quoting
this register at anybody, because the most dangerous register is one whose silences are
mistaken for findings.

### The one thing to notice before reading the rows

**Nora (AIS-002) and Cadence (AIS-004) sit on the same third-party model** — Halcyon
AI's hosted API [PRJ §1]. They are two entries, not one, because a register governs
**systems**, not models. They classify differently — one generative, one agentic — even
though the weights are identical, because what differs is everything around the model:
what it is connected to, what it is allowed to do, and whether a human stands between
its output and the world. One model, two systems, two classifications, two sets of
controls. If a reader takes one thing from artefact A, take that.

---

## 2. The register — summary

Four systems. Full records at §3.

| Ref | System | Lifecycle status | Type | Model realisation | Model provenance | Business owner | Human in the loop? |
|---|---|---|---|---|---|---|---|
| **AIS-001** | **MatchScore** — CV ranking for recruiter shortlists | In production | **Classic** (R1, R2) | **Not applicable — trained in-house from Kabini's own data** (R6) | Built in-house by Kabini [PRJ §1] | **Kavitha Rajagopal**, Head of Talent Operations — *confirmed* [PRJ §1] | Yes: a recruiter reads the ranked list. The design of that oversight is undocumented — **OI-04** |
| **AIS-002** | **Nora** — candidate- and worker-facing chatbot | In production | **Generative** (R1, R3) | **Fine-tuned**, on a licensed foundation model, branded as Kabini's own (R7). Whether it also retrieves live records at inference is undocumented — **OI-05** | Foundation model licensed from **Halcyon AI, Inc.**; fine-tuning performed by Kabini [PRJ §1] | **Kavitha Rajagopal** — *interim, appointed by this register*. Contract owner: **Deepa Sridharan** | Partly: Nora answers directly to the candidate with no human reviewing the answer, but takes no action |
| **AIS-003** | **Right-to-work check** — biometric identity verification | In production | **Classic** — *classified from the outside*, see the record (R1, R2, R9) | **Used as-is**: consumed as a finished service through a vendor API (R8) | Bought from **Attestra Inc.**, Delaware, United States [PRJ §1] | **Not appointed.** Interim accountable owner: **Meera Krishnamurthy**. Contract owner: **Deepa Sridharan** — **OI-02** | Not documented: whether a human reviews a "not verified" outcome before it affects the worker is unrecorded — **OI-06** |
| **AIS-004** | **Cadence** — scheduling assistant that books interviews and issues offers | **In pilot** | **Agentic** (R1, R4) | **Agentic architecture** over a licensed foundation model with tool access (R8) | Orchestration built in-house by Kabini over **Halcyon AI, Inc.**'s hosted API [PRJ §1] | **Arjun Sundaram**, CTO — *interim, for the duration of the pilot only*. A business owner must be named before Cadence leaves pilot — **OI-03** | **No — by design.** It books interviews and issues offers without a human in the loop [PRJ §1] |

**Read the "type" column with §3.** A one-word classification is a conclusion; the value
of the register is the paragraph under it that says why, and what would change it.

---

## 3. The register — full records

### AIS-001 · MatchScore

| Field | Entry |
|---|---|
| **Reference** | AIS-001 |
| **Name** | MatchScore |
| **Lifecycle status** | In production |
| **Business owner** | **Kavitha Rajagopal**, Head of Talent Operations. Confirmed — she is recorded as the model's business owner in [PRJ §1] and her recruiters' throughput depends on it |
| **Technical owner** | **Arjun Sundaram**, CTO — Kabini built it [PRJ §1] |
| **Business purpose (the use case)** | Rank applicants against an open role so that a recruiter works a shortlist instead of a pile. It exists to raise recruiter throughput |
| **Decision it touches** | Which candidates a human recruiter looks at, and in what order. It is an input to a hiring decision about a named person |
| **Type** | **Classic** — rule R1 then R2 |
| **Why that type** | It produces a **score over records that already exist**. It does not generate text, images or any new content, and it takes no action in the world: it writes a number into Talent Cloud and stops. Both the generative test (R3) and the agentic test (R4) fail. It is the ordinary supervised-learning case the blueprint calls "classic" [BOK-2.1 IV.A] |
| **Model realisation** | **Not applicable — trained in-house from Kabini's own data.** Rule R6. *Do not write "as-is" here.* The as-is / fine-tuning / retrieval-augmented / agentic axis is the blueprint's list of ways to **deploy a model somebody else pre-trained** [BOK-2.1 IV.A]. Kabini trained this one; the axis has nothing to say about it |
| **Model provenance** | Built in-house by Kabini on tabular and free-text data [PRJ §1] |
| **What happens at training time** (R5) | Supervised training on the **placement warehouse** — eight years of historical placement outcomes on Amazon-hosted infrastructure in `eu-west-1` [PRJ §1]. Performed by Kabini's **Bengaluru engineering team**, against a read replica of the warehouse in `ap-south-1` [PRJ §1]. **Retraining frequency is not documented — OI-07** |
| **Where the training data sits** | Two places, not one: the warehouse in `eu-west-1` and the **Bengaluru replica in `ap-south-1`**, stood up in 2023 and **recorded in no transfer record** [PRJ §1]. Written down here because the register is where a copy of personal data outside the Union stops being an engineering detail. **OI-12** |
| **What happens at inference time** (R5) | A candidate record is scored against a vacancy and a fit score is written back into Talent Cloud, where recruiters see it as a ranked list. Performed by Kabini, on Kabini's own infrastructure. **No data goes to a third party** for this system — which is not the same sentence as "no data leaves the EU", and the training row above is why |
| **Data in** | Candidate records — CVs, applications and structured fields — read from **Talent Cloud**, the applicant tracking system [PRJ §1] |
| **Data out** | A fit score written back into Talent Cloud against the candidate record |
| **Training data provenance** | The placement warehouse. **Kabini has never written down where all of it came from** [PRJ §1]. Recorded here as a stated fact, not as a finding; it is the opening question of the data governance dossier (use case 12) |
| **Interfaces and dependencies** | Talent Cloud (read and write); the placement warehouse (training only); the `ap-south-1` replica of it (training only) |
| **Human oversight** | A recruiter reads the ranked list and chooses whom to contact. Whether the ranking is advisory or effectively dispositive — whether anyone ever works below the fold — **is not documented. OI-04** |
| **Deployment context** | Internal, used by Kabini's own recruiters. Talent Cloud is the group applicant tracking system, so MatchScore is assumed to reach every region Kabini recruits in — the EU, South Korea and the United States [PRJ §1]. **Assumed, not confirmed — OI-08** |
| **Volume** | **Not measured.** Kabini places about **40,000 contract workers a year** [PRJ §1]; how many applications are scored to produce those placements is not recorded anywhere. **OI-01** |
| **Third parties** | None in the inference path |
| **Register entry sourced from** | [PRJ §1] system table and existing-systems list |

**Why this row is the one the trainer builds on screen.** MatchScore is the row a hurried
governance team writes as *"a CV-ranking model, XGBoost, trained on historical hires"* —
and that sentence governs nothing. Annex 2 sets that description beside the one above
and shows what the seven extra fields buy.

---

### AIS-002 · Nora

| Field | Entry |
|---|---|
| **Reference** | AIS-002 |
| **Name** | Nora |
| **Lifecycle status** | In production |
| **Business owner** | **Kavitha Rajagopal**, Head of Talent Operations — **interim, appointed by this register on 2026-09-07**, on the basis that Talent Operations owns the candidate journey. Nora also answers **payroll** questions about Kabini People, and that content has no named owner — **OI-09** |
| **Contract owner** | **Deepa Sridharan**, Head of Procurement — she signed the Halcyon AI agreement [PRJ §1] |
| **Technical owner** | **Arjun Sundaram**, CTO |
| **Business purpose (the use case)** | Answer candidates' and contractors' questions about placements and payroll in natural language, without a human answering each one |
| **Decision it touches** | None directly — it informs rather than decides. But it tells a worker things about their own placement and pay, and it is the only source many of them will consult |
| **Type** | **Generative** — rule R1 then R3 |
| **Why that type** | It **produces new natural-language text at inference**, composed for the question in front of it rather than selected from a list of prepared answers. That is the generative test in R3. It is not agentic: it takes no action beyond replying, and R4 fails |
| **Model realisation** | **Fine-tuned** — rule R7. Kabini fine-tunes a licensed foundation model on its own placement data and puts its own name on the output [PRJ §1] |
| **A gap that matters more than it looks** | Whether Nora also **retrieves live records** from Kabini People at inference time to answer a specific worker's question — retrieval-augmented generation — or answers only from general policy content, **is not documented**. The two designs are not the same system: one sends an identified worker's payroll data to a third-party API on every question, the other never does. **OI-05.** It is recorded here and resolved in the deploy-decision record (use case 17) |
| **Model provenance** | Foundation model **licensed from Halcyon AI, Inc.** under a commercial agreement signed **without legal review** [PRJ §1] |
| **What happens at training time** (R5) | **Pre-training was done by Halcyon AI** and Kabini has no visibility of it — not the data, not the method, not the cut-off. **Fine-tuning is done by Kabini** on its own placement data |
| **What happens at inference time** (R5) | Every question is answered by **Halcyon AI's hosted API**. The prompt — and whatever context is attached to it — leaves Kabini's control to reach the model. Where Halcyon hosts that endpoint is **not recorded — OI-05** |
| **Data in** | Free-text questions from candidates and contractors; Kabini placement data used in fine-tuning; content about Kabini People [PRJ §1] |
| **Data out** | Natural-language answers shown to the person who asked, under the Kabini brand |
| **Interfaces and dependencies** | Halcyon AI hosted API (hard dependency — Nora does not run without it); Kabini People as the subject matter; the candidate-facing channel |
| **Human oversight** | None per answer. No human reviews an answer before the candidate reads it |
| **Deployment context** | External-facing, to candidates and contractors, in **English, Dutch and Hindi** [PRJ §1], in every market Kabini operates in — the EU, South Korea and the United States [PRJ §1]. Three languages is a system fact and not a model fact: it is part of what any evaluation of Nora has to cover, which is where the test plan picks it up (use case 13). The market list and the language list do not obviously match, and confirming the deployment geography per market is **OI-08** |
| **Volume** | Not recorded. Kabini's population is about **40,000 contract workers a year plus 11,000 permanent staff** [PRJ §1], which bounds the audience but not the traffic. **OI-01** |
| **Third parties** | **Halcyon AI, Inc.** — model provider |
| **Register entry sourced from** | [PRJ §1] system table, existing-systems list and the Halcyon AI note |

---

### AIS-003 · The right-to-work check

| Field | Entry |
|---|---|
| **Reference** | AIS-003 |
| **Name** | The right-to-work check (Attestra biometric identity verification) |
| **Lifecycle status** | In production |
| **Business owner** | **Not appointed.** Interim accountable owner: **Meera Krishnamurthy**, General Counsel, from 2026-09-07 until a permanent owner is named — **OI-02**. That a system which decides whether a person may work has no business owner is a finding of this register, not an omission in it |
| **Contract owner** | **Deepa Sridharan**, Head of Procurement [PRJ §1] |
| **Technical owner** | None at Kabini. Kabini operates no part of it |
| **Business purpose (the use case)** | Verify that a candidate or contractor is who they say they are, as part of establishing their right to work |
| **Decision it touches** | Whether a person can be placed at all. A negative outcome stops the engagement |
| **Type** | **Classic** — rules R1, R2, **and R9** |
| **Why that type — and read this carefully** | Biometric verification compares a submitted sample against a reference and returns a determination. It creates no new content (R3 fails) and takes no action (R4 fails), so on the evidence Kabini has, it is classic. **But Kabini did not build it and cannot inspect it** [PRJ §1]. Attestra has never been asked what the system is, and has never stated it. This classification is therefore made **from the outside, from observed behaviour**, and is marked under rule R9 as *asserted by the deployer, unconfirmed by the provider*. Confirming it is question one of the third-party questionnaire (use case 7) and is closed in use case 18 |
| **Model realisation** | **Used as-is** — rule R8. Kabini consumes a finished service through a vendor API. It does not train it, tune it, retrieve into it or wrap it in an agent. This is the clean "as-is" entry in the register, and the contrast that makes the other three legible |
| **Model provenance** | Bought from **Attestra Inc.**, Delaware, United States [PRJ §1] |
| **What happens at training time** (R5) | **Nothing at Kabini.** Whether Attestra trains or re-trains on data Kabini submits is **not known** — it is a question for the questionnaire and a term for the contract. **OI-06** |
| **What happens at inference time** (R5) | Kabini calls **Attestra's API**. Personal data, including **biometric data**, leaves the EU to reach it [PRJ §1]. A verification outcome comes back |
| **Data in** | Identity data including biometric data about a named individual |
| **Data out** | A verification outcome recorded against the individual |
| **Internal mechanism** | **Not disclosed to Kabini, and Kabini cannot inspect it** [PRJ §1]. Recorded as unknown. A register that invents a mechanism it has not been shown is worse than one that says it does not know |
| **Interfaces and dependencies** | Attestra's API (hard dependency); the onboarding process that consumes the outcome |
| **Human oversight** | **Not documented.** Whether a "not verified" outcome is reviewed by a person before it stops an engagement, and whether the individual can contest it, is unrecorded — **OI-06** |
| **Deployment context** | Onboarding, in every market Kabini places into. Personal data crosses from the EU to a US-hosted service [PRJ §1] — **recorded as a data-flow fact. This register draws no legal conclusion from it**; that is use case 24 |
| **Volume** | Not recorded; bounded by the ~40,000 placements a year [PRJ §1]. **OI-01** |
| **Third parties** | **Attestra Inc.** — service provider, and the only party who knows what the system is |
| **Register entry sourced from** | [PRJ §1] system table and existing-systems list |

---

### AIS-004 · Cadence

| Field | Entry |
|---|---|
| **Reference** | AIS-004 |
| **Name** | Cadence |
| **Lifecycle status** | **In pilot** |
| **Business owner** | **Arjun Sundaram**, CTO — **interim, for the pilot only**, appointed by this register on 2026-09-07 because he owns the pilot. **A business owner must be named before Cadence leaves pilot — OI-03.** An autonomous system whose only owner is the person who built it has no independent challenge in it |
| **Technical owner** | **Arjun Sundaram**, CTO |
| **Business purpose (the use case)** | Take interview scheduling and offer issuance off recruiters' desks entirely |
| **Decision it touches** | When and whether a candidate is interviewed, and **the issuing of an offer** — an act with effect on a named person |
| **Type** | **Agentic** — rule R1 then R4 |
| **Why that type, and why it is not simply "generative"** | The model underneath Cadence is the same generative foundation model that sits under Nora [PRJ §1]. What makes Cadence agentic is not the model: it is that the **system plans a sequence of steps, calls tools that change the world — a calendar, a record in Talent Cloud, an offer — and completes them without a human approving each one** [PRJ §1]. R4's test is *does it act, or does it only produce output for a human to act on?* Cadence acts. **This is the sharpest model-versus-system point in the register: identical weights, different system, different class, different controls** |
| **Model realisation** | **Agentic architecture** over a licensed foundation model with tool access — rule R8, in the blueprint's own vocabulary [BOK-2.1 IV.A]. Whether any fine-tuning has additionally been applied is **not documented — OI-10** |
| **Model provenance** | **Halcyon AI, Inc.**'s hosted API [PRJ §1]; the orchestration and tool layer built in-house by Kabini |
| **What happens at training time** (R5) | Nothing at Kabini that is recorded. Pre-training is Halcyon's and is not visible to Kabini |
| **What happens at inference time** (R5) | Halcyon's hosted API is called, repeatedly, inside a loop that also calls Kabini's own systems. **Inference here is not one call and one answer** — it is a chain of calls whose intermediate steps nobody reads |
| **Data in** | Candidate and vacancy data, calendars, and whatever the agent gathers as it goes |
| **Data out** | **Actions**, not text: booked interviews, issued offers, updated records |
| **Interfaces and dependencies** | Halcyon AI hosted API; Talent Cloud; calendaring; the offer-issuing path. Each tool the agent can call is a way for it to act, and **the full list of tools it can reach is not documented — OI-10** |
| **Human oversight** | **None in the loop, by design** [PRJ §1] |
| **Deactivation** | **No documented way to stop it**, no named person who can, and no tested procedure. Recorded here; written in use case 22 |
| **Deployment context** | Pilot. **Scope of the pilot — which offices, which roles, how many candidates — is not recorded. OI-11** |
| **Volume** | Not recorded — pilot. **OI-11** |
| **Third parties** | **Halcyon AI, Inc.** |
| **Register entry sourced from** | [PRJ §1] system table and existing-systems list |

---

## 4. What the register shows when the four rows are read together

These are findings of version 1.0, and each one is evidenced by the rows above.

1. **Four systems, three models, two vendors, one register.** Counting models gives
   three; counting systems gives four; only the count of four can be governed, because
   the controls Nora needs and the controls Cadence needs are different even though the
   model is the same.
2. **All three of the blueprint's classes are present in one company.** Classic in
   AIS-001 and AIS-003, generative in AIS-002, agentic in AIS-004. A programme designed
   around one class would miss two.
3. **Three of the four realisations are present, and the fourth is absent for a reason.**
   As-is (AIS-003), fine-tuned (AIS-002), agentic architecture (AIS-004), and AIS-001
   which is off the axis entirely because Kabini trained it. Retrieval-augmented
   generation is **not confirmed anywhere** — it is the open question in AIS-002.
4. **Two of the four systems have no real business owner**, and they are the two whose
   outputs bear hardest on an individual: the check that decides whether someone may
   work at all, and the agent that issues offers.
5. **The two systems that decide most about a person are the two Kabini understands
   least.** AIS-003 cannot be inspected; AIS-004 acts without anyone reading its
   intermediate steps.
6. **Kabini sends personal data to two external endpoints** — Halcyon AI's API
   (AIS-002, AIS-004) and Attestra's API (AIS-003) — and in one of them the data is
   biometric and crosses out of the EU [PRJ §1]. That is a data-flow fact recorded now
   so that use cases 23 and 24 do not have to go looking for it.
7. **Personal data also leaves the Union where nobody was looking for it, and no vendor
   is involved.** The `ap-south-1` replica is an internal copy of eight years of
   placement outcomes, made for a good engineering reason, sitting in a country with no
   EU adequacy decision, in no transfer record. It is the register's most consequential
   finding and the clearest argument for doing an inventory at all: the two transfers
   in finding 6 were known because somebody signed a contract for them, and this one was
   not, because nobody had to. Use case 12 gives it a lineage record; use case 24 gives
   it a mechanism and a transfer impact assessment.
8. **Nobody measures how often any of them runs.** OI-01 is open against all four.

---

## 5. Open items

Every open item has an owner and a date. The dates were set by this register on
2026-09-07 and are to be confirmed by the AI governance forum when it is constituted
(use case 4).

| ID | Against | What is missing | Owner | Due | Closes in |
|---|---|---|---|---|---|
| **OI-01** | All four | No system records how often it runs. There is no inference volume for any of them | Arjun Sundaram | 2026-10-15 | Carried into the monitoring plan, use case 15 |
| **OI-02** | AIS-003 | No business owner for the right-to-work check. Interim owner is the General Counsel, which is not a permanent answer | Meera Krishnamurthy | **2026-09-30** | Use case 3 (roles), use case 4 (charter) |
| **OI-03** | AIS-004 | No business owner for Cadence other than the CTO who built it. Required **before** it leaves pilot | Meera Krishnamurthy | **2026-09-30** | Use case 3, use case 4 |
| **OI-04** | AIS-001 | Human oversight design not documented: is the ranking advisory or effectively dispositive? | Kavitha Rajagopal | 2026-10-15 | Use case 9 (design and build record) |
| **OI-05** | AIS-002 | Not documented whether Nora retrieves live records at inference, and where Halcyon hosts the endpoint. Decides whether identified worker data leaves Kabini on every question | Arjun Sundaram | 2026-10-15 | Use case 17 (deploy-decision record) |
| **OI-06** | AIS-003 | Not known whether Attestra trains on submitted data, nor whether a human reviews a negative outcome before it stops an engagement | Deepa Sridharan | 2026-10-31 | Use case 7 (questionnaire), use case 18, use case 19 |
| **OI-07** | AIS-001 | No documented retraining frequency | Arjun Sundaram | 2026-10-31 | Use case 15 (retraining schedule) |
| **OI-08** | AIS-001, AIS-002 | Per-market deployment geography assumed from Talent Cloud being the group system, not confirmed | Vikram Nair, with Kavitha Rajagopal | 2026-10-15 | Use cases 27 and 28 (EU, Korea, US) |
| **OI-09** | AIS-002 | The payroll-answer content Nora serves has no named content owner | Kavitha Rajagopal | 2026-10-15 | Use case 4 |
| **OI-10** | AIS-004 | The full list of tools Cadence can call is not documented, and it is not recorded whether the model is additionally fine-tuned | Arjun Sundaram | **2026-09-30** | Use cases 20 and 22 |
| **OI-11** | AIS-004 | Pilot scope not recorded: which offices, which roles, how many candidates | Arjun Sundaram | **2026-09-30** | Use case 20 |
| **OI-12** | AIS-001 | The `ap-south-1` replica of the placement warehouse is in no transfer record: no mechanism, no transfer impact assessment, and no written statement of who in Bengaluru may read it | Meera Krishnamurthy, with Arjun Sundaram | **2026-09-30** | Use case 12 (lineage), use case 24 (transfers) |

**An open item is an entry, not a blank.** The register is complete as version 1.0
precisely because it says what is not known, who is finding out, and by when. A field
left empty tells a reader nothing; a field that says "not documented, Arjun Sundaram,
2026-10-15" is a governance control.

---

## 6. What version 1.0 does not say, and where it gets said

The most expensive misuse of a register is quoting a silence as a finding. This version
makes **no legal claim about any of the four systems**. It does not say that MatchScore
is high-risk, that Article 50 reaches Nora, that Attestra's service involves a restricted
transfer, or that Cadence is high-impact AI. It records the facts those conclusions will
be drawn from, and stops.

| Not in version 1.0 | Added by | Why not now |
|---|---|---|
| The harms each system can do to individuals, groups, organisations and society; the characteristics that force governance; what each responsible-AI principle demands | Use case 2 | The description has to be right before the harm analysis can be attached to it |
| Developer / provider / deployer / user, assigned **per activity** rather than per company | Use case 3 | Those are task labels, not company labels, and assigning them needs the activity list this register only just created |
| Risk tier and the obligations that follow | Use case 26 | Classification under a legal framework is not the same as classification as classic / generative / agentic, and conflating the two is a standard error |
| Which EU, Korean and US obligations apply, and from what date | Use cases 27 and 28 | Those dates carry a compilation date and a verification status of their own. The research report records that EUR-Lex was unreachable and the EU timeline is corroborated rather than read from the Official Journal [RR §2.5] — so they are written once, carefully, in the applicability memo, not scattered here |
| Impact assessments, risk registers, data lineage, testing, model cards, monitoring, incidents, vendor redlines, deactivation | Use cases 8–22 | Each hangs off a row above and quotes its AIS reference |

---

## 7. How this register is kept

- **The register is written first and edited last** [PRJ §3]. Later artefacts add columns
  and cross-references to it; they do not restate its facts.
- **A fact lives in one place.** If a fact recorded here changes, it changes **here**,
  the version number goes up, and every artefact that quoted the row is re-issued. Two
  documents in this pack must never disagree about a fact [PRJ §5 item 14].
- **Every entry carries its source.** A row with no source is not an entry.
- **Every classification carries its rule.** R-numbers resolve in
  `A_annex_1_classification_rules.md`. If a rule is wrong, the fix is to the rule, and
  every row that used it is re-checked.

### Change control

| Version | Date | Author | Change |
|---|---|---|---|
| 1.0 | 2026-09-07 | AI governance workstream | First issue. Four systems recorded: description as a system, type, realisation, training and inference, ownership, data and dependencies. Twelve open items raised |
| 1.0.1 | 2026-09-09 | AI governance workstream | Correction release; no finding, classification, owner, open item or due date changed. (a) This change-control line said "eleven open items" where §5 has always carried twelve — corrected, and the same count corrected in Annex 3 and in `../use_case.md`. (b) The citation for "agentic architectures added to IV.A" pointed at §6 of the v2.0.1→v2.1 diff; it is in §5, "Other III/IV changes" — corrected in Annex 1 and `A_sources.md`. (c) The blueprint's question counts were written "of 100"; they are best read as counts of the **85 scored** questions, and that reading is now marked in `A_sources.md` as an inference from two published figures rather than as something the IAPP states, with the staleness of its source on the same row. (d) AIS-002 now records the three languages Nora answers in, which was in [PRJ §1] and had been left out |
| 1.0.2 | 2026-09-09 | AI governance workstream | Correction release raised by an independent check of the artefact against its sources; no finding, classification, owner, open item or due date changed. (a) The claim that Domains III and IV are "42–50 of 85 scored questions" was cited to §4 item 4 of the research report, which is about scenario questions. It is §3.3, "Disagreement 2" — corrected in Annex 1, Annex 2 and `../use_case.md`. (b) The closing line of Annex 3 and of `../use_case.md` said the register leaves "four owners — two of them interim"; §2 marks **three** as interim (AIS-002, AIS-003, AIS-004), and `A_sources.md` records that every owner except AIS-001's is appointed by this register. The count is corrected to three. Finding 4 of §4 is unchanged and still says *two* systems have no real business owner — AIS-003 and AIS-004, the two carrying OI-02 and OI-03; that is a judgement about ownership quality, not a count of interim appointments. (c) `A_sources.md` §4 had no claim-table row for the 42–50 figure; Domain III is added to the domain-weight row with the [BOK-2.1] pages and the [RR] §3.3 pointer |
| 1.0.3 | 2026-09-09 | AI governance workstream | Correction release raised by two source checks; **no finding, classification, owner, open item or due date changed, and no wording in this register changed** — the corrections fall in Annex 1, `A_sources.md` and the folder README. (a) **ISO/IEC 22989 has been read.** Annex 1 and `A_sources.md` had said the standard was never read, `iso.org` having returned HTTP 403 [RR §2.5]; that was true when written. A single-user licensed copy was bought and read on 2026-09-09 and is recorded as the new key **[ISO-22989]**. It confirms the attribution behind R1 — clause 3.1.4 defines an AI system as an engineered system that generates outputs, clause 3.1.23 defines a model as a representation. The licence prohibits reproduction, so the pack rule **tightens** from "named but not read, therefore not quoted" to "read, licensed, therefore clause numbers may be cited and clauses may not be quoted". No verbatim 22989 wording appears anywhere in the pack. (b) **The handbook re-verification listed in `A_sources.md` §6 has been done, and the answer weakens the figure.** A newer candidate handbook exists — the general **[HB-5.3.2]**, effective 1 June 2026 — because the IAPP has discontinued the AIGP-specific handbook; and it does **not** repeat the "100 questions, 85 scored" split, saying instead that the counts live on the designation's page, which carries none. The figure and its hedging are unchanged; its weakness is now established rather than suspected, and a narrower re-verification replaces the closed one |

---

## 8. Sign-off

| Role | Name | Position | Date |
|---|---|---|---|
| Document owner | **Meera Krishnamurthy** | General Counsel | 2026-09-07 |
| Accepted for AIS-001 | **Kavitha Rajagopal** | Head of Talent Operations | 2026-09-07 |
| Accepted for AIS-002, AIS-004 (technical) | **Arjun Sundaram** | Chief Technology Officer | 2026-09-07 |
| Accepted for vendor records (AIS-003, and the Halcyon AI agreement behind AIS-002 and AIS-004) | **Deepa Sridharan** | Head of Procurement | 2026-09-07 |
| Noted for the Seoul market | **Vikram Nair** | Regional Director, Seoul | 2026-09-07 |

*People, systems and vendors per [PRJ §1]. Sources and their verification status:
`A_sources.md`. Classification rules: `A_annex_1_classification_rules.md`.*
