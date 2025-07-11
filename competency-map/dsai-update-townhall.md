# DSAI Competency Framework

**SEA Townhall**
**4th Feb 2025**

***
*Slide Notes:*

Just to be clear for those who are reading this instead of attending the townhall:
DSAI pronounced as 4 letters: D-S-A-I

---

### TL;DR

* **New:**
    * Competency-based tech panel assessment
    * Leadership competencies inherited from SEA community
* **Merge:**
    * Single career progression track for DA and DS
* **Rename:**
    * Job title: "Data Analyst" → "Data Scientist"
    * Job family: "Data Analytics" → "Data Science and Artificial Intelligence"

***
*Slide Notes:*

(If you've already gone through the email announcement and the linked HCD confluence page, feel free to take a nap until
Q&A)

In short, what's new is:

1. There's a new competency-based assessment for tech panel
2. This is a unified framework across both DA and DS
3. DAs and DS-es are now all "Data Scientists" - and it's not just the same name, it's the same job progression track (and
   it uses the same unified competency-based assessment)
4. The "Data Analytics" job family is now called "Data Science and Artificial Intelligence"

---

### Competency-based assessment

We have rubrics now

***
*Slide Notes:*

**Extra:**
Why?
Well there's a long backstory: <link to a rant on my personal confluence page removed>
But the short version is that we got lucky, and PSD mandated a change to a better career framework.

What is a rubric?
https://kiwix.rapid.internal/wikipedia_en_all_maxi_2023-05/A/Rubric_(academic)

(Some of) the main goals were:

* Objectivity in panel assessments
* Clarity of tech panel expectations (and explainability of outcomes)
* Relevance to the data track
* Transparency of evaluation criteria
* Enabling self-directed learning

---

### From "themes" to "functional competencies"

**Before**

* **Design:** Able to design data science pipelines and components to handle specialized business problems
* **Build:** Able to configure chosen DS/ML/AI techniques to improve performance
* **Run:** Able to use appropriate tools to execute chosen techniques and partake in the development of data science
  pipelines and components

**After**

* **Data Project Design:** Understand the data science project lifecycle. Effectively manage end-to-end data projects to
  meet business needs. Make sure to solve the right problems in the right way.
* **Exploratory Data Analysis:** Explore, understand, and describe the dataset and its provenance. Relate the data to
  the problem space. Look for patterns, trends, and anomalies in data.
* **Data Preparation:** Collect, clean, impute, validate, label, enrich, augment, featurize, and fuse/integrate datasets
  to enable robust analysis and/or models.
* **Visualizations & Data Storytelling:** Design visualizations to explain insights. Craft compelling data narratives.
  Contextualize the discoveries. Inform decision making.
* **Statistical Analysis:** Extract insights and inform decisions by using statistical techniques (e.g., hypothesis
  testing, data modeling, and significance validation) to robustly identify and validate trends, patterns, and
  relationships in data.
* **Machine Learning:** Create a train, test, and validation set. Select/design, configure, train, tune, and evaluate
  models to predict, describe, or recommend. Deploy and run inference at scale. Interpret results for non-technical end
  users.
* **Specialization:** Apply specialized tools and techniques to solve different problem domains.

***
*Slide Notes:*

The old (existing) assessment is based on the "Design, Build, Run" framework we inherited from SE.
(To be fair, it makes sense for the Software Engineer folks, whose job usually consists of designing, building, and
running systems.)

The new one is designed to match the lifecycle of a data project, and makes more intuitive sense in how it matches our
work.

1. "Data Project Design" covers requirements gathering, user research, problem formulation, project scoping, and
   managing the project throughout its lifecycle.
