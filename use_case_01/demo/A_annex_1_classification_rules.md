# A · Annex 1 — The classification rules the register applied

**Artefact:** A. AI system inventory and use-case register — Annex 1
**Version:** 1.0.3 · **Issued:** 2026-09-07 · **Revised:** 2026-09-09 · **Owner:** Meera Krishnamurthy, General Counsel
**Parent:** `A_ai_system_inventory_and_use_case_register.md`
**Sources:** every key resolves in `A_sources.md`

---

## Why the rules are written down at all

A register that says "MatchScore: classic" and stops is an assertion. A register that
says "MatchScore: classic, rule R2, because both R3 and R4 fail" is a decision somebody
else can check, disagree with, and re-run when the system changes. The rules below are
what version 1.0 of the register actually applied, in the order it applied them.

They are deliberately short. The blueprint gives sub-domain I.A — where "know the
generally accepted definitions and types of AI" sits — a weight of **4 to 6 questions**
of what are **best read as the 85 scored** questions on a 100-question paper
[BOK-2.1 Domain I for the 4–6; RR §2.4 for the 85-of-100 split; the reading of the
denominator is an inference, and `A_sources.md` says so], and the research report's
recommendation is to
teach enough technology to make the governance vocabulary land and then stop [RR §3.3].
Nine rules on one page is that much and no more.

### One honest caveat, on the face of the annex

The model-versus-system distinction used here is the one the Body of Knowledge v2.1
adopted, which the research attributes to **ISO/IEC 22989**, the AI concepts and
terminology standard named in the blueprint [RR §2.5; BRO Module 1]. **The standard has
now been read, and it still may not be quoted.** When this pack was first written it had
not been read at all: the standard is paywalled and `iso.org` returned HTTP 403 from the
research environment [RR §2.5]. A single-user licensed copy was bought and read on
2026-09-09 [ISO-22989], and it confirms the attribution — clause **3.1.4** defines an AI
system as an engineered system that generates outputs, and clause **3.1.23** defines a
model as a representation. That is the separation R1 enforces, and it is now sourced to
the standard rather than to a description of it.

The licence changes less than that sounds. It is single-user and prohibits reproduction,
so **a clause number may be cited and a clause may not be quoted.** No verbatim ISO/IEC
22989 wording appears anywhere in this pack, and none may be added. Where wording is
quoted below, it is quoted from the blueprint, which the IAPP publishes free and which
was read in full.

---

## R1 — Govern the system, not the model

**The rule.** Every entry in the register describes an **AI system**: the model **plus**
the data going into it, the interfaces around it, the controls and human oversight on
it, and the deployment context it sits in. A description that names only the model is
not an entry.

**Why it is rule one.** Version 2.1 of the Body of Knowledge systematically replaced
"AI model" with "AI system" across both lifecycle domains — the design indicator, the
impact-assessment indicator, the monitoring indicator, the deactivation indicator and
the Domain IV.C competency title all changed [DIFF §5]. The governed object is now the
deployed system. Domains III and IV are together weighted **42 to 50** [BOK-2.1 Domain
III and IV pages] of what are best read as the 85 scored questions — [RR] §3.3
("Disagreement 2") states it as "42–50 of 85 scored questions", and `A_sources.md`
marks the denominator as an inference. The research report puts it plainly:
a candidate who thinks in weights answers the wrong question, across roughly 46
questions' worth of material [RR §4 item 2].

**The practical test.** Read the entry back. If nothing in it would change when the same
model is connected to a different tool, a different data source or a different human
process, you have described a model.

**Where it bites in this register.** AIS-002 and AIS-004 run on the **same** Halcyon AI
model [PRJ §1] and are different systems with different classes and different controls.
That difference is invisible to anyone describing models.

---

## R2 — Decide the type in this order: agentic, then generative, then classic

**The rule.** Test R4 first, then R3. **Classic is what remains.**

**Why the order.** A generative model inside a system that acts is an **agentic** system.
Testing "does it generate text?" first gets Cadence wrong, because the answer is yes and
the answer is irrelevant. The blueprint's own model-type indicator pairs "classic vs.
generative" as a **model** distinction [BOK-2.1 IV.A], while "agentic architectures" was
added in v2.1 to the **deployment options** list [DIFF §5, "Other III/IV changes"] — that is, agency is
something you build around a model, which is exactly why it is tested first at the
system level.

**Classic is not a lesser class.** AIS-001 and AIS-003 are classic, and they are the two
systems in this register that decide most about a named person. The class says what kind
of thing it is, not how much it matters.

---

## R3 — The generative test

**Ask:** does the system **produce new content** at inference — text, image, audio, code
— composed for the input in front of it, rather than selecting, scoring or classifying
something that already exists?

- **Yes → generative.** AIS-002 (Nora) composes an answer to each question.
- **No → not generative.** AIS-001 emits a number. AIS-003 emits a determination.

**The common error.** "It uses a large language model, so it is generative." The class
belongs to the system, not to the family of the model. A large language model used only
to classify incoming messages into five buckets is a classifier, and the system is
classic.

---

## R4 — The agentic test

**Ask:** does the system **act** — take steps that change something outside itself, by
calling tools, in a sequence it decides — **without a human approving each step**? Or
does it only produce output for a human to act on?

- **Acts → agentic.** AIS-004 (Cadence) books an interview and issues an offer with no
  human in the loop [PRJ §1].
- **Produces output only → not agentic.** AIS-002 answers and stops.

**Three things make it agentic, and all three are properties of the system:**

1. **Tool access** — it can call something that changes the world.
2. **Multi-step planning** — it decides its own sequence, and the intermediate steps are
   not read by anyone.
3. **Absence of a per-step human approval.**

