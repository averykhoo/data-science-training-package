# DSAI L2

**Consultant, JR11+ = Tier 2 SEA Competency**

## Key Tasks and Performance Standards

### Design and run end-to-end data project

Given a business question, design the project, from formulating hypotheses, exploring the data, performing robust
analysis, communicating the finding to users, and deriving the value, whether it rejects hypotheses and leads to new
discovery, or it confirms hypotheses and builds deeper confidence in an assessment. Solution could be simple yet it
should be robust - this means the need to assess feasibility of implementation or rigor of methodology.

**Performance Standards:**

* Demonstrate mastery of the data science process
* Bring value to users by refining business questions
* Deliver new discoveries and/or instil deeper confidence in analytical insights

---

### Address specialized operational problems by applying both data science and business domain knowledge

Specialized problems mean that the solution was neither obvious nor straightforward. Possible reasons:

* Data characteristics are significantly different, e.g. unavailable data, masked data for security/anonymity.
* Operational use case is non-trivial, e.g. suspicious activity monitoring via real-time analysis of multiple data
  streams.
* Solutions are not commonly available, e.g. not accessible to users in generally used platforms.

Possible approaches include:

* Develop bespoke data solution to generate actionable insights with data science techniques for decision-making
    * E.g. Custom hierarchical MGRM using `pymc` for ranking leadership performance using the annual survey results
* Design and train specialized, performant and robust ML solutions, incorporating business or domain expertise
    * E.g. PDNS pivoting on DomainTools for APT tracking
* Build analytical capabilities and deploy tools, APIs, and / or systems that provide analytical or investigative
  capabilities for a wide audience
    * E.g. apps on RAPID
    * Where required, work with MLEs to deploy scalable solutions. Systems should actually solve users' problems / help
      them to save time

**Performance Standards:**

* Demonstrate sufficient competency in data science to solve non-trivial problems.
* Demonstrate rigor in analysis.
* Demonstrate strong business understanding (domain and process knowledge) in the implemented solution
* Plan, manage, and execute a data science project end-to-end

---

### (Community Contribution) Active participation in community-wide initiatives

Influence beyond area of command and serve a wider community to help grow the technical competency of the community by
participating in community-wide initiatives, for example:

* Conduct sharing session
* Create reusable artefacts

**Performance Standards:**

* Demonstrate ability to influence the community to adopt useful technologies and best engineering/scientific practices
* Demonstrate good knowledge of common problems and limitations faced by the community

---

## Competencies

