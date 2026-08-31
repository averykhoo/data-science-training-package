# Assessment Chatbot: Gaps and Decisions

> **Cleanup note.** Scratch. Written here because it was the fastest place to write, not because it
> belongs here. The settled parts need to move into the real maps and the rest needs pruning.
> **Nobody currently reads this repo** (`D-repo-unread`), so nothing here counts as published.
> Open items are indexed in [`.scratch/HANDOFF.md`](../../.scratch/HANDOFF.md). Changes needed in
> the **published** maps go to [`competency-map/errata.md`](../errata.md), not into those files —
> they are a record of what was presented.

Working notes from designing `.claude/skills/dsai-competency/` (a chatbot for preliminary
self-assessment against the competency maps). Records **decisions already made**, **gaps verified
against the repo**, and **new gaps this thread surfaced**.

Attribution is marked throughout: **[decided]** = settled by the framework owner in discussion;
**[verified]** = checked against repo contents, with file:line; **[open]** = not yet resolved;
**[proposed]** = suggestion awaiting a decision.

---

## Part 1 — Decisions

### D1. Purpose of the chatbot **[decided]**

A **self-assessment aid and tutor**, not an assessor. Rationale: there aren't enough mentors to
coach everyone, so access to "teaching to the test" is currently uneven and correlates with which
team someone landed in. Making a coach uniformly available doesn't remove the unfairness — it makes
it **equally unfair**, which is an improvement over unfairness that tracks org structure.

Scope of what it should help with:

* coach someone toward meeting the standard
* scope a project that should pass
* redesign a presentation to improve visualisation and storytelling
* refine a project still in its early phases

**The human panel remains the final gatekeeper on whether competencies have been met.** The
chatbot never decides.

### D2. The PL descriptors are examples; the PL *definition* is the criterion **[decided]**

`dsai-update-townhall.md:218,617-618` says the descriptors are "neither necessary nor sufficient"
and "not a checklist". The reason is that it isn't feasible to enumerate every way of reaching a
given PL — **not** that the standard is unspecified.

**None of the binding documents say this.** `dsai-intro.md`, all four level files and
`dsai-source-tables.md` contain no guidance on how to read the descriptors **[verified]** — the
statement exists only in a townhall Q&A slide and in an unadopted draft at the end of `TODO.md`.
That silence is the ambiguity. §D2.5 below is drafted to fix it.

