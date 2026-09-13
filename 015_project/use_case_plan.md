# Use case plan — AIGP Certification Training

*The backlog that builds the Kabini AI Governance Pack. Read
`015_project/project.md` first; it is the fixed description of the client, the system
and the stack.*

*Written 2026-09-07 against `010_brochure/brochure.md` (the scope), the eleven modules
of its coverage map, `005_research/2026-09-07/` and `006_competitors/2026-09-07/`.*

**This plan does not allocate use cases to sessions.** The calendar is sixteen sittings
of two hours; the syllabus is the thirty use cases below, in order. The trainer covers
as much as the room takes and carries the rest forward.

---

## 1. The arc

The project moves through six movements, and the order is the brochure's deliberate
sequencing rather than the conventional one.

**It starts with a stock-take, not a lecture.** Use cases 1 and 2 walk into a company
with four AI systems and no inventory and produce the register the whole pack hangs
off — because the fastest way to teach the difference between a *model* and a *system*
is to make somebody write down which one they have four of. **Then the programme
(3–7):** roles assigned activity by activity, a charter, a training plan, the lifecycle
policy, the gaps in the policies Kabini already owns, and the questionnaire
procurement should have sent Attestra. **Then a single short cross-cutting piece (8):**
the five impact assessments set side by side once, so the four later use cases that
need one apply it instead of re-teaching it. **Then the build (9–16),** carried end to
end on one system — MatchScore — from "what is this for" through data governance,
testing with a real number on screen, the model card, the release decision, monitoring
and one incident that actually happened. **Then deployment (17–22),** carried on the
three systems MatchScore cannot teach: a licensed model, a bought biometric service and
an agent that acts without a human. **Then the law (23–28), after the lifecycle and not
before it,** so that every obligation lands on an artefact the room has already built:
by the time the risk tier arrives, the technical documentation it demands is sitting in
the pack with a date on it. **Then the standards (29)** as a map over work already done,
and **the handover (30)** — the pack reviewed against its checklist, the scenario
technique drilled, and a full mock under exam conditions.

Use case 11 comes after use case 10 because you cannot rate a risk you have not yet
identified in an impact assessment. Use case 19 comes after use case 7 because the
questionnaire tells you what to redline. Use case 26 comes after use case 14 because
"technical documentation" is a phrase, until the room has one.

The two things this market does not do are the two things this backlog is built out of:
**participants leave holding artefacts they produced**, and **the post-deployment
sub-domains — the heaviest on the exam and the dullest to teach — get six use cases, not
a closing slide.**

---

## 2. The use cases

