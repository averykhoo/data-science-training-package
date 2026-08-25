# Scoping a Project Up

How to add scope that a panel will read as a higher PL — **without** adding complexity for its own
sake. Each entry states the *question the addition answers*. If you can't state that question for a
suggestion, don't make the suggestion.

## The test every suggestion must pass

Before proposing anything, answer all three:

1. **What question does this answer, or what risk does it retire?** If the honest answer is "it
   makes the project look harder", stop.
2. **Would a competent practitioner do this anyway, given the stakes?** Scope-ups should feel
   overdue, not bolted on. The rigor is almost always genuinely worth it — that's why it's in the
   rubric — but not on every project.
3. **Is the underlying problem hard enough to carry it?** Rule 2 of the framework: an elaborate
   solution to an easy problem is evidence *against* the candidate. If the problem has no headroom,
   the answer isn't a bigger solution, it's a different project.

## Try these before adding any work

In rough order of cost:

1. **Look for evidence that already exists but wasn't presented.** The reframing conversation, the
   thing the data owner fixed, the chart that got redrawn three times. A large share of apparent
   gaps are presentation gaps, and the packet template has room for exactly this.
2. **Redistribute across projects.** The packet takes two. A second project that covers
   storytelling and stakeholder work is cheaper than retrofitting them onto a modelling project.
3. **Deepen one competency rather than broadening all seven.** Panels respond to integrated depth,
   not seven shallow ticks.
4. **Only then, extend the project.**

---

## Data Project Design

| From | To | Add | Because it answers |
|---|---|---|---|
| PL1 | PL2 | Go back to the requester and reconstruct the *original* ask, then document how and why you changed it | "Were we solving the right problem?" |
| PL1 | PL2 | Write down the assumptions the request depends on, then test the one that would be most expensive to be wrong about | "What is this whole project resting on?" |
| PL1 | PL2 | Define success criteria with the stakeholder *before* the result, and record what you'd have concluded if it failed | "How would we know if this worked?" |
| PL1 | PL2 | Do a real feasibility estimate — data availability, effort, what you'd drop first — and compare it to what happened | "Was this deliverable in the time we had?" |
| PL2 | PL3 | Diagnose the root cause behind the stated problem; show the stated problem was a symptom | "Why does this problem exist at all?" |
| PL2 | PL3 | Recommend a workflow or data-collection change the org would need to make for the solution to hold | "What has to change outside my notebook?" |

**Anti-patterns:** inventing a stakeholder narrative after the fact; "reframing" that's a rewording;
listing constraints nobody was ever bound by.

---

## Exploratory Data Analysis

| From | To | Add | Because it answers |
|---|---|---|---|
| PL1 | PL2 | State a hypothesis *before* looking, then test it and report that you were wrong where you were | "Did the data behave as we assumed?" |
| PL1 | PL2 | Take the most surprising anomaly and determine whether it's real or a collection artefact | "Is this signal or plumbing?" |
| PL1 | PL2 | Quantify what your biases, truncation and outlier handling did to the headline number | "How much would this conclusion move?" |
| PL1 | PL2 | Cluster or pattern-mine to identify a deep-dive area, then actually do the deep dive | "Which subpopulation should we care about?" |
| PL2 | PL3 | Bring in a second dataset (internal or open) to corroborate or enrich the finding | "Does this hold up against independent data?" |
| PL2 | PL3 | Trace provenance end to end and articulate how collection shaped every conclusion | "Who made this data, and what did they leave out?" |

**Anti-patterns:** more charts; a bigger correlation matrix; clustering with no downstream use.

---

## Data Preparation

| From | To | Add | Because it answers |
|---|---|---|---|
| PL1 | PL2 | An ablation on your own cleaning: rerun the analysis with and without each major decision | "Did my cleaning choices make the result?" |
| PL1 | PL2 | Build one non-obvious feature — temporal, text-derived, or a specialised type (lat/long) — and show it earns its place | "Is there signal the raw fields don't expose?" |
| PL1 | PL2 | Go to the data owner about a defect and get collection fixed at source | "Can we stop this problem recurring?" |
| PL1 | PL2 | Handle imbalance deliberately, then show what the remedy did to precision/recall — not just that you applied it | "Did resampling help, or just move the threshold?" |
| PL2 | PL3 | Construct a proxy variable where no ground truth exists, and validate the proxy | "Can we measure this at all?" |
| PL2 | PL3 | Run a small annotation exercise with two annotators and report agreement (IAA) | "How reliable are the labels we're trusting?" |
| PL2 | PL3 | Identify and correct a structural bias — survivorship, censoring, non-stationarity | "Is the data lying to us in a specific way?" |

**Anti-patterns:** applying SMOTE without measuring what it did; feature engineering that adds
columns no model uses; an automated pipeline for a dataset that is never refreshed.

---

## Visualisation and Data Storytelling

