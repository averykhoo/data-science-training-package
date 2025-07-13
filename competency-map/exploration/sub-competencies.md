### 1. Data Project Design & Problem Formulation

This competency ensures the right problems are solved in the right way by blending business acumen, research discipline,
and project management.

* **Business & Impact Analysis:** The ability to perform requirements **elicitation** to diagnose the root cause of a
  business problem, understand stakeholder needs, and evaluate the potential impact of a solution. At its highest
  level (PL4), this manifests as **"research taste"**—an expert intuition for distinguishing a merely interesting
  problem from a truly important one. [competency-map/future-content-problem-formulation-competency.md]
* **Problem Formulation & Scoping:** The skill of translating a vague business goal into a tractable, well-defined data
  science problem with measurable objectives, clear requirements, and identified
  constraints. [Foundation/data-science-project-scoping-guide.md, competency-map/dsai-l2.md]
* **Literature Review & Background Research:** The discipline of exploring academic literature, industry practices, and
  internal knowledge to understand prior art, inform the project's direction, and avoid reinventing the
  wheel. [README.md, Machine Learning/README.md]
* **Experiment Design:** The critical ability to design a rigorous research plan to generate or collect the right data
  and measure outcomes effectively. This includes designing standard validation frameworks (A/B tests, cross-validation)
  at the Independent level (PL2) and architecting complex, novel, or quasi-experimental approaches at the Strategic
  level (PL3). [competency-map/dsai-l2.md, competency-map/dsai-l3.md]
* **Project Management & Execution:** The end-to-end management of the project lifecycle, including determining
  feasibility, estimating effort, defining success criteria, identifying risks, and articulating trade-offs and
  considerations. [Foundation/data-science-project-scoping-guide.md, competency-map/dsai-l2.md]

### 2. Data Preparation

This competency covers the full lifecycle of sourcing, transforming, and preparing data to make it suitable and robust
for analysis and modeling.

* **Data Sourcing, Extraction & Integration:** The ability to identify data owners, perform ETL, access data from
  various systems (SQL, MinIO, etc.), and fuse disparate datasets without data loss or
  corruption. [competency-map/dsai-l1.md, competency-map/dsai-l2.md]
* **Data Cleaning & Validation:** The process of handling data quality issues: imputing missing values, correcting
  errors, removing duplicates, and handling unusual data types and
  formats. [competency-map/dsai-l1.md, competency-map/dsai-l2.md]
* **Conceptual Feature Engineering:** The creative process of conceptualizing and constructing meaningful new features
  that capture real-world context by combining multiple data fields. Examples include using passenger data to create a
  feature for "is this person royalty/aristocracy" or using cabin and deck data to engineer "proximity to
  lifeboat." [competency-map/dsai-l2.md, competency-map/dsai-l3.md]
* **Data Enrichment & Augmentation:** The skill of enhancing data by finding alternate sources, conducting formal data
  annotation projects, or using augmentation techniques to synthesize new training
  data. [competency-map/dsai-l2.md, competency-map/dsai-l3.md]
* **Data Governance & Automation:** Ensuring data quality and reproducibility by version-controlling scripts and data
  snapshots, establishing automated data pipelines, and adding clear descriptions to a data
  catalog. [competency-map/dsai-l1.md, competency-map/dsai-l3.md]

### 3. Exploratory Data Analysis (EDA)

EDA is the process of building an intimate understanding of the data, validating its integrity, and its relationship to
the problem space.

* **Data Characterization & Provenance:** Initial data discovery to understand schemas, distributions, and correlations,
  while critically evaluating the data's origin and potential for built-in
  biases. [competency-map/dsai-l1.md, competency-map/dsai-l3.md]
* **Hypothesis Generation:** Using statistical and visual techniques to formulate initial hypotheses about the data and
  its connection to the problem space. [competency-map/dsai-l2.md]
* **Insight & Anomaly Discovery:** Actively looking for patterns, trends, and outliers, and determining whether
  anomalies are genuine, valuable insights or simply data collection
  errors. [competency-map/dsai-l1.md, competency-map/dsai-l3.md]
* **Baseline Modeling & Setup Validation:** Running simple, standard models to establish a performance baseline. This is
  crucial for validating that the experimental setup is sound before committing to more complex
  solutions. [README.md, competency-map/dsai-l1.md]

### 4. Statistical Analysis

This competency uses statistical techniques to robustly identify patterns, validate relationships, and inform decisions
through rigorous inference.

* **Foundational Theory & Application:** A strong, practical understanding of linear algebra, probability theory, and
  core statistical concepts, and the ability to apply common techniques using standard
  libraries. [competency-map/dsai-l1.md]