| # | Use case | Status | Form | Delivers | Teaches | Est. min |
|---|---|---|---|---|---|---|
| 1 | Take stock: what these four systems actually are | Planned | Document | An AI system inventory and use-case register with a row for MatchScore, Nora, the right-to-work check and Cadence, each classified as classic, generative or agentic, each described as a *system* rather than a model, and each naming whether it is used as-is, fine-tuned, retrieval-augmented or agentic | **M1** Foundations — generally accepted definitions and types of AI; classic vs generative vs agentic; model vs system; training vs inference; fine-tuning vs RAG vs agentic; ISO/IEC 22989 vocabulary | 60 |
| 2 | Name the harm, and hold each system to the principles | Planned | Document | A risk-and-harm profile appended to the register: for each system, the harms it can do to individuals, groups, organisations and society, the characteristics that make it need governing, and what each responsible-AI principle demands of it in one line | **M1** Foundations — risk and harm types (misalignment, ethics and bias, complexity and scalability); characteristics requiring governance (complexity, opacity, autonomy, speed and scale, harm/misuse potential, data dependency, probabilistic vs deterministic); responsible-AI principles | 50 |
| 3 | Who is the developer and who is the provider, activity by activity | Planned | Document | A role assignment appended to the register in which developer, provider, deployer and user are assigned **per activity**, and Kabini is shown as two different roles in two different rows of the same system — including MatchScore, where the developer sits in Bengaluru and the provider is established in Amsterdam | **M2** The programme — developer / provider / deployer / user as task labels | 55 |
| 4 | A charter the board can sign, and a plan to teach eleven thousand people | Planned | Document | An AI governance charter — named roles, a RACI, terms of reference for a cross-functional forum with its membership justified — plus a training and awareness plan sized for eleven thousand staff, with the programme design explicitly reasoned from Kabini's size, maturity, industry, objectives and risk tolerance | **M2** The programme — roles and responsibilities for governance stakeholders; cross-functional collaboration for efficacy and diversity of expertise; training and awareness programme on terminology, strategy and governance; differentiating governance by size, maturity, industry, products, objectives, risk tolerance | 50 |
| 5 | One policy for the whole AI lifecycle | Planned | Document | An AI lifecycle policy covering all nine stages the Body of Knowledge names, each stage with a stated control, an owner and a decision gate | **M2** The programme — policies for oversight and accountability across all nine named lifecycle stages | 50 |
| 6 | Mark the gaps in the policies Kabini already has | Planned | Document | A gap-marked redline of Kabini's existing privacy, security, data governance and intellectual property policies, each marked change carrying the AI-specific reason it is needed, plus an acceptable use policy for staff use of AI | **M2** The programme — evaluating and updating existing privacy, security, data governance and **intellectual property** policies; acceptable use | 45 |
| 7 | Ask Attestra the questions procurement never asked | Planned | Document | A third-party AI assessment questionnaire fit to send to a vendor, with the contract clauses each answer must be backed by, and a completed first pass against Attestra's biometric right-to-work service | **M2** The programme — third-party risk policies, assessments and contracts across procurement, supply chain, HR and acceptable use | 45 |
| 8 | One grid for five impact assessments | Planned | Document | A single comparison grid setting the GDPR DPIA, the EU AI Act FRIA, the ISO/IEC 42005 AI system impact assessment, the US-state algorithmic impact assessment and Korea's fundamental-rights assessment against each other on trigger, scope, who performs them, what they produce and whether they are published — with each of Kabini's four systems placed against the grid | **M3** Impact assessment family — DPIA vs FRIA vs ISO/IEC 42005 vs algorithmic impact assessment vs Korea's fundamental-rights assessment, by trigger, scope, performer, output and publication | 50 |
| 9 | Write down what MatchScore is for, and how it was built | Planned | Document | A design and build control record for MatchScore: business context and use case, purpose, requirements gathering, architecture and model selection, human oversight design, data analysis, the metric and threshold to be evaluated, the stakeholder engagement and feedback route, and the operational controls — documented so it establishes compliance rather than merely recording activity | **M4** Design and build — define business context and use case; apply policies, procedures, best practice and ethics to design and build; document the design and build process | 45 |
| 10 | Run the impact assessment on MatchScore | Planned | Document | A completed AI system impact assessment on MatchScore in a format that maps to ISO/IEC 42005, showing on its face the points where a DPIA and a fundamental rights impact assessment attach to the same facts | **M4** Design and build — perform or review an impact assessment; **M3** applied | 45 |
| 11 | Put MatchScore's risks in a register with a matrix behind them | Planned | Document | A risk register for MatchScore built with a probability/severity harms matrix and a mitigation hierarchy, with stakeholder mapping, use-case evaluation and benchmarking behind the ratings, and a pre-deployment pilot and testing plan for the residual risks | **M4** Design and build — identify and manage internal and external risks and contributing factors (probability/severity harms matrix, risk mitigation hierarchy, stakeholder mapping, use-case evaluation, benchmarking, pre-deployment pilots and testing) | 45 |
| 12 | Prove Kabini may use the data it trained on | Planned | Document | A data governance dossier for the placement warehouse: a documented lawful-rights assessment for collecting and using the data at all, written criteria for quality, quantity, integrity and fitness for purpose with the assessment against them, and a lineage and provenance record naming each dataset's origin, what happened to it, who can attest to that, and **every place a copy of it now sits** — which is how the undocumented Bengaluru replica turns from an engineering convenience into a recorded transfer | **M5** Data governance — assess and document lawful rights to collect and use data; data quality, quantity, integrity and fit-for-purpose; data lineage and provenance | 65 |
| 13 | Test MatchScore, and write the number down | Planned | Both | A test plan and results summary spanning unit, integration, validation, performance, security, bias and interpretability testing, with **one fairness metric named and a numeric threshold written down**, an issues-and-risks log from testing, and the documentation that validates the results — produced after the room has watched selection rate and demographic parity difference computed live in Fairlearn on a synthetic set | **M5** Data governance — plan and perform training and testing (unit, integration, validation, performance, security, bias, interpretability); identify and manage issues and risks during training and testing; document the training and testing process; live fairness-metric demonstration | 70 |
| 14 | Decide whether MatchScore is fit to release | Planned | Document | A model card for MatchScore — intended use, out-of-scope uses, training data provenance, evaluation metrics and thresholds, limitations, human oversight, contact — plus a signed release-readiness checklist, the conformity and technical documentation that accompanies it, and the instructions for use handed to a deployer, all critiqued first against real public model cards | **M6** Release and monitoring — assess readiness and prepare for release; model card; conformity requirements; public disclosures — technical documentation and instructions for use to deployers | 55 |
| 15 | Watch it after release: monitoring, audits and a red team | Planned | Both | A monitoring and retraining schedule and an audit and red-team calendar, every row carrying an owner and a cadence, plus a post-market monitoring plan — written after the room has watched an LLM vulnerability scan run in NVIDIA garak and read the report artefact it produced | **M6** Release and monitoring — continuous monitoring and the maintenance/update/retraining schedule; periodic assessment via audits, red teaming, threat modelling and security testing; post-market monitoring plans; live LLM vulnerability-scan demonstration | 50 |
| 16 | The Tuesday the approval rate dropped | Planned | Document | An AI incident runbook — detect, triage, accountable owner, document, disclose or not, deactivate or not — and one worked incident record produced live from a tabletop, stating cause in the Body of Knowledge's own vocabulary | **M6** Release and monitoring — manage and document incidents, issues and risks; cross-functional root-cause work (brittleness, lack of robustness, poor data quality, insufficient testing, model and data drift) | 45 |
| 17 | Decide how Nora and Cadence should be built at all | Planned | Document | A deploy-decision record for Nora and for Cadence: the use-case context (business objectives, performance requirements, data availability, ethical considerations, workforce readiness), the model-type choice reasoned across classic vs generative, proprietary vs open source, small vs large and language vs multimodal, and the deployment option chosen across cloud vs on-premise vs edge and as-is vs fine-tuning vs RAG vs agentic architecture | **M7** Deploy decision and assessment — use-case context; model type differences; deployment options including **agentic architectures** | 70 |
| 18 | Assess a system Kabini did not build | Planned | Document | A review of the impact assessment on Attestra's biometric right-to-work check, done from the outside using the questionnaire responses, with the gaps Kabini cannot close listed as accepted risks — plus a written statement of the risks and opportunities that attach to Kabini deploying its **own** proprietary model instead | **M7** Deploy decision and assessment — perform or review an impact assessment on the selected system; risks and opportunities unique to deploying one's own proprietary model (increased obligations, higher liability) | 50 |
| 19 | Redline the Halcyon AI agreement | Planned | Document | A redlined extract of the Halcyon AI foundation-model agreement with the reason written beside each change, covering training on customer data, indemnity for IP claims, model-change notification, audit rights, and exit and portability | **M7** Deploy decision and assessment — identify and evaluate key terms and risks in the **vendor or licensing** agreement | 65 |
| 20 | Put controls around an agent that books interviews | Planned | Document | A deployment control set for Cadence covering deployer-side data governance, risk management, issue management and user training, plus the deployer's own monitoring and retraining schedule, audit, red-team, threat-modelling and security-testing cadence, and the incident and post-market monitoring documentation written from the deployer's seat rather than the developer's | **M8** Deployment and use — apply policies, procedures, best practice and ethics to deployment; deployer-side continuous monitoring and retraining schedule; periodic audits, red teaming, threat modelling, security testing; document incidents, issues, risks and post-market monitoring plans | 65 |
| 21 | Forecast what Cadence will be used for that nobody intended | Planned | Document | A secondary and unintended use and downstream harm forecast for Cadence, with a mitigation against each forecast use, and an external communication plan written before it is needed — naming who speaks, to whom, within what time, and with what holding statement | **M8** Deployment and use — forecast and reduce secondary or unintended uses and downstream harms; establish external communication plans | 55 |
| 22 | Write the kill switch down, and give it an owner | Planned | Document | A deactivation and localisation policy and procedure for Cadence: the triggers that fire it, the named person who can pull it, the steps in order, what happens to work in flight, how a partial localisation differs from a full stop, and the date the procedure was last tested | **M8** Deployment and use — create and implement policy and controls to deactivate or localise a system | 55 |
| 23 | Apply privacy law to all four systems | Planned | Document | The privacy section of the regulatory applicability memo: for each system, how transparency, choice, lawful basis and purpose limitation are satisfied, how data minimisation and privacy by design were applied to a method built on data volume, and what the special-category and biometric rules demand of the right-to-work check | **M9** Existing law — transparency, choice, lawful basis, purpose limitation; data minimisation and privacy by design; sensitive and special category data including biometrics | 55 |
| 24 | Discharge the controller obligations | Planned | Document | The controller-obligations section of the memo: privacy impact assessments, use of third-party processors, cross-border transfers — to Attestra, to Halcyon AI, and the intra-group copy of the placement warehouse in `ap-south-1`, each with its Chapter V mechanism and a transfer impact assessment naming the receiving country's law — data subject rights against a scoring model, automated decision making, incident management, breach notification and record keeping — each pointing at the pack artefact that evidences it | **M9** Existing law — controller obligations (privacy impact assessments, third-party processors, cross-border transfers, data subject rights, automated decision making, incident management, breach notification, record keeping) | 55 |
| 25 | IP, discrimination, consumer protection and product liability | Planned | Document | The existing-law section of the memo beyond privacy: where intellectual property law prohibits or limits Kabini's use of data for training, how non-discrimination law reaches MatchScore in employment and its analogues in credit, lending, housing and insurance, where consumer protection law's prohibition of unfair and deceptive acts bites on Nora, and how product liability law treats a design or manufacturing defect in an AI system | **M9** Existing law — intellectual property law including limits on training data; non-discrimination law in employment, credit, lending, housing, insurance; consumer protection and unfair or deceptive acts; product liability and design/manufacturing defects | 55 |
| 26 | Classify the four systems, and read off what follows | Planned | Document | A risk classification for each of the four systems and each of their *uses*, and the obligations that follow it: risk management, data governance, technical documentation, conformity and impact assessments, record keeping, human oversight, transparency and notification, quality management — plus the distinct general-purpose AI requirements that reach Halcyon AI, the enforcement framework and penalties, and how Kabini's duties differ where it is provider, deployer, importer or distributor | **M10** AI-specific law — risk classification framework and what systems **and uses** fall into each category; requirements around risk management, data governance, technical documentation, conformity and impact assessments, record keeping; human oversight, transparency and notification, quality management; distinct GPAI requirements; enforcement framework and penalties; differences by organisational context | 60 |
| 27 | The EU position, with dates on it | Planned | Both | The EU section of the applicability memo, stating for each system which EU AI Act obligation applies and from which date under the Act as amended by Regulation (EU) 2026/1744, what the GPAI Code of Practice does and does not buy Halcyon AI, and what Article 50 already requires of Nora — written after the room has inspected real transparency disclosure and content credentials live in the browser, and carrying the date it was compiled on its face | **M10** AI-specific law — EU AI Act with the Regulation (EU) 2026/1744 timeline; GPAI Code of Practice; Article 50 transparency and content marking | 60 |
| 28 | Korea and the United States | Planned | Document | The Korean and US sections of the applicability memo, completing it: Korea's AI Basic Act duties, whether each system is "high-impact AI" and what the fundamental-rights assessment and the grace period mean for Vikram Nair's client; and the US position taught as a pattern — the federal executive orders and preemption pressure, and Colorado SB 26-189 as the worked state example, with its notice, disclosure and impact-assessment duties applied to MatchScore | **M10** AI-specific law — South Korea AI Basic Act and high-impact AI; US federal EOs and preemption pressure; Colorado SB 26-189 as the state pattern; recognising a stale published timeline | 55 |
| 29 | A standards map an auditor can navigate | Planned | Document | A standards map placing ISO/IEC 42001 clauses, the four NIST AI RMF 1.0 functions and the OECD principles against the pack artefacts that satisfy each, so an auditor can find things — written after a live walk through one AI RMF Playbook subcategory in the browser, and carrying the three corrections in writing | **M11** Standards — OECD principles, framework, policies and recommended practices; NIST AI RMF 1.0 core functions Govern/Map/Measure/Manage, categories and subcategories, and the Playbook; NIST AI 600-1 Generative AI Profile; ISO/IEC 22989, 42001 and 42005; corrections — no AI RMF 2.0, NIST ARIA removed, ISO/IEC 42006 is certification-body requirements | 70 |
| 30 | Hand the pack over, and sit the exam you are about to sit | Planned | Document | The completed Kabini AI Governance Pack, reviewed row by row against the published artefact checklist for presence, completeness and internal consistency, with the index and every version, date and owner filled in — and each participant's full-length hundred-question mock sat under exam conditions with a per-sub-domain breakdown against the v2.1 weighting | **Consolidation** — blueprint structure and weighting; Bloom levels the exam targets; scenario technique by sequence, ownership and proportionality; exam mechanics; full-length mock under exam conditions; correction of the retired seven-domain structure | 105 |