The intended decidable criterion is the **PL definition** (`DSAI_PL`, e.g. PL2 = "understand and
apply concepts in order to solve well-defined problems") **together with the scope-of-work
description**. Those are meant to be sufficiently comprehensive. The bullets under each competency
are illustrative behavioural indicators.

Consequences:

* Assessment is analogical mapping of evidence onto an abstract criterion, not checklist matching.
  This suits an LLM better than a checklist would — and it avoids reinforcing the box-ticking the
  framework is explicitly trying to kill.
* "How many bullets must be met?" is the wrong question and needs no answer.
* What replaces it is a **calibration** problem: where does "well-defined problem" end and
  "open-ended problem" begin? Anchoring that needs real scored exemplars (see G11).

---

### D2.5. What "neither necessary nor sufficient" actually means **[decided]**

Draft text, intended for `dsai-intro.md`. Requested at `TODO.md:3` ("contrapositive definitions for
PLs so it's not taken as a checklist").

Two different things are being specified, and conflating them is what produces the checklist
reading:

| | Status | What it means |
|---|---|---|
| **The competency, at the PL in `DSAI_MAP`** | **Mandatory** | Every competency must be covered to at least the minimum level specified for the tier. There is no trading a surplus in one for a deficit in another. |
| **The bullets under each PL** | **Waterline indicators** | The level of work that should feel routine. Not a list to complete. |

#### The three conditions

A candidate demonstrates PL(n) in a competency when all three hold:

1. **Capability.** You need not have *performed* any particular
   bullet. But you should not be **unable** to do any of them had your project called for it. The
   bullets are not entry requirements; they are things you would be expected to handle if the work
   demanded them.

   *For assessors (the contrapositive):* "did X" does not imply PL(n) — that's the **not
   sufficient** half. "Is PL(n)" does imply "could do X if required" — so **"cannot do X" implies
   "not PL(n)"**. That is what makes the bullets binding without making them a checklist. Candidates
   need the plain version only: *you need not have done all of these, but you should not be unable
   to do them.*

2. **Complexity match.** What you *did* demonstrate must sit at the same complexity class as the
   PL definition. Work of the right kind at the wrong difficulty doesn't count — this is the
   existing principle that assessment is against *problem* complexity, not solution complexity.

3. **Bracketing.** See below.

#### Bracketing: locating a person, not just clearing a bar

A PL is a **threshold**, and the assessment is a measurement problem: to say *where* someone is,
rather than merely that they cleared something, you need evidence on **both sides** of the
threshold.

* **Points above the threshold** — evidence against the current PL's indicators.
* **Points below the threshold** — evidence against the *previous* PL's indicators.

Both are required. Evidence at PL2 alone does not establish PL2, because solid PL1 foundations are
**not implied** by an impressive PL2 artifact. This is the same principle as the "Lowest Full
Match" proposal (`TODO.md:136`): someone can produce sophisticated work and still make basic
errors, and the basic errors govern. The lower bracket is a genuine check, not a formality.

*Corollary:* an **upper** bound comes from the absence of the next level's behaviours. Evidence at
PL2 with nothing at PL3 supports "PL2". Evidence at PL2 with no PL3 probing attempted supports only
"at least PL2" — which is why panels probe past the claimed level. A preliminary evaluator should
distinguish these two verdicts rather than reporting both as "PL2".

This framing is also what makes the exemplars in G11 load-bearing: with an abstract criterion,
scored real packets function as anchor points on the scale.

#### Where this leaves PL0 **[open — gap]**

**PL1 has nothing below it to bracket against.** There is no descriptor for what falling short of
PL1 looks like, so the lower bracket that every other level gets is unavailable at the bottom of
the scale. See G4 and G18.

### D3. Level requirements, restated **[decided]**

Minimum requirements are those in `DSAI_MAP`, with the pairing conditions:

| Level | Stats / ML requirement | Specialisation | Community |
|---|---|---|---|
| L1 | PL1 in both | n/a | *should exist — see G6* |
| L2 | PL2 ×1 **and** PL1 ×1, either order | PL2 ×1 | *should exist* |
| L3 | PL3 ×1 **and** PL1 ×1, either order | PL3 + PL2 | *should exist* |
| L4 | PL3 ×1 **and** PL2 ×1, either order | PL4 + PL3 | *should exist* |

`DSAI_MAP` was produced early and **does not include Community Contribution, but it should**
**[decided]**. See G6.

### D4. All four tiers are evaluated **[decided]**

**L1 is an evaluated tier**, not just an entry state. L3 and L4 are also real, but have very few
candidates, so they are lower priority. Focus so far has been on L2.

Implication for the skill: L1 must be first-class, not an afterthought. Current reference material
(`elicit.md`, `worked-examples.md`) is L2-centric and needs L1 coverage.

### D4.5. Specialisation is intentionally floored at PL2 **[decided]**

Specialisation has no PL1 **[verified]**. This is not an omission to be filled — it wasn't needed,
and a PL1 in a specialisation isn't a useful construct: at that level, domain knowledge and general
competence aren't separable, so testing it would measure *the ability to pick up something new*
rather than the specialisation itself. A specialisation becomes distinct only where the work needs
the domain's own theory and literature, which is what PL2 already asks for.

Bracketing a PL2 specialisation therefore draws its lower bound from the corresponding **functional**
competency, not from a specialisation PL1. Full reasoning in
[`pl0-definition.md`](./pl0-definition.md) §7.

### D4.6. The lapse-vs-absence guard is assessor-only **[decided]**

The guard that distinguishes a one-off error from an absent foundation (recognition when the error
is pointed out) **must not be published to candidates**. Not because feigned recognition is
undetectable — it isn't — but because the behaviour shouldn't be encouraged in the first place, as a
matter of principle.

This cuts against "Transparency of evaluation criteria" (`townhall.md:60-64`) **[verified]**.
Proposed resolution: **publish the criterion, withhold the probe** — candidates are told that
assessment is of reliability rather than of any single artifact, and that a recognised isolated error
is weighed differently from a systematic gap; they are not told the probe or the inference drawn from
it. See [`pl0-definition.md`](./pl0-definition.md) §5.4.

Two consequences, both **[open]** — see G19.

### D7. Panel composition and voting **[decided]**

| Tier | Panel | Pass | Escalation |
|---|---|---|---|
| **L1** | 1 panelist **+ one of the candidate's supervisors** | *unstated — see G20* | *unstated* |
| **L2** | 3 panelists | 3 of 3 | 2 of 3 → **DSAI track lead** makes the final call |
| **L3** | 5 panelists | 4 of 5 | 3 of 5 → **DSAI track lead** |
| **L4** | *unstated — see G27* | | |

**L2 and L3 also seat a neutral third party.** Their job is to watch the *process* — blatant signs
of collusion with, or bias against, the candidate. They do not give technical judgements, though
they may ask a few questions if the presentation is not clear to them.

This answers question C of G1. Note the escalation thresholds are not vetoes: a single dissenter
does not fail the candidate, it moves the decision to the track lead.

### D8. The evidence model: green, red and pink flags **[decided]**

Practice is **positive-evidence-led**, closer to option A1 than A2. Assessors look for signs the
candidate did something matching the descriptors; the discussion afterwards is about whether *what
they did* constitutes meeting *some bullet*, and whether there is enough to bump them up — absent
red flags showing they are clearly not at the level.

Three kinds of finding:

* **Green flag** — positive evidence. Establishes *"at least PL(n)"*.
* **Red flag** — establishes *"no higher than PL(n)"*. A veto.
* **Pink flag** — a weak negative: something the project called for that was not done. **Not
  penalised on its own.** Pink flags *accumulate*; enough of them, spread across the work, signal
  that the candidate is not yet at the level.

Not doing something is only a pink flag if **the project required it**. The bullets are not
mandatory to demonstrate — but the candidate should not be *unable* to perform them had the project
required it, and by extension should have *known to* do them when required.

So the assessment reads both sides of the specific cutpoint the candidate is trying to clear:
positive evidence that they are at least there, negative evidence that they are no higher. It is
not a count, and not a max. It is unavoidably somewhat subjective.

### D9. The real criterion is performative **[decided]**

The competency grid is a proxy. Two questions are actually answered in the room:

> **1. Autonomy.** *"Would I feel comfortable giving them an arbitrary DSAI project and letting them
> run it autonomously?"*
>
> **2. Exemplarity.** *"Would the way they do their projects make a good example for others to
> follow?"*

Both are **performative descriptions, not competency descriptions**, and neither is written down.

**On exemplarity.** An earlier draft phrased this as "would they correctly guide a junior", which
conflates competency with coaching — mentoring ability is heavily personality-driven and is not what
the panel is measuring. The correct framing is a property of *the work*, not of the person:
**every project the panel passes is implicitly a stamp of approval that this is the right way to do
things**, and the panel is endorsing how the project was run. This has been discussed explicitly
between assessors.

That makes the panel an **endorsement** decision, not only a measurement one — which is part of why
red flags act as vetoes (D8). You cannot endorse work with a visible unaddressed flaw, however
strong the candidate is elsewhere.

**Technical Leadership is deliberately excluded at L2.** L2s are expected to display it, but they
inherit that responsibility *after* becoming L2, so it is intentionally not a panel criterion for
entry. **Community contribution is required, and is the closest proxy.** Exemplarity is therefore
*not* Technical Leadership under another name — it is a property of the artifact, assessable from
the artifact.

**On "arbitrary".** The word carries most of the weight. The panel wants a **predictor of whether
the candidate can generalise** — not whether this particular project was complex enough, nor whether
the presentation was sufficiently polished. This is the strongest argument for the portfolio
approach (D6): more samples, better generalisation estimate.

### D14. Overcomplication is penalised **[decided]**

Implicit but real. Jumping straight to graph neural nets to cluster friends in a social network,
based on some paper the candidate found, without having tried Jaccard or anything simpler — and
being unable to justify why the simpler option was not feasible or appropriate — counts against
them.

Note this is `TODO.md`'s proposed PL3 "Parsimony" trait, but operating at L2 **as a penalty** rather
than as a positive competency. It currently has no home in any descriptor. See G29.

### D15. L1 panels are low-stakes **[decided]**

* **No L1 failures have occurred.** The only route to failing is being blatantly unable to get work
  done — in which case the candidate would have no work to present in the first place.
* A candidate has been asked to present again after covering incorrect material.
* **HR does not track L1**, only L2 and above.
* **L2+ panels run on a 6-month cycle; L1 panels can happen any time and be repeated.**

Consequently L1 is taken considerably less seriously, and send-back friction (D13) applies to L2+
only. This lowers the priority of G20 and changes the motivation for PL0 — see the note in
[`pl0-definition.md`](./pl0-definition.md) §1.

### D16. One large project is an acceptable alternative to two **[decided]**

Two projects are strongly recommended, matching `dsai-slide-template.md`. Some candidates present a
single large project instead, which is fine.

### D10. Key Tasks are not explicitly assessed **[decided]**

They feed the subjective decision, but no one scores them. **This diverges from the published
framework** — see G24.

### D11. `DSAI_MAP` is a display table, not a requirements spec **[decided]**

It exists to drive lookup and display on Confluence: *what cells do I show on each page*, not *what
are the requirements*. That is why the Stats/ML conditional is not in it — the alternative was
written into the PL descriptor prose instead. Resolves most of G3; creates G23.

### D12. Exemplars already exist, outside this repo **[decided]**

* A Confluence page, *"how to L2"* — described as pretty decent, and containing **sample
  presentations from 2 past successful candidates**.
* A long archive of **almost all L1 presentations**, roughly 50–100. The overlap between those and
  what would pass an L2 panel is *maybe 1 or 2*. So it is a strong negative-example corpus for L2 —
  and, since L1 is an evaluated tier (D4), a positive-example corpus for L1.

**Important caveat.** The L1 presentations are *successful L1 attempts*, not *failed L2 attempts* —
they were explicitly never aiming at L2. As calibration data they are clean **lower-bracket
anchors**, but they are not examples of the near-miss cases that are actually hard to judge. See
G30.

Substantially closes G11, subject to G25, G26 and G30.

### D13. Send-backs are discouraged **[decided]**

Candidates have been sent back to rescope and re-present when competencies were not observed, but HR
strongly dislikes it. With the competency map published for over a year, ignorance is no longer an
excuse. Consequence in G24 and Part 6.

### D17. L1 projects are structurally ineligible for L2 **[decided]**

A candidate's onboarding project — which is also their L1 project — **cannot be used for L2**, by
explicit standing instruction. L1 projects are usually *intentionally scoped to be easy*.

This strengthens D12: the L1 archive is not a corpus of failures but of **deliberately easy work**,
which makes it a clean anchor for "this is L1 scope, and hence not enough for L2". Confirmed intended
use. It also softens G30 — the archive was never meant to contain near-misses.

### D18. Key Tasks describe what is expected *of* an L2, not of an aspirant **[decided]**

This resolves G24. Key Tasks and Performance Standards are **forward-looking role descriptions**, not
entry criteria. A candidate who already embodies them earns a **green flag**; not demonstrating them
fully is **not a significant problem**.

Same logic as the deliberate exclusion of Technical Leadership at L2 (D9): responsibilities inherited
*after* appointment are not gates *for* appointment.

**Community contribution is the exception** — it is required at entry, and is the closest available
proxy for the leadership dimension.

What remains is a documentation problem, not a policy one: `dsai-intro.md:28` and `townhall.md:565`
both say the panel assesses Key Tasks. That wording needs to change to match.

### D19. Where exemplarity goes **[proposed]**

Answers G28. **Not** a Performance Standard — those are now established as non-binding (D18), and
exemplarity *is* used in the decision. **Not** a functional competency — it is a property of the work
that cuts across all seven. It belongs as a **fourth Guiding Principle for Assessment**, alongside
the three in `bonus-content-proficiency-level-definitions.md`, with a candidate-facing echo in
`dsai-intro.md`.

Draft text:

> **4. Passing a project sets a precedent.** A pass is not only a measurement of the candidate; it
> is an implicit statement that this is a legitimate way to do the work. Ask: *would this be a sound
> precedent — if a junior copied how this project was run, would that serve them well?*
>
> This is a property of **the work**, not of the candidate's ability to mentor — coaching is largely
> a matter of personality, and technical leadership, though expected of an L2, is inherited after
> appointment rather than required for it.
>
> Two consequences. A visible, unaddressed flaw weighs more heavily than pure measurement would
> suggest, because the panel cannot endorse it. And **the complexity of the solution should be
> commensurate to the problem**: an elaborate approach adopted without having tried — or being able
> to rule out — the simpler one is not a precedent worth setting, however well executed.
>
> The test is soundness, not preference. A reasonable alternative approach, defended on its merits,
> sets a perfectly sound precedent. "I would have done it differently" is not an objection;
> "someone following this would come to grief, and here is why" is.

The final paragraph is a deliberate guard: without it, "not exemplary" becomes a socially acceptable
way to say "not how I would have done it", and the criterion turns into a conservatism ratchet.

### D20. Solution complexity should be commensurate to the problem **[decided]**

Resolves G29. Preferred phrasing, folded into D19's draft. Cheapest home is the existing principle
that assessment is against *problem* complexity rather than *solution* complexity — this makes the
converse explicit rather than adding a new rule.

### D21. Escalation and the neutral observer, in practice **[decided]**

* **Track lead on escalation:** looks at the slides and makes a decision after some thinking. No
  formal procedure, and none is felt to be needed. Closes most of G21.
* **The neutral observer has never vetoed a panel.** The one intervention heard of was not about
  bias or collusion: the candidate, asked why they wanted the appointment, said they did not — their
  boss had sent them — and on questioning turned out to genuinely prefer not to take it. See G32.

### D22. One large project is fine; coverage is the constraint **[decided]**

No penalty from the panel for presenting one project rather than two. The practical difficulty is
that unless the project was exceptional, or was a chain of smaller projects leading to one outcome,
sufficient **coverage** is hard to reach — which works against the candidate. Standing guidance
remains: recommend two, unless the project is huge and covers everything.

### D23. There is no central archive of past panels **[decided]**

Answers G30. One assessor keeps a personal store of what they have seen; there is no good central
list. The near-miss corpus therefore does not exist and cannot be assembled retroactively without
effort.

### D24. Code review is wanted but does not scale, and some code cannot be shared **[decided]**

Code review is desired. It is not scalable with the assessor time available, and **some code is
sensitive and cannot be shared at all**. This is a hard constraint on any artifact-based assessment,
automated or otherwise. See G31.

### D-repo-unread. Nobody reads this repo **[decided]**

Despite being the onboarding guide. Nobody reads git history either. Two consequences:

1. Writing something here does not make it communicated. The "published for over a year" argument
   (D13) rests on Confluence, not on this repo.
2. Git history is not viable as an integrity signal in this culture, whatever its technical merits.

### D25. Skill work is on hold **[decided]**

Sort out the maps first. `.claude/skills/dsai-competency/` stays as built, unmodified, until then.

### D5. Organisational context is self-reported **[decided]**

The chatbot cannot verify whether a problem was genuinely hard, whether data really was unavailable,
or whether a solution really wasn't commonly available. For a preliminary self-assessment this is
acceptable — the candidate self-reports and the panel verifies. The chatbot should make its
dependence on self-report explicit rather than pretending to have judged it.

### D6. Multiple artifacts, with timestamps **[decided]**

Input is not one deck. It is **multiple slide decks, code repositories and other artifacts, each
timestamped**, because people develop over time. Early repos may be below the current standard yet
still demonstrate a quality that should be attributed to the candidate.

See G12–G14 for the rules this requires that don't exist yet.

---

## Part 2 — What this makes feasible

Recorded so the next person doesn't re-litigate it.

### Now in reach (was not, with a single deck)

* **Probing for the "why".** The PL1/PL2 boundary is justification under questioning. A chat can
  do this; a static deck cannot. This was the single largest objection to automation and
  interactivity substantially answers it.
* **Reliability vs peak performance.** The contrapositive framing (`TODO.md`, "The Struggle Test")
  says a level is about what no longer requires struggle. One artifact samples peak performance.
  **Multiple artifacts across time is the right sample** — a behaviour present in three of four
  projects is reliability evidence; once is not.
* **Integrity signal from git history.** Commit cadence and authorship distinguish incrementally
  owned work from a single-dump "initial commit". This is mechanically available, needs no
  panelist time, and partly addresses the "polished turd" problem that `TODO.md:91` raises and the
  scalable-code-review problem at `TODO.md:155` that has no affordable answer.
* **Coverage triage and presentation-gap detection.** Which competencies have no evidence at all,
  and which work exists in a repo but never reached a deck. Given PL0 = "not observed", the second
  is high-yield and nobody currently does it.

### Still out of reach

* **A verdict.** By design (D1) and by the framework's own statement (D2).
* **Limit testing.** `TODO.md:96` wants the panel to probe until the candidate fails, distinguishing
  honest "I don't know" from BS. A chatbot can probe, but a candidate can **abandon an uncomfortable
  line of questioning** in a way they cannot with a panel. See G13.
* **Verifying problem complexity.** Self-reported (D5).
* **Community contribution evidence.** `townhall.md:610` — "the DSAI community is small, so we'll
  usually just know." Lives entirely outside the artifacts.

### Risks of the "equally unfair" design **[proposed mitigations]**

1. **Coach/judge conflict of interest, rebuilt in software.** `TODO.md:92` requires sponsors to
   recuse from panels; `TODO.md:95` says sponsors give verdicts, not solutions. If one skill both
   coaches and pre-assesses, the same conflict returns. *Mitigation:* keep coach mode and assessor
   mode separated, and make coach mode give "you are not ready because X" rather than "change X to
   Y", forcing the candidate to do the synthesis. The skill already switches modes; the asymmetry
   is not yet enforced.
2. **Vocabulary inflation.** Candidates learn to say "I validated the underlying assumption"
   without having done it. *Mitigation:* the skill must probe for the specific instance, never
   accept the general claim — same tactic the panel uses.
3. **Deck inflation.** Everyone's presentation improves, so the deck stops discriminating. Largely
   benign: the 15/45 split already treats the deck as non-decisive, and this moves panel time from
   decoding bad slides to probing. Worth being explicit that this is intended, not a side effect.
4. **Rubric entrenchment.** If everyone optimises against the map, the map's blind spots become the
   organisation's. Raises the priority of G6 (community, tech leadership, code craftsmanship).
5. **Same model coaches and answers.** A candidate can ask the model to generate the justification
   it will later ask for. Not fatal — articulating it is part of learning it — but it is exactly the
   gap between "can produce the words" and "owns it" that the human panel exists to close.

---

## Part 3 — Verified gaps in the repo

Ranked by how much they block a working preliminary evaluator.

### G1. No aggregation or decision rule anywhere **[verified] [open]**

No pass threshold, no panel size, no tie-break, no statement of what a PL1 in a required-PL2 row
does to the outcome. Two candidate rules exist in the repo and they are different:

* `townhall.md:565` — "All competencies must be explicitly demonstrated" (a **coverage** rule)
* `TODO.md:136` — "Lowest Full Match: if you make PL1 mistakes, you are a PL1" (a **min** rule,
  in exploration-in-progress, unadopted)

Neither is authoritative. D2 softens this — the chatbot doesn't decide — but a coach still has to
tell someone whether one weak row sinks them, and currently there is no answer to give.

**Two further things belong to this decision, not to PL0** (see
[`pl0-definition.md`](./pl0-definition.md) §5):

* **The override.** "Lowest Full Match" is general: mistakes characteristic of level n cap you at
  level n whatever sits above. A PL0 finding outranking PL2 evidence is just its bottom instance.
* **The guard.** A min rule is brutal without one. The lapse-vs-absence test — *does the candidate
  recognise the error when it is pointed out?* — is what separates a slip from a ceiling, and it
  applies at every level, not only at the bottom.

Ratify these once, here, for all levels.

### G2. `townhall.md:565` and `townhall.md:618` are in tension **[verified] [open]**

"All competencies must be explicitly demonstrated" vs "the descriptors are neither necessary nor
sufficient". Both in the same deck. D2 resolves most of it — coverage of *competencies* is
mandatory, satisfaction of *bullets* is not — but that resolution isn't written down anywhere
binding.

### G3. `DSAI_MAP` cannot be read literally **[verified] [open]**

* Rows 5 and 6 both show **PL2 at L2 and PL3 at L3**, with the Stats/ML conditional absent. This is
  by documented convention (`dsai-source-tables.md:85`: record the highest PL, elaborate the
  condition in the write-up) but it is **lossy** — anything reading the table gets the wrong
  requirement.
* **Corrected:** an earlier draft claimed `DSAI_MAP` has only six rows and no Specialisation. It has
  **seven**; row 7 is Specialization. The absent row is **Community Contribution**.
* The documented SQL derivation *is* broken, but for a different reason: `DSAI_MAP` uses American
  spellings (Visuali**z**ation, Speciali**z**ation) while `DSAI_PL` uses British. An inner join on
  `Competency` drops exactly those two rows — the two that do appear in the published level files.
  Logged as `errata.md` A1.
* `DSAI_PL` retains struck-through deprecated rows (`~~PL3~~` Visualisation, `~~PL4~~` ML).
* Specialisation has **no PL1** defined at all.

### G4. PL0 conflates two orthogonal things **[verified] [open]**

Defined as "not observed" (`dsai-source-tables.md:26`), and used on the panel form to mean both
"I saw no evidence" and "the evidence I saw fell short of PL1". These are independent axes:

| | Observed | Not observed |
|---|---|---|
| **At or above PL1** | PL1+ | *unrecorded — looks identical to failure* |
| **Below PL1** | *no code for this* | *unrecorded* |

One code cannot carry both. **[proposed]** Separate them: an observation status (observed / not
observed) and a proficiency value where PL0 means *genuinely below PL1*. Consequence for candidates
either way: on the current form, *not observed* and *not done* are indistinguishable.

> **A proposed definition now exists: [`pl0-definition.md`](./pl0-definition.md).** It covers the
> definition, the separation from "not observed", the override rule, the lapse-vs-absence guard, the
> confidentiality problem the guard creates, and the merge with G9.

### G18. No descriptor for "below PL1" — the bottom of the scale can't be bracketed **[open]**

Follows directly from D2.5. Every level from PL2 up is located by evidence above and below its
threshold. PL1 has no level beneath it, so the lower bracket is unavailable: there is no statement
of what falling short of PL1 looks like, and therefore no way to distinguish "PL1, thinly
evidenced" from "below PL1".

There is a drafted starting point — the contrapositive litmus test for L1 at the end of `TODO.md`:

> "If you are blocked by standard syntax errors, library installation issues, or basic data
> cleaning steps, and require a senior to unblock you on these 'mechanics', you are not yet fully
> L1."

That is a usable PL0 descriptor and is currently unadopted. This matters more now that L1 is
confirmed as an evaluated tier (D4): L1 is the one assessment where the *lower* bracket is the
whole question, and it's the bracket that doesn't exist.

### G5. Stats vs ML is defined three incompatible ways **[verified] [open]**

* `townhall.md:574` — by objectives, tasks, outcomes, libraries
* `TODO.md` §1B — Breiman's two cultures: by **intent** (inference vs prediction) and **validation
  direction** (ex ante assumption-checking vs ex post generalisation)
* `stats-vs-ml.md` — a third treatment

`TODO.md` §1A additionally proposes **moving experiment design out of Statistical Analysis into
Data Project Design**, which would rewrite the L2 Stats PL2 descriptor. Unadopted.

Consequence: "which row does this evidence count toward?" is genuinely undecidable for logistic
regression, LDA, or Bayesian work — and this is the row with the conditional pairing, so it changes
whether someone meets the level.

### G6. Ancillary competencies are half-integrated **[verified]; inclusion of Community **[decided]**

* Technical Leadership, Community Contribution and Code Fluency have full PL ladders in
  `ancillary-competencies.md`.
* Community Contribution appears as a **scored row with a required PL2** on
  `dsai-tech-panel-form-l2.md`.
* It is **not** among the seven functional competencies in `dsai-intro.md` and has **no `DSAI_MAP`
  row**. There is a separate "Community Building Definitions" PL0–PL4 table in the source tables,
  and PL descriptions by level in `townhall.md:358`.

So the form scores something the map doesn't define. **Decision: community should be in `DSAI_MAP`.**
Still open: whether Technical Leadership and Code Craftsmanship also become rows, or stay as Key
Tasks. Code craftsmanship is repeatedly cited as a failure mode (`TODO.md` items 1, 11 and the
entire "scalable code review" section) and appears in no map.

### G7. No rule for what makes two specialisations "distinct" **[verified] [open]**

L3 requires PL3 in one and PL2 in a second. The list is explicitly non-exhaustive. Are Text/NLP and
IR/RAG one specialisation or two? No adjudication procedure.

### G8. "Specialised problem" and "sizeable dataset" are undefined thresholds **[verified] [open]**

"Specialised problem" is the load-bearing term in the L2 Key Task, given as three examples with no
test. `TODO.md` item 4 wants a dataset size requirement as a filter against toy problems; unset.

### G9. No red-flag / disqualifier list exists **[verified] [open]**

`TODO.md` asks for one at least twice ("contrapositive definitions... maybe codify red flags";
"Red Flag Checks... training on a broken golden set"). Highest-value missing item for automation,
because disqualifiers are the one thing a machine can judge outright: temporal leakage, no held-out
set, training on a broken golden set, hardcoded paths, out-of-order notebook execution.

### G10. Slide template and panel form are organised on different axes **[verified] [open]**

Template is narrative (background / methodology / outcome); form is per-competency. No crosswalk
exists. This is mechanically why work gets recorded as PL0 — the candidate presents it, but not
where the assessor is looking for it.

### G11. No real scored exemplars **[verified] [open]**

Nothing in the repo maps a real project to the grid. The three in
`.claude/skills/dsai-competency/references/worked-examples.md` are invented and labelled as such.
Under D2 this is now the **most important** missing artifact: with the criterion abstract rather
than enumerable, exemplars are what calibrate both humans and models. Few-shot anchors beat more
rubric prose.

### G12. Syllabi unreconciled with the maps **[verified] [open]**

`syllabus.md`, `syllabus_2025.md`, `competencies.md` lag the competency maps. Handled in the skill
by an explicit precedence rule (map wins; syllabi advisory), but the underlying inconsistency
remains. `TODO.md` §3 wants modernisation (archive Kaldi/GMMs, shift NLP to transformers/LLMs,
retire Titanic for leakage, introduce dirty internal mocks).

---

## Part 4 — New gaps surfaced by the multi-artifact decision (D6)

None of these are addressed anywhere in the repo.

### G13. No recency or staleness rule **[open]**

How old can evidence be? A 2019 ASR project on Kaldi may have been PL3 work then and may not
evidence current proficiency. This cannot fall back on years-in-service, because `townhall.md:646`
explicitly rejects time norms. Needs an actual rule, e.g. a recency window for the *leading*
competency and none for *floor* evidence.

### G14. No rule for attributing qualities from below-standard artifacts **[open]**

Stated directly in discussion: early repos may be below standard yet demonstrate a quality that
should still be attributed. Three distinct uses that need distinguishing:

1. **Floor evidence** — an old repo cheaply establishes the PL1 half of the Stats/ML pair.
2. **Growth evidence** — the *delta* between early and recent work evidences self-directed learning
   (Fink's "Learning How to Learn"; the Dreyfus progression the framework is built on). Currently
   nothing in the map can score this.
3. **What it must *not* do** — support a claim about present proficiency when the artifact is old
   and the practice has moved.

### G15. No role/contribution declaration **[open]**

With multiple artifacts, "was this yours?" multiplies. Needs a per-artifact declaration: sole /
lead / contributor, and what it is offered as evidence for. Git authorship can corroborate but not
replace this.

### G16. No handling of abandoned probe threads **[open]**

A candidate can walk away from an uncomfortable line of questioning in chat; they cannot with a
panel. This is the main structural difference from `TODO.md:96` limit testing. The skill should
**record that a thread was abandoned** rather than silently dropping it — an unanswered probe is
information, and it's the closest available analogue to "admitting ignorance at the boundary".

### G17. No evidence manifest format **[open]**

Multi-artifact input needs a manifest: artifact, date, type, role, competencies claimed. Doubles as
the crosswalk G10 is missing, and as the thing a panelist could be handed.


### G19. Assessor-only material has nowhere to live **[open]**

Follows from D4.6. Two distinct problems:

1. **This repository is the training package — candidates read it.** Assessor-only material cannot
   live here. That arguably already applies to `dsai-tech-panel-form-l2.md`, which is marked
   CONFIDENTIAL while sitting in a repo whose purpose is to be read by the people being assessed.
2. **A coaching chatbot is a publication channel.** If the skill can read the guard and also coaches
   candidates, the guard leaks regardless of what mode it believes it is in. A soft instruction is
   not a control.

*Implication:* coach-facing and assessor-facing tooling should be **two separate skills with separate
bundled files**, superseding the mode-switching design currently in
`.claude/skills/dsai-competency/`. This is the sharper form of sponsor recusal (`TODO.md:92`) — not
role separation but **information** separation.
### G20. The L1 panel has a structural conflict of interest **[open]**

L1 seats "1 panelist plus one of the candidate's supervisors" (D7). The supervisor is the person
closest to a sponsor, and `TODO.md:92` requires sponsors to recuse from panels. On a two-person
panel, one of the two voters is conflicted — and L1 is the only tier with **no neutral observer**.

Also unstated: the L1 voting rule. Is it 2 of 2? Does the supervisor's vote count equally?

**Priority: low** in light of D15 — no L1 failures have occurred, HR does not track L1, and L1
panels can be repeated at any time. The conflict is structural rather than currently harmful. Worth
fixing if L1 ever becomes consequential.

### G21. The track lead's decision procedure is undefined **[open]**

D7 escalates 2-of-3 and 3-of-5 to the DSAI track lead, but nothing says what the track lead does:
re-review the packet, interview the dissenter, default to the majority, default to the dissenter?
Since escalation is triggered by any single dissenter, the track lead is the *de facto*
decision-maker in every contested case, which makes the absence of a procedure load-bearing.

Also unstated: what the neutral observer does if they *do* see bias or collusion — report to whom,
and does it void the panel?

### G22. The pink-flag accumulation threshold is undefined **[open]**

D8 says pink flags are not penalised individually but signal a shortfall when they happen all over
the place. How many, over what scope? Per competency, or across the whole packet? This is the
judgement the whole model now rests on, and it is exactly the kind of thing that varies between
assessors — which matters more under L2's 3-of-3 rule, where any single divergent assessor escalates.

Related and also unstated: the pivot for a pink flag is **"did the project require it"**, which is
itself a judgement about problem scope.

### G23. There is no requirements spec anywhere **[open]**

Follows from D11. If `DSAI_MAP` is a display table, then the binding requirements exist only as
prose scattered through four level files ("L2: if going for PL2 Statistical Analysis, to also
demonstrate PL1 in Machine Learning"). Nothing can validate that those prose statements agree with
each other or with the display table — and `errata.md` A1 shows the two source tables already
disagree on the competency names themselves.

*Correction to an earlier recommendation:* making `DSAI_MAP` machine-readable is the wrong fix, and
would overload a table that has a different job. Add a **separate requirements table** instead, and
leave the display table alone.

### G24. Key Tasks: documented practice diverges from actual practice **[verified] [open]**

D10 says Key Tasks are not explicitly assessed. The published framework says otherwise:

* `dsai-intro.md:28` — "Tech Panel will assess both the Key Tasks and Performance Standards and the
  Key Competencies."
* `townhall.md:565` — "All competencies must be explicitly demonstrated."

Two consequences:

1. **Community Contribution is orphaned.** It is a Key Task in `dsai-l2.md` (so: not assessed), a
   **scored row on the panel form** (so: assessed), and absent from `DSAI_MAP` (D3 says it should be
   added). Three sources, three statuses.
2. **This is appeal-shaped.** A candidate who reads the published material, prepares Key Tasks
   evidence, and is assessed on something else has a legitimate complaint — sharpened by D13, since
   the published-for-a-year argument cuts both ways.

### G25. Exemplar corpus: consent and confidentiality **[open]**

The 2 sample presentations on the "how to L2" page were presumably shared with consent. The 50–100
archived L1 presentations (D12) almost certainly were **not** shared on the basis that they would be
used as examples of work that would fail an L2 panel — still less as material fed to a chatbot.
"Assessors have seen these" and "these prompt a coaching tool available to everyone" are different
uses. Needs a decision before the corpus is used, and interacts with G19.

Practical note: 50–100 presentations will not fit in a skill's context. What is wanted is a distilled
set — a handful of representative cases plus the extracted patterns — not the raw archive.

### G26. Sources of truth exist outside this repo **[open]**

The "how to L2" Confluence page (D12) is candidate-facing, current, and absent from the skill's
source-precedence table. The panel process itself (D7) was also unwritten here until now. Any
coaching tool needs to know what that page says, or it will contradict it.

### G27. L4 panel composition is undefined **[open]**

D7 covers L1, L2 and L3. L4 is a real tier (D4) with no stated panel size, pass threshold, or
escalation path. Low volume, low priority — but currently unspecified.

### G28. The exemplarity criterion is unwritten **[open]**

D9's second question — *would the way they ran this project be a good example for others to follow* —
is a real, explicitly-discussed panel criterion with no home in any document. It is not Technical
Leadership (deliberately excluded at L2) and not a functional competency. Candidate homes: a
Performance Standard, or a stated panel principle alongside "assess the thinking, not the artifact".

It has a consequence worth stating too: because passing is an endorsement, a visible unaddressed
flaw weighs more heavily than a pure measurement model would predict.

### G29. Parsimony / overcomplication has no home **[open]**

D14 says overcomplication is penalised at L2, but nothing in the maps says so. `TODO.md` proposes
"Parsimony" as a **PL3** trait ("knowing what *not* to build"), which does not cover its use as an
**L2 penalty**. Needs a decision: red flag, pink flag, or a bullet under Data Project Design?

Note it is already half-present in the existing principle that assessment is against *problem*
complexity rather than *solution* complexity — an elaborate solution to an easy problem is evidence
against. Making that explicit may be the cheapest fix.

### G30. The exemplar corpus has no near-misses **[open]**

D12 gives 2 clear passes and 50–100 clear-below examples. **The decision boundary is exactly where
there is no data.** The genuinely hard cases — real L2 attempts that failed, and marginal passes —
are the highest-value calibration material and are not known to be retained.

L2+ panels have run on a 6-month cycle (D15) so such cases exist. Are the packets, forms, or
rationales kept? If so, that is the most valuable exemplar set available, and it is the one that
would most improve both assessor calibration and any tooling.

### G31. Sensitive code constrains any artifact-based assessment **[open]**

From D24. Some candidate code cannot be shared with assessors at all, let alone with a tool. Any
design that assumes repository access is wrong for a portion of candidates — probably the portion
doing the most operationally interesting work.

Implications, unresolved: does an assessment run on candidate-provided excerpts? On the candidate's
own machine? Is there a separate track for candidates whose work cannot be shown? The existing
proposal in `TODO.md:167` (the "Code Walk" — panelist picks a file at random during
the call) sidesteps sharing entirely, and may be the only workable form.

### G32. Candidate willingness is not part of the process **[open]**

From D21. A candidate was once found, mid-panel, not to want the appointment — sent by their boss.
Nothing in the framework covers consent to being nominated, and it is not asked before a panel is
convened. Rare, but it consumed a panel slot on a 6-month cycle and there is no defined handling.

---

## Part 5 — Recommended order of work **[proposed]**

0. **Adopt §D2.5 into `dsai-intro.md`.** Cheapest item here and it unblocks the reading of every
   other document. Currently no binding doc says how to read a descriptor.
1. **G9 — write the red-flag list.** Mechanical, high-yield, already on the TODO, and the one place
   automation can carry real weight. Overlaps with G18: many red flags *are* below-PL1 indicators.
2. **G11 — publish 3–5 real anonymised scored packets.** Under D2 this is what makes the abstract
   criterion operable, and under D2.5 the exemplars are the anchor points on the scale. Highest
   value per effort for both humans and the chatbot.
3. **G1/G2 — state the aggregation rule**, even if it is "the panel decides; here are the inputs".
   D2.5 supplies the coverage half; what remains is what a shortfall in one row does to the outcome.
4. **G4/G18 — adopt or amend [`pl0-definition.md`](./pl0-definition.md).** Required for L1
   assessment to work at all (D4). Note §6 there: this is the *same* piece of work as item 1. The override
   and guard rules moved out of this doc into G1 (item 3), so PL0 itself is now a smaller decision.
5. **G19 — decide where assessor-only material lives**, before any of it is written down. Cheap
   now, expensive after the fact.
6. **G6 — add Community to `DSAI_MAP`** (decided), and rule on Technical Leadership and Code
   Craftsmanship.
7. **G3 — make the source tables machine-readable**: add missing rows, encode the Stats/ML
   conditional explicitly rather than by "record the highest" convention, drop strikethroughs, fix
   the SQL so it actually derives what it claims to.
8. **G13/G14/G15/G17 — the multi-artifact rules**, needed before the chatbot can accept a portfolio.
9. **G10 — the template→grid crosswalk.**
10. **G5 — resolve stats vs ML**, and decide on moving experiment design into DPD.

---

## Part 6 — Implications for the skill **[proposed]**

Changes to `.claude/skills/dsai-competency/` implied by the above, not yet applied:

* **Split into two skills, not two modes** (D4.6, G19). Coach-facing and assessor-facing tooling
  need separate bundled files so the lapse-vs-absence guard cannot leak through the coach. This
  supersedes the mode-switching design currently in place.
* **Enforce the coach/assessor asymmetry** (risk 1). Coach mode: verdicts, not solutions.
* **Floor Specialisation at PL2** (D4.5), and bracket it from the corresponding functional
  competency rather than looking for a specialisation PL1.
* **Carry PL0 as a distinct finding** — separate from "not observed", with different advice
  attached (learn it vs present it).
* **Assess against the PL definition, not the bullets** (D2). Currently the skill leans on
  quoting bullets; it should quote the *definition* and use bullets as illustration.
* **Elicit on both sides of the threshold** (D2.5). The grid currently records evidence for the
  *required* PL only. It should record evidence at PL(n) **and** PL(n−1), and treat a missing lower
  bracket as an unresolved question rather than a pass. In practice this means probing downward when
  someone leads with their most impressive work — the opposite of what candidates volunteer.
* **Distinguish "PL2" from "at least PL2"** (D2.5 corollary). If no PL3 probing was attempted, say
  so instead of reporting a bounded result. This is also the honest way for a *preliminary*
  evaluator to defer to the panel.
* **Probe capability, not just performance** (D2.5 condition 1). For an indicator the project never
  called for, the question is "could you have, and how would you have gone about it?" — not "did
  you". Treat inability as disqualifying and non-performance as neutral.
* **Check complexity match explicitly** (D2.5 condition 2) — right kind of work at the wrong
  difficulty is a distinct finding from missing work, and has a different remedy.
* **Make L1 first-class** (D4) — `elicit.md` and `worked-examples.md` are L2-centric.
* **Accept a portfolio, not a project** (D6) — needs the manifest (G17), the recency rule (G13),
  and the reliability heuristic (a behaviour in n of m artifacts).
* **Read git history** where a repo is offered — cadence and authorship as an integrity signal.
* **Record abandoned probe threads** (G16).
* **Mark self-reported context as self-reported** (D5).
* **Probe for the specific instance, never accept the general claim** (risk 2).
