# Concepts — Use case 1: Take stock: what these four systems actually are

*AIGP Certification Training · Rathinam Trainers & Consultants · The AI Engineering Series*
*Written 2026-09-09, after the section in [`../demo/`](../demo/) was built and checked,
by reading it backwards to the ideas a room has to hold before it can follow the
register.*

**These pages are trainer material.** They are not part of the Kabini AI Governance
Pack, they carry no artefact letter, no pack version and no document owner, and nothing
in them is signed by anybody. The artefact is in `../demo/`; this is what gets taught
before it.

**This is use case 1 of thirty, so nothing is carried in.** There is no earlier
`concepts/` folder to point at, and no idea below has been taught elsewhere in this
course. Later use cases should point back here rather than re-teaching model versus
system, the three types or the realisation axis.

---

## The order, and what each page reaches

| # | Page | The one idea | The answer it works through to | Weight |
|---|---|---|---|---|
| 00 | [`00_definitions.md`](00_definitions.md) | The vocabulary, settled once and re-used — starting with **AI system**, **AI model**, and the table of differences between them | A definition is fixed in one place, with the clause or indicator it rests on and whether that source may be quoted. It grows as later use cases add terms | Reference |
| 01 | [`01_one_indicator_rewritten.md`](01_one_indicator_rewritten.md) | The governed object changed from the model to the system, and one line of the blueprint proves it | Reading the same performance indicator in v2.0.1 and v2.1 moves the recruiter inside the boundary of an impact assessment | Grounding |
| 02 | [`02_the_standard_you_may_name.md`](02_the_standard_you_may_name.md) | ISO/IEC 22989 is named by the blueprint; it was unreadable when the pack was written and is now bought under a licence that forbids reproduction — so it may be named, cited by clause, and never quoted | Four sentences a trainer may write, one they may not, and why the same prohibition under two different reasons is worth saying out loud | Grounding |
| 03 | [`03_model_or_system_one_sentence.md`](03_model_or_system_one_sentence.md) | The swap test: hold each sentence against the two states Kabini's live system might be in, and see which sentence can tell them apart | "Outputs a fit score from 0 to 1" reads identically whether or not anyone works below the fold, so it is a model fact; the sentence naming the recruiter is a system fact, and it is what makes OI-04 askable | **Load-bearing** |
| 04 | [`04_three_types_one_order.md`](04_three_types_one_order.md) | Classic, generative and agentic are two yes/no questions, and the order decides the answer | Cadence is **agentic**; asking about content first yields "generative", which is true evidence and the wrong answer, and the deactivation question never gets asked | **Load-bearing** |
| 05 | [`05_one_model_two_systems.md`](05_one_model_two_systems.md) | The class belongs to the system, not to the weights | The same Halcyon AI model gives **generative** for Nora and **agentic** for Cadence. One model, two systems, two control sets | **Load-bearing** |
| 06 | [`06_where_does_the_data_go.md`](06_where_does_the_data_go.md) | Training and inference are separate questions with separate answers | Asked once: "nowhere". Asked twice: eight years of placement outcomes sit in a replica in `ap-south-1`, outside the Union, with no vendor involved and no transfer record | **Load-bearing** |
| 07 | [`07_the_axis_that_does_not_apply.md`](07_the_axis_that_does_not_apply.md) | As-is / fine-tuned / RAG / agentic describes what you do to somebody else's model | MatchScore's realisation cell is **"not applicable — trained in-house"**, and "as-is" points the data obligations at a vendor who does not exist | **Load-bearing** |
| 08 | [`08_which_realisation_is_it.md`](08_which_realisation_is_it.md) | The four realisations are answers to three separate questions, and they compose | Nora is **fine-tuned**, and whether it also retrieves is **not documented** — which decides whether an identified worker's payroll record leaves Kabini on every question | **Load-bearing** |
| 09 | [`09_classified_from_the_outside.md`](09_classified_from_the_outside.md) | A classification made from observed behaviour is marked, not deleted and not asserted | The Attestra check is **classic, asserted by the deployer and unconfirmed by the provider**, with an open item and a named owner | **Load-bearing** |

**Reference** is page 00, which is not taught in sequence — it is looked up, and appended to. **Grounding** pages say where the vocabulary comes from and how far it can be cited; a
room that already accepts model-versus-system can be given 01 in five minutes. **Load-
bearing** pages each produce one cell of the register that the room will otherwise fill
in wrongly, and 03 to 07 are the ones the section cannot be followed without.

---

## What every page carries

The idea in a paragraph · the real material, quoted and located · the example worked all
the way to its answer · one Mermaid diagram of the decision, using the real names ·
the turn, meaning the moment it lands and what to say while it is on screen · where the
same idea does real work in `../demo/` · and what learners reliably get wrong.

## Source keys, as the demo uses them

| Key | What it is | Where |
|---|---|---|
| **[PRJ]** | The fixed description of the teaching client, its four systems, its people and its data | `015_project/project.md` |
| **[BOK-2.1]** | IAPP AIGP Body of Knowledge and Exam Blueprint v2.1, approved 9 September 2025, effective 2 February 2026 | Text extract at `005_research/2026-09-07/extracts/aigp-bok-v2.1.txt`; its predecessor at `...aigp-bok-v2.0.1.txt` |
| **[DIFF]** | The itemised v2.0.1 to v2.1 change list | `005_research/2026-09-07/bok-v2.0.1-to-v2.1-diff.md` |
| **[RR]** | The dated research report, cited by section | `005_research/2026-09-07/report.md` |
| **[ISO-22989]** | ISO/IEC 22989:2022, AI concepts and terminology — a single-user licensed copy, bought and read 2026-09-09. Clause numbers may be cited; nothing may be quoted | `005_research/2026-09-07/extracts/pdf/official/` |

Line numbers quoted on these pages are line numbers in the two extract files, so a
trainer can put the source on screen in one `sed -n` and read the words the room is
being asked to take seriously.

**Kabini is a teaching client.** Kabini Workforce Services B.V., MatchScore, Nora,
Cadence, Attestra Inc., Halcyon AI, Inc. and the five named people were authored in
`015_project/project.md` and exist nowhere else. Every fact about them on these pages
resolves there. Facts about the certification and its blueprint are quoted from the
extracted IAPP text and located by line.

## Where these pages stop

The register stops at what each system **is**, and so do these. Nothing here names a
harm (use case 2), assigns developer, provider, deployer or user (use case 3), states a
risk tier (use case 26) or names a legal obligation or a date (use cases 27 and 28).
Page 06 in particular records that personal data sits outside the Union and draws no
conclusion from it; page 08 records whose name is on Nora's output as a fact and applies
no role label to it. Keeping those apart is the course's sequencing decision in
miniature, and a trainer who volunteers the conclusion early spends use case 3 arguing
with a room that already has an answer.