---

## 3. The use cases in detail

### 1 — Take stock: what these four systems actually are

**Objective.** Turn Kabini's four undocumented AI systems into a register that says
what each one *is*, in the vocabulary the exam and the regulator both use.

**Before.** Meera Krishnamurthy knows there are "some AI things". Nobody can list them.
**After.** The register exists: four rows, each naming the system, its business owner,
what it does, whether it is classic, generative or agentic, and whether the model is
used as-is, fine-tuned, wrapped in retrieval augmentation, or acting agentically.

**Demonstrated live.** The trainer builds row one on screen and gets it wrong on
purpose — describing MatchScore as a model — then repairs it into a system description
that names the data, the interfaces, the human oversight and the deployment context.
The room fills the other three rows and argues about Cadence.

**By the end, a participant can** describe any AI system in their own organisation as a
system rather than a model, and classify it as classic, generative or agentic without
guessing.

### 2 — Name the harm, and hold each system to the principles

**Objective.** Attach to each register row the harms it can do and what responsible AI
demands of it.

**Before.** The register says what the systems are. **After.** It also says who they can
hurt and how, which characteristics of each one force governance, and what fairness,
safety and reliability, privacy and security, transparency and explainability,
accountability and human-centricity each require of it in one concrete line.

**Demonstrated live.** A four-way split: each half of the room takes two systems and
names harms to individuals, groups, organisations and society. The trainer then draws
out the characteristic behind each harm — opacity behind the appeal a candidate cannot
make, speed and scale behind an error repeated forty thousand times.

**By the end, a participant can** state, for a system in front of them, which of the
governance-forcing characteristics it has, and turn a principle into a demand rather
than a slogan.

### 3 — Who is the developer and who is the provider, activity by activity

**Objective.** Break the habit of classifying an *organisation* into one role, by making
the room classify *activities*.

**Before.** The register describes systems. **After.** Every activity in every system
carries developer, provider, deployer or user against Kabini or a third party — and
Nora shows Kabini as deployer in one row and provider in the next, the moment it
fine-tunes and rebrands.

**Demonstrated live.** The provider-or-deployer drill: a scenario in which one company
procures a foundation model, fine-tunes it, rebrands it and sells it on. The room votes
per paragraph; the trainer holds the disagreement open rather than resolving it early,
because the disagreement *is* the lesson.

**By the end, a participant can** assign the four roles per activity in a scenario where
one organisation fills several, which is the single most reliable trap in the exam's
case studies.

### 4 — A charter the board can sign, and a plan to teach eleven thousand people

**Objective.** Turn the roles into a standing structure with named people and a
teachable programme.

**Before.** Roles exist on paper against activities. **After.** There is a charter with a
RACI, a cross-functional forum with terms of reference and a justified membership, and a
training and awareness plan tiered across eleven thousand staff — a different programme
for recruiters, for Arjun Sundaram's engineers and for the board.

**Demonstrated live.** The trainer builds the RACI and then asks the room to break it:
what happens when the accountable person is on leave, and what happens if legal is
merely consulted on a deploy decision. The differentiation argument is run explicitly —
the same charter is shown failing in a two-hundred-person firm.

**By the end, a participant can** stand up a governance forum and size a training
programme against an organisation's actual size, maturity, industry and risk tolerance.

### 5 — One policy for the whole AI lifecycle

**Objective.** Write the policy that governs every stage the Body of Knowledge names,
once, with gates rather than aspirations.

**Before.** Kabini has structure and no rules. **After.** An AI lifecycle policy
covering use case assessment, risk management, ethics by design, data acquisition and
use, model and system development, training and testing, deployment and monitoring,
documentation and reporting, and incident management — each with a control, an owner and
a gate that can be failed.

**Demonstrated live.** The trainer drafts two stages fully and shows the difference
between a stage that can stop a release and one that cannot. The room drafts the rest
against Cadence, which is already in pilot without having passed a single gate.

**By the end, a participant can** write a lifecycle policy that an auditor can test,
rather than one that describes intentions.

### 6 — Mark the gaps in the policies Kabini already has

**Objective.** Update what exists instead of writing a parallel universe of AI documents.

**Before.** Four pre-AI policies and one new AI policy that ignore each other.
**After.** The privacy, security, data governance and intellectual property policies each
carry marked changes with the AI-specific reason beside them, and an acceptable use
policy tells eleven thousand staff what they may and may not put into a chatbot.

**Demonstrated live.** The policy gap review: the trainer reads a real-sounding
pre-AI security policy clause aloud and the room finds what breaks when the asset is a
model. Intellectual property gets its own pass, because v2.1 added it and most existing
policy sets have nothing on training data.

**By the end, a participant can** take their own organisation's existing policy set and
mark, clause by clause, what AI changes.

### 7 — Ask Attestra the questions procurement never asked

**Objective.** Give procurement a third-party AI assessment it can actually send, and use
it on a live vendor.

**Before.** Deepa Sridharan buys AI services on the standard IT template.
**After.** A third-party AI assessment questionnaire exists, each question tied to the
contract clause that must back the answer, and a first pass against Attestra is complete
with the unanswerable questions flagged.

**Demonstrated live.** The trainer answers three questions as Attestra's sales engineer
would — plausibly, and without committing to anything — and the room rewrites the
questions until the evasion stops working.

**By the end, a participant can** build a third-party AI assessment covering procurement,
supply chain, HR and acceptable use, and tell an answer from a non-answer.

### 8 — One grid for five impact assessments

**Objective.** Separate five artefacts that learners reliably conflate, once, before
anything needs one.

**Before.** "Impact assessment" means five things at once. **After.** A grid sets the
GDPR DPIA, the EU AI Act FRIA, the ISO/IEC 42005 AI system impact assessment, the
US-state algorithmic impact assessment and Korea's fundamental-rights assessment against
each other on trigger, scope, performer, output and publication — with Kabini's four
systems placed against it.

