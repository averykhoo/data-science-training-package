# Errata and Corrigenda

Corrections and proposed amendments to the published competency map documents.

**Why this file exists.** The documents in this folder are copies of material that has already been
presented. They are a record, so they are not edited in place. Findings are logged here instead, and
folded in deliberately at the next revision.

**Scope.** Files in `competency-map/` other than this one and `exploration-in-progress/`. Working
notes and reasoning live in
[`exploration-in-progress/assessment-chatbot-gaps-and-decisions.md`](./exploration-in-progress/assessment-chatbot-gaps-and-decisions.md)
(symbols `D…`/`G…`, greppable) and [`../.scratch/HANDOFF.md`](../.scratch/HANDOFF.md).

Status: **[defect]** breaks something · **[stale]** no longer matches practice · **[wording]**
misleads · **[add]** missing · **[correct]** verified right, do not "fix" · **[fixed]** transcription
error already repaired in this copy.

**One exception to not editing in place.** Where the *original* was correct and the error was
introduced by OCR or format conversion, the copy is repaired directly — that restores fidelity to
the record rather than amending it. Such repairs are logged in section 0.

---

## 0. Corrections already applied to this copy

### 0.1 `PLO` → `PL0` in the panel form **[fixed]** — 2026-08-21

`dsai-tech-panel-form-l2.md`, both "not observed" cells, were written `PLO` with a letter O. The
other four dropdown values (`PL1`–`PL4`) transcribed correctly as digits, confirming a conversion
artifact rather than an error in the original. Repaired in place; two occurrences.

Note the code's *meaning* is separately under revision — see B3.

---

## A. Functional defects

### A1. Competency names disagree between the two source tables **[defect]**

`dsai-source-tables.md` — `DSAI_MAP` uses American spellings; `DSAI_PL` uses British:

| `DSAI_MAP` | `DSAI_PL` |
|---|---|
| Visuali**z**ation and Data Storytelling | Visuali**s**ation and Data Storytelling |
| Speciali**z**ation | Speciali**s**ation |

The other five match. This matters because the documented derivation in `dsai-l1.md`–`dsai-l4.md`
joins on the name:

```sql
INNER JOIN DSAI_PL ON DSAI_MAP.Competency = DSAI_PL.Competency ...
```

An inner join on those keys **drops rows 4 and 7** — Visualisation and Specialisation — which are
precisely the two rows present in the published level files. So the SQL as written cannot have
produced them.

Pick one spelling and use it in both tables. Across the folder there are currently four spellings of
the Visualisation competency and two of Specialisation.

### A3. Deprecated rows are still in the source table **[defect]**

`dsai-source-tables.md`, `DSAI_PL` retains struck-through rows: `~~PL3~~` for Visualisation and
`~~PL4~~` for Machine Learning. Legible to a human reading the page; a hazard for anything parsing
the table, and confusing to a candidate who finds a PL3 Visualisation descriptor that no level
requires.

### A4. Editorial note leaked into published text **[defect]**

`dsai-l2.md:128`, Data Preparation PL2, and its source at `dsai-source-tables.md:53`:

> handle imbalanced datasets e.g. oversampling/smote/adasyn *(todo: imbalanced-learn is covered in
> bseac, maybe mention that somewhere)*

---

## B. Statements that no longer match practice

### B1. Key Tasks are described as assessed, but are not scored **[stale]**

* `dsai-intro.md:28` — "Tech Panel will assess both the 'Key Tasks and Performance Standards' and
  the 'Key Competencies'."
* `dsai-update-townhall.md:565` — "All competencies must be explicitly demonstrated."

Actual practice (`D10`, `D18`): Key Tasks describe what is expected **of** an L2, not of someone
aspiring to be one. A candidate who already embodies them earns a green flag; not demonstrating them
fully is not a significant problem. They feed the subjective decision but nobody scores them.

This is the highest-value item in this file. A candidate who reads the published wording, prepares
Key Tasks evidence, and is assessed on something else has a legitimate complaint — and the
"published for over a year" argument cuts both ways.

Fixing this wording also resolves most of section C, since the vague intensifiers are concentrated
in exactly the sections nobody scores.

### B2. Community Contribution has three different statuses **[stale]**

| Source | Status |
|---|---|
| `dsai-l2.md` — listed as a Key Task | Not scored (per B1) |
| `dsai-tech-panel-form-l2.md` — a scored row, required **PL2** | Assessed |
| `dsai-source-tables.md`, `DSAI_MAP` | Absent — the table has 7 rows, none of them Community |

Decided (`D3`, `D9`): community contribution **is required**, and is the closest proxy for the
leadership dimension. It should be in the requirements table. Note that a separate "Community
Building Definitions" PL0–PL4 table already exists in `dsai-source-tables.md` and is not referenced
by `DSAI_MAP`.

### B3. PL0 conflates two orthogonal things **[stale]**

`dsai-source-tables.md:26` defines PL0 as "not observed"; the panel form uses it to mean both *no
evidence was presented* and *what was presented fell short of PL1*. These are independent axes and
the remedies are opposite — present it, versus learn it.

