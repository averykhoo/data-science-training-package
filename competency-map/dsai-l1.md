# DSAI L1

**JR11 = Tier 1 SEA Competency**

## Key Tasks and Performance Standards

### Address well-defined data science problems

"Well-defined problems" are those where the problem statement has been defined, the algorithms/methodologies/techniques
have been identified, and the data is available.

Officer is expected to independently complete routine tasks which are achievable by following established solutions,
guides, playbook and/or best practices in this org, academia, or industry, using enterprise and/or common platforms and
internal tools (e.g., RAPID, JupyterHub).

Adopt good documentation and coding practices for knowledge management (KM) which can help to facilitate on-boarding of
new officers and prevent loss of work.

* Document the analytical process and findings on KM (Confluence) spaces for knowledge sharing
* Version control scripts and notebooks, consider reusability, no hard-coding password, etc.

**Performance Standards:**

* Demonstrate knowledge and usage of the data science project workflow
* Demonstrate the ability to use common enterprise tools
* Execute your data project tasks and present your work

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
                        AND DSAI_MAP.L1 = DSAI_PL.PL;
```

---

### **Data Project Design**

**PL1**

* Understand a given problem statement for a data project
    * how it translates into data analytics question(s) / hypothesis
    * how the data analytics question(s) / hypothesis would be answered by the dataset
* Adhere to the data science project lifecycle
    * e.g. CRISP-DM, Tidymodels, or whichever specific framework is used by your team

---

### **Exploratory Data Analysis**

**PL1**

* Use analytical tools and techniques to discover the dataset's characteristics, patterns, trends, and outliers
    * basic data exploration e.g. schema, field descriptions, enum meanings, expected distributions, invariances, and
      correlations
    * use a programming language (e.g. Python, R) to compute calculated fields defined in the project scope
    * (If using ML) select an unbiased data sample, correct class imbalance, and plan the train/test data split
* Relate the findings from the data exploration to the data question(s)

---

### **Data Preparation**

**PL1**

* Understand the dataset
    * evaluate the data schemas to identify relevant data fields to be extracted and merged
    * understand the various data types e.g. number, date, string
    * understand the underlying representation in common data formats e.g. CSV, JSON, XML
    * understand common storage technologies e.g. MySQL, MinIO
* Extract data for analysis
    * Work with system owners to extract data without corruption e.g. SQL with operators 'join', 'count', 'distinct', '
      group by', 'where', etc.
    * Impute appropriate values to replace missing/inadequate fields e.g., nulls, outliers, and corrupted data
    * Snapshot the data at each stage of transformation
    * Version control the data cleaning script(s)
* Understand common featurization techniques
* Add a suitably detailed description and well-defined field descriptions to the data catalog

---

### **Visualisation and Data Storytelling**

**PL1**

* Design and develop visualizations
    * validate the accuracy and clarity of information presented
    * utilize analytics products (e.g. Tableau), open-source tools and libraries for visualization
* Assess and select the best visualization to present the data / information
    * e.g. tables, bar graphs, line graphs, pie chart, scatter plots, box-and-whisker plots
    * understand the pros and cons in using different visualization techniques and charts for presenting of various data
      types and information
    * experiment with various visualization charts to best convey insights from the data
* Understand and apply design principles and color theory to the visualizations
    * e.g., green color is generally perceived as ok / healthy, red color is generally perceived as alert / danger
* Explain discoveries, insights, team's conclusions and recommendations
    * explain findings related to specific analytical questions or problem statements
    * explain the limitations of the available data and the impact on the overall analysis
    * translate individual findings from data into relevant insights for stakeholders

---

### **Statistical Analysis**

**PL1**

* Understand linear algebra, probability theory, and statistics.
    * Calculate and interpret the significance of statistical measures (e.g., standard deviation, correlation, r-value)
    * Recognize common distributions in data (e.g., normal, uniform, zipf, linear, logistic)
* Apply common statistical / analytical techniques using common libraries
* Create simple charts and graphs and use them to interpret data.

---

### **Machine Learning**

**PL1**

* Create a test set
* Use supervised and unsupervised ML models in commonly used libraries (e.g. sklearn, sk-lego)
* Benchmark against common models (e.g. xgb/lgbm)
* Understand the effects of bias-variance tradeoff, over- and under-fitting, the curse of dimensionality,
  cross-validation, ensembling, and hyperparameter tuning
* Use common evaluation metrics (e.g. confusion matrices, recall/precision/F1) to measure model performance
* Use common tools or techniques to explain results (e.g. shap, visualize linear model weights)
* Process numerical, categorical, and ordinal values for ML tasks
* Able to use well-known ML libraries (e.g. sklearn, nltk, xgb, lgbm)