**Demonstrated live.** The room fills the grid cold, then the trainer corrects it. The
correction is the teaching. This module is short on purpose and every later use case
that needs an impact assessment refers back to it rather than re-explaining.

**By the end, a participant can** say which assessment a given fact pattern triggers, who
performs it, and whether anyone outside the company will ever see it.

### 9 — Write down what MatchScore is for, and how it was built

**Objective.** Do the step that is skipped most often, and that every later control
depends on: state the business context and the use case.

**Before.** MatchScore is in production and nobody has written down its purpose.
**After.** A design and build control record exists: purpose, requirements gathering,
architecture and model selection, human oversight design, data analysis, the metric and
threshold to be evaluated, the stakeholder engagement route, and the operational
controls — documented in a way that establishes compliance rather than logging activity.

**Demonstrated live.** The trainer asks Kavitha Rajagopal's question — "what is this
model *for*?" — and shows three answers that sound the same and imply different
controls: rank candidates, filter candidates, and reject candidates.

**By the end, a participant can** define a business context and use case tightly enough
that a control can be tested against it.

### 10 — Run the impact assessment on MatchScore

**Objective.** Perform, not describe, an AI system impact assessment.

**Before.** MatchScore's purpose and controls are documented. **After.** A completed
assessment in an ISO/IEC 42005-shaped format, showing where a DPIA and a fundamental
rights impact assessment attach to the same facts rather than duplicating them.

**Demonstrated live.** The trainer completes two sections live and deliberately writes a
weak mitigation, then asks the room whether the residual risk statement is now false.

**By the end, a participant can** perform or review an AI system impact assessment and
show a reviewer which parts of it also discharge a DPIA or a FRIA.

### 11 — Put MatchScore's risks in a register with a matrix behind them

**Objective.** Rate risks with a method, not a feeling, and mitigate them in order.

**Before.** Risks are named inside the impact assessment. **After.** A risk register
exists with probability and severity rated against a published matrix, a mitigation
hierarchy applied in order rather than jumping to the cheapest control, stakeholder
mapping and benchmarking behind the ratings, and a pre-deployment pilot defined for what
is left.

**Demonstrated live.** Two participants rate the same risk differently and the trainer
does not adjudicate — the room writes the matrix definition that would have made them
agree. Internal and external risks and their contributing factors are separated
explicitly.

**By the end, a participant can** build a risk register with a defensible matrix and
apply a mitigation hierarchy rather than a preference.

### 12 — Prove Kabini may use the data it trained on

**Objective.** Answer the question nobody at Kabini has asked about eight years of
placement history: were we ever allowed to use this?

**Before.** The placement warehouse is a training set of unknown origin. **After.** A
data governance dossier holds a documented lawful-rights assessment, written quality,
quantity, integrity and fit-for-purpose criteria with the assessment against them, and a
lineage and provenance record naming where each dataset came from, what happened to it,
and who can attest to that.

**Demonstrated live.** The trainer traces one dataset backwards until the trail goes
cold, and the room decides what to do with data whose provenance cannot be established —
which is the decision most organisations avoid making explicitly.

**By the end, a participant can** establish data governance for a training set: lawful
rights, quality, integrity, fitness for purpose, lineage and provenance.

### 13 — Test MatchScore, and write the number down

**Objective.** Turn "metric and threshold evaluation" from an abstraction into a number
with a decision attached.

**Before.** MatchScore's data is governed and untested. **After.** A test plan and results
summary spans unit, integration, validation, performance, security, bias and
interpretability testing; **one fairness metric is named and a numeric threshold is
written down**; issues and risks found in testing are logged with owners; and the whole
process is documented to validate results.

**Demonstrated live.** The trainer runs **Fairlearn** on a small synthetic tabular set and
computes selection rate and demographic parity difference across a group, on screen, with
the library release printed on the output. Then the harder question: the room chooses the
threshold, and has to say who signs off when the number misses it. A recorded fallback
exists if the venue network blocks the demonstration.

**By the end, a participant can** plan and document testing across all seven regimes and
defend a named metric with a written threshold.

### 14 — Decide whether MatchScore is fit to release

**Objective.** Produce the artefact a board will ask for in week one — a model card — and
make the release decision it supports.

**Before.** MatchScore is tested and undocumented for release. **After.** A model card
covers intended use, out-of-scope uses, training data provenance, evaluation metrics and
thresholds, limitations, human oversight and contact; a release-readiness checklist is
signed; the conformity and technical documentation is assembled; and the instructions for
use that a deployer would receive are written.

**Demonstrated live.** Public model cards from Hugging Face and Google are opened and
critiqued against the checklist before the room writes MatchScore's — including one that
looks complete and says nothing about out-of-scope use.

**By the end, a participant can** produce a model card and a release-readiness decision,
and say what conformity documentation asks them to *do*.

### 15 — Watch it after release: monitoring, audits and a red team

**Objective.** Build the schedule that turns "we monitor it" into rows with owners and
dates.

**Before.** MatchScore is released with no post-release regime. **After.** A monitoring
and retraining schedule, an audit and red-team calendar with cadence and owner per row,
and a post-market monitoring plan.

**Demonstrated live.** The trainer runs an **NVIDIA garak** vulnerability scan against a
model endpoint and opens the report, with the tool release pinned and printed. The room
then decides what in that report would go into a calendar, at what cadence, and who would
read it — which is the difference between running a scan and having a programme. A
recorded fallback exists if the network blocks it.

**By the end, a participant can** set a monitoring, audit and red-team regime with named
owners and defensible cadences, and say what threat modelling and security testing add
that monitoring does not.

### 16 — The Tuesday the approval rate dropped

**Objective.** Run an incident, not read about one.

**Before.** Monitoring exists and there is no incident process. **After.** An incident
runbook exists — detect, triage, accountable owner, document, disclose or not, deactivate
or not — and one worked incident record is in the pack, stating cause in the Body of
Knowledge's own vocabulary.

**Demonstrated live.** The tabletop: MatchScore's approval rate for one group dropped
forty per cent after last month's retrain. The room works it in real time. The trainer
pushes on the causal vocabulary — brittleness, lack of robustness, poor data quality,
insufficient testing, model drift, data drift — until the record says which, and why.

**By the end, a participant can** run and document an AI incident, and explain it
cross-functionally in causal terms rather than as "the model broke".

### 17 — Decide how Nora and Cadence should be built at all

**Objective.** Make the deploy decision the way the blueprint asks — context first,
model type second, deployment option third.

**Before.** Nora and Cadence exist because somebody chose a vendor. **After.** A
deploy-decision record reasons the use-case context (business objectives, performance
requirements, data availability, ethical considerations, workforce readiness), then the
model type across classic vs generative, proprietary vs open source, small vs large and
language vs multimodal, then the deployment option across cloud, on-premise and edge, and
across as-is, fine-tuning, retrieval-augmented generation and **agentic architecture**.

**Demonstrated live.** The same requirement is run to two different answers by changing
one line of context — data residency for the Korean client — so the room sees that the
decision is downstream of the context, not the technology.

**By the end, a participant can** evaluate a deploy decision across context, model type
and deployment option, including agentic architectures, and say what each choice costs in
governance.

### 18 — Assess a system Kabini did not build

**Objective.** Assess from the outside, where you cannot inspect the model and cannot
choose to.

**Before.** Attestra's questionnaire responses sit in the pack unassessed. **After.** A
review of the impact assessment on the biometric right-to-work check, with the gaps
Kabini cannot close recorded as accepted risks and escalated — plus a written
statement of the risks and opportunities that attach to Kabini running its **own**
proprietary model instead: more obligations, higher potential liability, and nobody else
to point at.

**Demonstrated live.** The trainer applies the impact-assessment grid from use case 8 to a
system with three unknowable sections, and shows the difference between "not assessed" and
"assessed and unknown".

**By the end, a participant can** review an impact assessment on a bought system and state
the residual risk honestly.

### 19 — Redline the Halcyon AI agreement

