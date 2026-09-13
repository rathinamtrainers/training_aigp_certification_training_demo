# Use case 1 — Take stock: what these four systems actually are

**AIGP Certification Training · Rathinam Trainers & Consultants**
**Section A of the Kabini AI Governance Pack** · Version 1.0.3 · Issued 2026-09-07,
revised 2026-09-09 (a correction release — what changed is in §7 of the register)

---

## What is in this folder

This is **the first section of the product the whole course builds** — the Kabini AI
Governance Pack. It is not a demo of the section and not a template for one: it is the
section, written out, filled in, dated, owned and sourced.

Nothing here needs installing, an account, a key or a network. It is Markdown, read in
any editor or rendered on a projector. That is the deliberate answer to the open
question the backlog left for the trainer — the pack is version-controlled in this
repository as Markdown rather than in Word or Google Docs, and that decision had to be
made before use case 1, not after [`015_project/use_case_plan.md` §6 item 8].

| File | What it is | Written from |
|---|---|---|
| **`A_ai_system_inventory_and_use_case_register.md`** | **The section.** Artefact A of the pack: the AI system inventory and use-case register, version 1.0.3. Four full records — AIS-001 MatchScore, AIS-002 Nora, AIS-003 the right-to-work check, AIS-004 Cadence — plus a summary table, eight findings, twelve open items with owners and dates, a scope statement of what version 1.0 does not say, change control and sign-off | `015_project/project.md` §1 and §3 for every Kabini fact; `005_research/2026-09-07/` for every vocabulary and blueprint claim |
| `A_annex_1_classification_rules.md` | The nine rules R1–R9 the register applied — govern the system not the model; agentic then generative then classic; the generative and agentic tests; training and inference recorded separately; when the as-is/fine-tuned/RAG/agentic axis does not apply; the four realisations told apart; marking a classification made from the outside | IAPP Body of Knowledge v2.1 indicator wording (Domains I.A and IV.A), the v2.0.1→v2.1 diff, and the research report |
| `A_annex_2_worked_repair_matchscore.md` | The AIS-001 entry written first as a **model** description and then repaired into a **system** description, field by field, with what each addition unlocks later in the pack. This is what the trainer builds on screen | The register's AIS-001 record; the "Demonstrated live" line of use case 1 in the backlog |
| `A_annex_3_room_worksheet.md` | The blank record the room fills for the other three systems, the question to push on for each, the four arguments to let the room have, and the two-minute close | The register and Annex 1 |
| `A_sources.md` | Every citation key — [PRJ], [UCP], [BRO], [BOK-2.1], [DIFF], [RR] — with what it is, where it was read, the date on it, how far it can be trusted, and a claim-by-claim table of what was taken from each | The repository's own dated material |

The use-case document for the trainer and the first slide of the deck is one level up at
`015_project/use_case_01/use_case.md`.

**There is no `.gitignore` in this folder, on purpose.** Every file here is the
deliverable and belongs in the commit.

---

## Read them in this order

1. `A_ai_system_inventory_and_use_case_register.md` — the section itself
2. `A_annex_1_classification_rules.md` — why each row says what it says
3. `A_annex_2_worked_repair_matchscore.md` — the live build
4. `A_annex_3_room_worksheet.md` — what the room does
5. `A_sources.md` — where everything came from

## How it is used in the room

Sixty minutes, per row 1 of `015_project/use_case_plan.md`. Roughly: fifteen minutes on
Annex 2 with the trainer building AIS-001 on screen and getting it wrong on purpose;
thirty minutes with the room filling the other three rows from Annex 3; fifteen minutes
reading the finished register back and closing on the open items.

**No software runs. Nothing is installed. There is no fallback needed**, because there is
nothing to fail.

---

## What somebody checking this should be able to verify

Each of these is checkable against files already in this repository, without taking
anybody's word for it.

1. **Four rows exist**, one each for MatchScore, Nora, the right-to-work check and
   Cadence — the four systems named in `015_project/project.md` §1 — and each carries a
   reference AIS-001 to AIS-004 that later artefacts can quote.
2. **Every row is described as a system, not a model.** Each record names the data going
   in, the data coming out, the interfaces and dependencies, the human oversight and the
   deployment context, not only the model. Test it the way Annex 2 does: if a row could
   have been written about the model alone, it fails.
3. **Every row carries a type** — classic, generative or agentic — **and the numbered
   rule that produced it.** Two are classic, one generative, one agentic. Every R-number
   used anywhere in this folder resolves to a rule in
   `A_annex_1_classification_rules.md`. Checkable mechanically:

   ```
   grep -oh "R[1-9]" *.md | sort -u        # R1 … R9, nothing else
   grep -o  "^## R[0-9] " A_annex_1_classification_rules.md | sort -u
   ```

   The two lists must have the same nine members.
