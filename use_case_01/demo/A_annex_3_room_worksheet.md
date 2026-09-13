# A · Annex 3 — The blank record, and what the room fills in

**Artefact:** A. AI system inventory and use-case register — Annex 3
**Version:** 1.0.3 · **Issued:** 2026-09-07 · **Revised:** 2026-09-09 · **Owner:** Meera Krishnamurthy, General Counsel
**Parent:** `A_ai_system_inventory_and_use_case_register.md`
**Use:** hand out after the trainer has built AIS-001 on screen. Sixty minutes is the
budget for the whole use case [UCP §2 row 1]; this worksheet is about thirty of them.

---

## The blank record

Copy it once per system. Every field is answerable, and **"not documented" is an
answer** — it becomes an open item with an owner and a date, and that is a control, not
a blank.

| Field | Your entry |
|---|---|
| Reference | AIS-0__ |
| Name | |
| Lifecycle status | in production / in pilot / retired |
| Business owner (a **person**, not a department) | |
| Technical owner | |
| Business purpose — the use case, in one sentence | |
| The decision it touches | |
| **Type** — classic / generative / agentic | |
| **Why that type**, naming the rule (R2, R3, R4) | |
| **Model realisation** — as-is / fine-tuned / RAG / agentic architecture / not applicable (R6, R8) | |
| Model provenance — built in-house, licensed from whom, bought from whom | |
| What happens at **training** time, and who performs it (R5) | |
| What happens at **inference** time, and who performs it (R5) | |
| Data in | |
| Data out | |
| Interfaces and dependencies | |
| Human oversight — is there a human, and what can they actually change? | |
| Deployment context — who uses it, in which markets | |
| Volume — how often does it run? | |
| Third parties | |
| Classified from the outside? (R9) | yes / no |
| Open items raised | |

---

## The three rows the room fills

The trainer has just built **AIS-001 MatchScore** on screen — wrongly, then repaired
(Annex 2). Split the room and take the other three.

### Group 1 — AIS-002 Nora

*A candidate-facing chatbot on a foundation model licensed from Halcyon AI, Inc.,
fine-tuned on Kabini's own placement data, answering placement and payroll questions
under Kabini's brand* [PRJ §1].

**The question to push on:** at inference time, what leaves Kabini? A question typed
by a candidate goes to Halcyon's hosted API. Does anything **else** go with it?

### Group 2 — AIS-003 The right-to-work check

*A biometric identity verification service bought from Attestra Inc., Delaware, United
States. Kabini did not build it and cannot inspect it. Personal data including
biometric data leaves the EU to reach it* [PRJ §1].

**The question to push on:** you are asked for the type. You have never seen inside it
and Attestra has never told you. What do you write in the box?

### Group 3 — AIS-004 Cadence

*An agentic scheduling assistant in pilot that books interviews and issues offers
without a human in the loop, built by Kabini over the same Halcyon AI hosted API that
sits under Nora* [PRJ §1].

**The question to push on:** it is the same model as Nora. Is it the same class?

---

## The four arguments to let the room have

They are all the same argument arriving from four directions, and the answers are in the
register and Annex 1. Do not pre-empt them.

| # | The argument | Where it lands |
|---|---|---|
| 1 | **"Cadence is generative — it is the same model as Nora."** | Rule R1 and rule R2. Identical weights, different system, different class, different controls. This is the one the plan says the room argues about [UCP §3 entry 1] |
| 2 | **"MatchScore is used as-is."** | Rule R6. The realisation axis describes what you do to a model **somebody else** trained [BOK-2.1 IV.A]. Kabini trained this one, and writing "as-is" hides the fact that the data obligations land on Kabini |
| 3 | **"We can't classify the Attestra system, so leave it blank."** | Rule R9. You classify on the behaviour you can observe, and you **mark it** as asserted-by-the-deployer and unconfirmed. Blank tells the next reader nothing; marked tells them exactly how far to trust it |
| 4 | **"Nora is fine-tuned, so the realisation column is done."** | Rule R8. Fine-tuned and retrieval-augmented are not alternatives, and nobody has written down which Nora is. One design sends an identified worker's payroll data to a third party on every question; the other never does. That is open item OI-05 |

---

## The close — the two-minute check

Each group reads out one row. For each, ask the room three questions only:

1. **Could this row have been written about the model alone?** If yes, it is not finished
   (R1).
2. **Is there a person's name in the owner field?** A department is not an owner.
3. **What did you write "not documented" against, and who is going to find out by when?**
   That is the open item, and it is the part of the register that does work between now
   and the next sitting.

**Then the point of the whole hour.** Kabini started this session with four AI
systems and no inventory, no policy, no impact assessment and no named owner [PRJ §1].
It ends it with four rows, four owners — three of them interim and marked as such — and
twelve things it now knows it does not know. Nothing was built and nothing was fixed.
**Every other artefact in the pack hangs off one of these rows** [PRJ §3], and none of
them could have been started an hour ago.
