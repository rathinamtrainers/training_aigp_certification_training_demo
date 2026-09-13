# The project: the Kabini AI Governance Pack

*AIGP Certification Training · Rathinam Trainers & Consultants · The AI Engineering Series*
*Written 2026-09-07 against `010_brochure/brochure.md`, `005_research/2026-09-07/` and
`006_competitors/2026-09-07/`.*

This document describes **what is built during the course**. It is the fixed reference
for every use case in `015_project/use_case_plan.md`. The client's name, the system's
name and the stack below **do not change once the course has begun.**

---

## 1. The client

**Kabini Workforce Services B.V.**

A workforce services company headquartered in Amsterdam, founded in Bengaluru in 2011
and re-domiciled to the Netherlands in 2019, the year European placements passed half
its revenue. It places around **forty thousand contract workers a year** across the
European Union, South Korea and the United States, and employs **eleven thousand
permanent staff** of its own — most of them in Europe, and about **two thousand three
hundred in its Bengaluru delivery centre**, which runs payroll operations, candidate
support and, since 2023, its own engineering team. Recruiters, account managers, payroll
administrators and a compliance function — plus a **legal team of six** in Amsterdam who
already carry GDPR, employment law in nine countries and the commercial contract book.

Kabini has **no AI governance function at all**. It has no AI inventory, no AI policy, no
impact assessment and no named owner for any AI system. What it does have is four AI
systems already running or in pilot, and two deadlines it did not set for itself.

**Kabini is not part of the Kaveri group, and the room should be told so once.** It is a
supplier: Kabini staffs Kaveri Direct's Rotterdam fulfilment operation and part of
Kaveri's Bengaluru back office, which is why Kaveri appears in Kabini's client records
and in one procurement questionnaire later in the course. The shared world is a
convenience for a trainer who teaches both courses; it is not a group relationship, and
nothing Kabini runs is one of Kaveri's five AI activities.

### The people the room deals with

These are the names a participant hears in every scenario. They exist so that
"stakeholder engagement" has a face and "who is accountable" has an answer.

| Person | Role at Kabini | What they want |
|---|---|---|
| **Meera Krishnamurthy** | General Counsel, Amsterdam, and the board's sponsor for this work | Something she can put in front of the board and an auditor without hedging |
| **Arjun Sundaram** | Chief Technology Officer, Amsterdam, with the engineering team reporting from Bengaluru | To keep shipping; he owns the two systems Kabini built itself |
| **Kavitha Rajagopal** | Head of Talent Operations | The CV-ranking model's business owner; her recruiters' throughput depends on it |
| **Vikram Nair** | Regional Director, Seoul | Holds the relationship with the Korean client that started asking AI Basic Act questions |
| **Deepa Sridharan** | Head of Procurement | Signs the vendor contracts and has never had an AI clause set to work from |

### The constraint and the ask

Kabini's board has committed to **publishing an EU AI Act readiness statement** in order
to bid for a public-sector staffing framework. Separately, its largest client — a Korean
electronics manufacturer — has begun putting **AI Basic Act questions into procurement
questionnaires**, and Vikram Nair has no answers to give. A third letter arrived in
August: Kaveri Direct's procurement team, working through its own governance exercise,
has asked Kabini what personal data reaches India and under what basis.

The ask, in Meera Krishnamurthy's words: *"Give me a governance programme I can put in
front of a board, an auditor and a procurement officer. Not a strategy deck. The actual
documents, with owners and dates on them."*

### The four AI systems

Chosen because between them they reach every corner of the Body of Knowledge.

| # | System | What it is | Why it is in the course |
|---|---|---|---|
| 1 | **MatchScore** | A CV-ranking model built in-house **by the Bengaluru engineering team** on tabular and free-text data, scoring candidate fit for a role | Employment decisions → non-discrimination law, high-risk under the EU classification, high-impact under Korea's. Kabini is developer, provider and deployer at once — and the developer sits outside the Union while the provider is established inside it. |
| 2 | **Nora** | A candidate-facing chatbot on a procured foundation model, answering placement and payroll questions in English, Dutch and Hindi | Article 50 transparency, vendor licensing terms — and the provider/deployer question the moment Kabini fine-tunes it on its own placement data and puts its own name on the output |
| 3 | **The right-to-work check** | A biometric identity verification service bought from **Attestra Inc.** (Delaware, United States) | Special category data, cross-border transfer, third-party assessment of a system Kabini did not build and cannot inspect |
| 4 | **Cadence** | An agentic scheduling assistant in pilot that books interviews and issues offers without a human in the loop | Agentic deployment, secondary and unintended use, downstream harms, and the deactivation control |

