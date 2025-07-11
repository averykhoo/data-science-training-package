# DSAI L3

**Senior Specialist, JR10 = Tier 3 SEA Competency (STS)**

## Key Tasks and Performance Standards

### Address complex organizational problems by applying data science with deep analysis of the insights generated

Anticipate issues, identify opportunities, and work on open-ended problems where outcomes can be effectively achieved
with data science and analytics. The complex problems will require breaking down into smaller and manageable components.
This requires leading the efforts to architect and implement through team effort or leveraging external resources.

The data solution developed should be reusable or reproducible by others in the community. This also means being able to
articulate the complex problem and convince the different stakeholders for actionable outcome / decision-making such as
willingness to invest resource to develop and/or adopt the solution.

Possible approaches include:

* Lead technical projects and deliver new ML/AI capabilities that meet organizational needs
    * To make new things possible or to make existing things easier
* Develop methodology, approach, and/or capability to enable analysis and insights generation for complex issues
    * Such projects usually have longer time frame with novel elements of experimentation / exploration or, reusable
      across data domains

**Performance Standards**

* Identify, diagnose, and solve open-ended problems
* Demonstrate mastery in understanding and applying choice of data science models / algorithms with deep analysis on the
  insights generated
* Develop bespoke data solution useful for the community and the organization

---

### (Technical Leadership) Provide technical guidance to your group

Provide technical leadership to lead technological advancement and improve scientific performance by guiding the group
to adopt the right strategies, solution, methodologies, practices, technologies and culture. This may include:

* Place judgement on practices and technologies to adopt and abort
* Convince extended stakeholders to prioritise and manage system changes
* Measure engineering/scientific & team performance

**Performance Standards**

* Demonstrate good knowledge of trending technologies, processes, best practices and modern methodologies to measure
  scientific performance
* Understand business needs and how it translate technically

---

### (Community Contribution) Being an active and effective contributor in the community

Influence beyond area of command and serve a wider community to help grow the technical competency of the community by
being an active and effective contributor in the community, for example:

* Being a significant contributor to at least one track of work
* Be an effective technical mentor within section

This requires good knowledge of the different community virtual groups, tech knowledge management (KM) sites and
community initiatives.

**Performance Standards**

* Demonstrate effective coaching and mentoring for team members
* Ability to influence the community to adopt useful technologies and best engineering/scientific practices

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
                        AND DSAI_MAP.L3 = DSAI_PL.PL;
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

**L3: PL3 x 1 AND PL1 x 1**
If going for **PL3** Statistical Analysis, to also demonstrate **PL1** in Machine Learning

---

### **Machine Learning**

**PL3**

* Understand the mathematics, concepts, theory, and implementation details of machine learning algorithms
* Customize/tune SOTA models for your business domain
* Conduct ablation studies and benchmark against SOTA models / algorithms
* Trade-off between goodness of outcome, efficiency, and solution availability
* Design interpretable ML systems

**L3: PL3 x 1 AND PL1 x 1**
If going for **PL3** Machine Learning, to also demonstrate **PL1** in Statistical Analysis

---

### **Specialization**

**PL3**

* Understand the fundamental theory behind the shortlisted approaches
* Adapt / re-implement specialized models and algorithm, contextualizing them to business needs / data constraints
* Evaluate multiple approaches
* Assess confidence and accuracy of insights generated / capability developed

**L3: PL3 x 1 specialization AND PL2 x 1 specialization**
To demonstrate PL3 in at least 1 specialisation and demonstrate PL2 in at least 1 other specialization