Result of the following query on 
[`DSAI_MAP`](./dsai-source-tables.md#DSAI_MAP) and [`DSAI_PL`](./dsai-source-tables.md#DSAI_PL):

```sql
SELECT DSAI_MAP.Competency,
       DSAI_PL.PL,
       DSAI_PL.Description
FROM DSAI_MAP
         INNER JOIN DSAI_PL
                    ON DSAI_MAP.Competency = DSAI_PL.Competency
                        AND DSAI_MAP.L2 = DSAI_PL.PL;
```

---

### **Data Project Design**

**PL2**

* Define/refine problem statements given a business requirement or question
    * decompose / reframe the problem statement into one or more data questions
    * determine and validate the assumptions underlying the problem statement
* Manage data projects over the entire lifecycle
    * determine feasibility of the problem statement and estimate the effort required
    * determine dataset requirements
    * discover business requirements and specialized / domain-specific constraints
    * define success criteria for the data project
    * articulate considerations, trade-offs and thought processes for the project

---

### **Exploratory Data Analysis**

**PL2**

* Develop and test hypotheses
* Use advanced data wrangling techniques
    * estimate missing values, identify trends, handle outliers
    * make predictions, evaluate model performance
* Discover insights and identify potential areas for deep-dives
    * e.g., clustering, pattern mining
    * review and refine the problem statements on an ongoing basis as more insights are discovered
* Evaluate the impact of anomalies, biases, and data truncation on the overall analysis

---

### **Data Preparation**

**PL2**

* Find, ETL, and clean data
    * identify the right data owner to obtain the required permissions
    * extract, transform and load (ETL) complete dataset(s) without data loss or corruption
    * investigate corrupted, erroneous, or incomplete data, and work with the data owners to rectify data collection
      problems
    * impact of removing duplicate entries and/or incomplete entries
* Enrich and/or augment data
    * consult data owners/catalogs to identify alternate data sources
    * assess the need to label or annotate the dataset and do so if required
    * handle imbalanced datasets e.g. oversampling/smote/adasyn (todo: imbalanced-learn is covered in bseac, maybe
      mention that somewhere)
* Construct meaningful new features
    * Identify and process chronologically ordered fields (e.g. timestamps, most sequential ids, UUID v6)
    * Process freeform text fields using simple NLP techniques or common tools (e.g. langid, keyword counts, nltk)
    * Correctly featurize specialized datatypes (e.g. latlong coordinates)
    * Able to use feature importance and selection techniques
    * Able to use normalization and binning
* Evaluate the impact of data imbalance, data cleaning, etc. to the overall analysis

---

### **Visualisation and Data Storytelling**

**PL2**

* Design clean and comprehensible visualizations
    * simplify complex insights by using clear, precise, efficient visuals and analogies, yet boosting readability,
      retention of the information, and reducing misunderstandings
    * assess how users perceive the visualized information and recommend enhancements to the visualizations
    * use visualization's color, style and chart types in synergy to help users read the information faster, retain the
      information longer, and reduce overall probability of misunderstandings
    * ensure visualizations look well put-together, color palette is consistent, works well together, and
      colorblind-friendly, etc.
* Help users to derive their own insights
    * allow users to easily customize the display of important information to enhance the usability of the dashboard
    * build interactive charts / dashboards to facilitate derivation of insights from underlying data by the users
* Guide the thinking of problem owners and stakeholders
    * develop a coherent data story leveraging the discoveries and insights from the data analysis work
    * advise stakeholders on actionable insights that emerge from the analysis and help identify possible metrics to
      monitor for improvement
    * iteratively review problem statement, approach and findings to sharpen the narrative in the storytelling to
      uncover valuable insights for the stakeholders

---

### **Statistical Analysis**

**PL2**

* Construct statistical hypotheses and design experiments to answer the data questions
* Perform hypothesis testing and measure statistical significance and confidence intervals
* Perform data interpolation or extrapolation/forecasting (e.g., ARIMA)
* Understand and tune parameters and configure common tools.
* Interpret findings with an understanding of the underlying mathematics/algorithms for the statistical/ML model

**L2: if going for PL2 Statistical Analysis, to also demonstrate PL1 in Machine Learning**

---

### **Machine Learning**

**PL2**

* Understand, select, and ensemble ML models
* Ensure the test set has no leakage, even with temporal data
* Perform regularization, cross-validation, and hyperparameter tuning
* Evaluate, describe, and make detailed comparisons of model performance (e.g. AUC/AUPRC/ROC, MAP/MRR/MAE, Elo,
  micro/macro-averaging, model cards)
* Tweak model outputs for decision support (e.g. normalize predictions to 0-100%)
* Determine when and how to include a human in the loop

**L2: if going for PL2 Machine Learning, to also demonstrate PL1 in Statistical Analysis**

---

### **Specialization**

**PL2**
Apply acquired knowledge to solve problems to demonstrate good understanding of the specific specialization(s), e.g.:

* Research: explore and understand academic literature and industry tools
* Describe: explain why approaches/techniques/models/algorithms were shortlisted due to their use cases and/or
  assumptions
* Benchmark: results from (selected) techniques / models / algorithms, using well known benchmarks and/or a curated test
  set
* Explain: final choice(s) of models and algorithms, and approach(es) taken

| Specialization (not exhaustive!)                                                                                                                 | Examples                                                                                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **In the area of Text:**<br>NLP, MT, LLMs, IR/RAG, summarization, etc.                                                                           | *   Sentiment analysis of geopolitical data (YouTube videos, social media posts & images, speeches, etc.) on specific topics of interest<br>*   Do something useful with LLM agents (note: this is not gonna remain L2 for long)<br>*   Finetune and deploy a translation tool for users |
| **In the area of Audio:**<br>STT, speaker ID, noise removal, etc.                                                                                | *   Deploy, finetune, and benchmark Whisper, Kaldi, Sphinx, etc.; and determine what works best on the dataset                                                                                                                                                                           |
| **In the area of Images / Video:**<br>OCR, CV, GANs/diffusion, face recognition, video analytics, deepfake detection, etc.                       | *   Apply CV/OCR techniques to analyze images to understand facebook profiles<br>*   Build an internal clearview clone (i.e. face ID) (e.g., maybe using face2vec with ann, and cross-encoders to improve precision)                                                                     |
| **In the area of Structured Data / Quantitative:**<br>tabular, nested data structures, quantitative data, geospatial, timeseries, metadata, etc. | *   *   Apply research theories to analyze surveys to learn about traits of an interest group<br>*   Perform online advertisement data analysis at scale<br>*   Build a commodities price forecasting system (to track critical supplies)                                                |
| **In the area of Graph:**<br>SNA, KG, etc.                                                                                                       | *   Use graph search algorithms in concert with ML to automatically pivot on known (e.g., published in CTI reports) malicious infra domains to map out APT infra<br>*   Social network analysis to identify friends, acquaintances, etc                                                  |

**L2: PL2 x 1 specialization**

To demonstrate PL2 in at least 1 specialization