**The foundation model behind Nora** is licensed from **Halcyon AI, Inc.** under a
commercial agreement Deepa Sridharan signed without legal review. That agreement is the
one the room redlines.

### Kabini's existing systems and data

The governance work does not land on empty ground. It lands on this:

- **Talent Cloud** — the applicant tracking system. Source of every CV, application and
  outcome. MatchScore reads from it and writes a score back into it.
- **Kabini People** — the HR and payroll platform for eleven thousand staff and forty
  thousand contractors. Nora answers questions about it.
- **The placement warehouse** — eight years of historical placement outcomes on
  Amazon-hosted infrastructure in `eu-west-1`. This is MatchScore's training data, and
  nobody has ever written down where all of it came from.
- **The Bengaluru replica** — a read replica of the placement warehouse in `ap-south-1`,
  stood up in 2023 so the engineering team could train against real data without a
  four-hour round trip. Nobody wrote that down either, and it is not in any transfer
  record. It is how MatchScore is actually built.
- **Attestra's API** — the biometric check. Personal data leaves the EU to reach it.
- **Halcyon AI's hosted API** — the foundation model behind Nora, and behind Cadence.
- **The existing policy set** — a privacy policy, an information security policy, a data
  governance standard and an IP policy, all written before anyone at Kabini had heard
  the phrase "training data".

---

## 2. The system

Kabini is handed **the Kabini AI Governance Pack**: one coherent, cross-referenced
set of governance documents that says, for every AI system Kabini runs, what it is,
who owns it, what law reaches it and from when, what was assessed and what was found,
what is measured and against what threshold, what happens when it goes wrong, and who
can turn it off. It is written to be read by three different readers who never read the
same thing — a board, an external auditor, and a procurement officer at a client — and
it is built so that a fact stated in one document is the same fact everywhere else.

---

## 3. The architecture

The pack is not a pile of documents. It has a spine: **the register is the index, and
every other artefact hangs off a row in it.**

```
                      ┌──────────────────────────────────────────┐
                      │  A. AI SYSTEM INVENTORY & USE-CASE       │
                      │     REGISTER  — the spine                │
                      │  one row per system: MatchScore, Nora,   │
                      │  right-to-work check, Cadence            │
                      │  + classification, roles per activity,   │
                      │    owner, risk tier, obligation dates    │
                      └───┬───────┬───────────┬──────────┬───────┘
                          │       │           │          │
        ┌─────────────────┘       │           │          └──────────────────┐
        ▼                         ▼           ▼                             ▼
┌───────────────┐   ┌─────────────────────┐  ┌─────────────────────┐  ┌──────────────┐
│ B. PROGRAMME  │   │ C. BUILD FILE       │  │ D. DEPLOYMENT FILE  │  │ E. LEGAL &   │
│               │   │   (MatchScore)      │  │  (Nora, Cadence,    │  │   STANDARDS  │
│ · charter,    │   │ · design & build    │  │   right-to-work)    │  │              │
│   RACI, forum │   │   control record    │  │ · deploy-decision   │  │ · regulatory │
│ · training &  │   │ · AI system impact  │  │   record            │  │   applica-   │
│   awareness   │   │   assessment (42005)│  │ · third-party       │  │   bility     │
│   plan        │   │   + DPIA/FRIA map   │  │   assessment &      │  │   memo (EU,  │
│ · AI lifecycle│   │ · risk register     │  │   review            │  │   KR, US)    │
│   policy      │   │ · data governance   │  │ · vendor agreement  │  │ · standards  │
│ · existing-   │   │   dossier           │  │   redline           │  │   map (42001,│
│   policy gap  │   │ · test plan +       │  │ · deployment        │  │   NIST RMF,  │
│   redline     │   │   results           │  │   control set       │  │   OECD)      │
│ · acceptable  │   │ · model card        │  │ · secondary-use &   │  │              │
│   use policy  │   │ · release-readiness │  │   downstream-harm   │  │              │
│ · third-party │   │   checklist         │  │   forecast          │  │              │
│   assessment  │   │ · monitoring &      │  │ · external comms    │  │              │
│   questionn-  │   │   retraining sched. │  │   plan              │  │              │
│   aire        │   │ · audit & red-team  │  │ · deactivation and  │  │              │
│               │   │   calendar          │  │   localisation      │  │              │
│               │   │ · post-market       │  │   procedure         │  │              │
│               │   │   monitoring plan   │  │                     │  │              │
│               │   │ · incident runbook  │  │                     │  │              │
│               │   │   + incident record │  │                     │  │              │
└───────────────┘   └─────────────────────┘  └─────────────────────┘  └──────────────┘
        │                     │                        │                     │
        └─────────────────────┴────────────┬───────────┴─────────────────────┘
                                           ▼
                            ┌───────────────────────────────┐
                            │  F. THE PACK INDEX            │
                            │  artefact checklist, owners,  │
                            │  version and date on every    │
                            │  page                         │
                            └───────────────────────────────┘
```