**Objective.** Find the money and the risk in a contract, clause by clause.

**Before.** Deepa Sridharan signed a foundation-model agreement without legal review.
**After.** A redlined extract sits in the pack with the reason written beside every
change, covering training on customer data, indemnity for IP claims, model-change
notification, audit rights, and exit and portability.

**Demonstrated live.** Two paragraphs are read aloud in their original form and the room
finds nothing wrong with them. The trainer then reads the same paragraphs with one
scenario attached — Halcyon AI changes the model under Nora without notice, two weeks
before an audit — and the room redlines them properly.

**By the end, a participant can** identify and redline the key terms and risks in an AI
vendor or licensing agreement, and justify each change commercially as well as legally.

### 20 — Put controls around an agent that books interviews

**Objective.** Govern from the deployer's seat, which is where most of this room will
actually sit.

**Before.** Cadence is a pilot with no controls. **After.** A deployment control set
covers deployer-side data governance, risk management, issue management and user
training, with the deployer's own monitoring and retraining schedule, its own audit,
red-team, threat-modelling and security-testing cadence, and its own incident and
post-market monitoring documentation.

**Demonstrated live.** The trainer puts the developer-side artefacts from use cases 14 and
15 side by side with the deployer-side ones and asks what changes — the answer is the
evidence available, not the obligation. This is the heaviest sub-domain on the exam and it
is taught as application, not repetition.

**By the end, a participant can** govern a system they did not build, using only what a
deployer can actually see.

### 21 — Forecast what Cadence will be used for that nobody intended

**Objective.** Think about the use nobody designed for, before it happens.

**Before.** Cadence has controls for what it was built to do. **After.** A secondary and
unintended use and downstream harm forecast exists, with a mitigation against each
forecast use, and an external communication plan is written before it is needed — naming
who speaks, to whom, within what time, and with what holding statement.

**Demonstrated live.** The room is asked what a recruiter will do with an agent that can
issue offers, once the recruiter is behind on targets. The forecasts the room produces are
better than any list a trainer could hand out, and that is why the exercise is live.

**By the end, a participant can** forecast secondary and unintended uses and downstream
harms, and have a communication plan that exists before the phone rings.

### 22 — Write the kill switch down, and give it an owner

**Objective.** Make deactivation a control rather than an assumption.

**Before.** Everyone assumes Cadence can be switched off and nobody has tried.
**After.** A deactivation and localisation policy and procedure exists: the triggers, the
named person who can pull it, the steps in order, what happens to interviews already
booked and offers already issued, how localisation for one jurisdiction differs from a
full stop, and the date it was last tested.

**Demonstrated live.** The trainer asks who at Kabini can stop Cadence right now, and
walks the room to the answer that nobody can, because the credentials belong to a vendor.
Then the room writes the procedure that fixes it.

**By the end, a participant can** create and implement a deactivation and localisation
control that has an owner and a test date, rather than a paragraph that assumes one.

### 23 — Apply privacy law to all four systems

**Objective.** Start the applicability memo with the law that already applied.

**Before.** The pack has lifecycle artefacts and no legal statement. **After.** The
privacy section of the memo states, for each system, how transparency, choice, lawful
basis and purpose limitation are satisfied, how minimisation and privacy by design were
applied to a method built on data volume, and what the special-category and biometric
rules demand of the right-to-work check.

**Demonstrated live.** The trainer runs the two-lens rule: a privacy answer and an
operational answer to the same question about MatchScore, and shows where the privacy
professional's instinct over-reaches into a question that is not a privacy question.

**By the end, a participant can** apply lawful basis, purpose limitation, minimisation and
privacy by design to a concrete AI system, and handle special category and biometric data
correctly.

### 24 — Discharge the controller obligations

**Objective.** Turn controller duties into evidence that already exists in the pack.

**Before.** The privacy section states principles. **After.** The controller-obligations
section covers privacy impact assessments, third-party processors, cross-border transfers
to Attestra and Halcyon AI, data subject rights against a scoring model, automated
decision making, incident management, breach notification and record keeping — each
pointing at the pack artefact that evidences it.

**Demonstrated live.** A subject access request arrives for a candidate MatchScore ranked
low. The room works out what must be produced, from which artefact, and what cannot be
produced — and the automated-decision-making question is argued rather than asserted.

**By the end, a participant can** discharge controller obligations against an AI system and
show where the evidence for each one lives.

### 25 — IP, discrimination, consumer protection and product liability

**Objective.** Cover the four bodies of law where enforcement is actually happening while
the AI-specific regimes phase in.

**Before.** The memo covers privacy only. **After.** It also states where intellectual
property law prohibits or limits Kabini's use of data for training, how
non-discrimination law reaches MatchScore in employment and how the same reasoning
transfers to credit, lending, housing and insurance, where consumer protection's
prohibition of unfair and deceptive acts bites on Nora, and how product liability treats a
design or a manufacturing defect in an AI system.

**Demonstrated live.** The room is given one fact pattern and asked which of the four
reaches it. Most rooms answer with one; the correct answer is usually three, and that is
the exam's habit too.

**By the end, a participant can** apply existing IP, non-discrimination, consumer
protection and product liability law to a concrete AI system.

### 26 — Classify the four systems, and read off what follows

**Objective.** Teach AI-specific law as a method — classify, then read off the obligations
— before any statute is named.

**Before.** The memo covers existing law. **After.** Each system and each *use* carries a
risk classification, and the obligations that follow are written out: risk management,
data governance, technical documentation, conformity and impact assessments, record
keeping, human oversight, transparency and notification, quality management — plus the
distinct general-purpose AI requirements that reach Halcyon AI, the enforcement framework
and penalties, and how Kabini's duties change where it is provider, deployer, importer
or distributor.

**Demonstrated live.** The risk-tier classification drill: eight one-line use cases —
CV screening, a spam filter, emotion recognition in a workplace, a chatbot for order
status, credit scoring, a recommender and two more — placed and justified. The trainer
then points at the technical documentation the obligation demands, which is already in the
pack from use case 14, and the room sees why law came last.

**By the end, a participant can** classify a system under a risk framework, identify the
obligations that follow, and distinguish provider, deployer, importer and distributor
duties.

### 27 — The EU position, with dates on it

**Objective.** Apply the method to the EU, and teach the calendar as a dated handout
rather than as a fact.

**Before.** Obligations are classified but not dated. **After.** The EU section of the memo
states for each system which EU AI Act obligation applies and from which date under the
Act as amended by Regulation (EU) 2026/1744, what the GPAI Code of Practice does and does
not buy Halcyon AI, and what Article 50 already requires of Nora — carrying its compilation
date on its face and marking which dates are corroborated rather than read from the
Official Journal.

**Demonstrated live.** Article 50 in the wild: a consumer chatbot and an image generator
opened in the browser, checked for AI disclosure, and their outputs inspected at
`contentcredentials.org/verify` for content credentials. This is the only regulatory
obligation in the whole course that can be watched working right now, and it is in force.

**By the end, a participant can** state the current EU position on a given system with
dates, and recognise when a published timeline has gone stale.

### 28 — Korea and the United States

**Objective.** Run the same method through two more jurisdictions and complete the memo.

**Before.** The memo covers the EU. **After.** It is complete: Korea's AI Basic Act duties,
whether each system is "high-impact AI", what the fundamental-rights assessment and the
ministry grace period mean for Vikram Nair's client; and the US taught as a pattern — the
federal executive orders and preemption pressure, and Colorado SB 26-189 applied to
MatchScore as the worked state example of notice, disclosure, impact assessment and
algorithmic discrimination framing.

**Demonstrated live.** The same eight use cases from use case 26 are re-run against Korea's
high-impact categories, and the answers move. Colorado is taught as a story — postponed,
blocked, repealed, re-enacted narrower — because the lesson is volatility, not section
numbers.

