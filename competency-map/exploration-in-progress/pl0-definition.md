# Defining PL0

> **Cleanup note.** Scratch — see [`.scratch/HANDOFF.md`](../../.scratch/HANDOFF.md) for the
> current open-items index.

**[proposed]** — a definition for PL0 and the rules around it. Companion to
[`assessment-chatbot-gaps-and-decisions.md`](./assessment-chatbot-gaps-and-decisions.md), which
raises the need for this at G4 and G18.

Tags as in that document: **[decided]** = settled in discussion; **[verified]** = checked against
repo contents; **[open]** = unresolved; **[proposed]** = awaiting a decision.

---

## 1. Why PL0 needs defining

Three converging reasons:

1. **PL0 currently conflates two orthogonal things** **[verified]**. `dsai-source-tables.md:26`
   defines it as "not observed", and the panel form uses it to mean both "I saw no evidence" and
   "what I saw fell short of PL1".
2. **The bottom of the scale cannot be bracketed.** Under the threshold model, a level is located by
   evidence above *and* below it. PL1 has nothing beneath it, so "PL1, thinly evidenced" and "below
   PL1" are indistinguishable.
3. **Red flags at L2 are below-PL1 findings.** The veto in the green/red/pink model (D8) needs
   something to name: a red flag *is* the observation that a foundation is absent, and PL0 is the
   code for it.

   *Corrected:* an earlier draft justified PL0 by L1 assessment — "at L1 the lower bracket is the
   whole question". D15 undercuts that: no L1 failures have occurred, HR does not track L1, and L1
   panels are repeatable at will. PL0 earns its place at **L2 and above**, as the code for a red
   flag, not at L1.

## 2. PL0 is structurally different from the other levels

PL1→PL4 are distinguished by **cognition and scope**: Bloom's rungs, Dreyfus stages, a widening
problem space. Both ladders bottom out *at* PL1 — Bloom's has nothing below Remember, Dreyfus has no
stage below Novice.

So "below PL1" is not a worse kind of thinking. Someone below PL1 is attempting the same routine
tasks PL1 attempts. What is missing is **independence**. PL0 is therefore defined by **dependency**,
not by cognitive level, and that is the only place in the ladder where this is true.

## 3. Proposed definition **[proposed]**

Fits the existing grammar of `DSAI_PL` — same task scope as PL1, different means:

| Proficiency Level | Meaning |
|:---|:---|
| **PL0** | <ins>requires direct assistance</ins> in order to <ins>complete routine tasks</ins> |
| **PL1** | <ins>remember and apply basic skills</ins> in order to <ins>complete routine tasks</ins> |

**Level name:** *Assisted Execution* — in the register of Foundational Application, Independent
Application, Adaptive Synthesis, Generative Creation.

This completes a ladder already drafted in `TODO.md` (the "Reliability Rule"):

> **PL0: needs a person** · PL1: needs a guide · PL2: needs a problem · PL3: needs a goal

PL0 is where a document is not enough and a human has to intervene. In the culinary analogy used
elsewhere in the framework: they can chop what they are told to chop, but when the recipe says
"reduce by half" and they have not seen it done, the dish stops until someone comes over.

**No internal resolution.** PL0 deliberately does not distinguish "no capability at all" from
"capable only with help". The actionable fact is above/below the bar; the framework has no decision
that depends on how far below.

## 4. Separating PL0 from "not observed" **[proposed]**

These are independent axes and one code cannot carry both:

| | Observed | Not observed |
|---|---|---|
| **At or above PL1** | PL1+ | *currently indistinguishable from failure* |
| **Below PL1** | *no code exists for this* | *unrecorded* |

**Minimal fix:** keep one dropdown per row on the panel form, but with distinct entries — *Not
observed*, *PL0 (assisted execution)*, *PL1*, *PL2*… "Not observed" stops being a proficiency value,
which it never really was.

**Why it's worth the change: the remedy differs.**

* *Not evidenced* — they may well have the competency; it never reached the packet. Remedy:
  **present it**. ("Not observed" invites the reply "but I did do it" — the neutral term locates the
  gap in the packet, which is where the remedy is.)
* *PL0* — the capability isn't there. Remedy: **learn it**.

Same cell on today's form, opposite advice.

The "Community Building Definitions" table in `dsai-source-tables.md` has the same PL0 = "not
observed" entry and needs the same fix.