4. **Every row names its realisation in the blueprint's own words** — as-is (AIS-003),
   fine-tuned (AIS-002), agentic architecture (AIS-004), and "not applicable, trained
   in-house" (AIS-001). The verbatim indicator wording those four come from is quoted in
   Annex 1 and located in `A_sources.md`.
5. **Every row separates training from inference** and says who performs each.
6. **Every row names an owner who is a person**, and where the owner is interim or
   appointed by the register rather than confirmed by `project.md`, it says so on the
   row.
7. **Every Kabini figure resolves to `015_project/project.md`** — 40,000 contract
   workers a year, 11,000 permanent staff, 2,300 of them in Bengaluru, eight years of
   placement outcomes, `eu-west-1`, the `ap-south-1` replica, Attestra Inc. of Delaware,
   Halcyon AI, Inc. There is no figure in this folder whose
   source is not named, and the only number carrying no source anywhere in the folder is
   the "accuracy 0.83" in Annex 2, which is shown as **the example of what to refuse**.
8. **Every blueprint claim resolves to the dated research** under
   `005_research/2026-09-07/`, and `A_sources.md` records which items are second-hand.
   In particular: ISO/IEC 22989 is named but **never quoted**. The reason changed on
   2026-09-09 and the rule did not. Originally the standard had not been read at all —
   `iso.org` returned HTTP 403. A single-user licensed copy has now been bought and read,
   and it confirms the attribution at clauses 3.1.4 and 3.1.23; but the licence prohibits
   reproduction, so a **clause number may be cited and a clause may not be quoted**. No
   verbatim 22989 wording appears anywhere in this folder, and none may be added.
9. **Version 1.0 makes no legal claim about any system.** Grep the register for
   "high-risk", "Article 50", "high-impact" and "restricted transfer": each appears
   **only** in §6 and only in a sentence saying this version does *not* claim it. §6
   names the use case that adds each — 2 for harms, 3 for roles per activity, 26 for
   risk classification, 27 and 28 for dates. Cross-border data movement appears in the
   rows as a **data-flow fact** (`ap-south-1`, Attestra's API, Halcyon's API) with the
   legal conclusion explicitly withheld.
10. **Twelve open items — OI-01 to OI-12** — each with a named owner, a due date and the
    use case that closes it, and no field in the register is simply blank. Checkable
    mechanically:

    ```
    grep -oh "OI-[0-9]*" *.md | sort -u          # OI-01 … OI-12
    ```

    Every one of the twelve must have a row in §5 of the register, and every row in §5
    must be referenced from at least one system record. Twelve is also the number stated
    in the register's change-control line and in `../use_case.md`; if those three
    disagree, the register is wrong by its own rule
    (`015_project/project.md` §5 item 14).
11. **Every one of the five artefact files carries a version, a date and a named owner**
    in its header, which is the pack rule set in `015_project/project.md` §5 item 14.
    This README is the folder's guide rather than a pack artefact, so it carries a
    version and dates but no owner: attributing a repository guide to Kabini's
    (fictional) General Counsel would be the wrong kind of accurate.
12. **Where an external figure has a weak source, the weakness is on the page.** The one
    external figure in this folder that is not blueprint wording is the exam's
    **100 questions / 85 scored** split, which gives the blueprint's 4–6 and 42–50
    question counts a denominator. Two things are marked, both on the `A_sources.md` row
    where the figure is used. First, `005_research/2026-09-07/report.md` §2.4 reads the
    split from an IAPP candidate handbook copy dated **2 April 2024** that is stale on the
    exam's structure — so nothing in this folder takes exam *structure* from that
    handbook. Second, **that the domain counts are counts of the 85 rather than of the
    100 is an inference** — they sum to 77–93, which brackets 85 — and it is written as an
    inference at every one of the three places it is used, not as something the IAPP
    states. Third, added 2026-09-09: the re-verification that used to be listed before the
    first sitting has been **done, and it went the wrong way**. The IAPP has discontinued
    the AIGP-specific handbook in favour of a general one that does not repeat the figure,
    and the AIGP designation page — the only place the new handbook says the count lives —
    carries none. The figure is unchanged and so is the hedging; what changed is that its
    weakness is now established rather than suspected.

## What the next use case inherits

Use case 2 appends the risk-and-harm profile to these same four rows. It should quote
the AIS references, keep the citation keys defined in `A_sources.md`, raise the register
to version 1.1, and add a line to the change-control table. It must not restate a fact
recorded here; a fact lives in one place in this pack.
