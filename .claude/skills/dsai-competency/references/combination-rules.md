# Combination Rules

The grid is not seven independent cells. Verify these against
`competency-map/dsai-source-tables.md` (`DSAI_MAP`) and the target level's file — that's the
binding version; this is the working summary.

## Required proficiency by level

| # | Competency | L1 | L2 (Consultant) | L3 (STS) | L4 (LTS) |
|---|---|---|---|---|---|
| 1 | Data Project Design | PL1 | PL2 | PL3 | PL3 |
| 2 | Exploratory Data Analysis | PL1 | PL2 | PL3 | PL3 |
| 3 | Data Preparation | PL1 | PL2 | PL3 | PL3 |
| 4 | Visualisation and Data Storytelling | PL1 | PL2 | PL2 | PL2 |
| 5 | Statistical Analysis | PL1 | PL2 / *PL1* | PL3 / *PL1* | PL3 / *PL2* |
| 6 | Machine Learning | PL1 | PL1 / *PL2* | PL1 / *PL3* | PL2 / *PL3* |
| 7 | Specialisation | NA | PL2 ×1 | PL3 + PL2 | PL4 + PL3 |

## Rule 1 — Statistics and Machine Learning are a pair, not two cells

Rows 5 and 6 are assessed together. The candidate picks which one they lead with; the other must
still be demonstrated at the lower level.

| Level | Requirement | Satisfied by either |
|---|---|---|
| L1 | PL1 in both | (no choice) |
| L2 | **PL2 ×1 and PL1 ×1** | Stats PL2 + ML PL1 **or** Stats PL1 + ML PL2 |
| L3 | **PL3 ×1 and PL1 ×1** | Stats PL3 + ML PL1 **or** Stats PL1 + ML PL3 |
| L4 | **PL3 ×1 and PL2 ×1** | Stats PL3 + ML PL2 **or** Stats PL2 + ML PL3 |

Practical consequences:

- Asking "which of these two is your strong side?" early saves a lot of time — it determines which
  competency you probe hardest and which one only needs a floor.
- A candidate strong in both is not penalised, but they only need the pair satisfied. Don't send
  someone off to build ML evidence they don't need because their statistics carries the pair.
- The floor still has to be *shown*. "I know how to do a t-test" is not PL1 evidence; PL1 requires
  applying it in the work.
- At L3 the lower half of the pair stays at PL1 — the jump is in the leading competency only.

## Rule 2 — Specialisation counts differ by level

- **L1:** not applicable. Don't assess it.
- **L2:** PL2 in **one** specialisation.
- **L3:** PL3 in one **and** PL2 in a **second, different** specialisation.
- **L4:** PL4 in one **and** PL3 in a second.

The specialisation list (Text / Audio / Images-Video / Structured-Quantitative / Graph) is
explicitly non-exhaustive; each level file gives examples. If someone's work doesn't fit a listed
area, judge it against the PL descriptors rather than refusing to count it — but check that the
two claimed specialisations at L3+ are genuinely distinct areas and not one area described twice.

## Rule 3 — Key Tasks and Performance Standards are assessed too

The panel assesses **both** the Key Tasks and Performance Standards **and** the Key Competencies.
The Key Tasks sit at the top of each level file and differ substantially by level:

- **L1** — address well-defined problems (statement defined, methods identified, data available);
  independently complete routine tasks; good documentation and version control for KM.
- **L2** — design and run an end-to-end data project; address **specialised** operational problems
  (data significantly different or unavailable/masked; non-trivial operational use case; solution
  not commonly available); **plus Community Contribution**.
- **L3** — address complex *organisational* problems with deep analysis; **plus Technical
  Leadership** (guidance to your group); **plus Community Contribution**.
- **L4** — architect/design/lead development of a capability or product; **plus Technical
  Leadership** to senior management and working level; **plus Community Contribution** (growing the
  competency of the whole community).

Read the actual text each time. The L2 definition of "specialised problem" in particular is a real
bar: a well-defined problem solved competently with standard tools on clean available data may
satisfy every competency row and still not satisfy the Key Task.

## Rule 4 — Visualisation does not escalate

PL2 is the requirement at L2, L3 **and** L4. There is no PL3 target for this competency. Extra
effort here doesn't raise the level; spend it on the rows that do.

## Rule 5 — What the panel actually records

`competency-map/dsai-tech-panel-form-l2.md` records, per competency: required PL,
**exhibited** PL, and an observation/rationale. Exhibited PL can be recorded as PL0 ("not
observed") — which is the outcome for a competency the candidate simply never talked about, even if
they did the work. That is worth telling a candidate: *not observed* and *not done* look identical
on the form.

The form also captures Strengths / Improvements (shared with the candidate) and a nomination
recommendation (not shared). Don't draft the latter.

## Escalation cues between levels

Useful when someone asks "is this L2 or L3 work?":

- **Problem definition:** given (L1) → refined by the candidate (L2) → vague/conflicting and
  decomposed by the candidate (L3) → identified by the candidate as a strategic opportunity (L4).
- **Scope of impact:** own tasks (L1) → own project end-to-end (L2) → across the group /
  organisational change (L3) → a capability others build on (L4).
- **Method:** followed a known approach (L1) → chose among standard approaches on principle (L2) →
  synthesised a custom approach because none fit (L3) → created a generalisable one (L4).