## 5. Aggregation and the guard are *general* rules, not PL0 rules

An earlier draft of this document claimed PL0 must be able to override higher evidence, and that
this made PL0 asymmetric with the other levels. **That was wrong** and is corrected here, because it
changes what needs ratifying.

### 5.1 The override is the general aggregation rule → belongs to G1

`TODO.md:136` ("Lowest Full Match") states it generally: *"if you make PL1 mistakes, you are a
PL1"* — mistakes **characteristic of** level n cap you at level n, whatever you demonstrated above.
That form applies at every level: PL2-characteristic mistakes cap you at PL2 even where PL3 work is
present. PL0 outranking PL2 evidence is simply the bottom instance of a rule that runs all the way
up. Nothing about it is specific to PL0.

**So this is not a PL0 decision.** It is the aggregation rule that
[`assessment-chatbot-gaps-and-decisions.md`](./assessment-chatbot-gaps-and-decisions.md) records as
**G1** — max (highest sustained evidence) versus min (lowest characteristic failure). Ratify it
there, once, for all levels.

### 5.2 The guard also generalises

Without a guard, every slip under time pressure becomes a ceiling. Real projects contain minor errors
that are rightly flagged but should not sink the candidate.

The guard follows from the reliability framing — the levels are about what is *reliable*, so:

> **The diagnostic is not the error. It is whether they recognise it when it is pointed out.**

Show them the temporal leakage. If they see it immediately, that is a lapse by someone who has the
foundations. If they still do not see the problem once it is on the table, the foundation is absent.

This is the same test as `TODO.md:97`: admitting ignorance at the boundary passes; not knowing there
*is* a boundary does not.

**It is not PL0-specific either.** Someone who makes a PL2-characteristic mistake and recognises it
the moment it is raised had a lapse, not a ceiling. The guard is the necessary companion to a min
aggregation rule at *any* level — without it, min-aggregation is brutal. Both belong together in G1.

### 5.3 What *is* actually asymmetric about PL0

Four things, none of them the override rule:

1. **A different axis.** PL1–PL4 are separated by cognition and scope; PL0 is separated from PL1 by
   dependency (§2). This is the real asymmetry.
2. **No positive demonstration path.** Nobody presents evidence of requiring assistance as a claim.
   PL1–PL4 are claimed and shown; PL0 is only ever **inferred** — from failures, from absence, or
   from the recognition probe.
3. **Never a target, only ever a finding.** PL0 appears in no `DSAI_MAP` cell. It exists only in the
   "exhibited" column, never the "required" one.
4. **No lower bracket.** Every other level is located by evidence on both sides of a threshold. PL0
   can only be fallen into, not located — an absorbing state at the bottom. Acceptable, because no
   decision depends on how far below the bar someone is.

### 5.4 The guard cannot be published to candidates **[decided]**

If candidates learn the guard, they learn a behaviour to perform: feign recognition, say they'll fix
it next time. Fake recognition is detectable, but **that is not the reason to withhold it** — the
reason is that the behaviour should not be encouraged in the first place, as a matter of principle.

**This cuts against a stated design goal** **[verified]**. `townhall.md:60-64` lists "Transparency of
evaluation criteria" and "Clarity of tech panel expectations (and explainability of outcomes)" among
the main goals of moving to rubrics.

**Proposed resolution: publish the criterion, withhold the probe.**

* **Publishable** — *"Assessment is of reliability, not of any single artifact. An isolated error,
  recognised and understood, is weighed differently from a systematic gap."* This is honest, tells
  candidates what is actually being assessed, and offers nothing to perform.
* **Not publishable** — the specific probe, and the inference drawn from the response to it.

Transparency of *criteria* does not require publication of *detection methods*. This is the standard
split between a public rubric and an assessor's guide, and the panel form is already marked
CONFIDENTIAL, so there is precedent.

### 5.5 The leakage problem **[open]**

Two consequences that follow, and neither is currently handled:

1. **This repository is the training package. Candidates read it.** Assessor-only material cannot
   live here — including, arguably, `dsai-tech-panel-form-l2.md`, which is marked CONFIDENTIAL while
   sitting in a repo whose purpose is to be read by the people being assessed. Needs a separate home
   for assessor material.