**By the end, a participant can** state the Korean and US position on a given system, and
recognise the shared architecture underneath three different statutes.

### 29 — A standards map an auditor can navigate

**Objective.** Place the standards over work already done, in the proportion the blueprint
rewards.

**Before.** The pack is complete and unmapped. **After.** A standards map places ISO/IEC
42001 clauses, the four NIST AI RMF 1.0 functions and the OECD principles against the pack
artefacts that satisfy each, and the three corrections are written down: there is no NIST
AI RMF 2.0, NIST ARIA was removed from the Body of Knowledge in v2.1, and ISO/IEC 42006
sets requirements for certification bodies and is not an impact assessment standard.

**Demonstrated live.** One NIST AI RMF Playbook subcategory opened in the browser and its
suggested actions read against an artefact the room built. ISO/IEC 22989, 42001 and 42005
are each given the shape and purpose treatment and no more — this sub-domain is three to
five questions and teaching NIST deeply against it is poor economics, which the trainer
says out loud.

**By the end, a participant can** use the OECD principles, the NIST AI RMF and Playbook,
and ISO/IEC 22989, 42001 and 42005 for what each is actually for.

### 30 — Hand the pack over, and sit the exam you are about to sit

**Objective.** Hand over a finished, self-consistent pack, and turn the whole course into
exam performance.

**Before.** Thirty artefacts exist in twenty-nine folders. **After.** The pack is indexed,
every document carries a version, a date and a named owner, no two documents contradict
each other, and the artefact checklist is signed off row by row. Each participant has sat a
full-length hundred-question mock under exam conditions and holds a per-sub-domain
breakdown against the v2.1 weighting.

**Demonstrated live.** The handover walkthrough — the trainer reads the pack as Meera de
Vries would, then as an auditor would, then as the Korean client's procurement officer
would, and the three readers want different things. Then the blueprint's weighting is put
on screen against where the course spent its hours, the scenario technique is drilled
explicitly on **sequence, ownership and proportionality**, the retired seven-domain
structure is named and corrected, and the mock is sat.

**By the end, a participant can** hand over a governance programme somebody else can use,
and answer a scenario question by finding its discriminator rather than by recognising its
vocabulary.

---

## 4. Coverage check

Every module and aspect in the brochure's coverage map (§8), against the use case that
carries it.

| Module | Aspect | Carried by |
|---|---|---|
| **M1** Foundations | Generally accepted definitions and types of AI | 1 |
| **M1** Foundations | Classic vs generative vs agentic | 1 |
| **M1** Foundations | Model vs system | 1 |
| **M1** Foundations | Training vs inference | 1 |
| **M1** Foundations | Fine-tuning vs RAG vs agentic | 1 (revisited as a deploy choice in 17) |
| **M1** Foundations | ISO/IEC 22989 vocabulary as the source of the model/system distinction | 1 (placed on the standards map in 29) |
| **M1** Foundations | Risk and harm types to individuals, groups, organisations, society — misalignment, ethics and bias, complexity and scalability | 2 |
| **M1** Foundations | Characteristics requiring governance — complexity, opacity, autonomy, speed and scale, harm/misuse potential, data dependency, probabilistic vs deterministic | 2 |
| **M1** Foundations | Responsible-AI principles — fairness, safety and reliability, privacy and security, transparency and explainability, accountability, human-centricity | 2 |
| **M2** The programme | Roles and responsibilities for governance stakeholders | 4 |
| **M2** The programme | Cross-functional collaboration for efficacy and diversity of expertise | 4 |
| **M2** The programme | Training and awareness programme on terminology, strategy and governance | 4 |
| **M2** The programme | Differentiating governance by size, maturity, industry, products, objectives, risk tolerance | 4 |
| **M2** The programme | Developer / provider / deployer / user as task labels | 3 |
| **M2** The programme | Policies for oversight and accountability across all nine named lifecycle stages | 5 |
| **M2** The programme | Evaluating and updating existing privacy, security, data governance and **intellectual property** policies | 6 |
| **M2** The programme | Third-party risk policies, assessments and contracts across procurement, supply chain, HR and acceptable use | 6 (acceptable use), 7 (procurement, supply chain, HR, contracts) |
| **M3** Impact assessment family | DPIA vs FRIA vs ISO/IEC 42005 vs algorithmic impact assessment vs Korea's fundamental-rights assessment — trigger, scope, who performs, output, published or not | 8 (applied in 10, 18, 26, 28) |
| **M4** Design and build | Define business context and use case | 9 |
| **M4** Design and build | Apply policies, procedures, best practice and ethics to design and build — purpose, requirements gathering, architecture and model selection, human oversight, data analysis, metric and threshold evaluation, stakeholder engagement and feedback, operational controls | 9 |
| **M4** Design and build | Document the design and build process | 9 |
| **M4** Design and build | Perform or review an impact assessment | 10 |
| **M4** Design and build | Identify and manage internal and external risks and contributing factors — probability/severity harms matrix, risk mitigation hierarchy, stakeholder mapping, use-case evaluation, benchmarking, pre-deployment pilots and testing | 11 |
| **M5** Data governance | Assess and document lawful rights to collect and use data | 12 |
| **M5** Data governance | Data quality, quantity, integrity and fit-for-purpose | 12 |
| **M5** Data governance | Data lineage and provenance | 12 |
| **M5** Data governance | Plan and perform training and testing — unit, integration, validation, performance, security, bias, interpretability | 13 |
| **M5** Data governance | Identify and manage issues and risks during training and testing | 13 |
| **M5** Data governance | Document the training and testing process | 13 |
| **M5** Data governance | Live fairness-metric demonstration (Fairlearn) | 13 |
| **M6** Release and monitoring | Assess readiness and prepare for release | 14 |
| **M6** Release and monitoring | Model card | 14 |
| **M6** Release and monitoring | Conformity requirements | 14 (obligations read off in 26) |
| **M6** Release and monitoring | Public disclosures — technical documentation, instructions for use to deployers | 14 |
| **M6** Release and monitoring | Continuous monitoring and the maintenance/update/retraining schedule | 15 (deployer-side in 20) |
| **M6** Release and monitoring | Periodic assessment via audits, red teaming, threat modelling and security testing | 15 (deployer-side in 20) |
| **M6** Release and monitoring | Post-market monitoring plans | 15 (deployer-side in 20) |
| **M6** Release and monitoring | Live LLM vulnerability-scan demonstration (garak) | 15 |
| **M6** Release and monitoring | Manage and document incidents, issues and risks | 16 (deployer-side in 20) |
| **M6** Release and monitoring | Cross-functional root-cause work — brittleness, lack of robustness, poor data quality, insufficient testing, model and data drift | 16 |
| **M7** Deploy decision and assessment | Use-case context — business objectives, performance requirements, data availability, ethical considerations, workforce readiness | 17 |
| **M7** Deploy decision and assessment | Model type differences — classic vs generative, proprietary vs open source, small vs large, language vs multimodal | 17 |
| **M7** Deploy decision and assessment | Deployment options — cloud vs on-premise vs edge; as-is, fine-tuning, RAG, **agentic architectures** | 17 |
| **M7** Deploy decision and assessment | Perform or review an impact assessment on the selected system | 18 |
| **M7** Deploy decision and assessment | Risks and opportunities unique to deploying one's own proprietary model — increased obligations, higher liability | 18 |
| **M7** Deploy decision and assessment | Identify and evaluate key terms and risks in the **vendor or licensing** agreement | 19 |
| **M8** Deployment and use | Apply policies, procedures, best practice and ethics to deployment — data governance, risk management, issue management, user training | 20 |
| **M8** Deployment and use | Deployer-side continuous monitoring and retraining schedule | 20 |
| **M8** Deployment and use | Periodic audits, red teaming, threat modelling, security testing | 20 |
| **M8** Deployment and use | Document incidents, issues, risks and post-market monitoring plans | 20 |
| **M8** Deployment and use | Forecast and reduce secondary or unintended uses and downstream harms | 21 |
| **M8** Deployment and use | Establish external communication plans | 21 |
| **M8** Deployment and use | Create and implement policy and controls to deactivate or localise a system | 22 |
| **M9** Existing law | Transparency, choice, lawful basis, purpose limitation | 23 |
| **M9** Existing law | Data minimisation and privacy by design | 23 |
| **M9** Existing law | Sensitive and special category data including biometrics | 23 |
| **M9** Existing law | Controller obligations — privacy impact assessments, third-party processors, cross-border transfers, data subject rights, automated decision making, incident management, breach notification, record keeping | 24 |
| **M9** Existing law | Intellectual property law including limits on training data | 25 |
| **M9** Existing law | Non-discrimination law in employment, credit, lending, housing, insurance | 25 |
| **M9** Existing law | Consumer protection and unfair or deceptive acts | 25 |
| **M9** Existing law | Product liability and design/manufacturing defects | 25 |
| **M10** AI-specific law | Risk classification framework and what systems **and uses** fall into each category | 26 (re-run against Korea in 28) |
| **M10** AI-specific law | Requirements — risk management, data governance, technical documentation, conformity and impact assessments, record keeping | 26 |
| **M10** AI-specific law | Human oversight, transparency and notification, quality management | 26 |
| **M10** AI-specific law | Distinct GPAI requirements | 26 (Code of Practice in 27) |
| **M10** AI-specific law | Enforcement framework and penalties | 26 |
| **M10** AI-specific law | Differences by organisational context — providers, deployers, importers, distributors | 26 |
| **M10** AI-specific law | EU AI Act with the Regulation (EU) 2026/1744 timeline | 27 |
| **M10** AI-specific law | GPAI Code of Practice | 27 |
| **M10** AI-specific law | Article 50 transparency and content marking, inspected live | 27 |
| **M10** AI-specific law | South Korea AI Basic Act and high-impact AI | 28 |
| **M10** AI-specific law | US federal EOs and preemption pressure | 28 |
| **M10** AI-specific law | Colorado SB 26-189 as the state pattern | 28 |
| **M11** Standards | OECD principles, framework, policies and recommended practices for trustworthy AI | 29 |
| **M11** Standards | NIST AI RMF 1.0 core functions Govern/Map/Measure/Manage, categories and subcategories, and the Playbook | 29 |
| **M11** Standards | NIST AI 600-1 Generative AI Profile | 29 |
| **M11** Standards | ISO/IEC 22989, 42001 and 42005 | 29 (22989 introduced in 1; 42005 format used in 10) |
| **M11** Standards | Corrections — no AI RMF 2.0, NIST ARIA removed, ISO/IEC 42006 is certification-body requirements and is not in the BoK | 29 |
| **Consolidation** | Blueprint structure and weighting; Bloom levels the exam targets | 30 |
| **Consolidation** | Scenario technique by sequence, ownership and proportionality | 30 (drilled in miniature in 3, 8, 26) |
| **Consolidation** | Exam mechanics — 100 questions, 85 scored and 15 pilot, ~30% case-study-linked, 2 h 45 min plus a 15-minute optional break, scaled 100–500 with 300 to pass, no prerequisites, Pearson VUE or OnVUE, two-year term, 20 CPE credits | 30 |
| **Consolidation** | Full-length mock under exam conditions | 30 |
| **Consolidation** | Correction of the retired seven-domain structure still circulating | 30 |

