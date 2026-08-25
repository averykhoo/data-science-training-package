# Eliciting Evidence, Competency by Competency

For each competency: what to ask, and what an answer at each PL sounds like. The PL descriptions
here are compressed cues for recognising a level in conversation — the binding wording is in
`competency-map/dsai-l{1,2,3,4}.md`, which you must read and quote when you assess.

Work through one competency at a time. Don't fire seven questions at once; people answer the first
and ignore the rest.

---

## 1. Data Project Design

**Ask**
- Who asked for this, and what did they originally ask for? How is that different from what you built?
- What assumptions were baked into the request? Did you check any of them?
- How did you decide it was feasible? What did you estimate, and how wrong were you?
- What did success mean, and who agreed to that definition before you started?
- What did you decide *not* to do?

**PL1** — Understood a problem statement someone else defined; can explain how it became a data
question; followed the team's lifecycle. "My lead scoped it, I did the analysis."

**PL2** — Decomposed or reframed a business question into data questions themselves; validated the
underlying assumptions; determined feasibility and effort; defined success criteria; can articulate
trade-offs. "They asked for a churn model. Churn was 2%/yr and they couldn't act on individual
predictions anyway, so I reframed it as which segments to prioritise for outreach."

**PL3** — Broke down vague or conflicting goals into requirements; prioritised among problem
statements; diagnosed the root cause behind the stated "problem"; recommended organisational or
workflow changes (e.g. new data collection) to make the project work at all.

**Watch for:** the single most common L2 gap. If the problem arrived fully specified and they never
pushed back on it, they may have no Data Project Design evidence at all, however good the analysis.
Also the most common *presentation* gap — the reframing often happened in a corridor conversation
and never made it into the slides.

---

## 2. Exploratory Data Analysis

**Ask**
- What did you expect to see before you looked? Were you wrong?
- What hypothesis did you form, and how did you test it?
- What anomaly did you find, and how did you decide whether it was real or a collection artefact?
- Did anything you found change the problem statement?

**PL1** — Computed the dataset's characteristics: schema, distributions, correlations, outliers;
related findings back to the data question; planned an unbiased sample and train/test split.

**PL2** — *Developed and tested hypotheses*; advanced wrangling (estimating missing values,
identifying trends, handling outliers); found insights that opened deep-dives (clustering, pattern
mining); revised the problem statement as insights accumulated; evaluated how anomalies, biases and
truncation affected the analysis.

**PL3** — Articulated how provenance shaped the whole analysis; recommended additional internal or
open datasets to enrich it; determined whether trends were real or artefacts of collection bias.

**Watch for:** `df.describe()` plus a correlation heatmap is PL1, no matter how many cells the
notebook has. The PL1→PL2 line is *"I had a hypothesis and I tested it"*. Ask what surprised them —
if nothing did, they probably weren't predicting, just plotting.

---

## 3. Data Preparation

**Ask**
- Where did the data come from, and what did you have to do to get access?
- What was broken about it? How did you find out?
- What did you have to throw away, and what did that do to the result?
- Which features did you build that weren't in the source data? Why those?
- Did you go back to the data owner about anything?

**PL1** — Understood schemas, types, formats, storage; extracted without corruption; imputed
missing values; snapshotted and version-controlled the cleaning; documented fields in the catalog.

**PL2** — Identified the right data owner and got permissions; investigated corrupted or incomplete
data and worked with owners to fix collection problems; consulted catalogs for alternate sources;
assessed the need for labelling and did it; handled imbalance; *constructed meaningful new features*
(temporal fields, freeform text, specialised types like lat/long); used feature importance,
selection, normalisation, binning; **evaluated the impact of imbalance and cleaning choices on the
overall analysis**.

**PL3** — Constructed proxy variables where no ground truth existed; controlled for survivorship
bias and systematic error; handled truncation/censoring, heteroskedasticity, multicollinearity,
non-stationarity; established automated pipelines with the data owner; planned an annotation project
with IAA validation; augmented or synthesised training data using known invariances.

**Watch for:** the last PL2 bullet is the one people miss — not "I dropped 12% of rows" but "I
dropped 12% of rows, they were disproportionately from one region, and here's what that did to the
conclusion." Also: going back to the data owner to fix collection at source is strong PL2 evidence
that people never think to mention.

---

## 4. Visualisation and Data Storytelling

**Ask**
- Who saw this, and what did they do differently afterwards?
- What did you change after showing it to someone the first time?
- How did you decide what *not* to show?
- Could they explore it themselves, or only see what you chose to show them?

**PL1** — Designed accurate, clear visualisations; chose appropriate chart types and could explain
the trade-offs; applied design principles and colour theory; explained findings and the limitations
of the data.

**PL2** — Simplified complex insights with clear visuals and analogies; assessed how users actually
perceived the visuals and revised accordingly; colour/style/chart type working in synergy;
colourblind-friendly and consistent; **let users derive their own insights** (customisable,
interactive dashboards); developed a coherent data story; advised stakeholders on actionable
insights and metrics to monitor; iterated the narrative with them.

**PL3** — Required PL2 at L3 and L4 too; this competency does not escalate.

