# The Proficiency Ladder

Condensed from `competency-map/exploration-in-progress/bonus-content-proficiency-level-definitions.md`.
That file is the fuller treatment (Bloom's, Dreyfus, the culinary analogy); read it if someone wants
the reasoning behind the ladder. This file is the working version for a conversation.

The PLs measure **cognitive process and scope of impact**, not subject matter. The same ladder
applies to Machine Learning, to Community Contribution, and to everything in between.

| PL | Name | Core skill | Scope of work | Impact |
|---|---|---|---|---|
| **PL1** | Foundational Application | Execute a known procedure | Routine tasks: clear instructions, known-correct output | Correctness — done reliably, to spec |
| **PL2** | Independent Application | Solve a standard problem independently | Non-trivial but standard; needs independent diagnosis and choice of method | Value & reliability — delivered without close supervision |
| **PL3** | Adaptive Synthesis | Navigate ambiguity and complexity | Open-ended; no single pre-defined right answer, no standard recipe applies | An effective custom solution to a unique problem |
| **PL4** | Generative Creation | Invent a new, generalisable capability | Strategic/generative; reflecting on the problem space itself | Leverage — a force multiplier others build on |

The knowledge type shifts as you climb: **facts and steps** (PL1) → **principles, the "why"**
(PL2) → **knowledge *about* methods: their limits, how to combine and adapt them** (PL3) →
**metacognition: knowing the limits of current knowledge and defining new approaches** (PL4).

## The probes

These are the questions that actually separate adjacent levels. Use them verbatim or adapted.

**Establishing PL1**
> "Can you walk me through the exact steps you took to get this result?"

Looking for: correct, reliable execution of a known procedure. If they can't reconstruct what they
did, that's below PL1 regardless of how good the outcome was.

**PL1 vs PL2**
> "Why was this the right method here? What other standard approaches did you consider, and why
> were they less appropriate?"

Looking for: the shift from *how* to *why*. A PL2 justifies a choice from a set of known
alternatives, on principle. A PL1 answers "because that's what the tutorial/team/notebook used", or
names alternatives without being able to say what would have made one of them right.

Common false positive: a long list of models tried. Trying five models is PL1 if the choice among
them was "highest F1". It's PL2 if they can say why one *should* win given the data and the
decision it feeds.

**PL2 vs PL3**
> "What were the most significant assumptions you made? What would have happened if they were
> violated, and what was your plan B? Walk me through the trade-offs of the approaches you
> evaluated before designing this."

Looking for: navigating ambiguity. A PL3 knows where their solution is load-bearing on an
assumption, has stress-tested it, and synthesised something custom because nothing standard fit.
A PL2 solved it with a standard method, correctly chosen — which is exactly what PL2 is, not a
deficiency.

Common false positive: a bespoke-looking pipeline that is really five standard steps in sequence.
Ask what would break, and why they departed from the standard approach. If the answer is "the
standard approach worked fine, I just wired it up", that's PL2.

**PL3 vs PL4**
> "How would you generalise this? What would a framework, library, or methodology guide look like
> so that ten other teams could solve *similar* problems without your help?"

Looking for: the shift from solving one hard problem to creating reusable capability. PL4 output is
a tool, standard, or system others use.

## Guiding principles for assessment

1. **Assess the thinking, not just the artifact.** Outcome matters, but process and reasoning are
   paramount. The quality of their justification reveals their true level.
2. **Evaluate against problem complexity, not solution complexity.** A simple, elegant solution to a
   hard problem is mastery. A needlessly complex solution to a simple problem is immaturity.
3. **Seek integrated skills, not isolated tasks.** The ideal candidate shows how project design
   informed data prep, how EDA drove feature engineering, how storytelling landed the result — not
   seven boxes ticked independently.

## Calibration notes for a chatbot

- People systematically over-rate themselves on Data Project Design and under-rate themselves on
  Data Preparation and Storytelling. Probe the first harder than they expect; give credit on the
  latter two that they don't think to claim.
- "It's just cleaning" and "it's just a dashboard" are almost always understatements of PL2 work
  that never made it into the packet.
- A PL rating is per *competency*, not per project. Someone can be PL3 in EDA and PL1 in ML in the
  same piece of work, and that's normal.