2. "EDA" covers everything you do to understand the data, including running common benchmark tests.
3. "Data Prep" covers ETL, cleaning, labelling, featurization, augmentation, and fusing multiple datasets.
4. "Visualizations & Storytelling" covers how well you communicate, be it visual or verbal.
5. "Statistical Analysis" covers using statistical methods.
6. "ML" covers using machine learning methods. (Note: statistical ("traditional") machine learning is still machine
   learning; it doesn't count towards both competencies.)
7. "Specialization" covers technical depth in a specialized domain.

**FAQ:**

* What's the difference between stats and ML?
* So we need to meet the PL checklist?

---

### (Non-exhaustive) examples of specializations

| Data Domain    | Specializations                               |
|:---------------|:----------------------------------------------|
| **Text**       | NLP, LLMS, MT, IR/RAG, summarization          |
| **Audio**      | STT, speaker ID, noise removal                |
| **Media**      | OCR, CV, GANs, face ID, video                 |
| **Structured** | tabular/nested, quant, geospatial, timeseries |
| **Graphs**     | SNA, KG                                       |

***
*Slide Notes:*

(In the last slide you may have noticed that "specializations" sounds a bit general; this was intentional.)
You can pick any specialization you like, as long as it's relevant to your work.
You can pick more than one, and as many as you like.
You can swap or pick up a new one at any time.
What you pick does not limit the projects you can take up, does not limit where you can rotate to, and does not limit
how far you can progress.

**Extra:**
Note the granularity at which they're defined - they're not super narrowly scoped, but neither are they very broadly
scoped.
The segregation by domains is primarily for visual clarity, but also provides a "safe" delineation of what would clearly
be separate competencies.
OCR + face identification doesn't feel very different (both kinda under CV tbh), but OCR + diffusion models could indeed
count as 2 specializations.

**FAQ:**

* If I choose a specialization can I change it?

---

### Before: "more complex" and "more products"

|            | JR11+                                                                                                                              | JR10                                                                                                                                | JR9                                                                                                                                                          |
|:-----------|:-----------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Design** | Able to design data science pipelines and components to handle specialized business problems                                       | Able to design **complex** data science systems, or diagnose and break down complex problems into smaller and manageable components | Able to drive and validate technical direction of an **entire product line** to ensure all systems within and across product lines work seamlessly together. |
| **Build**  | Able to configure chosen DS/ML/AI techniques to improve performance                                                                | Able to configure and adapt chosen DS/ML/AI techniques for more **complex** usage                                                   | Able to drive engineering excellence across an **entire product line** to ensure the delivery of quality products to user.                                   |
| **Run**    | Able to use appropriate tools to execute chosen techniques and partake in the development of data science pipelines and components | Able to use appropriate tools to execute chosen techniques and partake in the development of **complex** data science solutions     | Able to drive operational excellence across an **entire product line** to achieve the desired performance, reliability and maintainability.                  |

***
*Slide Notes:*

In the old (existing) framework, senior engineers will be forced to sprinkle in a little extra complexity, and the very
senior ones will end up building extra systems to form a product line.
But data science doesn't intrinsically value complexity and complication, and we really don't want to reward people for
creating solutions that are more complex than necessary.
So we wanted a foundational change in how we grade competencies.

---

### (There are also leadership competencies)

|                          | JR11+                                                                                                                              | JR10                                                                                                                                                                                                                  | JR9                                                                                                                                                                                                                                                          |
|:-------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Design**               | Able to design data science pipelines and components to handle specialized business problems                                       | Able to design complex data science systems, or diagnose and break down complex problems into smaller and manageable components                                                                                       | Able to drive and validate technical direction of an entire product line to ensure all systems within and across product lines work seamlessly together.                                                                                                     |
| **Build**                | Able to configure chosen DS/ML/AI techniques to improve performance                                                                | Able to configure and adapt chosen DS/ML/AI techniques for more complex usage                                                                                                                                         | Able to drive engineering excellence across an entire product line to ensure the delivery of quality products to user.                                                                                                                                       |
| **Run**                  | Able to use appropriate tools to execute chosen techniques and partake in the development of data science pipelines and components | Able to use appropriate tools to execute chosen techniques and partake in the development of complex data science solutions                                                                                           | Able to drive operational excellence across an entire product line to achieve the desired performance, reliability and maintainability.                                                                                                                      |
| **Technical Leadership** | NA                                                                                                                                 | Able to provide technical leadership by guiding the group to adopt the right strategies, solution, methodologies, practices, technologies and culture to improve productivity and engineering/scientific performance. | Able to provide technical leadership by guiding senior management and working level to adopt and implement the right strategies, solution, methodologies, practices technologies and culture to improve productivity and engineering/scientific performance. |
| **Community Contrib**    | Able to help grow the technical competency of the community by participating in community-wide initiatives.                        | Able to grow the technical competency of the community by participating in community-wide initiatives                                                                                                                 | Able to grow the technical competency of the community by participating in tech panels, developing training programs, and fostering an innovative and learning culture.                                                                                      |

***
*Slide Notes:*

This slide is hidden because it doesn't quite fit in the storyline I have in mind.
Also the community requirements have been slightly rephrased to match them with our PL framework, so this isn't an
accurate reference for our final state.

---

### After: "more proficient"

| After                                  | Proficiency Level 1                                                                                                                                                                           | Proficiency Level 2                                                                                                                                                                                |
|:---------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Data Project Design**                | Understand a given problem statement for a data project. Adhere to the data science project lifecycle.                                                                                        | Define/refine problem statements given a business requirement or question. Manage data projects over the entire lifecycle.                                                                         |
| **Exploratory Data Analysis**          | Use analytical tools and techniques to discover the dataset's characteristics, patterns, trends, and outliers. Relate the findings from the data exploration to the data question(s).         | Develop and test hypotheses. Use advanced data wrangling techniques. Discover insights and identify potential areas for deep-dives. Evaluate the impact of anomalies, biases, and data truncation. |
| **Data Preparation**                   | Understand the dataset. Extract data for analysis. Understand common featurization techniques. Add a suitably detailed description and well-defined field descriptions to the data catalog.   | Find, ETL, and clean data. Enrich and/or augment data. Construct meaningful new features. Evaluate the impact of data imbalance, data cleaning, etc. to the overall analysis.                      |
| **Visualizations & Data Storytelling** | Design and develop visualizations. Assess and select the best visualization to present the data / information. Understand and apply design principles and color theory to the visualizations. | Design and develop clean and comprehensible visualizations. Help users to derive their own insights. Guide the thinking of problem owners and stakeholders.                                        |
| **Statistical Analysis**               | Apply common statistical techniques using libraries. Create simple charts and graphs.                                                                                                         | Construct hypotheses, design experiments, perform significance testing. Answer questions or make forecasts.                                                                                        |
| **Machine Learning**                   | Use supervised and unsupervised ML models in commonly used libraries.                                                                                                                         | Ensure the test set has no leakage. Ensemble, regularize, tune, and evaluate models.                                                                                                               |
| **Specialization**                     | NA                                                                                                                                                                                            | Perform research, describe shortlisted approaches, benchmark and test, explain choices.                                                                                                            |

*... and +PL3, PL4*

***
*Slide Notes:*

So we pivoted from levels of complexity to levels of proficiency.
(Aside from making more sense, it's also what PSD now recommends for the entire civil service.)

On this slide you'll see PLs 1 and 2.
We've also defined higher levels of PLs - internally, up to PL4 for the competencies where it makes sense.
(The higher PLs just didn't fit in this slide.)

These statements are not intended to be a checklist; the listed tasks are neither necessary nor sufficient for
assessment.
Instead they're merely descriptors - a list of behavioral indicators that describe what a person at that specified level
of proficiency should be able to do day to day.
So while this serves as a guide, you shouldn't try to memorize how the PLs are described; instead, you should try to
understand what the PLs mean.

**Extra:**
The sharp-eyed (and fast readers) among you may have noticed there's no PL1 definition specifically for "Data
Storytelling". That's because at the PL1 level, storytelling is largely performative (i.e., superficial exhibited
behavior), making it hard to quantifiably measure in a candidate. But PL1 for this competency is never measured at tech
panel anyway, so it doesn't really matter.

**FAQ:**

* What's the difference between stats and ML?
* So we need to meet the PL checklist?

---

### How are PLs defined?

* **PL1**
    * **Consultant:**
    * <ins>Remember</ins> and <ins>apply</ins> basic skills
    * In order to complete routine tasks
* **PL2**
    * **Consultant:**
    * <ins>Understand</ins> and <ins>apply</ins> concepts
    * In order to solve well-defined problems
* **PL3**
    * **STS:**
    * <ins>Analyze</ins> assumptions and <ins>evaluate</ins> multiple approaches
    * In order to diagnose and solve open-ended problems
* **PL4**
    * <ins>Create</ins> novel solutions
    * <ins>Foresee and forestall</ins> problems

***
*Slide Notes:*

A quick rule of thumb is that Consultants are generally expected to exhibit mostly PL2 behaviors, and STS-es are
expected to exhibit mostly PL3 behaviors.
This trend doesn't extend to LTS-es because their work tends to skew towards organizational initiatives and
cross-disciplinary projects.
(Hence LTS-es will exhibit a mix of PL4s, PL3s, and PL2s, depending on whether that specific project is mostly within
their domain of expertise.)

The underlined keywords indicate the levels of cognitive process expected at each proficiency level.
You may recognize these words from Bloom's Taxonomy (specifically, the revised edition from 2001), which is used (among
other things) to guide curriculum development.
The other words on the slide aren't just filler: they indicate the expected task and problem scopes.

**Extra:**
There's also an implicit link to the levels of knowledge needed at each PL:

* PL1: factual knowledge; e.g., terminology
* PL2: conceptual knowledge; e.g., principles, theories
* PL3: procedural knowledge; e.g., techniques, evaluation criteria
* PL4: metacognitive knowledge; e.g., strategy

So there are 4 separate dimensions of proficiency that are distilled into these sentences: cognitive process, knowledge,
task scope, and problem scope.

PSD actually has 5 PLs, but we've compressed it into 4 to simplify the framework, and because (I feel) their
expectations are a bit too low.
(Their PL5 also starts to diverge from technical competency and veers off into the realm of planning and management,
which was not super relevant to our tech panel.)

**FAQ:**

* Is JR11 the same as "Citizen Data Scientist"?

---

### Consultant, focusing on statistical analysis

|                                        | Proficiency Level 1 | Proficiency Level 2 |
|:---------------------------------------|:--------------------|:--------------------|
| **Data Project Design**                |                     | ✓                   |
| **Exploratory Data Analysis**          |                     | ✓                   |
| **Data Preparation**                   |                     | ✓                   |
| **Visualizations & Data Storytelling** |                     | ✓                   |
| **Statistical Analysis**               |                     | ✓                   |
| **Machine Learning**                   | ✓                   |                     |
| **Specialization**                     |                     | (if applicable)     |

***
*Slide Notes:*

So how does this apply to you?
For the majority of you who use statistical analysis to find/generate insights, this is what you'll need for the
consultant tech panel.
Pretty much all PL2, except for PL1 in machine learning.

---

### Consultant, focusing on machine learning

|                                        | Proficiency Level 1 | Proficiency Level 2 |
|:---------------------------------------|:--------------------|:--------------------|
| **Data Project Design**                |                     | ✓                   |
| **Exploratory Data Analysis**          |                     | ✓                   |
| **Data Preparation**                   |                     | ✓                   |
| **Visualizations & Data Storytelling** |                     | ✓                   |
| **Statistical Analysis**               | ✓                   |                     |
| **Machine Learning**                   |                     | ✓                   |
| **Specialization**                     |                     | (if applicable)     |

***
*Slide Notes:*

Conversely, those of you whose work focuses on machine learning will need PL1 in stats, but PL2 in ML.

(Toggle back and forth one slide to emphasize the difference)

---

### We also inherit competencies from SEA

* Technical Leadership (only for STS and above)
* Community Contribution

***
*Slide Notes:*

We inherit both our leadership competencies from our parent SEA family.
This includes "technical leadership", which covers how well you give technical direction, plus what you do to grow
organizational culture.
And also includes "community contribution", which covers facilitation, coaching, mentoring, and working on tech
initiatives.

**Extra:**
(This bit skipped for SEA townhall to avoid antagonizing any SE folks who may be present.)
We also chose to inherit our requirements for code quality and writing documentation from the Software Engineering
track;
And so just like them, we conspicuously have zero requirements for either those things - yolo.

---

### PLs for leadership/community competencies

* **PL2 (Consultant)**
    * <ins>Guide</ins> new data scientists in your <ins>team</ins> (not a requirement for SEA)
    * Provide technical assistance, support, or consultation
    * <ins>Participate</ins> in the wider tech community
* **PL3 (STS)**
    * <ins>Coach, mentor, and facilitate</ins> within your <ins>section</ins>
    * Make solid technical recommendations (that your group* adopts)
    * <ins>Actively contribute</ins> to the wider tech community
* **PL4 (LTS)**
    * Provide technical oversight within your <ins>cluster/dte</ins>
    * Provide trusted advice to senior management
    * <ins>Take up leadership roles</ins> in the wider tech community
    * <ins>Leverage</ins> academia or the industry for technical collaboration or talent outreach

*\*SEA framework does not specify whether "group" refers to team or section*

***
*Slide Notes:*

This time, I've underlined the words that indicate the scope of your leadership and expected contributions.

* There's no PL1, because that just doesn't make sense.
* PL2 applies to consultants, and is generally scoped to your team (plus participation in the wider community).
* PL3 applies to STS-es, and is generally scoped to your section (plus being an active contributor).
* PL4 applies to LTS-es, is generally scoped at the cluster or directorate level, and also starts to touch on external
  engagement (plus leading internal initiatives).

(If you're wondering; yes, it was slightly force-fit into the PL framework.)

**FAQ:**

* How do you track community contribution?

---

### Summarized overview

|                                         | **Consultant (JR11+)** | **STS (JR10)** | **LTS (JR9)** |
|:----------------------------------------|:-----------------------|:---------------|:--------------|
| **Data Project Design, EDA, Data Prep** | PL2                    | PL3            | PL3           |
| **Visualization & Data Storytelling**   | PL2                    | PL2            | PL2           |
| **Statistical Analysis**                | PL2 / _PL1_            | PL3 / _PL1_    | PL3 / _PL2_   |
| **Machine Learning**                    | PL1 / _PL2_            | PL1 / _PL3_    | PL2 / _PL3_   |
| **Specialization**                      | PL2                    | PL3 + PL2      | PL4 + PL3     |
| **Technical Leadership**                |                        | PL3            | PL4           |
| **Community Contribution**              | PL2                    | PL3            | PL4           |

***
*Slide Notes:*

Overall this is what the expectations look like for consultants, STS-es, and LTS-es.
Just to be extra clear, that means this is the level you should be at when you go for the tech panel to become a
consultant, STS, or LTS respectively.

**Extra:**
I doubt anybody cares, but please note that this competency-based assessment does not replace the OCC framework; this is
simply one layer above it.
Technically this is two layers: functional competencies + leadership competencies.
But PSD has not published enough about how they want leadership competencies to work, so for now we're making do by
pretending they're functional competencies.

---

### Renaming the track

Same job, new title

---

### Job Titles

* "Data Analyst" → "Data Scientist"
* "Data Scientist" → "Data Scientist" (no change)

**External titles:**

* Consultant = "Senior Data Scientist"
* STS = "Staff Data Scientist"
* LTS = "Senior Staff Data Scientist"

***
*Slide Notes:*

Should be pretty straightforward to understand this change, about half of you can go update your LinkedIn job title.
This name change may also help with <previously the Data Analyst Cluster> recruitment and hiring.
If they're still hiring, which they probably aren't since (I think) their estab is full.

This also affects the job title you provide externally.
Which in turn affects your namecards, but I'm pretty sure nobody here has any.
(The job titles are slightly inflated relative to industry standards, but I guess that's fine.)

---

### Job Role Profiles (no change)

* **Data Scientist (JR11)**
    * Work with well-defined requirements and constraints, with close guidance and regular oversight, and complete
      routine <ins>tasks</ins>. Document your work to facilitate other data scientists.
* **Consultant (JR11+)**
    * Diagnose and solve specialized operational problems. Execute projects end-to-end collaboratively, with minimal
      guidance and oversight, to deliver project <ins>outcomes</ins>.
* **STS (JR10)**
    * Identify, diagnose, prioritize, and solve open-ended problems to meet organizational needs, and create
      meaningful <ins>impact</ins>. Lead teams to deliver technical solutions.
* **LTS (JR9)**
    * Diagnose and prioritize organizational problems within your domain of expertise. Devise novel technical solutions
      to complex/unpredictable problems. Drive organizational <ins>initiatives</ins>.

***
*Slide Notes:*

There's no change to the kinds of work you do at each level.
If you cross-reference this with your understanding of the PLs, you'll be able to get a feeling for how they correspond
to each other.

This time the underlined words indicate the scope of the work you're usually performing at that level.
(These are accurate for technical roles across all job families, and should also be reasonably accurate for the
management track.)

**Extra:**
What most people (regardless of skill level) would consider a problem suitable for your level:

* Newbie: a Jira task
* Consultant: stuff that's niche, non-routine, and (often) tedious
* STS: a working solution isn't hard to imagine, but it has a lot of stakeholders, moving parts, and/or inherent
  complexity, and is too much work for a single (normal) person to complete - so it's usually a team project
* LTS: most people aren't sure how to approach the problem, much less solve it; even if it was solved, it's hard to
  guess the impact

While the career framework does not reach PTS, you can extrapolate upwards pretty easily.
A reasonable analytic continuation from the current definitions could be to require the PTS to:

* Strategize, define organizational goals, and ensure success.

---

### Job Family

* "Data Analytics" → "Data Science and Artificial Intelligence"
* Now we're all one big data science family
* And in keeping with current industry trends, we included ✨ AI ✨

***
*Slide Notes:*

The old name (Data Analytics) was no longer fashionable.
Also now that everyone is a data scientist, it made extra sense to update the name.
And you know what's fashionable now?
✨ AI ✨

(...yeah there's not much to say here, just skip to the end)

**Afternote:**
I kind of undersold the work done for this slide tbh, we did a bunch of market research etc. to determine what the
correct names should be to optimize our recruitment and hiring

---

### Timeline

---

### When will things actually change

* **Now:**
    * ✅ New competency framework approved
    * ✅ Published to HR site
    * ✅ Email announcement ("Letter from the SEA Team")
    * 👋 SEA Townhall
* **April 2025 (upcoming tech panel):**
    * Choose old "Design, Build, Run" or new competency-based assessment
* **October 2025 (the following tech panel, and onwards):**
    * New competency-based assessment only

***
*Slide Notes:*

So we've gotten approval, we've published the materials, and we've sent the mass mailer.
And here we are at townhall today.

At the upcoming cycle of the tech panel, you get to choose if you prefer to stick to the old framework or go with the
new one.
(Honestly not much is different.)

Fingers crossed we won't hit any teething issues, or if we do we'll be able to easily iron them out.
And so from the following cycle onwards the new competency framework will apply to all tech panel candidates.

---

### Q&A

***
*Slide Notes:*

So now we come to what is actually the main part of the townhall presentation.
Please ask questions, or raise concerns that something might go wrong, or ask about your specific scenario.
(Or just complain about yet another complex structural change nobody asked for.)

---

### How does the tech panel assessment change?

* **New requirements:**
    * Visualization & storytelling
    * Community contribution & tech leadership
* **All competencies must be explicitly demonstrated**

***
*Slide Notes:*

There's also going to be an [updated slide template](./dsai-slide-template.md)

---

### What's the difference between stats and ML?

Stats (especially bayesian methods) are more like models with expert knowledge and use less data,
while ML is more about data and less (or no) expert knowledge.
This isn't a strict rule, and there are overlaps (like LDA). 

|                          | **Statistical Analysis**                                                  | **Machine Learning**                                                                                 |
|:-------------------------|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| **Objectives**           | Extract insights and meaning from data to inform business decisions       | Develop and deploy predictive models to drive business outcomes                                      |
| **Technical Foundation** | Linear algebra, probability theory, statistics, data visualization        | Machine learning algorithms, programming languages (e.g. Python), ML libraries and frameworks        |
| **Sample Tasks**         | Hypothesis testing, determining confidence intervals, regression analysis | Supervised and unsupervised learning, model evaluation, hyperparameter tuning                        |
| **Data Pipeline**        | Data acquisition, cleaning, EDA, maybe labeling                           | Integration with data systems, preprocessing and pipelining, feature engineering, maybe augmentation |
| **Outcomes**             | Data visualization, insight generation, reporting and dashboards          | Model development and deployment, predictive analytics, APIs and apps                                |
| **Common libraries**     | statsmodels, pystan, pymc                                                 | sklearn, xgb/lgbm, autogluon, pytorch                                                                |

---

### If I choose a specialization can I change it?

* Yes
* Demonstrating your proficiency in a specialization does not limit your career path in any way, feel free to learn as
  many specializations as you the time and capacity for
* Your assigned projects will also not be limited to your specialization - but if your specialization is rare, then you
  can expect that you will be given all the relevant projects that nobody else knows how to do

***
*Slide Notes:*

"Dropping" your proficiency in a specialization implies unlearning, i.e., "forgetting how to ride a bike" - you *can*,
with a lot of trying (or a car accident).
But even if you can, why would you want to? ¯\\\_(ツ)\_/¯

---

### How do you track community contribution?

* There will be a slide in the [template](./dsai-slide-template.md) for you to write this all down
* But the DSAI community is small (for now), so we'll usually just know

---

### So we need to meet the PL checklist?

* No, and it's not a checklist
* The PL descriptors are neither necessary nor sufficient
* The description of each PL is a list of behavioral indicators that describe what a person at that specified level of
  proficiency should be able to do pretty easily on a day to day basis

***
*Slide Notes:*

But also *kind of* yes - if you meet all the PLs, you're probably safe

---

### Is JR11 the same as "Citizen Data Scientist"?

* **No, CDS-es are (generally) non-tech:**
    * Not required to hold relevant qualifications
    * Not held to any specific competency standard
    * Not eligible for tech / hot skills allowance
* **(See next slide for JR11 requirements)**

---

### Are there requirements for JR11?

* Yes, but it (probably) doesn't affect you
* See [DSAI Proficiency Level Requirements](./dsai-intro.md#dsai-proficiency-level-requirements)

---

### Isn't it all time-normed anyway?

* No
* In general we *should be* moving away from CEP and time norms
* But as you may expect, there's always a statistical distribution
    * Person joins: 0 YIS
    * L1 / Confirmation after BSEAC: 1 YIS
    * L2 / Consultant: 3 YIS
    * L3 / STS: 6 YIS
    * L4 / LTS: 10+ YIS (lots of variance)
    * L5 / PTS: insufficient data

***
*Slide Notes:*

After someone joins, in their first year they have:

* About a month of the internal foundation programme
* A month of leave
* A month (4 weeks) of other mandatory courses
* A couple months to properly onboard
* Maybe 6+ months to be helpful

Please take the numbers with a grain of salt: I don't have access to actual career progression stats, I'm basing this on
anecdotes

The fastest (maybe the 99th percentile) fresh grad → consultant could be about 2 YIS - expect this to happen very rarely
Similarly, the 99th percentile fresh grad → STS could be around 4-5 YIS

You can think of the timeline as approximately matching big tech levels in this way:

* Newbie = L3
* Consultant = L4
* STS = L5
* LTS = L6 (usually 10-20 YIS)
* PTS = probably L7/8 (usually 15-20+ YIS, but the variance is huge)

---

### What if my work does not help development?

* Well... not all work helps your progression or development (unless you're super lucky)
* The goal is usually to have some sort of equitable (i.e., fair) task distribution across these usually overlapping
  categories:
    * Toil
    * High-impact, high-visibility
    * Skill-building / learning
    * Firefighting
    * (New) Competency-demonstrating