**Nothing in the brochure's coverage map is dropped.** The three duplicated performance
indicators the Body of Knowledge states verbatim in both III.C and IV.C — monitoring
cadence, periodic audit and red teaming, incident and post-market documentation — are
taught once in use cases 15 and 16 and applied from the deployer's position in use case
20, exactly as the brochure's capacity ledger states.

### The fourteen pack artefacts, against the use case that produces them

| # | Artefact from brochure §4 | Produced by |
|---|---|---|
| 1 | AI system inventory and use-case register, with roles per activity | 1, 2, 3 |
| 2 | AI governance charter — roles, RACI, forum terms of reference, training and awareness plan | 4 |
| 3 | AI policy set — lifecycle policy, existing-policy gap redline, acceptable use policy, third-party assessment questionnaire | 5, 6, 7 |
| 4 | Completed AI system impact assessment on the CV-ranking model, ISO/IEC 42005-mapped, with DPIA and FRIA attachment | 10 |
| 5 | Risk register with probability/severity matrix and mitigation hierarchy | 11 |
| 6 | Data governance dossier — lawful rights, quality and fitness, lineage and provenance | 12 |
| 7 | Test plan and results summary, with the fairness metric and threshold | 13 |
| 8 | Model card and release-readiness checklist | 14 |
| 9 | Post-market monitoring plan, monitoring and retraining schedule, audit and red-team calendar | 15 |
| 10 | AI incident runbook with one worked incident record | 16 |
| 11 | Redlined extract of the foundation-model vendor agreement | 19 |
| 12 | Deployment control set for the agentic scheduling assistant — secondary-use limits, external communication plan, deactivation and localisation procedure | 20, 21, 22 |
| 13 | Regulatory applicability memo — EU, Korea, US, system by system, with dates | 23, 24, 25, 26, 27, 28 |
| 14 | Standards map — ISO/IEC 42001 clauses, NIST AI RMF functions, OECD principles against the artefacts | 29 |
| — | Pack index and checklist sign-off | 30 |

### The twenty outcomes, against the use case that delivers them

| Outcome | Carried by |
|---|---|
| O1 Explain what an AI system is, distinguish it from a model, classify as classic/generative/agentic | 1 |
| O2 Identify risks and harms and name the characteristics that need governance | 2 |
| O3 Apply responsible-AI principles to a concrete system | 2 |
| O4 Define roles, stand up a cross-functional forum, design a training programme | 4 |
| O5 Assign developer, provider, deployer and user per activity | 3 |
| O6 Write a lifecycle policy set, mark gaps in existing policies, build a third-party assessment | 5, 6, 7 |
| O7 Distinguish DPIA, FRIA, ISO/IEC 42005 assessment and algorithmic impact assessment | 8 |
| O8 Define a use case and business context, run design and build controls, manage risk with a matrix and hierarchy | 9, 11 |
| O9 Establish data governance for training data | 12 |
| O10 Plan and document testing with a named metric and a written threshold | 13 |
| O11 Produce a model card and a release-readiness decision, specify conformity documentation | 14 |
| O12 Set up monitoring, an audit and red-team schedule and an incident process, and explain incidents causally | 15, 16, 20 |
| O13 Evaluate a deploy decision including agentic architectures | 17 |
| O14 Identify and redline the key terms and risks in a vendor or licensing agreement | 19 |
| O15 Govern a deployed system, including downstream harms, external comms and a tested deactivation control | 20, 21, 22 |
| O16 Apply existing privacy, IP, non-discrimination, consumer protection and product liability law | 23, 24, 25 |
| O17 Classify under a risk framework and distinguish provider, deployer, importer, distributor duties | 26 |
| O18 State the current EU, Korean and US position with dates, and spot a stale timeline | 27, 28 |
| O19 Use OECD, NIST AI RMF and Playbook, ISO/IEC 22989, 42001 and 42005 for what each is for | 29 |
| O20 Sit the exam prepared for its weighting, answering by sequence, ownership and proportionality | 30 |

---

## 5. The time ledger

**Ceiling: 32.0 live hours** — 16 sessions × 2 hours. That shape is the only thing this
ledger sums against.

| | Minutes | Hours |
|---|---|---|
| Use cases 1–30 | **1,700** | **28.33** |
| Recap and out-of-flow Q&A, ~8 minutes across each of 15 sittings | 120 | 2.00 |
| **Committed** | **1,820** | **30.33** |
| **Unallocated overrun margin** | **100** | **1.67** |
| **Ceiling** | **1,920** | **32.00** |

