# 00 · Definitions

**Reference page · Use case 1 — Take stock: what these four systems actually are**
*Trainer material. Not part of artefact A, and it carries no artefact version or owner.*
*Started 2026-09-09. Source keys resolve in `README.md` of this folder.*

---

## What this page is, and the one rule it obeys

The vocabulary of use case 1, in one place, so that a definition is settled once and
then re-used rather than re-invented on a slide. It grows: later use cases append their
terms here rather than redefining a word this course has already fixed.

**The rule, and it is not negotiable.** Three sources sit behind these definitions and
they may be handled differently:

| Source | May it be quoted? |
|---|---|
| **The AIGP Body of Knowledge and Exam Blueprint v2.1** [BOK-2.1] | **Yes, verbatim.** The IAPP publishes it free. Quoted wording below is marked with `>` and is exact |
| **ISO/IEC 22989:2022** [ISO-22989] | **No.** The pack holds a single-user licensed copy; the licence prohibits reproduction. **A clause number may be cited and the sense paraphrased. No ISO wording appears below, and none may be added** |
| **This pack's own working definitions** | Yes, and they are labelled as ours |

That distinction is itself examinable behaviour, and concept 02 works through why.
Where a definition below is a paraphrase, it says so on its face.

---

## AI system

**Working definition, this pack's wording, grounded in [ISO-22989] clause 3.1.4:**

> An **AI system** is an engineered assembly that produces outputs — content, forecasts,
> recommendations or decisions — for objectives a human has set. It is the model
> **plus** the data used to build it, the data fed to it in operation, the outputs and
> what is done with them, the human oversight arrangement or its documented absence, and
> the deployment context it runs in.

**Where each part comes from.** The "engineered … generates outputs … for human-defined
objectives" shape is the sense of ISO/IEC 22989 clause 3.1.4, paraphrased. The list of
components is this pack's expansion, and it is what makes a register row answerable; it
is not a quotation from anybody.

**The six fields the definition forces you to fill.** A row that leaves any of these
blank is not an entry:

1. **Purpose** — the human-defined objective. What is it *for*?
2. **The model** — what it is, and who trained it.
3. **Data in** — split in two: the data it was **trained** on, and the data fed to it **in
   operation**. Different data, different sources, often different countries.
4. **Output, and what is done with it** — a score a person may ignore and a score that
   automatically rejects an applicant are the same number and two different systems.
5. **Human oversight** — who can see the output and overrule it. **"Nobody" is an
   answer, not a blank.** A system that acts with no per-step approval is still a system;
   it is a system whose oversight field reads *none*, and that is precisely what raises
   its stakes.
6. **Deployment context** — where it runs, in which country, in which domain, on whom.

**What the blueprint itself says, verbatim, and what it declines to say.** Sub-domain
I.A's first indicator is:

> "Know the generally accepted definitions and types of AI"

[BOK-2.1, Domain I.A]. "Generally accepted" is the blueprint **declining to publish a
definition of its own** — which is why the definition above is sourced to the standard
and to this pack rather than to the IAPP. Do not tell a room the IAPP defines "AI
system". It does not.

---

## AI model

**Working definition, this pack's wording, grounded in [ISO-22989] clauses 3.1.23 and
3.3.7:**

> An **AI model** is a representation — physical, mathematical or logical — of a system,
> process or body of data, which maps an input to an output. A **machine learning model**
> is the sub-case whose parameters were determined from data by a learning algorithm.

**Two corrections most people need.**

**It does not mean "neural network".** A logistic regression scoring loan applications is
a model. A decision tree with forty branches is a model. A gradient boosting ensemble is
a model. Transformers and diffusion models are models, but they are examples, not the
definition. Candidates who read "model" as "LLM" misclassify every classic system they
meet.

**It is not the estate.** "All the AI in our organisation" is an **AI estate** or a
**portfolio** — that is what the inventory as a whole describes. One model is one
representation; one system is one built thing. Neither word means "everything".

---

## AI model vs AI system — the difference, and why it is examinable

| | **AI model** | **AI system** |
|---|---|---|
| **What it is** | A representation that maps input to output | An engineered assembly serving a human-defined purpose |
| **Scope** | The weights, the equation, the learned mapping | The model **and** everything wrapped around it |
| **Has a purpose?** | No. A model computes; it does not intend | **Yes**, by definition — objectives set by a human |
| **Has an owner?** | Not meaningfully | **Yes.** A named person accountable for it |
| **Has a deployment context?** | No | **Yes** — country, domain, affected people |
| **Can it have human oversight?** | Not as such | **Yes**, and the answer may be *none* |
| **Unit of the inventory** | No | **Yes.** One system, one row |
| **What the regulator governs** | Rarely | **This** |

### The one-model-two-systems consequence

The same unchanged model, wired into a recruitment tool and into an IT helpdesk, is
**two AI systems**. Two rows, two owners, two oversight arrangements, two risk
conversations. One decides whether a person gets a job; the other says where the printer
driver is. Identical weights, entirely different stakes.

**Govern the model and you cannot express that difference. Govern the system and it is
visible in the first column.** That is the whole reason the distinction is on the exam,
and concept 05 works it through on Kabini's Nora and Cadence, which share one hosted
model and classify differently.

### Why v2.1 made this a Domains III and IV problem

Version 2.1 of the Body of Knowledge systematically replaced "AI model" with "AI system"
across Domains III and IV — six specific indicator rewrites, itemised in [DIFF] §5. Those
two domains together carry **21–25 questions each** [BOK-2.1], so a candidate who thinks
in weights is answering the wrong question across roughly half the paper. Concept 01
reads one of those rewrites line by line.

---

## Terms to be added as the course reaches them

Left deliberately empty rather than guessed, so that nothing here is defined before the
use case that teaches it: **classic / generative / agentic AI** (concept 04),
**training / inference** (concept 06), **as-is / fine-tuning / retrieval augmented
generation / agentic architectures** (concepts 07 and 08), **AI agent** and
**autonomy / heteronomy** (concept 04). Each gets the same treatment: this pack's
wording, the clause or indicator it rests on, and a note on whether the source may be
quoted.