**How the pieces talk to each other.**

- **The register is written first and edited last.** Use case 1 creates it; almost every
  later use case adds a column or a cross-reference to it. If a fact changes, it changes
  in the register and the dependent artefact is re-issued.
- **The build file (C) is MatchScore only.** One system carried all the way through the
  development lifecycle is worth four systems carried a third of the way.
- **The deployment file (D) is the other three systems**, because each of them teaches
  something MatchScore cannot: a bought system, a licensed model, an autonomous agent.
- **The legal and standards file (E) is written last and reaches backwards.** Every
  obligation it names points at an artefact in B, C or D that already exists. This is
  the whole reason law comes after the lifecycle in this course.
- **Where Kabini's real systems sit.** Talent Cloud and the placement warehouse are
  the data sources the data governance dossier traces. Attestra's API and Halcyon AI's
  API are the third-party boundaries the vendor assessment and the redline sit on. The
  existing policy set is the input to the gap redline, not a blank page.

**There is no software component in this architecture, and that is the point.** The
deliverable is documents. Two of the demonstrations put a tool on screen so that a
number in a document is a number the room watched being produced, but nothing in the
pack is generated by a program.

---

## 4. The stack

This is a governance course. The "stack" is the body of law, standards, frameworks and
artefact formats participants will be able to operate, plus a small number of tools the
trainer runs on screen. **Versions and dates verified 2026-09-07.**

### Certification blueprint

| Item | Version |
|---|---|
| IAPP AIGP Body of Knowledge and Exam Blueprint | **v2.1**, approved 9 September 2025, effective 2 February 2026 |
| Superseded version, used only for the diff | v2.0.1, effective 3 February 2025 |
| Structure taught | Four domains, thirteen sub-domains |

### AI-specific law

| Instrument | Status used in the course |
|---|---|
| **EU AI Act**, as amended by **Regulation (EU) 2026/1744** (Digital Omnibus on AI) | In force 27 July 2026. Prohibited practices and AI literacy since 2 Feb 2025; GPAI provider obligations since 2 Aug 2025; Article 50 transparency commenced 2 Aug 2026 and was **not** deferred; standalone Annex III high-risk deferred to **2 Dec 2027**; embedded Annex I high-risk to **2 Aug 2028** |
| **EU General-Purpose AI Code of Practice** | Published 10 July 2025 |
| **South Korea AI Basic Act** and Enforcement Decree | In force 22 January 2026, with a ministry grace period running through 2026 |
| **US federal executive orders** | EO 14179 (January 2025, rescinding EO 14110); the December 2025 preemption order |
| **Colorado SB 26-189** | Enacted May 2026, effective 1 January 2027 — the worked example of the US state pattern |

**Every timeline handout carries the date it was compiled on its face.** EUR-Lex was
unreachable from the research environment; the core deferral dates are corroborated
across independent legal analyses and the finer Omnibus detail is marked unverified in
the source notes. Nothing in the pack asserts a date it cannot cite.

### Existing law applied to AI

Data protection and privacy law — lawful basis, purpose limitation, minimisation,
privacy by design, controller obligations, data subject rights, automated decision
making, cross-border transfer, breach notification, special category and biometric data
· intellectual property law including limits on the use of data for training ·
non-discrimination law in employment, credit, lending, housing and insurance · consumer
protection and unfair or deceptive acts or practices · product liability and design and
manufacturing defects.

**India is a receiving country here, not a fourth jurisdiction.** The Bengaluru replica
makes a transfer to a third country with no EU adequacy decision, so it is worked under
Chapter V — the transfer mechanism, the transfer impact assessment, and the receiving
country's own law named as context — inside the existing-law module. The **DPDP Act 2023
and the DPDP Rules 2025** are named for that purpose and are not taught as a regime;
the three worked jurisdictions remain the EU, South Korea and the United States.

### Standards and frameworks