| From | To | Add | Because it answers |
|---|---|---|---|
| PL1 | PL2 | Show it to a real user, record what they misread, redesign, and report both versions | "Does this land with the people who need it?" |
| PL1 | PL2 | Make one chart interactive or filterable so users can answer their *own* next question | "What will they want to ask next?" |
| PL1 | PL2 | Propose the metric the stakeholder should monitor from here, and how they'd act on it | "What changes on Monday?" |
| PL1 | PL2 | Fix palette consistency and colourblind-safety, and say why the palette encodes what it does | "Is the visual encoding doing work?" |

**Anti-patterns:** a dashboard nobody asked for; interactivity with no question behind it; more
slides. This competency stays at PL2 for L2, L3 and L4 — there's no scope-up past PL2, so don't
manufacture one. Excess effort here is better spent elsewhere on the grid.

---

## Statistical Analysis

| From | To | Add | Because it answers |
|---|---|---|---|
| PL1 | PL2 | State the hypothesis and null formally, then test with confidence intervals rather than a point estimate | "How sure are we, and how sure could we be?" |
| PL1 | PL2 | Check the assumptions your test makes and report the ones your data violates | "Is this test valid here?" |
| PL1 | PL2 | Design the experiment or comparison prospectively rather than analysing what happened to be collected | "Can this design actually detect the effect?" |
| PL1 | PL2 | Add a forecast or interpolation with a stated horizon and error bars | "What happens next, and how wrong might we be?" |
| PL2 | PL3 | Chain techniques — e.g. survival analysis on censored durations, or a hierarchical model in pymc/stan for partially pooled groups | "What do we do when the standard test doesn't fit?" |
| PL2 | PL3 | Adapt a method to your constraint and justify the accuracy/speed trade-off | "What do we give up to make this run?" |

**Anti-patterns:** a p-value for a hypothesis nobody stated; Bayesian machinery for a question a
t-test answers; a forecast with no error bars. Remember the pairing rule — pushing Statistics to
PL2 obliges PL1 evidence in ML (`combination-rules.md`).

---

## Machine Learning

| From | To | Add | Because it answers |
|---|---|---|---|
| PL1 | PL2 | Rebuild the split to eliminate leakage — temporal, group, or entity-level — and show what the score was before and after | "Was the original number real?" |
| PL1 | PL2 | Compare models on a metric chosen for the *decision*, not for the leaderboard, and justify it (AUPRC under imbalance, MRR for ranked output) | "What does the user actually pay for errors?" |
| PL1 | PL2 | Calibrate outputs so they mean something to a decision-maker (0–100%, thresholded tiers) | "What does a score of 0.73 mean to them?" |
| PL1 | PL2 | Design the human-in-the-loop: what gets auto-actioned, what gets reviewed, at what threshold | "Where does the human stay in charge?" |
| PL1 | PL2 | Write a model card: intended use, training data, known failure modes | "Who's allowed to use this, and for what?" |
| PL2 | PL3 | An ablation study isolating which component earns the performance | "Which part is actually doing the work?" |
| PL2 | PL3 | Benchmark against a SOTA approach on your own data, not on the paper's dataset | "Does the published result transfer to us?" |
| PL2 | PL3 | Customise the model — loss, architecture, decoding — to a domain constraint standard models mishandle | "Why doesn't the off-the-shelf answer work?" |

**Anti-patterns:** a deep model where logistic regression was within noise (this is *negative*
evidence under rule 2); hyperparameter sweeps reported as rigor; fine-tuning with no benchmark to
compare against.

---

## Specialisation

| From | To | Add | Because it answers |
|---|---|---|---|
| — | PL2 | A short literature/tooling review: what the standard approaches are and what each assumes | "What has the field already worked out?" |
| — | PL2 | Curate a test set from *your* data conditions and benchmark 2–3 shortlisted approaches on it | "Which of these works on our data?" |
| — | PL2 | Write the shortlist rationale: why these candidates, given their assumptions and your constraints | "Why these three and not others?" |
| PL2 | PL3 | Re-implement or adapt an approach to a constraint your data imposes | "What does our situation break?" |
| PL2 | PL3 | Quantify the confidence and accuracy of the capability you built, not just its benchmark score | "How much can we trust the output?" |

**Anti-patterns:** benchmarking on the public test set the model was tuned on; citing papers you
didn't read; claiming a specialisation on one API call.

---

## Key Tasks, and community contribution

Not a competency row, but assessed. If community contribution is missing at L2, the cheapest real
options are: a sharing session on something you had to learn the hard way during the project; a
reusable artefact extracted from your own code (the ETL wrapper, the annotation tool, the eval
harness); or mentoring a junior through a defined piece of work. All three are things people
usually half-did already — check before prescribing new effort.

For end-to-end ownership: if the candidate owned only the middle of a project, the gap may be
closable by taking the result the last mile — deploying it, or running the stakeholder session — 
rather than starting over.

## When a project genuinely can't carry the target level

Say so. The honest options are: (a) find a second project for the packet that covers the missing
competencies; (b) extend this project along a dimension that the problem actually has — usually
stakeholder impact or data difficulty, rarely model sophistication; (c) target the level the
evidence supports now and plan the next project deliberately against the grid. Padding an easy
problem is the one option that reliably fails, because the panel is calibrated to notice exactly
that.