### Where the minutes go, by module

| Module | Use cases | Minutes | Hours | Brochure's indicative hours |
|---|---|---|---|---|
| M1 Foundations | 1, 2 | 110 | 1.83 | 2.0 |
| M2 The programme | 3, 4, 5, 6, 7 | 245 | 4.08 | 4.0 |
| M3 Impact assessment family | 8 | 50 | 0.83 | 0.8 |
| M4 Design and build | 9, 10, 11 | 135 | 2.25 | 2.2 |
| M5 Data governance | 12, 13 | 135 | 2.25 | 2.5 |
| M6 Release and monitoring | 14, 15, 16 | 150 | 2.50 | 2.6 |
| M7 Deploy decision and assessment | 17, 18, 19 | 185 | 3.08 | 3.6 |
| M8 Deployment and use | 20, 21, 22 | 175 | 2.92 | 3.0 |
| M9 Existing law | 23, 24, 25 | 165 | 2.75 | 3.0 |
| M10 AI-specific law | 26, 27, 28 | 175 | 2.92 | 3.0 |
| M11 Standards | 29 | 70 | 1.17 | 1.2 |
| Consolidation | 30 | 105 | 1.75 | 2.0 |
| **Total** | **30** | **1,700** | **28.33** | **29.9** |

**It fits, and it fits with room.** The backlog is 1.57 hours below the brochure's
indicative module-plus-consolidation total, and 1.67 hours below the ceiling once the
per-sitting recap time is booked. That margin is deliberate and it is the difference
between this ledger and the brochure's, which committed 31.9 of 32.0 and left 0.1 hours
for every question nobody planned for. Every estimate in the table above is optimistic,
because estimates made before a room exists always are.

**Where the 1.57 hours came from, and why it costs no coverage.**

- **M7 gives up 31 minutes**, the largest single trim. By the time use case 18 runs, the
  room has already performed a full impact assessment in use case 10 and built the
  third-party questionnaire in use case 7, so reviewing an assessment on a bought system
  is applying a known form rather than learning a new one. Nothing in IV.A or IV.B is
  dropped; use case 17 keeps 70 minutes because the agentic deployment option is new to
  v2.1 and the room will not have met it before.
- **M5 and M9 give up 15 minutes each.** M5's demonstration is fifteen minutes of the
  seventy in use case 13 and the rest is documentation the room can carry between
  sittings. M9's three use cases each sit on a legal regime this audience already works
  inside — the brochure's own seniority bar is what makes that trim safe.
- **M1 and Consolidation give up 10 and 15 minutes.** M1 is vocabulary that pays off
  later rather than needing to be complete on the night. Consolidation's 105 minutes
  fits a hundred-question mock and its review inside a sitting; the brochure's 120 did
  not, because it left nothing for the sitting's own recap.
- **M2 takes 5 minutes more** than the brochure allows, because it carries thirteen
  scored questions, three of the fourteen pack artefacts and the single most reliable
  trap in the exam.

**If it overruns anyway, cut in this order.** Do not shrink estimates to make the
arithmetic work; drop scope and say so.

1. **Use case 4** loses the training and awareness plan to a between-sittings exercise
   with a template, saving ~20 minutes. It is the most template-able artefact in the pack.
2. **Use case 25** merges consumer protection and product liability into one worked fact
   pattern instead of two, saving ~15 minutes. Both are four-to-six-question territory
   shared with IP and non-discrimination.
3. **Use case 18** drops the proprietary-model risks-and-opportunities discussion into
   use case 17's deploy-decision record, saving ~15 minutes.
4. **Use case 2** moves the responsible-AI principles pass to a between-sittings annex,
   saving ~15 minutes, and the trainer reviews it at the start of use case 3.

Cut in that order and the backlog absorbs a full extra hour of questions without losing
a brochure aspect. **Do not cut use cases 13, 15, 16, 20, 21 or 22** under any pressure:
III.C and IV.C are up to twenty-one of the eighty-five scored questions, they are the
sub-domains this market under-serves, and they are the only reason the pack is worth more
than a question bank.

---

## 6. What the trainer must decide

Assumptions made in writing this plan, and open decisions that belong to the trainer.

1. **The schedule.** The weekday, the clock time and the start date are not recorded.
   They are stated as to be announced in `project.md` and no local-time table is written,
   because with no clock time there is nothing to convert. Re-run this plan's schedule
   section once they are settled. The 32.0-hour ceiling is unaffected and was scoped
   against exactly.
2. **The named people and the named vendors are invented here.** Meera Krishnamurthy, Arjun
   Sundaram, Kavitha Rajagopal, Vikram Nair, Deepa Sridharan, Attestra Inc. and Halcyon AI,
   Inc., and the system names MatchScore, Nora and Cadence, do not appear in the
   brochure. The brochure fixed the client, the four systems and the pack; these names
   make them teachable. They are now fixed too — the demo builder reads them.
3. **The brochure's capacity ledger commits 31.9 of 32.0 hours.** That is not survivable
   in a live room. This backlog trims 1.57 hours of indicative module time, itemised
   above, and every brochure aspect is still carried. If the trainer wants the brochure's
   original module hours restored, the reserve goes to 0.1 hours and the first overrun
   eats a use case.
4. **The two tool demonstrations need a decision about the machine.** garak needs a
   model endpoint and network access from the teaching machine; Fairlearn needs nothing
   but Python. Both are trainer-side and neither is a participant lab, per the brochure.
   Assumed here: a current Python 3.x (3.12 or newer) in a throwaway environment, exact
   releases pinned and printed on the output, and a pre-recorded fallback for each in
   case the venue network blocks them. The trainer must record the endpoint garak points
   at, and it must not be a client system.
5. **The Fairlearn dataset is synthetic and must be authored.** No real candidate data,
   ever. Somebody has to build a small tabular set that produces a demographic parity
   difference large enough to be visible and small enough to be arguable.
6. **The mock exam does not exist yet.** Use case 30 assumes a hundred-question,
   four-option, single-answer paper written in house against v2.1 with the blueprint's
   weighting and roughly thirty per cent case-study-linked, plus a per-sub-domain scoring
   sheet. The brochure commits to it and forbids dump material. It is a build in its own
   right and is not inside any use case's estimate.
7. **The artefact checklist that use case 30 signs off against must be published to the
   cohort in advance**, because the brochure ties the Certificate of Completion to it.
   Assumed here: the fourteen artefacts in `project.md` §5, checked for presence,
   completeness and internal consistency, not legal correctness.
8. **The format participants write in.** Assumed: Microsoft Word or Google Docs, per the
   brochure's prerequisites, with the trainer issuing a template per artefact. If the
   trainer wants the pack version-controlled in the repository instead, the templates
   should be Markdown and that decision has to be made before use case 1, not after.
9. **The EU AI Act timeline is corroborated, not read from the Official Journal.**
   EUR-Lex was unreachable from the research environment. Every timeline handout in use
   cases 26–28 must carry its compilation date and mark which dates are second-hand. The
   trainer should re-verify the Regulation (EU) 2026/1744 detail before the first
   delivery.
10. **The IAPP candidate handbook may have a newer revision behind login.** The public
    copy is dated 2 April 2024 and still says seven domains. Use case 30 teaches the
    four-domain structure from the Body of Knowledge and names the handbook's staleness
    as a known error; if the trainer has IAPP login access, check for a newer revision
    before delivery.
11. **Between-sitting work is assumed and not costed.** The brochure sells "thirty-two
    hours of live instruction on top of your own reading" and says artefacts are built
    between sessions and reviewed in the next one. Every use case's estimate is live
    time only. The trainer must decide how much drafting is homework and say so in
    session one, because several use cases — 5, 6, 12, 19, 24 — depend on it.
12. **No use case is allocated to a session, on purpose.** If the trainer wants a
    provisional split for their own planning, it is theirs to make in private notes; it
    does not belong in a document a participant sees.