| Standard | Version | What it is used for here |
|---|---|---|
| **ISO/IEC 22989** | current edition | AI concepts and terminology — the source of the model/system distinction |
| **ISO/IEC 42001** | current edition | The certifiable AI management system; its clause structure is the skeleton of the standards map |
| **ISO/IEC 42005** | **:2025** | AI system impact assessment — the format the MatchScore assessment is written in |
| **NIST AI RMF** | **1.0** (there is no 2.0) | Govern / Map / Measure / Manage, plus the AI RMF Playbook |
| **NIST AI 600-1** | Generative AI Profile | Applied to Nora and Cadence |
| **OECD AI Principles** | current | The principles row of the standards map |

### Artefact formats produced

AI system inventory · use-case register · governance charter and RACI · AI lifecycle
policy · acceptable use policy · third-party AI assessment questionnaire · AI system
impact assessment · DPIA and FRIA mapping · risk register with probability/severity
matrix · data lineage and provenance record · test plan across validation, performance,
security, bias and interpretability · model card · release-readiness checklist ·
post-market monitoring plan · monitoring and retraining schedule · incident runbook and
incident record · vendor agreement redline · deactivation procedure · regulatory
applicability memo · standards map.

### Tools demonstrated by the trainer

| Tool | Where | What the room sees |
|---|---|---|
| **NIST AI RMF Playbook** | browser | One subcategory opened and its suggested actions read |
| **Content Credentials verifier** (`contentcredentials.org/verify`) | browser | Real Article 50 transparency and synthetic-content marking inspected in the wild |
| **Public model card exemplars** (Hugging Face, Google) | browser | Real cards critiqued before the room writes MatchScore's |
| **Fairlearn** | trainer's Python environment | Selection rate and demographic parity difference computed live on a small tabular set |
| **NVIDIA garak** | trainer's Python environment | An LLM vulnerability scan run against a model, and the report artefact it produces |

**These five are trainer-led demonstrations, not participant labs.**

### What a participant must have installed

- A laptop with a current browser — Chrome, Edge, Firefox or Safari — and a working
  microphone. A camera is welcome, not required.
- **Microsoft Teams**, desktop client or browser. Every session runs there.
- A document editor they can produce and share files from: Microsoft Word, Google Docs
  or equivalent. The pack is written in documents.
- A PDF reader and a downloaded copy of the **IAPP AIGP Body of Knowledge and Exam
  Blueprint v2.1**, which the IAPP publishes free.
- **Nothing else.** No Python, no API key, no GPU, no account with any AI vendor.

### What the trainer must have installed

- A current Python 3.x (3.12 or newer) in a throwaway virtual environment, with
  **Fairlearn** and **NVIDIA garak** installed and the exact release of each pinned and
  printed on the demonstration output, so the number the room saw is reproducible.
- A small synthetic tabular dataset for the Fairlearn demonstration — synthetic, never
  real candidate data.
- A model endpoint garak can reach, and network access from the teaching machine. Both
  demonstrations have a recorded fallback in case the venue network blocks them.

---

## 5. The end state

When the last use case is done, `015_project/` and the use-case folders together hold a
complete Kabini AI Governance Pack. Somebody could open it and check every one of
these without taking anyone's word for it:

1. **The register** lists all four systems, and for each one gives its classification
   (classic / generative / agentic, model versus system), its business owner by name,
   its risk tier, and the developer / provider / deployer / user roles assigned **per
   activity** rather than per company — with at least one system where Kabini is two
   different roles in two different rows.
2. **MatchScore has a completed AI system impact assessment** in a format that maps to
   ISO/IEC 42005, showing on its face where a DPIA and a fundamental rights impact
   assessment attach to the same facts.
3. **MatchScore has a risk register** built with a probability/severity matrix and a
   mitigation hierarchy, with every high-severity row carrying a named mitigation and an
   owner.
4. **MatchScore has a data governance dossier**: a lawful-rights assessment for the
   placement warehouse, written quality and fit-for-purpose criteria, and a lineage and
   provenance record that names each dataset's origin.
5. **MatchScore has a test plan and a results summary** across validation, performance,
   security, bias and interpretability, with **one fairness metric named and a numeric
   threshold written down** — and the room watched that metric being computed.
6. **MatchScore has a model card and a signed release-readiness checklist**, with the
   conformity documentation and the instructions for use that go with them.
7. **There is a monitoring and retraining schedule and an audit and red-team calendar**,
   each row carrying an owner and a cadence, and a post-market monitoring plan.
8. **There is an incident runbook and one worked incident record** produced from the
   tabletop, stating cause in the Body of Knowledge's own vocabulary — brittleness, lack
   of robustness, poor data quality, insufficient testing, model or data drift.
9. **The Halcyon AI foundation-model agreement carries a redline with a stated reason
   beside every change**, covering training on customer data, IP indemnity,
   model-change notification, audit rights, and exit and portability.