Proposal in [`exploration-in-progress/pl0-definition.md`](./exploration-in-progress/pl0-definition.md):
separate them, define PL0 as *"requires direct assistance in order to complete routine tasks"*, and
rename the observation status to **not evidenced**. The Community Building Definitions table carries
the same PL0 = "not observed" entry and needs the same treatment.

---

## C. Wording that misleads

All of these sit in Key Tasks / Performance Standards sections. If B1 is fixed and those become
explicitly forward-looking role descriptions rather than assessed criteria, intensifier language is
defensible there and most of this section can stand. C1 should be changed regardless.

### C1. "Mastery" is used at both L2 and L3 **[wording]**

* `dsai-l2.md:16` — "Demonstrate mastery of the data science process"
* `dsai-l3.md:28` — "Demonstrate mastery in understanding and applying choice of models / algorithms"
* `dsai-intro.md:43` — "Mastery in specific specialisation(s) is recommended ... (i.e. L2 and above)"

The same word at two levels gradates nothing. At L2 it is also wrong in kind: PL2 is *"understand and
apply concepts in order to solve well-defined problems"*, Dreyfus **Competent**. Mastery is PL4
language. A candidate self-calibrating against "mastery" will misjudge in both directions — some
will not apply, others will overclaim.

### C2. "Sufficient competency" is circular **[wording]**

`dsai-l2.md:45` — "Demonstrate sufficient competency in data science to solve non-trivial problems."
Sufficient for what, if not for the thing being assessed?

### C3. "Good knowledge" appears at two levels **[wording]**

`dsai-l2.md:63`, `dsai-l3.md:45`, `dsai-l3.md:59`. Undefined and identical across tiers.

---

## D. Terminology changes

| Current | Proposed | Why |
|---|---|---|
| "behavioural indicators" | **waterline indicators** | A waterline is what you stay above, not a target you hit. Floor-shaped, and it is already the term used in `exploration-in-progress/TODO.md`. Pair with the gloss "the level of work that should feel routine". |
| "not observed" | **not evidenced** | "Not observed" invites "but I did do it", and implies either the assessor missed it or the candidate lacks it. "Not evidenced" locates the gap in the packet, which is where the remedy is. |

---

## E. Missing sections

### E1. How to read the competency maps **[add]**

Nothing in `dsai-intro.md`, the four level files, or `dsai-source-tables.md` says how to read a
descriptor. The "not a checklist / neither necessary nor sufficient" statement exists only in a
townhall Q&A slide (`dsai-update-townhall.md:218,617-618`) and an unadopted draft in
`exploration-in-progress/TODO.md`.

Draft text ready at `D2.5`: competencies are mandatory at their specified level; bullets are
waterline indicators; three conditions (capability, complexity match, bracketing).

### E2. A fourth Guiding Principle for Assessment **[add]**

*Passing a project sets a precedent.* Draft at `D19`, to sit with the three principles in
`exploration-in-progress/bonus-content-proficiency-level-definitions.md`, with a candidate-facing
echo in `dsai-intro.md`.

### E3. Solution complexity commensurate to the problem **[add]**

Overcomplication is penalised in practice (`D14`) — reaching for an elaborate method without having
tried, or being able to rule out, the simpler one. Nothing says so. Cheapest home is as the explicit
converse of the existing "assess against problem complexity, not solution complexity" principle.

### E4. A requirements table **[add]**

`DSAI_MAP` is a **display** table — it drives what cells appear on each Confluence page, not what
the requirements are (`D11`). Conditional requirements are deliberately written into the `DSAI_PL`
prose instead. Consequently no single authoritative statement of the requirements exists; they are
distributed across four level files as prose.

Add a separate requirements table. Do **not** repurpose `DSAI_MAP` — it has a different job.

---

## F. Verified correct — do not "fix"

Things that look like errors and are not.

### F1. `DSAI_MAP` shows only the highest PL for conditional rows **[correct]**

Rows 5, 6 and 7 show `L2: PL2 / PL2 / PL2` and `L3: PL3 / PL3 / PL3`, losing the Stats-ML pairing
and the two-specialisation requirement. This is the documented convention stated above the table at
`dsai-source-tables.md:85` — record the highest requirement, elaborate the condition in the
write-up. Correct for a display table (see E4).

### F2. L3's Stats/ML rule is asymmetric with L4's **[correct]**

L3 requires PL3 ×1 **and PL1** ×1; L4 requires PL3 ×1 **and PL2** ×1. The lower half of the pair
stays at PL1 at L3 and rises only at L4. Confirmed intentional (`D3`).

### F3. Specialisation has no PL1 **[correct]**

Deliberate (`D4.5`). At PL1 a domain and general competence are not separable, so testing it would
measure the ability to pick up something new rather than the specialisation. Worth **stating** as a
design decision so it stops reading as an omission.

### F4. `DSAI_MAP` has seven rows **[correct]**

An earlier working note claimed six and no Specialisation row. Wrong — row 7 is Specialization. The
absent row is Community Contribution (B2), and the reason the documented SQL fails is the spelling
mismatch in A1, not a missing row.