* **Model Selection & Assumption Validation:** The skill of selecting the appropriate statistical technique (including
  frequentist or Bayesian methods) and demonstrating **analytical rigor** by validating the model's underlying
  assumptions (e.g., IID for time-series, or the requirements for an
  ANOVA). [competency-map/dsai-l2.md, competency-map/dsai-l3.md]
* **Model Validation & Comparison:** Measuring statistical significance and power, and interpreting both frequentist *
  *Confidence Intervals** and Bayesian **Credible Intervals** to communicate uncertainty. For Bayesian models, this
  involves interpreting results from techniques like LOO-CV and LOOIC. [competency-map/dsai-l2.md]
* **Inference & Interpretation:** The critical final step of interpreting findings from the model—understanding the
  significance of results and explaining them with an understanding of the underlying
  mathematics. [competency-map/dsai-l2.md]

### 5. Machine Learning

This competency uses algorithms to find patterns, make predictions, and optimize objective
functions. [competency-map/dsai-intro.md]

* **Model Selection:** Understanding and selecting appropriate algorithms, models, or ensembles that are fit for the
  purpose.
* **Model Training:** Fitting the model to data, including debugging and fixing edge cases.
* **Model Tuning:** Efficiently tuning hyperparameters and performing regularization to manage the bias-variance
  tradeoff.
* **Model Evaluation:** Correctly creating a test set and using appropriate metrics to measure, benchmark, and compare
  performance.
* **Model Inference:** The engineering skill of deploying and running ML models at scale.
* **Model Interpretability:** Using tools (e.g., SHAP) to explain model outputs to non-technical users.

### 6. Visualisations and Data Storytelling

This is the ability to translate data-driven findings and complex concepts into compelling narratives that drive action
and understanding.

* **Insight Communication:** The technical skill of choosing the right chart or graph and applying design principles to
  create visualizations that clearly and accurately communicate data-driven insights. [competency-map/dsai-l1.md]
* **Conceptual Communication:** Using visualization as a tool beyond data, such as creating diagrams and flowcharts to
  explain complex processes, system workflows, and the inner workings of statistical or ML models.
* **Narrative Crafting & Contextualization:** Developing a coherent data story, explaining discoveries and limitations,
  and translating findings into relevant insights for
  stakeholders. [competency-map/dsai-l1.md, competency-map/dsai-l2.md]
* **Stakeholder Engagement & Influence:** Guiding the thinking of problem owners, advising on actionable insights, and
  iteratively sharpening the narrative to secure buy-in for recommendations. [competency-map/dsai-l2.md]
* **Interactive Dashboarding:** Building interactive tools that allow users to derive their own insights from data,
  which may include connecting to live data streams without necessarily requiring real-time processing
  skills. [competency-map/dsai-l2.md]

### 7. Specialisation

This competency is about achieving deep, orthogonal knowledge in a specific data domain (e.g., Text, Audio) and
combining it with analytical competencies to create value.

* (This section's breakdown into "Quantitative/Statistical Path" and "Predictive/ML Path" remains highly relevant and
  well-defined based on your previous input.)

### 8. Code Fluency (Future Competency)

The ability to use programming languages (primarily **Python**) to explore, analyze, and create solutions that are not
just functional but also correct, efficient, and clear. This is treated as a linguistic skill for expressing analytical
thought.

* **The Grammar (Correctness & Fundamentals):** Writing code that is functionally correct. This involves a solid grasp
  of core data structures, algorithms (e.g., when to use a hash map for lookups vs. iterating a list), and control flow
  within a **Jupyter Notebook** or script. The focus is on producing the right answer and avoiding bugs.
* **The Style (Clarity & Idiomatic Code):** Writing code that is fluent, readable, and maintainable. This includes using
  descriptive names, clear comments, docstrings, type hints, and leveraging **idiomatic Python** (e.g., comprehensions).
  It is supported by using linters (`flake8`/`ruff`) and static analyzers (`mypy`) to ensure consistency and clarity.
* **The Vocabulary (Library & Algorithmic Fluency):** Effectively selecting and using the right tools for the job. This
  means fluency with core libraries (`pandas`, `scikit-learn`, `numpy`) and understanding when to apply specific
  algorithms for efficiency (e.g., knowing the time/space complexity trade-offs of different approaches, using
  `collections.deque` for queues). It also includes the ability to design and implement simple, reliable APIs for
  models (e.g., with `fastapi`).
* **The Workshop (Tooling & Environment Proficiency):** The practical ability to work effectively in a modern data
  science environment. This includes proficiency with **Linux**, version control with **Git**, and using platforms for
  training and experimentation (e.g., CML, Run:AI, basic Kubernetes). This also covers automating analytical workflows
  for reproducibility, which might involve simple CI/CD pipelines.