**Watch for:** "I made a dashboard" is not automatically PL2. The PL2 markers are *iteration with
real users* and *the stakeholder taking an action*. A beautiful static deck presented once is PL1.
Conversely, someone who kept revising a chart because their user kept misreading it has clean PL2
evidence and usually doesn't realise it.

---

## 5. Statistical Analysis

**Ask**
- What was the hypothesis, formally? What was the null?
- How confident are you in that number, and what's the interval?
- What assumptions does that test make? Do they hold for this data?
- Why that test and not the obvious alternative?

**PL1** — Understands the underlying linear algebra/probability/statistics; calculates and
interprets standard measures; recognises common distributions; applies common techniques using
libraries; makes simple charts and interprets them.

**PL2** — Constructed statistical hypotheses and **designed experiments** to answer the data
questions; performed significance testing with confidence intervals; interpolation or
forecasting (e.g. ARIMA); understands and tunes the parameters of common tools; interprets findings
with an understanding of the underlying mathematics.

**PL3** — Chained and adapted techniques (survival analysis, time series, PCA) and tools
(statsmodels, pymc, stan); adapted or augmented methods to better fit the question; traded accuracy
against speed; developed innovative experimental designs.

**Watch for:** a p-value with no stated hypothesis is PL1 at best. Ask whether the test's
assumptions hold — a PL2 knows which ones their data violates and what they did about it. See
`combination-rules.md`: this competency is assessed jointly with Machine Learning.

---

## 6. Machine Learning

**Ask**
- How did you split the data? Why that way?
- What could have leaked, and how did you rule it out?
- Which metric, and why that one rather than accuracy?
- What did the model get wrong, and does the pattern of errors make sense?
- Who consumes the output, and in what form?

**PL1** — Created a test set; used supervised and unsupervised models from common libraries;
benchmarked against xgb/lgbm; understands bias-variance, over/underfitting, curse of
dimensionality, cross-validation, ensembling, hyperparameter tuning; used common metrics
(confusion matrix, precision/recall/F1) and explanation tools (SHAP, linear weights); processed
numerical, categorical and ordinal features.

**PL2** — Understands, selects and ensembles models; **ensures the test set has no leakage, even
with temporal data**; regularisation, cross-validation, hyperparameter tuning; evaluated and made
detailed comparisons (AUC/AUPRC/ROC, MAP/MRR/MAE, Elo, micro/macro averaging, model cards);
tweaked outputs for decision support (e.g. calibrating to 0–100%); determined when and how to put a
human in the loop.

**PL3** — Understands the mathematics and implementation details of the algorithms; customises/tunes
SOTA models for the domain; ablation studies and SOTA benchmarking; trades goodness of outcome
against efficiency and availability; designs interpretable ML systems.

**Watch for:** temporal leakage is the highest-yield probe at PL2 — a random split on time-ordered
data is disqualifying regardless of the score. Suspiciously good performance almost always means
leakage; ask about it. Human-in-the-loop design is a PL2 bullet that people rarely claim.

---

## 7. Specialisation

**Ask**
- What's the specialisation you're claiming? (Text / Audio / Image-Video / Structured-Quantitative /
  Graph — the list in the level map is non-exhaustive.)
- What does the literature say the standard approaches are here? What did you read?
- What did you benchmark against, and on what test set?
- Why did you shortlist those approaches specifically?

**PL2** — Research (explored academic literature and industry tools); Describe (why approaches were
shortlisted, given their assumptions and use cases); Benchmark (results from selected techniques on
well-known benchmarks or a curated test set); Explain (the final choice, and the approach taken).

**PL3** — Understands the fundamental theory behind the shortlisted approaches; adapts or
re-implements specialised models, contextualised to business needs and data constraints; evaluates
multiple approaches; assesses the confidence and accuracy of the insights generated.

**PL4** — See `competency-map/dsai-l4.md`.

**Watch for:** the four verbs — research, describe, benchmark, explain — are a checklist. Most
candidates have three of four; the missing one is usually **benchmark** on a curated test set. "I
used Whisper and it seemed good" fails; "I benchmarked Whisper, Kaldi and a fine-tune on 200
manually transcribed clips from our actual audio conditions" passes. Note that the specialisation
count differs per level — see `combination-rules.md`.

---

## Key Tasks and Performance Standards

Assessed alongside the competencies. Read the top section of the target level's file — the
requirements differ meaningfully by level.

**Ask**
- Did you run this end to end, or own one part of it?
- What made this problem non-obvious? Would another team have solved it the same way?
- What do you know about this business domain that a competent outsider wouldn't?
- What have you done for the wider community — a sharing session, a reusable artefact, mentoring?

At **L1** the bar is executing well-defined problems reliably, with good documentation and version
control. At **L2** it is designing and running a project end-to-end, addressing *specialised*
problems (data that's unavailable or masked, non-trivial operational use cases, solutions not
commonly available), demonstrable domain understanding, plus community contribution. At **L3** and
**L4** technical leadership becomes an explicit Key Task.

**Watch for:** community contribution is a hard L2 requirement and is the single most common
last-minute scramble. Ask early. A sharing session, a reusable library, or mentoring a junior all
count.
