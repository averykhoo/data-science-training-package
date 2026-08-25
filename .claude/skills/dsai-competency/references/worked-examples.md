# Worked Examples

Three sketches, mapped to the grid against **L2**. They are illustrative, not precedents — the
descriptors in `competency-map/dsai-l2.md` decide, not the resemblance of a case to one of these.

Use them to calibrate your own reasoning, and to show a candidate what "evidence" means concretely.
Don't quote them at a candidate as "this is what a pass looks like".

---

## Example A — strong analysis, invisible design ("the common near-miss")

*A candidate is handed a request: "predict which cases will breach their SLA." They build a
gradient-boosted classifier, tune it carefully, get AUC 0.89, and present a deck of results.*

| Competency | Req | Evidence | Prov. | Note |
|---|---|---|---|---|
| Data Project Design | PL2 | Accepted the problem as stated; no reframing, no success criteria agreed up front | **PL1** | The gap |
| EDA | PL2 | Distributions, correlations, outlier removal. No hypothesis stated or tested | **PL1** | The gap |
| Data Preparation | PL2 | Joined four systems, fixed a broken timestamp field, went to the owner to correct it at source, built duration features | PL2 | Strong, under-claimed |
| Visualisation | PL2 | Static deck presented once; charts accurate and clean | PL1–PL2 | Borderline |
| Statistical Analysis | PL1 (floor) | Descriptive stats, correlation | PL1 | Floor met |
| Machine Learning | PL2 (lead) | Tuned GBM, CV, AUC + AUPRC comparison, SHAP for the top drivers | PL2 | Met |
| Specialisation (Structured) | PL2 | No literature review, no benchmark against alternatives beyond the leaderboard | **PL?** | The gap |
| Key Tasks | — | Owned the modelling; scoping and rollout owned by the lead. No community contribution | **short** | The gap |

**Diagnosis.** Depth is fine where it exists; the failure is **coverage** — Design, EDA and
Specialisation have no qualifying evidence, and the Key Task of end-to-end ownership isn't met.

**What to do.** Mostly *not* more modelling. In order of cost: (1) check whether the reframing and
hypothesis work happened and just wasn't presented — with four source systems it very often did;
(2) take the result the last mile, run the stakeholder session, and agree what they'll monitor,
which touches Design, Storytelling and Key Tasks at once; (3) add the specialisation four-verb
sequence — a short review of standard approaches for this problem shape, and a benchmark on a
curated test set. Adding a neural model would add nothing: the problem is tabular and the GBM is
the right answer, so a deeper model would read as *negative* evidence under rule 2.

---

## Example B — modest-looking project that clears the bar

*A candidate is asked to "clean up the duty roster data". They find the underlying complaint is that
shift handovers lose information, reframe it as measuring where handover data is lost, and discover
the loss is concentrated in one shift pattern.*

| Competency | Req | Evidence | Prov. | Note |
|---|---|---|---|---|
| Data Project Design | PL2 | Reframed "clean the data" into "where and why is handover information lost"; validated the assumption that loss was uniform (it wasn't); agreed success criteria | PL2–PL3 | Strong |
| EDA | PL2 | Hypothesised uniform loss, tested it, was wrong; traced the anomaly to a collection artefact vs real behaviour | PL2 | Met |
| Data Preparation | PL2 | Parsed freeform handover notes with simple NLP; quantified what dropping malformed records did to the estimate | PL2 | Met |
| Visualisation | PL2 | Iterated a chart three times after the ops lead misread it; ended with a filterable view the team uses weekly | PL2 | Met, well-evidenced |
| Statistical Analysis | PL2 (lead) | Formal hypothesis, CI on the loss rate, checked the test's assumptions, noted which were violated | PL2 | Met |
| Machine Learning | PL1 (floor) | Small classifier to flag likely-incomplete handovers; proper test set, precision/recall | PL1 | Floor met |
| Specialisation (Text) | PL2 | Reviewed standard approaches for short noisy text, shortlisted three with rationale, benchmarked on 200 hand-labelled notes | PL2 | Met |
| Key Tasks | — | Owned end-to-end; ran a sharing session on parsing operational freeform text | met | — |

**Diagnosis.** No individual component is technically impressive. Every competency has evidence,
the reasoning is visible throughout, and the problem was genuinely ill-specified at the start.
This is what "simple, elegant solution to a hard problem" looks like — and it is a stronger L2 case
than Example A.

---

## Example C — sophisticated work, wrong level of problem

*A candidate fine-tunes a transformer to classify support tickets into eight categories. Extensive
hyperparameter search, LoRA, quantised deployment. 94% accuracy. The prior system was a keyword
rule set at 91%.*

| Competency | Req | Evidence | Prov. | Note |
|---|---|---|---|---|
| Data Project Design | PL2 | Never asked what the 3pp buys, or whether misclassification cost is symmetric | **PL1** | Gap, and telling |
| EDA | PL2 | Class distribution only | **PL1** | Gap |
| Data Preparation | PL2 | Standard tokenisation; no discussion of label quality despite human-assigned categories | **PL1** | Gap |
| Visualisation | PL2 | Confusion matrix and a training-curve plot; no stakeholder-facing artefact | **PL1** | Gap |
| Statistical Analysis | PL1 (floor) | None beyond accuracy | **PL0** | Floor not met |
| Machine Learning | PL2 (lead) | Fine-tuning, LoRA, quantisation, held-out test set | PL2–PL3 | Met |
| Specialisation (Text) | PL2 | No benchmark against the incumbent rules on a common test set; no shortlist rationale | **PL1** | Gap |

**Diagnosis.** The strongest technical work of the three examples and the weakest case. Under rule
2 the sophistication is assessed against problem complexity: an eight-class classification with
abundant labels and a working baseline is a standard problem, so the elaborate solution is neutral
at best. A panel will ask "why not the rules?" and there's no answer prepared.

**What to do.** Don't add technique. Recover the case by adding the *reasoning layer*: benchmark
honestly against the incumbent on a shared test set (specialisation PL2, and it may show the
transformer isn't worth its deployment cost — which is a good result to present); audit label
quality, since human-assigned categories on support tickets are usually noisy and that reframes the
94% ceiling entirely; work out the cost of each confusion type and calibrate the decision threshold
to it. That last one turns a leaderboard number into a decision-support tool, which is the PL2 ML
bullet, and gives Storytelling something real to communicate.

---

## Patterns worth naming to a candidate

- **The invisible-design gap (A).** Strong technically, no evidence of having shaped the problem.
  Extremely common, and often a presentation gap rather than a real one — ask before prescribing.
- **The under-claimed pass (B).** People discount their own data cleaning, stakeholder iteration and
  domain reasoning because it "wasn't hard". Those are three competency rows.
- **The impressive miss (C).** Technique substituting for judgement. The tell is that nobody can say
  what the extra capability bought.
- **PL0 vs not-done.** In A, B and C alike, several rows would be recorded as "not observed" if the
  candidate presented only their notebook. The packet is the evidence, not the work.
