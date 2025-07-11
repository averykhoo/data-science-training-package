# DSAI L4

**Lead Specialist, JR9 = Tier 4 SEA Competency (LTS)**

## Key Tasks and Performance Standards

### Architect, design, or lead the development of a data related capability / product

Find gaps and/or opportunities to leverage data science to produce business value or organization-wide impact. Lead
cross-functional teams to deliver new technical capabilities.

You may be required to:

* Devise novel technical solution
* Combine techniques across domains or other fields
* Work with variety of data: e.g. need to combine different data set for insights and/or capability development

**Performance Standards**

* Identify and diagnose organizational problems within your domain of expertise
* Drive the adoption of technical standards and innovations

---

### (Technical Leadership) Guide senior management and working level

Provide technical leadership to lead technological advancement and improve scientific performance by guiding the guiding
senior management and working level to adopt the right strategies, solution, methodologies, practices, technologies and
culture. This may include:

* Present and convince extended senior stakeholders to prioritise and manage system changes
* Select the best methodologies to measure engineering/scientific & team performance
* Advise and guide teams in sub-domain of expertise, including neighbouring sub-domains

**Performance Standards**

* Demonstrate good knowledge of trending technologies, processes, best practices and modern methodologies to measure
  scientific performance
* Understand business needs and how it translate technically

---

### (Community Contribution) Grow the technical competency of the DSAI community

Influence beyond area of command and serve a wider community to help grow the technical competency of the community by
being on tech panel(s), developing training programs, and fostering an innovative and learning culture. This includes:

* Co-lead / Lead a community track of work e.g. chair tech panels / recruitment interview panels, lead RTS (raise,
  train, sustain) efforts for your community
* Be an effective technical mentor for senior officers in the community e.g. build and lead high performing technical
  teams
* Leverage the industry for collaboration and talents outreach

This requires good knowledge of the different community virtual groups, tech knowledge management (KM) sites and
community initiatives; as well as knowing our external partners' and vendors' contacts

**Performance Standards**

* Be a recognized technical leader within the organization
* Demonstrate effective coaching and mentoring
* Ability to conduct interviews for external candidates and internal tech panels to identify technical leaders
* Ability to influence the community to standardize technologies and engineering/scientific practices

---

## Competencies

Result of the query:

```sql
SELECT DSAI_MAP.Competency,
       DSAI_PL.PL,
       DSAI_PL.Description
FROM DSAI_MAP
         INNER JOIN DSAI_PL
                    ON DSAI_MAP.Competency = DSAI_PL.Competency
                        AND DSAI_MAP.L4 = DSAI_PL.PL;
```

---

### **Data Project Design**

**PL3**

* Break down complex / vague business goals into well-defined requirements and constraints
    * evaluate options and simplify requirements to improve the quality of the solution
    * prioritize problem statements to work on
    * diagnose and describe the root cause(s) behind a business or workflow "problem"
* Design, recommend, and lead organizational changes to increase the impact of the data project
    * e.g. formalize new data collection processes or user workflows
* Keep abreast of state-of-the-art developments and identify promising research directions
    * identify new opportunities in existing business domains
    * recommend new business or research domains to bring about new value from data

---

### **Exploratory Data Analysis**

**PL3**

* Articulate the impact of data sources / provenance on the overall analysis
* Use understanding of problem space to recommend other (internal or open source) datasets to enrich the analysis
* Source for additional analytics tools, techniques, libraries, etc. to enhance analysis as required
* Determine whether trends and anomalies are real insights or if they occur due to data collection biases

---

### **Data Preparation**

**PL3**

* Apply featurization
    * Identify or construct (e.g. via triangulation) proxy variables when ground truth labels do not exist
    * Control for biases in the data (e.g. survivorship bias, systematic errors)
    * Handle data with unusual properties (e.g. truncation/censoring, heteroskedasticity, multicollinearity,
      non-stationarity)
* Ensure data quality
    * Work with relevant product team / data owner to establish data pipeline and automate data preparation effort
    * Handle unusual data types and formats
    * Identify and reduce/mitigate data biases e.g. refining the data collection methodology, post-processing, etc.
    * Aggregate/fuse or otherwise improve the usefulness of existing datasets
* Prepare data e.g. to train models
    * Plan and conduct a data annotation project, use baseline algorithms or foundation models to semi-automate the
      annotation job, and validate annotator agreement (IAA)
    * Use common data augmentation techniques (e.g. synonym replacement, adding noise to audio,
      cropping/flipping/rotating/scaling images, ...)
    * Use known dataset invariances to synthesize new training data

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

**PL3**

* Construct, chain together and adapt statistical techniques (e.g., survival analysis, time series analysis, principal
  component analysis) and tools (e.g., statsmodels, pymc, stan) to analysis work
* Understand tools and techniques, and adapt or augment them to better answer the data question
* Advise modifications to existing statistical techniques to balance accuracy of results versus speed of analysis in the
  data models
* Evaluate key trends and research developments in new statistical models and adopt suitable techniques for the analysis
  work
* Develop innovative experimental design approaches to solve analytics problems

**L4: PL3 x 1 AND PL2 x 1**
If going for **PL3** Statistical Analysis, to also demonstrate **PL2** in Machine Learning

---

### **Machine Learning**

**PL3**

* Understand the mathematics, concepts, theory, and implementation details of machine learning algorithms
* Customize/tune SOTA models for your business domain
* Conduct ablation studies and benchmark against SOTA models / algorithms
* Trade-off between goodness of outcome, efficiency, and solution availability
* Design interpretable ML systems

**L4: PL3 x 1 AND PL2 x 1**
If going for **PL3** Machine Learning, to also demonstrate **PL2** in Statistical Analysis

---

### **Specialization**

**PL4**

* Diagnose organizational problems within the specialization of expertise and suggest solution(s)
* Recommend, present and defend opinions in terms of validity, criteria, evaluation and etc.
* Lead new capability development in the specialization, e.g.
    * Techniques: Design specialized models and algorithms to handle at least one specialization and contextualize to
      our stakeholders' needs
    * Able to make trusted recommendations with clear and sound judgements to influence decisions

**L4: PL4 x 1 specialization AND PL3 x 1 specialization**
To demonstrate PL4 in at least 1 specialisation and demonstrate PL3 in at least 1 other specialization