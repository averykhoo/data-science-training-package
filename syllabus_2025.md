# Data Scientist Syllabus: zero to hero

* *"Appreciate the existence of"* means:
  * Know that this thing exists and roughly what it does
  * But it's *not* necessary to know how or why it works
* ~~Strikethrough~~ means:
  * This topic is not being covered *on purpose*, to minimize the scope of the syllabus

## Content

* Foundation
* Visualisation
* Statistics
* Machine Learning & Deep Learning
* LLM
* Natural Language Processing
* Graph
* Automatic Speech Recognition

### Foundation

| Topic | Sub Topic | Description | Applied DS or Pure DS | Core or Appreciation |
| --- | --- | --- | --- | --- |
| Mathematics | Linear Algebra | vectors, matrices and their operations | Both | Core |
| | Probability and statistics | Distributions and Bayes' Theorem | Both | Core |
| Programming | Markdown | | Both | Core |
| | Python3 | NON-EXHAUSTIVE list: jupyter, (basic) regex, pandas, gensim, nltk, spacy, pydantic, fastapi, streamlit, sklearn, pytorch, transformers, huggingface | Both | Core |
| | Python3 | NON-EXHAUSTIVE list: jieba, modelscope | Both | Appreciation |
| Git | | | Both | Core |
| Unix tools and scripting | | | Pure DS<br />Applied DS | Core<br />Appreciation |
| minimal SQL | | * `SELECT <named column> AS <renamed column>`<br />* `COUNT(*)` and `COUNT(DISTINCT <column_name>)`<br />* `UPDATE`<br />* only 3 joins: `(INNER) JOIN`, `LEFT JOIN`, `LEFT OUTER JOIN`<br />* `UNION`<br />* `GROUP BY`<br />* `WHERE`<br />* `DATE('YYYY-mm-dd')` (or whatever is native to your SQL dialect)<br />* `START TRANSACTION`, `ROLLBACK`, `COMMIT` | Both | Core |
| Code Styles/Code Quality | | * Provide type hints for core algorithmic functions (and comments if the algo is not obvious)<br />* Name functions and variables properly | Both | Core |
| Distance Measures | Equal length vectors / sequences | Manhattan / Euclidean<br />Hamming<br />Cosine Similarity<br />Pearson's coefficient (aka the linreg r²), covariance | Both | Core |
| | Variable length strings | Edit / Levenshtein | Both | Core |
| | Variable size sets | Jaccard similarity | Both | Core |
| | | BLEU / Smoothed BLEU<br />edit distance backtracking<br />METEOR<br />ROUGE<br />Damerau-Levenshtein<br />haversine<br />Overlap coefficient<br />Spearman's coefficient (monotonicity)<br />gini coefficient | Both | Appreciation |
| HTML / CSS | | understand the python package beautifulsoup for Scraping<br />KNOW HOW TO SPELL `SCRAPE`/`SCRAPING` instead of `SCRAP`/`SCRAPPING`, THEY MEAN DIFFERENT THINGS OMG | Both | Core |

### Visualisation

| Topic | Sub Topic | Description | Applied DS or Pure DS | Core or Appreciation |
| --- | --- | --- | --- | --- |
| Python packages | | matplotlib<br />seaborn<br />plotly | Both | Core |
| | | geojson (for choropleth) | Both | Appreciation |
| Tableau | | understand how to use it | Both | Appreciation |

### Statistics

| Topic | Sub Topic | Description | Applied DS or Pure DS | Core or Appreciation |
| --- | --- | --- | --- | --- |
| Basic stats | | descriptive stats like mean, median, mode, quartiles, etc<br />correlation<br />independence | Both | Core |
| Hypothesis testing | | know the different types of tests like chi-square<br />null and alternate hypotheses, p-value | Both | Core |
| Other stuff | | know to check assumptions and whether it applies to your problem | Both | Core |

### Machine Learning & Deep Learning

| Topic | Sub Topic | Description | Applied DS or Pure DS | Core or Appreciation |
| --- | --- | --- | --- | --- |
| train-test-validation-split | | Know how to do it *properly* | Both | Core |

### LLM

| Topic | Sub Topic | Description | Applied DS or Pure DS | Core or Appreciation |
| --- | --- | --- | --- | --- |
| Chat completions | | know how to call it through API | Both | Core |
| Guided generation | | know how to call it through API | Both | Core | 