2. **A coaching chatbot is a publication channel.** If the skill can read the guard, and the skill
   coaches candidates, the guard leaks — no matter what mode it thinks it is in. A soft instruction
   ("do not use this in coach mode") is not a control.

   *Implication:* the coach-facing and assessor-facing tools should be **two separate skills with
   separate bundled files**, not one skill with modes. This supersedes the mode-switching design
   currently in `.claude/skills/dsai-competency/`. It is also the sharper form of the sponsor-recusal
   principle (`TODO.md:92`): not merely role separation, but information separation.

## 6. Indicators: this is the same work as the red-flag list **[proposed]**

Under the threshold model, PL0 needs behavioural indicators like every other level. Two layers:

* **Generic** (lives with the definition, in `DSAI_PL`): cannot reconstruct their own work; cannot
  self-unblock on mechanics; needs a person rather than a document. `TODO.md`'s L1 litmus test is
  most of a first draft:

  > "If you are blocked by standard syntax errors, library installation issues, or basic data
  > cleaning steps, and require a senior to unblock you on these 'mechanics', you are not yet fully
  > L1."

* **Per-competency**: these *are* the red flags — random split on temporally ordered data, training
  on a broken golden set, no held-out set, hardcoded paths, no version control of the cleaning
  script, out-of-order notebook execution.

So **writing PL0's indicators and writing the red-flag list (G9) are one piece of work**, not two.

Note the interaction with §5.4: the red-flag *list* is publishable and should be — telling people not
to leak their test set is pure benefit. It is only the **inference rule** (what a given response to
being shown a flag implies about proficiency) that stays in the assessor's guide.

## 7. The Specialisation exception **[decided]**

Specialisation has no PL1 **[verified]** — `DSAI_PL` starts it at PL2. This is **not an omission to
be filled**: it wasn't needed, and on inspection it should stay undefined.

**Why a PL1 in a specialisation isn't a useful construct.** The functional competencies are
*process* competencies — steps performed in every project. PL1 in a process step is coherent:
execute the routine version of it. Specialisation is a *domain* competency — a body of knowledge,
usually a special branch of ML or statistics, not a step.

At PL1, a domain and general competence are **not separable**. "Remember and apply basic skills to
complete routine tasks in NLP" describes someone competent in general ML who has read a library's
documentation. The specialisation adds nothing that couldn't be obtained by pointing an existing
PL1/PL2 practitioner at the docs for a weekend.

Testing it would therefore measure **the ability to pick up something new**, not proficiency in the
specialisation — a construct validity failure: the test would not measure what it claims to. It also
duplicates something the framework values elsewhere (self-directed learning) and would score it
under the wrong heading.

A specialisation only becomes a distinct thing once the work requires the domain's **own theory and
literature** — which is precisely what PL2 asks for (research, describe, benchmark, explain).

**Decision: Specialisation is intentionally floored at PL2.** State this in the source tables as a
design decision rather than leaving it to read as an accidental gap.

### 7.1 Consequence for bracketing

If Specialisation starts at PL2, a PL2 specialisation claim appears to have no lower bracket.

**Resolution:** the lower bracket comes from the corresponding **functional** competency, not from a
specialisation PL1. Someone claiming PL2 in NLP brackets it from below with their PL1 Machine
Learning or Statistical Analysis — they can do the general thing routinely, and the specialisation is
what they add on top. This is consistent with the L2 requirement already pairing a PL2 specialisation
with PL2/PL1 across the Stats/ML pair.

**Consequence for PL0:** below PL2 in a specialisation, the only available code is PL0, covering a
much wider band than elsewhere in the framework. PL0 is therefore **not uniform across rows** — a
wrinkle worth stating rather than hiding.

## 8. Open questions

* **[open]** Ratify the aggregation rule (G1) — min vs max — together with the guard (§5.2). This
  supersedes what an earlier draft framed as a PL0-specific override decision; see §5.1.
* **[open]** Where does assessor-only material live, given this repo is candidate-facing? (§6.2)
* **[open]** Does the two-skills split (§6.2) get built, or is the guard simply kept out of any tool
  candidates can reach?
* **[open]** Should PL0 appear in `DSAI_MAP` as an explicit floor, or only in `DSAI_PL`?
* **[open]** Does Technical Leadership / Community Contribution need the same PL0 treatment, or does
  "not observed" suffice there?