**The common error.** "Cadence is generative — it is the same model as Nora." Identical
weights, different system, different class, different controls. This is R1 arriving in
the form of a concrete argument, and it is the argument the room has [UCP §3 entry 1].

---

## R5 — Training and inference are separate entries, and each one names who performs it

**The rule.** Every record answers two questions separately: *what happens at training
time, and who does it* and *what happens at inference time, and who does it*.

**Why it earns its place in a governance register.** The two have different data,
different geography and different parties.

- **AIS-001**: Kabini trains, on eight years of placement outcomes in `eu-west-1` —
  but **in Bengaluru, against a replica in `ap-south-1`**; Kabini infers, in-house. No
  third party is in either path, and the training data is still outside the Union
  [PRJ §1]. This is the row that shows why the two questions are asked separately: a
  record that answered "where does the data go?" once would have said "nowhere".
- **AIS-002**: **Halcyon AI** pre-trains and Kabini cannot see it; **Kabini**
  fine-tunes; **inference happens on Halcyon's API**, so the prompt leaves Kabini
  every time.
- **AIS-003**: Kabini performs **no** training. It only causes inference — by making
  an API call that sends biometric data out of the EU [PRJ §1].
- **AIS-004**: inference is not one call and one answer; it is a chain of calls inside a
  loop.

Half the questions the pack asks later — whose data, whose obligation, crossing which
border — resolve differently depending on which of the two you are talking about.

---

## R6 — The realisation axis applies only to a model somebody else trained

**The rule.** *As-is / fine-tuned / retrieval-augmented / agentic architecture* is the
blueprint's list of **AI deployment options** — "using the AI model **as is** or with
**fine-tuning**, **retrieval augmented generation**, **agentic architectures**, or other
techniques to improve performance and fit" [BOK-2.1 IV.A, verbatim]. Every item on that
list is something a deployer does to a model that already exists.

**So if the organisation trained the model itself, the correct entry is "not
applicable", with a note saying why.**

**Where it bites.** AIS-001 is trained in-house from Kabini's own data. Writing
"as-is" against it is a mistake that reads as an answer, and it hides the single most
consequential fact about MatchScore: **Kabini made the training decisions**, so the
data-provenance, quality and testing obligations land on Kabini and not on a vendor.

---

## R7 — Fine-tuning is the realisation that changes whose output it is

**The rule.** Record fine-tuning wherever the deployer adapts a third party's model on
its own data, and record beside it **whose name is on the output**.

**Why it is called out separately.** Kabini fine-tunes Halcyon AI's model on its own
placement data and puts its own name on the result [PRJ §1]. The research report is
blunt that scenario questions exploit exactly this move — the same company is a deployer
in one paragraph and a provider in the next, "e.g. by fine-tuning and putting its own
name on the output" [RR §4 item 3].

**Version 1.0 of the register records the fact and stops there.** It does not assign
developer, provider, deployer or user, because those are task labels applied per
activity, not per company [RR §4 item 3], and that is use case 3. Recording the fact now
is what makes use case 3 possible.

---

## R8 — The four realisations, told apart

| Realisation | What the deployer does | Are the model's weights changed? | Does new data reach the model at inference? | In this register |
|---|---|---|---|---|
| **As-is** | Calls a finished model or service and uses what comes back | No | Only the input | **AIS-003** — Attestra's service, consumed through an API |
| **Fine-tuned** | Continues training the model on its own data | **Yes** | Only the input | **AIS-002** — Nora, on Kabini placement data |
| **Retrieval-augmented (RAG)** | Fetches relevant records at question time and puts them in front of the model | No | **Yes — retrieved records go to the model on every call** | **Not confirmed anywhere.** Open item OI-05 asks whether Nora does this |
| **Agentic architecture** | Gives the model tools and lets it plan and act | No | Yes, and it also **sends actions out** | **AIS-004** — Cadence |

**They are not mutually exclusive.** A system can be fine-tuned *and* retrieval-augmented
*and* agentic. Record all that apply, and record what is unknown as unknown.

**Why the RAG row matters even though nothing in the register is confirmed as RAG.**
The difference between "fine-tuned only" and "fine-tuned plus retrieval" is the
difference between a system that never sends an identified worker's payroll record to a
third-party endpoint and one that does it on every question. Nobody at Kabini has
written down which Nora is. That is OI-05, and it is the clearest illustration in the
pack of why a register asks a question the architecture diagram does not.

---

## R9 — Mark any classification you made from the outside

**The rule.** Where the classification rests on **observed behaviour** rather than on
anything the provider has stated, mark it *asserted by the deployer, unconfirmed by the
provider*, and raise an open item to confirm it.

**Where it bites.** AIS-003 is recorded as classic because that is what it appears to do.
Kabini did not build it and cannot inspect it [PRJ §1], and Attestra has never been
asked. The mark is what stops a plausible guess from hardening into a fact that three
later artefacts quote. It closes through the third-party questionnaire (use case 7) and
the outside-in assessment (use case 18).

---

## The rules as one page, for the room

| # | Rule | The question it makes you ask |
|---|---|---|
| R1 | Govern the system, not the model | What is around the model? |
| R2 | Agentic, then generative, then classic | In that order — what does it *do*? |
| R3 | Generative test | Does it create new content? |
| R4 | Agentic test | Does it act without a human per step? |
| R5 | Training and inference are separate | Who does each, where, on whose data? |
| R6 | The realisation axis is for models you did not train | Did we train it? Then the axis does not apply |
| R7 | Fine-tuning changes whose output it is | Whose name is on the answer? |
| R8 | As-is / fine-tuned / RAG / agentic, told apart | Weights changed? New data at inference? Actions out? |
| R9 | Mark what you classified from the outside | Did the provider tell us, or did we guess? |
