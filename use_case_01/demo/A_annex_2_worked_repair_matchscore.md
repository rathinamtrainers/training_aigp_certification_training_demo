# A · Annex 2 — The worked repair: MatchScore described as a model, then as a system

**Artefact:** A. AI system inventory and use-case register — Annex 2
**Version:** 1.0.3 · **Issued:** 2026-09-07 · **Revised:** 2026-09-09 · **Owner:** Meera Krishnamurthy, General Counsel
**Parent:** `A_ai_system_inventory_and_use_case_register.md`
**Purpose:** this is the AIS-001 entry the trainer builds on screen — wrong first, then
repaired [UCP §3 entry 1, "Demonstrated live"]

---

## The draft entry, as Kabini first wrote it

> **MatchScore.** An XGBoost gradient-boosting model trained on eight years of
> historical placement outcomes. Tabular features plus TF-IDF over CV free text.
> Outputs a fit score from 0 to 1. Owner: engineering. Accuracy 0.83.

Nothing in that paragraph is false. It is a competent description of a **model**, and it
would pass unchallenged in most technical reviews.

**It governs nothing.** Every question a board, an auditor or a procurement officer asks
next is unanswerable from it.

| Question a reader will ask | Can the draft answer it? |
|---|---|
| Whose data goes in, and where does it come from? | No |
| Where does the score go, and who sees it? | No |
| Does a human decide, or does the score decide? | No |
| Who is accountable — a person, not a department? | No. "Engineering" is not a name |
| Which markets is it used in? | No |
| How often does it run? | No |
| Was Kabini allowed to train on that data? | No |
| Accuracy of 0.83 against what, measured when, on whom? | No |

The number is the trap. **"Accuracy 0.83" is the only figure in the draft and it has no
source, no date and no population** — which is exactly the kind of number this course
teaches a board to refuse. It does not appear in the register. The register's testing
numbers arrive in use case 13, with a named metric, a written threshold and a
demonstration the room watched.

---

## What was wrong with it, in one line

**It described the model. The thing Kabini has to govern is the system.**

Version 2.1 of the Body of Knowledge made that substitution across both lifecycle
domains — "AI model" became "AI system" in the design indicator, the impact-assessment
indicator, the monitoring indicator, the deactivation indicator and the Domain IV.C
competency title [DIFF §5]. Those two domains carry **42 to 50** questions [BOK-2.1
Domain III and IV pages] of what are best read as the 85 scored ones — [RR] §3.3
("Disagreement 2") states it that way, and `A_sources.md` marks the denominator as an
inference rather than a published figure. The research report's finding is that a candidate
who thinks in weights answers the wrong question across roughly 46 questions' worth of
material [RR §4 item 2].

The same is true off the exam. A governance professional who thinks in weights governs
the wrong object, and every control they write lands somewhere the harm is not.

---

## The repair, field by field

Seven additions turn the model description into a system description. Each one is
sourced.

| # | What was added | The AIS-001 entry | Source | What it unlocks later in the pack |
|---|---|---|---|---|
| 1 | **The data going in, and where it comes from** | Candidate records — CVs, applications, structured fields — read from **Talent Cloud**, the applicant tracking system | [PRJ §1] | Data governance dossier, use case 12 |
| 2 | **The training data, named, with its provenance status** | The **placement warehouse**: eight years of placement outcomes, Amazon-hosted, `eu-west-1`. **Nobody has written down where all of it came from** | [PRJ §1] | The lawful-rights assessment, use case 12 |
| 2a | **Where that data actually sits, and where training happens** | The warehouse in `eu-west-1` **and a read replica in `ap-south-1`**, trained against by the Bengaluru team since 2023 and **in no transfer record — OI-12** | [PRJ §1] plus a gap found by writing the row | Lineage and provenance, use case 12; cross-border transfers, use case 24 |
| 3 | **The output, and where it lands** | A fit score written back into Talent Cloud, shown to recruiters as a ranked list | [PRJ §1] | The transparency and explainability questions, use case 2 onward |
| 4 | **The human oversight, and whether it is real** | A recruiter reads the list. Whether the ranking is advisory or effectively dispositive is **not documented — OI-04** | Gap found by writing the row | Human oversight design, use case 9; automated decision making, use case 24 |
| 5 | **The deployment context** | Internal recruiters; assumed group-wide across the EU, South Korea and the US because Talent Cloud is the group system — **assumed, not confirmed, OI-08** | [PRJ §1] plus a marked assumption | Jurisdiction, use cases 27 and 28 |
| 6 | **A named accountable person** | **Kavitha Rajagopal**, Head of Talent Operations | [PRJ §1] | Roles per activity, use case 3; the charter and RACI, use case 4 |
| 7 | **The decision it touches** | Which candidates a human looks at, and in what order — an input to a hiring decision about a named person | Derived from the purpose in [PRJ §1] | Everything. This is the sentence that makes anyone care |

**Then the classification, which the draft did not attempt at all:**

- **Type: classic.** Rules R1 and R2 — it scores existing records, so the generative test
  (R3) fails; it takes no action, so the agentic test (R4) fails.
- **Realisation: not applicable — trained in-house.** Rule R6. The
  as-is / fine-tuning / retrieval-augmented / agentic axis is the blueprint's list of
  ways to deploy **someone else's** pre-trained model [BOK-2.1 IV.A]. Kabini trained
  this one.

---

## The second trap, and it is subtler than the first

Once the row is repaired, the tempting entry in the realisation column is **"as-is"** —
because Kabini is not fine-tuning anything and is not doing retrieval, so "as-is"
looks like the honest residual.

It is wrong, and it costs something. "As-is" implies a model that arrived from
somewhere, which quietly implies somebody else made the training decisions. **Kabini
made them.** The whole weight of data provenance, data quality, fitness for purpose and
bias testing sits on Kabini because of it — which is the reason MatchScore, and not
one of the bought systems, is the system carried end to end through the build file
[PRJ §3].

"Not applicable — trained in-house" is four words longer and is the difference between a
register that points at the obligation and one that points away from it.

---

## What the room does next

The trainer builds AIS-001 live: the draft first, then the seven repairs, then the two
classification lines. The room then fills AIS-002, AIS-003 and AIS-004 from the same
blank record — `A_annex_3_room_worksheet.md` — and argues about Cadence [UCP §3 entry 1].

**The argument to let run.** Somebody will say Cadence is generative, because it is the
same Halcyon AI model as Nora. That is the right thing to say and the wrong answer, and
it is the fastest route into rule R1 there is: **identical weights, different system,
different class, different controls.** Let the room get there rather than telling it.