10. **Cadence has a deployment control set**: documented secondary-use limits, a
    downstream-harm forecast, an external communication plan, and a written deactivation
    and localisation procedure with a named owner and a test date.
11. **The regulatory applicability memo states, system by system, which EU, Korean and
    US obligations apply and from which date**, and says plainly where a date is
    corroborated rather than read from the Official Journal.
12. **The standards map** places ISO/IEC 42001 clauses, the four NIST AI RMF functions
    and the OECD principles against the artefacts above, so an auditor can find things.
13. **The programme file** holds the charter, the RACI, the forum terms of reference, a
    training and awareness plan sized for eleven thousand people, the AI lifecycle
    policy covering all nine stages, the gap-marked redline of the four existing
    policies, the acceptable use policy and the third-party AI assessment questionnaire.
14. **Every document in the pack carries a version, a date and a named owner**, and no
    two documents contradict each other about a fact.

And each participant has sat a full-length hundred-question mock under exam conditions
and holds a per-sub-domain breakdown of the result against the v2.1 blueprint weighting.

---

## 6. What is deliberately out of scope

- **Building, training or fine-tuning any model, and any programming by participants.**
  The AIGP is a governance credential. There is no mathematics on the exam and no code.
  Two tools are run on screen by the trainer so that "metric and threshold evaluation"
  and "red teaming" are things the room has watched rather than phrases it has read.
  Leaving out model development costs no coverage, because the blueprint's verbs are
  *perform, review, create, implement, document, establish* — not *train*.
- **Real personal data of any kind.** MatchScore's demonstration data is synthetic. A
  course that handles real CVs to teach data governance has failed the first lesson it
  teaches.
- **A real conformity assessment, and a real ISO/IEC 42001 certification audit.**
  Neither can be honestly simulated: no notified body is operating in the Annex III
  high-risk flow, whose deadline is now 2 December 2027, and a certification audit needs
  an accredited certification body. The pack contains the documentation a conformity
  assessment would consume, which is the part the blueprint actually asks for.
- **Legal advice.** The course teaches the architecture of AI obligations against a
  fictional company. Nothing in the pack is advice on a participant's own organisation,
  and the applicability memo says so on its cover.
- **A jurisdiction-by-jurisdiction world survey.** Three jurisdictions are worked
  properly — the EU, South Korea and the United States — because those are the three the
  Body of Knowledge's Domain II scope note names. Others appear only where they
  illustrate the same pattern. Teaching a fourth would teach the same method twice.
- **India as a fourth worked jurisdiction.** India appears as the country the placement
  data reaches and the country the developers sit in — a Chapter V transfer question and
  a data-residency question, both of which belong to modules the course already teaches.
  Working the DPDP Act as a regime in its own right would teach the same method a fourth
  time and cost hours the blueprint has other uses for.
- **Commercial AI governance platforms.** The market churns fast and vendor demos date
  badly. The pack is built in a document editor, which is what the participants' own
  organisations will actually have.
- **NIST ARIA and ISO/IEC 42006.** ARIA was removed as a performance indicator in v2.1;
  42006 sets requirements for the bodies that certify AI management systems and is not
  in the Body of Knowledge. 42006 is named exactly once, to clear up its confusion with
  42005.
- **The IAPP exam voucher, IAPP membership and official IAPP courseware.** This is
  independent preparation and does not present itself otherwise.
- **A published pass rate, an exam-pass guarantee, and any salary, placement or
  employment claim.** The IAPP publishes no AIGP pass rate and neither do we.
- **A live negotiation with a real vendor.** The Halcyon AI agreement is fictional and
  redlined against a stated commercial position. What cannot be simulated is the other
  side's behaviour, and the course says so rather than pretending a role-play is a
  negotiation.

---

## 7. Schedule

| | |
|---|---|
| Sessions | 16 |
| Length of a session | 2 hours of live time |
| Total live hours | 32.0 |
| Delivery | Live online on Microsoft Teams, trainer-led, every session recorded |
| Schedule timezone | India Standard Time (IST) |
| Weekday and clock time | **To be announced** |
| Start date | **To be announced** |

The weekday, the clock time and the start date are not recorded yet. They are settled
with the cohort once it forms. **No local-time table is published here**, because with
no clock time recorded there is nothing to convert; one will be published together with
the schedule, and it will state the local weekday as well as the local hour.

**Use cases are not allocated to sessions.** The calendar is the sixteen sessions; the
syllabus is the use cases in `use_case_plan.md`. The trainer covers as much as the room
takes in a sitting and carries the rest forward.
